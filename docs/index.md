# Magnetic Resonance Imaging in Cognitive Neuroscience (MRICN), Spring 2025

Welcome to the website covering the practical workshops for the MRICN module at the University of Birmingham! 

The practicals are two hour workshops scheduled in computer labs on campus to give hands-one experience of using BlueBEAR (university supercomputer), Linux and FSL tools for MRI data analysis. The workshops will be accompanied by pre-session materials, please make sure that you review the relevant materials prior to attending workshops (see week-by-week materials). In some weeks you will be asked to complete simple tasks ahead of workshop and in some weeks complete pre-session readings or review workshop notes.

## Aims and learning outcomes

### Aims
* To have a broad understanding of the use of MRI for mapping structural and functional brain organisation in cognitive neuroscience, both in theory and in practice.

### Learning outcomes
At the end of the course you will be able to:

* Demonstrate an understanding of the basic concepts involved in MRI
* Show an understanding of how to design fMRI experiments
* Have the ability to work with BlueBEAR in a Linux environment and to use appropriate software to view and interpret MRI data
* Be able to analyse simple fMRI experiments and conduct basic tractography analysis

---

## Note

!!! note "Note"
    This website is intended for current staff and students at the [Centre for Human Brain Health](https://www.birmingham.ac.uk/research/centre-for-human-brain-health/index.aspx) and [University of Birmingham](https://www.birmingham.ac.uk/). It is not likely to be useful for anyone else...

## Example code block

Here's an example of a basic FSL analysis script:

```bash
#!/bin/bash

# Set up FSL environment
. /etc/fsl/5.0/fsl.sh

# Define input and output
INPUT_FILE="sub-01_func.nii.gz"
OUTPUT_DIR="fsl_results"

# Create output directory
mkdir -p $OUTPUT_DIR

# Run brain extraction
bet $INPUT_FILE $OUTPUT_DIR/brain_extracted -F

# Run motion correction
mcflirt -in $INPUT_FILE -out $OUTPUT_DIR/motion_corrected

# Run spatial smoothing
susan $OUTPUT_DIR/motion_corrected $OUTPUT_DIR/smoothed 3 3 3 1 1 1

echo "FSL analysis complete!"
```

## Example image 

<p align="center">
  <img src="assets/images/chbh_logo.jpg" alt="CHBH Logo" width="150" height="100">
</p>