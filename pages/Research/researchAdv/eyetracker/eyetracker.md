---
layout: default
title: Eye Tracker
parent: Device Specific Info
grand_parent: Research
nav_order: 1
permalink: /eyetracker
---

# Eye tracker
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

* TOC
{:toc}

---

### Preparation 

Things to check before starting the program for a study. 

- Ensure participants are sitting comfortably on the chair  
- Ensure their posture is straight 
- Have them face the monitor

- Check the distance, ideally between **500 to 700 mm**
- Ensure there is a stable detection of the target sticker and both eyes (i.e., no flicking)  
- The participant's head should be at the centre of the tracking area
- Check the volumes on the speaker to ensure it is not too loud or quiet.


### Calibration 

Lets the machine knows how to translate eye images into gaze coordinates on the screen

1. Both eyes should be tracked (i.e., there should be green and blue crosses on both eyes) 
2. When calibration starts, confirm fixation *IMMEDIATELY AFTER* the eyes move by pressing the Return key.  
3. Valid key pressing during calibration will make the target appears in another location 
4. Press again if a key pressing calibration is not valid 
5. At the end of calibration, the looking pattern indicated by the green and blue crosses should match the layout of calibration target on the screen.  If not, restart the calibration.  

### Validation

Verifies the accuracy of calibration

- Operates similarly to calibration 

- Watch the size of error (indicated by the length of white lines) for each target location.  
    - The smaller the error the better. 

- Both eyes should have GOOD results.  
- If not, either redo the calibration (when participants looked very attentively during validation) 
- Or redo the validation, if participants move their bodies during the validation

### Drift Correction 

Monitoring the tracking accuracy AMID a study 

- Operates similarly to calibration and validation

- Pressing the Return key to confirm participants' looking 

- An accurate drift correction will allow the study to continue 
- If the error is too large (i.e., long white lines), we need to redo calibration & validation 

## Starting the Program 

- Open VsCode (u can put like a symbol here)
- Open up your project folder with **File -> Open Recent...** function. 
- Then, look for your project folder name.
- Then bring up Terminal in VSCode with **View -> Terminal function.** You will see a Terminal panel appears at the bottom.
- Use Up Arrow key to navigate to the specific file. Once found the file, press Enter/Return key to run the program
- Now you will see a Welcome window showing up. The window lists several key information, such as participant ID. Note the ID down!! 
- Click OK to start the program.

## Short Cuts 

- Press q to skip the initial text (you will not see them. - Text here refers to the text shown on the monitor the participant is looking at)
- Press the right Arrow key to skip the initial animation 
after skipping the animation, press Enter to bring eye tracker view to the participant monitor. 
- C for Calibration.
- V for Validation
