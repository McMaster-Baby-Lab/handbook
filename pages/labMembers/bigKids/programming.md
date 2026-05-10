---
layout: default
title: Programming
parent: Grad Students & Post-docs
grand_parent: For Lab Members
nav_order: 2
permalink: /gradsPostDocs/programming
---

{: .warning }
> WIP

# Programming
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

* TOC
{:toc}

---

Our research relies heavily on computers. To a large extent, the ability to use computers determines the quality of our research. In our lab, programming refers to using computer scripts to design research experiments, analyze research data, and/or accomplish research-related tasks (e.g., creating experimental materials). What makes it different from using software via a Graphical User Interface (GUI) is the emphasis on computer scripts, which look like text files. Scripts record every step of our thinking, thus playing a key role in ensuring the reproducibility of our research. The following are the principles of programming in our research projects.

## Learn and Practice by Yourself

Though computer skills are so important in scientific research, it's nearly impossible to master them by taking classes or reading textbooks alone. After learning basic syntax, you should start practicing with code examples. There are tons of them available online. Then, you can write your own scripts by using existing ones as templates. Learning computer languages is much easier than learning a natural language. In coding practices, you will receive instant feedback, which can be addictive.

{: .important }
> Like reading papers, reading other people's programs offers excellent opportunities to learn how to program. To enhance the learning process, it is recommended to question yourself about the purpose of each line or section of code. When encountering code that proves challenging to comprehend, it indicates an opportunity for further learning.
>
> Don't copy others' scripts without asking why. You are responsible for the code under your name.

## Question-Driven Approach

The functions of any computer language are overwhelming. It is not possible or necessary to learn them all. Since our work is never about computer science, we should focus our computer skills on addressing specific questions. This often requires us to analyze our questions by breaking a big, complex question into several operational steps. With these questions and possible solutions in mind, you will seek how to **translate** these questions and solutions into computer scripts.

{: .note }
> When it comes to searching for solutions, you should treat what you find cautiously.
> - Solutions are specific to certain software versions. Software is constantly evolving, sometimes making previous solutions no longer valid for an issue in a more recent version.
> - Before copy-and-pasting a piece of code, you should fully understand the purpose of each line of the code.
> - Attach the source of a solution as a comment in your code.

## General Procedures for Programming Experiments

Programming an experiment is one of the major areas that we use scripts. Given the complexity of an experiment, the script often needs to control a wide range of functions, such as audio-visual presentation, timing control, and communication with external devices (e.g., eye tracker and fNIRS). Programming could become overwhelming, especially if this is your first project. The following are some general steps for programming an experiment.

### Start with the Basic Unit of an Experiment

The most common structure of a psychological experiment involves repeating similar stimuli presentations multiple times. We refer to the stimuli presentation component as a ***trial***, which should be the most basic unit of an experiment. Thus, it is important to identify what is included within a ***trial***. For example, a trial can start with a fixation cross, followed by a presentation of an image for 3 seconds. During the image presentation, record which key participants pressed on the keyboard.

At this stage, focus on these things:
- Identify the key variables within a trial (e.g., specific image file, duration).
- Ensure the trial runs as expected.

Meanwhile, you DON'T need to consider complex features, such as how to communicate with the eye tracker / fNIRS (e.g., start recording, sending messages).

### How to Repeat Trials

Once you have a functional trial component, the next thing is to create a loop to repeat the same stimuli presentation structure with changing variables. Here, on every trial, you are expected to assign new values to the variables set within the trial component.

### Including a Section / Function / Component to Control Variables

The next question is how to create the values of each variable for each trial at the beginning of a study. It would be ideal to have a component, section of code, or function specifically generating values per trial. Here, you will need to consider the organization of values (e.g., fully or pseudo-randomized across trials, block variables, etc.).

### Collecting Data (If Applicable)

We need to save two types of information by the end of each trial:
- Key variables to indicate what was shown in each trial.
- Participants' responses, such as key pressing and reaction time.

It's ideal to save the data in the form of a spreadsheet (e.g., .csv file). It is also helpful to save all experiment variables (generated in the previous step) as original data.

### Instructions and Practice Sections (If Applicable)

By this point, your program should be able to run as expected. It is time to include instructions for the experiment. There are two types of instructions: those for participants and those for experimenters. The former should inform participants what is about to happen (e.g., "Please take a break"). The latter will be shown on the experimenter's computer to indicate experiment status and/or how to control the program (e.g., "Press Enter to proceed").

### Adding Complex Features

The program should be fully functional as a traditional behavioral experiment. Most of our studies are associated with other devices, such as eye trackers or fNIRS systems. Add these complex features once the core experiment is working correctly.
