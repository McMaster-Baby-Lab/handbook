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

Our research relies heavily on computers. To a large extend, the ability to use computers deterimes the quality of our research. In our lab, programming refers to using computer scripts to design research experiments, analyzing research data, and/or accomplish research-related tasks (e.g., creating experimental materials). What makes it different from using software via Graphical User Interface (GUI) is the emphaise on computer scripts, which look like text files. Scripts record every step of our thinking, thus playing a key role in ensuring the reproducibility of our research. The following are the principles of programming in our research projects.


## Learn and practice by yourself
Though computer skills are so important in scientific research, it's nearly impossible to master them by taking classes or reading textbooks. After learning basic syntax, you should start practice with code examples. There are tons of them available online. Then, you can write your own scripts by using existing ones as templates. Learning computer languages is much easier than learning a natural language. In coding practices, you will receive instant feedback, which can be addictive.


## Question driven approach
The functions of any computer language are overwhelming. It is not possible or necessary to learn them all. Since our work is never about computer sciences, we should focus computer skills on addressing specific questions. This often require us to analyze our questions by breaking a big complex question into several operational steps. With these questions and possible solutions in mind, you will seek how to **translate** these question and solutions into computer scripts.

{: .note }
> When it comes to searching for solutions, you should treat what you find cautiously.
> - Solutions are specific to certain software versions. Software is constantly evolving, sometimes making previous solution no longer valid for an issue in a more recent version.
> - Before copy-and-paste a piece of code, you should fully understand the purpose of each line of the code.
> - Attach the source of a solution as a comment in your code.

## General procedures for programming experiments

Programming an experiment is one of the major areas that we use scripts. Given the complexity of an experiment, the script often needs to control a wide range of functions, such as audio-visual presentation, timing control, communication with external devices (e.g., eye tracker & NIRS). Programming could become overwhelming especially if this is your frist projects. The following are some general steps for prgramming an experiment.

### Start with the basic unit of an experiment

The most common structure of psychological experiment involves repeating similar stimuli presentation over multiple times. We refer the stimuli presentation component as ***trial***, which should be the most basic unit of an experiment. Thus, it is important to identify what are included within a ***trial***. For example, a trial can start with a fixation cross, followed by a presentation of an image for 3 seconds. During the image presentation, record which key participants pressed on keyboard.

At this stage, focus on these things:
- identify the key variables within a trial (e.g., specific image file, duration)
- ensure the trial runs as expected

Meanwhile, you DON'T need to consider complexed features, such as how to commuicate with eye tracker / NIRS (e.g., start recording, sending messages).

### How to repeat trials

Once you have a functional trial component, the next thing is to create a loop to repeat the same stimuli presentation structure with changing variables. Here, on every trial, you are expected to assign new values to the variables set within the trial component.

### Including a section / function / component to control variables

The next question is how to create the values of each variables for each trial at the beginning of a study. It would be ideal to have a component, section of code, or function specifically generating values per trial. Here, you will need to consider the organization of values (e.g., fully or pseudo randomized across trials, block variables, etc).

### Collecting data (if applicable)

We need to save two type of information by the end of each trial:
- key variables to indicate what was shown in each trial
- participants' response, such as key pressing and reaction time

It's ideal to save the data in the form of spreadsheet (e.g., .csv file). It is also helpful to save all experiment variables (generated in the previous step) as original data.

### Instructions & practice sections (if applicable)

At to this point, your program should be able to run as expected. It is the time to include instructions to the experiment. There are two types of instructions: those for participants and those for experimenters. The former should inform participants what's about to happen (e.g., please take a break). The latter will be shown in Experimenter's computer to indicate experiment status and / or how to control the program (e.g., press Enter to proceed).


### Adding complex features

The program should be fully functional as a traditional behavioural experiment. Most of our studies associate with other devices, such as eye tracker and NIRS, which often require additional fucntions integrated into an experiment. For example, in an eye tracking study, we need to know where participants are looking at to determine what stimuli to present. These communication with other devices involves adding additional codes to your program. You should check some official examples to learn how to achieve these complex functions.



## Code efficiency is NOT that important
Tinkering your codes to make it run faster is always a fun thing to do. Though it definitly will make feel good about yourself, it often costs much time. Given that our research uses codes, rather studies them, we should refrain ourselves from spending too much time on code efficiency. **As long as a script can deliver the function we need, it's good enough.** What's the point of exchanging hours of label for an improvement for a few seconds? If code efficiency really matters, we tend to solve it with money (rather than your time).

## Review your codes
Not every wish comes true. Not every line of code does what we intended to do. A good practice is to have someone to review your codes. It's fun to do it as a group, which provides the best learning opportunities.

## Focus on ONE language
Most of our needs for computer are not that special, and can be fulfiled by multiple languages. Again, mastering a computer language is not our goal. As long as you're comfortable with a language (e.g., R, Python, and MATLAB), stay with it. Focusing on one language allows you to have a deeper understanding of how computer language works. These knowledge will help you learn other languages faster, when you really need to.


## Use the BEST (free) tools
We are professional, so are the tools. Luckly, nearly all the tools for coding are free. Here are a few to consider:

For general code editing
- **[Visual Studio Code](https://code.visualstudio.com/)**

For data analysis
- **[RStudio](https://posit.co/download/rstudio-desktop/)**
    
    You will need to install [R langugae](https://www.r-project.org/) first.
- **[MATLAB](https://posit.co/download/rstudio-desktop/)**

    [McMaster offers free copies to students](https://www.mathworks.com/academia/tah-portal/mcmaster-university-31501097.html)
- **[Python](https://www.python.org/)**
    
    Python is very popular but sometimes confusing. Make sure you are running it in virtual environments like [Conda](https://docs.conda.io/projects/conda/en/stable/index.html).

For experiment design
- **[Psychtoolbox](http://psychtoolbox.org/)**

    We use Psychtoolbox for in-lab studies. It works well with Eye Link eye trackers used in the lab. Psychtoolbox relies on `MATLAB`.

- **[PsychoPy](https://www.psychopy.org/)**

    We use PsychoPy for online studies. You will use `JavaScript`to code online studies.

- **[Arduino](https://www.arduino.cc/)**

    We use Arduion and its accessories to design specifically purposed studies. To interface with Arduino, you will use `C++`.

For code management and sharing
- **[GitHub](https://github.com/)**
- **[GitLab](https://gitlab.com/)**
- **[Open Science Foundation](https://osf.io/)**

    Make sure your repositories stay `private` before you're ready to share them.

## Stay hungry. Stay foolish.
Technology evolves rapidly. We should always thinking about how emerging technology can guide our reasoning and make us a better researcher.