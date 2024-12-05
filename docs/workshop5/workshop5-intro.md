# Workshop 5 - First level fMRI analysis

Welcome to the fifth workshop of the MRICN course! 

The module lectures provide a basic introduction to fMRI concepts and the theory behind fMRI analysis, including the physiological basis of the BOLD response, fMRI paradigm design, pre-processing and single subject model-based analysis. 

In this workshop you will learn how to analyse fMRI data for individual subjects (i.e., at the first level). This includes running all pre-processing stages and the first level fMRI analysis itself. 
<b>The aim of this workshop is to introduce you to some of the core FSL tools used in the analysis of fMRI data and to gain practical experience with analyzing real fMRI data.</b>

Specifically,  we will explore [FEAT](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/task_fmri/feat/index) (FMRI Expert Analysis Tool, part of FSL) to walk you through basic steps in first level fMRI analysis. 
We will also revisit the use of Brain Extraction Tool (BET), and learn how to troubleshoot problematic ”skull-stripping” for certain cases.

!!! success "Overview of Workshop 5"
    Topics for this workshop include:

    - Troblueshooting problematic skull-stripping by using BET options (recursive BET, `robustfov`)
    - Renaming fMRI data and understanding the importance of having suitable file names
    - Running a first-level fMRI analysis on single subjects using FEAT
    - Examining the processed fMRI data using the FEAT Report and FSLeyes

We will not go into details as to why and how specific values of the default settings have been chosen.
Some values should be clear to you from the lectures or resource list readings, please check there or if you are still unclear feel free to ask. 
We will explore some general examples. Note that for your own projects you are very likely to want to change some of these settings/parameters depending on your study aims and design. 

<b>The copy of this workshop notes can be found on Canvas 39058 - LM Magnetic Resonance Imaging in Cognitive Neuroscience in Week 05 workshop materials.</b>