---
layout: default
title: Programming Tips
parent: Device Specific Info
grand_parent: Research
nav_order: 3
permalink: /programmingTips
---

# Programming Tips
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

* TOC
{:toc}

---

## Test psychtoolbox program
Psychtoolbox experiment is running in full-screen mode by default. This may create challenges when the program crashes, because it is hard to return to MATLAB interface to close the experiment screen. A work-around is to set the screen size a quarter of the monitor.

```matlab
% the 4th parameter represents the screen size and location.
% scrWidth: screen width
% scrHeight: screen height
Screen('OpenWindow', screenNumber, gray, [0, 0, scrWidth/2, scrHeight/2);
```

## Quit and Close a Psychtoolbox program
```matlab
Screen('CloseAll');
```

## Stimuli preparation
### Images
- Set a reasonable size of images presented in a study (e.g., 600px height).
- Choose `.png` format for images with transparent areas. Otherwise, `.jpg` is good enough.


### Audio files
- Set all sound files with **the same** sample rate (e.g., 48k) and number of channels (2)
- Choose **48000Hz** as audio sample rate (including the sounds for calibration animations).

### Videos
- Set a reasonable size of video stimuli (e.g., 600px height).
- Choose the right video codec. Currently, the reliable option is **MPEG-4**
- Keep a reasonable large bitrate (> 2M).
- Frame rate should be 60Hz or 120Hz.
- Prepare video stimuli with **ffmpeg**. Here is a sample code (running it in Terminal):

```shell
for FILE in *mp4;
    do ffmpeg -i $FILE -vf fps=120, scale=600:-1 -c:v mpeg4 -b:v 3M -an "${FILE/.mp4/"_resized.mp4"}";
done
```

## Stimuli presentation

### Visual
- Screen refresh rate: 144 Hz or the frame rate matches that of video stimuli

### Movie
Our movie stimuli usually have much slower frame rate than monitor. When playing movies, psychtoolbox would hold the current frame until the next movie frame is available. In other words, the screen refresh rate would be much slower during movie presentation. It would cause unstable and slower frame rate, which are crucial for time sensitive manipulations, such as gaze-contingent design.

To solve this issue, we just need to update the code allowing flip frame regardless of the availability of a new movie frame. This method is described in detail [here](https://psychtoolbox.discourse.group/t/simultaneous-movie-and-image-presentation/4313/2?u=dbneg).

And here is an example we use:
```matlab
    buffertex=[];
    while KeyCode(nextKey)==0
        [KeyIsDown, KeyTime, KeyCode]=KbCheck;

        % Wait for next movie frame, retrieve texture handle to it
        tex = Screen('GetMovieImage', w, movieRest);

        % Valid texture returned? A negative value means end of movie reached:
        if tex > 0
            if ~isempty(buffertex) && ...
                buffertex > 0 && ...
                buffertex ~= tex && Screen(buffertex, 'WindowKind') == -1

                try Screen('Close', buffertex); end
                buffertex=[]; 

            end
            
            % Draw the new texture immediately to screen:
            Screen('DrawTexture', w, tex);
            Screen('Close', tex);
            buffertex = tex; %copy new texture to buffer

        elseif buffertex > 0
            Screen('DrawTexture', w, buffertex);
            Screen('Close', buffertex);
        end

        Screen('Flip', w, [], 2, 2);

    end
```

### Sounds
- We should open the audio device only **once** at the beginning of the program and use it as global variable through out the program. We only close it at the very end of the program.

```matlab
global pahandle = PsychPortAudio('Open', deviceIndex,[],[],fs);
```
- Load corresponding sound information before we need to play it. For example, before calibration, we load the sound of calibration to the device.

```matlab
[attentionGetterSound, fs] = audioread('../sounds/attentionGetter.wav');

PsychPortAudio('FillBuffer', pahandle, attentionGetterSound');
```

- [sound device matters](https://psychtoolbox.discourse.group/t/psychportaudio-only-lets-me-use-sampling-frequency-48000/4464/2?u=dbneg){:target="_blank"}

### When sound video stimuli are included in the experiment
- save the videos in silent video (.mp4) and sound (.wav) files
- write code to play the video and audio together
- this approach has two advantages:
    - freely manipulate the temperal congruency between audio and visual signals
    - avoid interference between sound play and movie play in Psychtoolbox (2023.07). [check here for more details](https://psychtoolbox.discourse.group/t/audio-device-disappeared-after-movie-playback/5005/4){:target="_blank"}

## Octve (7.2) compatibility
We use Octave (rather than MATLAB) to launch our Psychtoolbox programs on Linx systems due to the simplicity of Octave. Though Octave has an impressive compatibility with MATLAB syntax, there are several places we need to be aware of in our scripts:

- Octave has limited string and character support. For example, it will treat an array of texts as a concatnated string. So, using cell structure is the best practice.

```matlab
AG = {"AG1_s.mp4", "AG2_s.mp4", "AG3_s.mp4", "AG4_s.mp4", "AG5_s.mp4"};

%% when retrieve a value, make sure to use {}, rather than ():
ag = AG{1};
```

- other text related issues:
    - "+" is not supported in cancatenating strings, please use `strcat` or `[]`.
    - to compare two strings, please use `strcmp`.

- For pop-up input windows, please use the native functions, such as `inputdlg` and `listdlg`. 

- For writing data into a .csv file, `writematrix` is not supported. Instead, we use a homemade function `saveCSV`.

```matlab
%% Please check existing program to see how to place the following sections in a program.
% open a file
file_id = fopen(strcat('Results/', Participant, ".csv"), 'w');

% write headers
saveCSV(file_id, {"studyName" "participant"})

% append data
saveCSV(file_id, {studyName, Participant})

% close file
fclose(file_id)
```
- Please use code comparison function in Visual Studio Code to compare Octave code with MATLAB code to see where need to be updated. Here is a [tutorial](https://vscode.one/diff-vscode/){:target="_blank"}.