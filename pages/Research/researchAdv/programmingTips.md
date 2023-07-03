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
Screen(‘CloseAll’);
```

## Stimuli presentation

### Visual
- Screen refresh rate: 144 Hz

### Sounds
- Set all sound files with the same sample rate (e.g., 48k) and number of channels (2)
- [sound device matters](https://psychtoolbox.discourse.group/t/psychportaudio-only-lets-me-use-sampling-frequency-48000/4464/2?u=dbneg){:target="_blank"}

### When sound video stimuli are included in the experiment
- save the videos in silent video (.mp4) and sound (.wav) files
- choose **MPEG-4** as video codec
- choose **48000Hz** as audio sample rate
- write code to play the video and audio together
- this approach has two advantages:
    - freely manipulate the temperal congruency between audio and visual signals
    - avoid interference between sound play and movie play in Psychtoolbox (2023.07). [check here for more details](https://psychtoolbox.discourse.group/t/audio-device-disappeared-after-movie-playback/5005/4){:target="_blank"}