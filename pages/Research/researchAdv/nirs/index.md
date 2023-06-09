---
layout: default
title: Near infrared spectroscopy (NIRS)
parent: Device Specific Info
grand_parent: Research
nav_order: 2
permalink: /nirs
---

# Near infrared spectroscopy
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

* TOC
{:toc}

---

{: .warning}
> You are our treasure. But the easiest way to hurt yourself is to stare at the sensors (when they emit red lights). DON'T.
>
> Also, fNIRS machine is ridculously expensive. The one we are using costed **half a million**. The best ways to break the sensor cables (THEY ARE OPTIC FIBRES) are to FOLD or TANGLE them. DON'T.

## How does fNIRS measure brain activity?
FNIRS (functional Near Infrared Spectroscopy) is a safe and non-invasive technique for measuring localized blood flow/volume in the human brain. FNIRS employs nearly identical methods to the pulse oximeter, which has been employed extensively for decades in clinical settings to monitor blood oxygen levels during surgery and for high-risk individuals during hospitalization (e.g., infants born prematurely). This technique has been widely used in our every life. Apple Watch or similar wearable health-tracking devices also use this technique to monitor blood flow changes.
 
Specifically, fNIRS is based on the fact that hemoglobin absorbs near-infrared wavelengths in proportion to the state of blood oxygenation. Importantly, brain activation is correlated with increased metabolic demand, and the ratio of oxyhemoglobin/deoxyhemoglobin concentration has been shown to be a reliable index of neural activity. These changes in blood oxygenation are also the physiological correlate of neural activity used in fMRI (functional Magnetic Resonance Imaging) recordings. FMRI employs a combination of fluctuations in magnetic fields and radio waves are used to measure changes in blood oxygenation in the brain. Thus, fNIRS records similar physiological signals as fMRI while using light. 
 
FNIRS works by shining a near-infrared light source (delivered via fiberoptic) onto the exterior of the scalp and using a photodetector to sample the variations in light scattered back from the brain surface. 

{: .important }
> If you are new to this technique, we highly recommend you to watch this tutorial video by Dr. Sagi Jaffe-Dax from Hebrew University of Jerusalem: <a href="https://mcmasteru365.sharepoint.com/:v:/r/sites/labtest/Shared%20Documents/Resources/fNIRS/NIRS%20background%20training%20videos%20from%20Sagi/1-Intro%20to%20fNIRS%20(Sagi%20Jaffe-Dax).mp4?csf=1&web=1&e=Nbx8ZI" target="_blank">Introduction to fNIRS</a>  

## Safety with fNIRS
FNIRS has been used to study perceptual and cognitive processing in adults and infants for over 20 years. There are no known medical risks associated with fNIRS because the light source(s) are not intense (less than 1 mw/cm2), the light sources are largely transparent to biological tissue (i.e., there is insufficient absorption to cause heating), and the light source(s) and photodetectors are placed on the surface of the scalp using a comfortable headband.  
 
## The most important things
Like any measurement, being reliable is crutial. Though fNIRS is believed to have higher motion tolerrance than other neuroimaging measures, its data suffer greatly by participants' body and head movements. Specifically, these movements would likely to loose the contact between sensors and the scalp, causing infrared light not being able to emit to or receive from the brain tissues properly. These data noises introduced by motion is referred to as motion artifacts. Thus to reduce motion artifacts is one of the most important things for fNIRS studies, especially with infants.

Here are a few strategies mitigating the impact of motion from infant participants:
- ***Make sure the cap covers the full head***
- ***After placing the probes on the target region, tight the chin strap to secure the cap on participants' head***
- ***Use the elastic strips to improve the contact between sensors and the scalp***
- ***Ask parents to help control their children's movement***

## How to prepare a fNIRS study with infants?

### Prepare the machine

{: .important }
> The ***Laser*** switch needs warm-up for at least ***30-mins before any measure starts***.


1. Turn on NIRS machine (see section 3-1 in <a href="https://mcmasteru365.sharepoint.com/:b:/r/sites/labtest/Shared%20Documents/Resources/fNIRS/HITACHI%20ETG4000/ETG4000_manual.pdf?csf=1&web=1&e=0CUxdf" target="_blank">ETG-4000 Operation Manual</a>)
    1. Make sure Power switch and Laser switch are set to OFF 
    2. Turn on Main switch at the back 
    3. Turn on Power switch in the front 
    4. Turn on Laser switch in the front 
2. Prepare the recording cap
    1. Check the sensor placement with the probe layout showing on the machine
    2. Fibers should not be tangled
3. Input participant information (ID, name, age, gender)
4. Check camera
    1. if the tap has been rewinded to the beginning

### NIRS machine parameters examination

The NIRS machine sometimes will reset its parameters to default setting, which would result in issues such as losing stimuli marks and trial numbers. Given the fact that we have no clue how this happens, we need to double-check the settings of the NIRS before collecting any data. This parameter examination is very simple, requiring two steps: 

1. Check Stimuli Record Type. 
    1. Click **“Operation Measurement Event”** button 
    2. In the pop-up menu, make sure there is a “√” in front of **Event** 
    3. If **“Event”** is not checked, check it by clicking. 

2. Load parameter preset. 
    1. Click **“Parameter Set Serial”** button 
    2. In the pop-up window **“Parameter”**, there is a dropped-down box at the top, named **“parameter Name”**
    3. In this drop-down box, select **“Infant VS preset”** and click Import button. 

{% include imageGallery.html folder="assets/images/fNIRSprocedure" %}

### Starting study program on the experiment computer
- Open ***MATLAB*** from the Dock
- In MATLAB, navigate to the program folder in the address bar
- In the folder panel on the left-hand side, right-click the program file. Click ***Run*** in the pop-up menu to launch the program
- Pay attention to the instructions in the ***Command Window*** at the bottom.

## Typical procedures for NIRS study with infants
### Placing the cap on the participant

**E2:** 
- Use a toy to distract the participant’s attention 
- Bring the cap over the parent's shoulder
- Collect the NIRS cap cables with the velcro on the cable belt 

**E1:** 
- Put the NIRS cap on the participant 
- Make sure the cap is on the right spot and fasten the cap 


### Communicate with parents
- What is fNIRS and how does it help us understand the neural foundation of our cognitive abilities
- What will they and their children (i.e., participants) experience during a study

### Remind the parents of the following items
- Sit comfortably in the couch 
- Do not speak to infants and remain silent in the study 
- Do not shake their legs or tap infants in the study
- Hold infants to restrain their body movements 
- If infants try to grab the fiber or cap, try to remove their hands gently
- Silence their phones


## fNIRS training materials
https://mcmasteru365.sharepoint.com/:f:/r/sites/labtest/Shared%20Documents/Resources/fNIRS?csf=1&web=1&e=gXydeW


## Contents needed

- [] screenshots to explain UIs
- [] importance of checking the sensor placement before each studay starts
- [] what is AutoGain?
- [] how to accomendate different head sizes? Focus on the key channels. Identify the key channels in each study.
- [] troubleshooting, camera failure, program crash etc.
- [] setup camera
<!-- [a link](/nirs/manual).

[a link](/nirs/cameraprocedure).

[a link](/nirs/nirsprocedure).

[a link](/nirs/parametersExam).

[a link](/nirs/studyBreak). -->