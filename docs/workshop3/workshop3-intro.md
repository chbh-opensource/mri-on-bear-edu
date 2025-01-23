# Workshop 3 - Basic diffusion MRI analysis

Welcome to the third workshop of the MRICN course! Prior lectures in the module introduced you to basics of the diffusion MRI and its applications, including data acquisition, the theory behind diffusion tensor imaging and using tractography to study structural connectivity. <b>The aim of the next two workshops is to introduce you to some of the core FSL tools used for diffusion MRI analysis.</b> 

Specifically, we will explore different elements of the [FMRIB's Diffusion Toolbox (FDT)](https://fsl.fmrib.ox.ac.uk/fsl/docs/#/diffusion/index) to walk you through basic steps in diffusion MRI analysis. We will also cover the use of Brain Extraction Tool (BET). 

By the end of the two workshops, you should be able to understand the principles of correcting for distortions in diffusion MRI data, how to run and explore results of a diffusion tensor fit, and how to run a whole brain group analysis and probabilistic tractography. 

!!! success "Overview of Workshop 3"
    Topics for this workshop include:

    - Visualizing diffusion data using FSLeyes (before and after distortion correction)
    - Using FSL's Brain Extraction Tool (BET) to create a brain mask
    - Performing diffusion tensor fitting (DTIfit) to generate key diffusion metrics like FA (Fractional Anisotropy) and MD (Mean Diffusivity)
    - Learning to conduct Tract-Based Spatial Statistics (TBSS) for group-level comparisons of diffusion data

We will be working with various previously acquired datasets (similar to the data acquired during the CHBH MRI Demonstration/Site visit). We will not go into details as to why and how specific sequence parameters and specific values of the default settings have been chosen. Some values should be clear to you from the lectures or assigned on Canvas readings, please check there, or if you are still unclear, feel free to ask. 

Note that for your own projects, you are very likely to want to change some of these settings/parameters depending on your study aims and design. 

<b>The copy of this workshop notes can be found on Canvas 39058 - LM Magnetic Resonance Imaging in Cognitive Neuroscience in Week 03 workshop materials.</b>