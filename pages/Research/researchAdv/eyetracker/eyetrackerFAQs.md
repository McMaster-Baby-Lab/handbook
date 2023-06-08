---
layout: default
title: Eye tracker FAQs
parent: Eye Tracker
grand_parent: Device Specific Info
nav_order: 1
permalink: /eyetracking/FAQs
---

# Eye tracker FAQs
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

* TOC
{:toc}

---

## How often should I calibrate?

You should calibrate your participant before you start recording and only recalibrate if you need to. Drift-checks can be used between trials / blocks of trials to check whether the current calibration model is still accurate. If there is an offset between the gaze cursor and the drift check target (which is not corrected by asking the participant to look at the target) then the ESC key can be pressed and a new calibration performed. 

Recalibrating in the absence of any indication that the current calibration model is inaccurate risks replacing a good calibration model with a less good model.

## Can the EyeLink systems be used with participants who are wearing glasses?

While some adjustments may be required, glasses should not present any issue. The lenses of the glasses can reflect the IR illumination back into the camera, which appears as glare. If this glare occurs near or in front of the Pupil and / or Corneal Reflection, it can disrupt tracking. With the Desktop mount in Head-Stabilized mode, this can usually be avoided by having the participant tilt their head up or down a little, thus changing the angle of the glasses so reflection shifts away from the Pupil / Corneal Reflection.

With some glasses, it's possible that the eye tracker may suddenly try to track part of the glasses frame. This typically occurs when there is a small reflection that gets mistaken for the Corneal Reflection. This can be prevented by enabling the Search Limits feature (make sure Use Search Limits is highlighted on the Camera Setup screen), then resizing the size of the limiting ellipse so that it fits entirely within the frame of the glasses and excludes the problematic reflection. The Search Limits can be resized by holding down the ALT key and pressing the arrow keys on the Host PC keyboard. Be sure not to make the Search Limits any smaller than the green box which bounds the eye.

In Remote mode, glasses are typically fine, but with the caveat that since the participant is free to move their head, they may move into a position where the glare off the lenses which can disrupt tracking.

{% include oneImg.html url="assets/images/eyetracking/glasses.jpeg" caption = "" shortCap="" %} 


## Can the EyeLink systems be used with participants who are wearing contact lens?

Most soft contact lenses (i.e. most daily and monthly contacts) will have absolutely no impact on eye tracking. Some heavily tinted contacts may make it difficult to get proper thresholding of the pupil, but these are not common. Hard contact lenses, however, will almost certainly cause problems because they are smaller than soft contact lenses and tend to float around as the eye moves. As a result, the corneal reflection may not be in a predictable location and the eye tracker can find it difficult to compute the center of the pupil if the edge of the lens is obscuring it. If possible ask participants who normally wear hard contact lenses to bring glasses instead.