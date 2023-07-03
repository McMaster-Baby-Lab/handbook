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
- Set all sound files with the same sample rate (e.g., 48k) and number of channels (2)
- Choose **48000Hz** as audio sample rate

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

### Sounds
- [sound device matters](https://psychtoolbox.discourse.group/t/psychportaudio-only-lets-me-use-sampling-frequency-48000/4464/2?u=dbneg){:target="_blank"}

### When sound video stimuli are included in the experiment
- save the videos in silent video (.mp4) and sound (.wav) files
- write code to play the video and audio together
- this approach has two advantages:
    - freely manipulate the temperal congruency between audio and visual signals
    - avoid interference between sound play and movie play in Psychtoolbox (2023.07). [check here for more details](https://psychtoolbox.discourse.group/t/audio-device-disappeared-after-movie-playback/5005/4){:target="_blank"}