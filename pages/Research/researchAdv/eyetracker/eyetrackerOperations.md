---
layout: default
title: Start an eye tracking study
parent: Eye Tracker
grand_parent: Device Specific Info
nav_order: 1
permalink: /eyetracker/operations
---

# Start an eye tracking study
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

* TOC
{:toc}

## for PsychoPy studies on Windows system
- Open ***Visual Studio Code*** (u can put like a symbol here)
- Open up your project folder with **File -> Open Recent...** function. 
- Then, look for your project folder name.
- Then bring up Terminal in VSCode with **View -> Terminal function.** You will see a Terminal panel appears at the bottom.
- Use Up Arrow key to navigate to the specific file. Once found the file, press Enter/Return key to run the program
- Now you will see a Welcome window showing up. The window lists several key information, such as participant ID. Note the ID down!! 
- Click OK to start the program.

## for Psychtoolbox studies on Linux system
- Open ***Visual Studio Code*** from the Dock
- Open up your project folder with **File -> Open Recent...** function. Look for your project folder name.
- Right click the program file (e.g., ***_Octave.m), and choose ***Open in Integrated Terminal*** in the pop-up menu.
- In the Terminal window, type `octave` followed by your program file name (e.g., ***_Octave.m), then press return.

```bash
octave faceDetection_Octave.m
```
### a video demo

<img src="assets/videos/octaveDemo.gif" alt="octaveDemo">


## Eye-tracker operation shortcuts

When you're at the eye-tracker preparation screen (before experimental trials start).
- ***C*** for Calibration
- ***V*** for Validation
- ***Return*** for confirming looking during calibration, validation & drift-correction.
- ***O*** for starting experimental trials