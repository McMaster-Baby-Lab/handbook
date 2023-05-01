---
layout: default
title: test page
parent: Research
nav_order: 1
permalink: /tPage
---

# Typography
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Future updates
* check the distribution of initial seed. Possibly update the program.
* shorter event duration: (1.5 s?). Also related to shorter audio play (shorter than the 15% event duration)
* end an block when it reaches 5 successful iterations. Meanwhile, set the max number of trials per block to 7
* running the program until the max number of trials reaches 80.
* for child and infant studies, place an animation at the beginning of each iteration: targets moving from a certain location to their final location. Would be interesting to young participants.
* respond by pressing trigger button on a controller.
* the target will move to the next box but becomes transparent after 100 ms (before arrive at the next box)

## Update history
### *2023.03.25*
- reset initial seed at the beginning of each block. 10 blocks in total.

### *2023.03.18*
 - each trial takes 11 iterations, instead of 10. The calculation of interval will skip the first iteration.
 - option to continue practice trials or moving forward to experiment trials after each practice trial (11 iterations).


### *2023.03.17*
 - in practice trials, target presentations are isochronous. This will avoid any impact on the experimental trials.
 - looked-at target is showed by a golden circle, less confusing with the target.
 - instructions for experimenter on the experimenter screen. It will tell you what's on participants' screen and what you need to do, such as pressing the space bar.
 - 1.5s blank screen after each iteration, giving participants a little break.
minor bug fixes.

### *2023.03.14*
 - ***looking feedback***: successfully looking at the target will fill the target area with color
 - ***practice session***: a total of 10 iterations will start after calibration/validation. When the practice is over, press space bar to start real experiment.
 - ***force quit***: press delete key during target presentation will terminate the program upon the end of the current trial. Force quit will retain all data in the results folder
 - ***data organization***: participants' data are organized in a folder within the ***results*** folder
 - ***target area***: is now circle, rather than rectangle
