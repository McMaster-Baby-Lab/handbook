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

## What is eye tracker?

Eye tracker is a specialized camera system. It takes hundreds of pictures of participants eyes every second and translates these images into coordinates on the screen based on the the shape of the pupil and the position of reflection from the corneal.

## The most important things

To achieve high-quality eye tracking, it requries high-quality eye images. Just like every camera system (e.g., the ones in your phone), having camera lens in focus is the most important thing. However, eye tracking system does NOT (and should not) have auto-focus functions that we are used to on our phones, keeping participants' eyes in focus depends on a few factors:
- ***whether their distance to the screen is optimal***
- ***whether they are siting within the tracking area of the camera***
- ***whether they are facing the camera with opening eyes***

Luckily, you can read all of the information from the eye tracker screen.

{% include oneImg.html url="assets/images/eyetracking/Focus.jpg" caption = "" shortCap="" %} 

{: .important }
> Always remember that your participants are unlikely to know how eye tracker works or what are the key factors to ensure good tracking.
>
> As an experimenter, you should be explicit about the things participants should pay attention, and remind them whenever necessary.
>
> When it comes to infant / child studies, you need to communicate the key factors above to the parents who are holding their kids in front of the screen. ***Let parents help you to achieve good tracking quality is very very important!*** 

## EyeLink quick tips 

### Preparation 

Things to check before starting the program for a study. 

- Ensure participants are sitting comfortably in the chair  
- Ensure their posture is straight 
- Have them face the monitor

- Check the distance, ideally between **500 to 700 mm**
- Ensure there is a stable detection of the target sticker and both eyes (i.e., no flicking)  
- The participant's head should be at the centre of the tracking area
- Check the volumes on the speaker to ensure it is not too loud or quiet.

### Adjust thresholds

To prperly translate eye images into looking coordinates, eye tracker relies on a set of thresholds to detect pupil and corneal reflection.

In most of cases, the eye tracker will automatically adjust the thresholds for pupil and corneal reflection detection. However, the automatic adjustment might not work sometimes. If this happens, you need to adjust the thresholds manually by pressing the adjustment keys.

When the Pupil is properly thresholded (i.e., fully filled in blue with no additional blue in the iris), its threshold value should be at least 75. If lower than 75, the eye needs more illumination. The level of illumination can be adjusted via the Illuminator Power setting on the Camera Setup screen, and / or by moving the illuminator closer to the participant.

Once the illumination is adjusted, make sure the Corneal Reflection is properly thresholded (fully filled in light-blue with no additional thresholding in the sclera) without worrying too much about its threshold value, as long as it is below 255.

{% include oneImg.html url="assets/images/eyetracking/Thresholds.JPG" caption = "" shortCap="" %} 

### Calibration 

Lets the machine knows how to translate eye images into gaze coordinates on the screen

1. Both eyes should be tracked (i.e., there should be green and blue crosses on both eyes) 
2. When calibration starts, confirm fixation *IMMEDIATELY AFTER* the eyes move by pressing the Return key.  
3. Valid key pressing during calibration will make the target appears in another location 
4. Press again if a key pressing calibration is not valid 
5. At the end of calibration, the looking pattern indicated by the green and blue crosses should match the layout of calibration target on the screen.  If not, restart the calibration.  

{% include oneImg.html url="assets/images/eyetracking/Calib2.JPG" caption = "" shortCap="" %} 

### Validation

Verifies the accuracy of calibration

- Operates similarly to calibration 

- Watch the size of error (indicated by the length of white lines) for each target location.  
    - The smaller the error the better. 
- Both eyes should have GOOD results.  
- If not, either redo the calibration (when participants looked very attentively during validation) 
- Or redo the validation, if participants move their bodies during the validation


### Drift Correction 

Monitoring the tracking accuracy **amid** a study 

- Operates similarly to calibration and validation
- Pressing the Return key to confirm participants' looking 
- An accurate drift correction will allow the study to continue 
- If the error is too large (i.e., long white lines), we need to redo calibration & validation 

## Starting the Program 

### for PsychoPy studies on Windows system
- Open VsCode (u can put like a symbol here)
- Open up your project folder with **File -> Open Recent...** function. 
- Then, look for your project folder name.
- Then bring up Terminal in VSCode with **View -> Terminal function.** You will see a Terminal panel appears at the bottom.
- Use Up Arrow key to navigate to the specific file. Once found the file, press Enter/Return key to run the program
- Now you will see a Welcome window showing up. The window lists several key information, such as participant ID. Note the ID down!! 
- Click OK to start the program.

### for MATLAB studies on Linux system
- Open ***MATLAB*** from the Dock
- In MATLAB, navigate to the program folder in the address bar
- In the folder panel on the left-hand side, right-click the program file. Click ***Run*** in the pop-up menu to launch the program
- Pay attention to the instructions in the ***Command Window*** at the bottom.


## Eye-tracker operation short-cuts

When you're at the eye-tracker preparation screen (before experimental trials start).
- ***C*** for Calibration
- ***V*** for Validation
- ***Return*** for confirming looking during calibration, validation & drift-correction.
- ***O*** for starting experimental trials

## Tutorials

- <a href="https://mcmasteru365.sharepoint.com/:f:/r/sites/labtest/Shared%20Documents/Resources/EyeTracking/EyeLink%201000%20Plus%20Intro%20videos?csf=1&web=1&e=fiarbn" target="_blank">EyeLink Intro Videos</a>
