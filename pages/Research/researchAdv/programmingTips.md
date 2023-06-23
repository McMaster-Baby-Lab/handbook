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
- Set all sound files with the same sample rate and number of channels
- [sound device matters](https://psychtoolbox.discourse.group/t/psychportaudio-only-lets-me-use-sampling-frequency-48000/4464/2?u=dbneg){:target="_blank"}
