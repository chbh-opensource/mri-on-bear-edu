# MRI-on-BEAR

Welcome to the MRI-on-BEAR website, a freely available resource created by researchers at the [Centre for Human Brain Health](https://www.birmingham.ac.uk/research/centre-for-human-brain-health), University of Birmingham. The website is made for students on the 'Magnetic Resonance Imaging in Cognitive Neuroscience' course, but may be useful to students and researchers outside. However, please BEAR in mind that the course materials were designed to run on computing resources at the University of Birmingham. 

This README is primarily for students, and will help you navigate the course materials and get started with the practical workshops.

## Course Overview

The series of workshops collectively provide a comprehensive introduction to Magnetic Resonance Imaging (MRI) techniques in cognitive neuroscience, including the analysis of diffusion and functional magnetic resonance imaging (fMRI) data. In doing so, you will also learn how to access the BEAR Portal, BlueBEAR and basic programming skills required for working with neuroimaging data (e.g., Linux commands and bash scripting). 

## Workshop Schedule

The MRICN course during Spring Term 2024-25 will have the following dates:

<div align="center">

| **Week** | **Workshop** |
|:--------:|:------------:|
| Week 1 | No workshop |
| Week 2 | Introduction to BlueBEAR and Linux |
| Week 3 | No workshop |
| Week 4 | Basic MRI Skills |
| Week 5 | Basic diffusion MRI analyses |
| Week 6 | MRI demo (optional) |
| Week 7 | Advanced diffusion MRI analyses |
| Week 8 | First-level fMRI analysis |
| Week 9 | No workshop (Reading Week) |
| Week 10 | Higher-level fMRI analysis |
| Week 11 | Bash scripting and statistical analysis of fMRI data |
| Week 12 | Functional connectivity (optional) |

</div>

Workshops will be held at Computer Room (x), Gisbert Kapp, School of Psychology during all weeks with the exception of Weeks 6 and 12.

## Getting Started

Before the first workshop, it is important that you have access to the BlueBEAR system. Instructions on how do do so can be found on the website (see the 'Getting Started' page). 

Whilst not mandatory, additional resources related to the course can also be found on the website (see the 'Resources' page).


## Support and contact

If you encounter any issues or have questions please contact the following:

For any general issues relating to the course, assignments, absences etc:

- <b>Dr Magda Chechlacz</b> (Module Lead) [m.chechlacz@bham.ac.uk](mailto:m.chechlacz@bham.ac.uk)

For any issues relating to IT, including access to BlueBEAR, VPN access etc:

- <b>Charnjit Sidhu</b> (Lead Computing Officer, CHBH) [c.sidhu@bham.ac.uk](mailto:c.sidhu@bham.ac.uk)

For any issues relating to the course website or the associated GitHub repository:

- <b>Aamir Sohail</b> (PhD Student) [axs2210@bham.ac.uk](mailto:axs2210@bham.ac.uk)

Please try to contact us within working hours 9am-5pm!

## Contributing 

We welcome contributions from students and the wider community both at the CHBH and beyond! To do so, please follow the instructions below.

### Creating a Development Environment and Installing `mkdocs`

You will firstly need to re-create the website locally. The website is built using [MkDocs](https://www.mkdocs.org/), which is nice and easy to work with. After cloning the repository, to install all the required `mkdocs` Python packages, use the provided requirements.txt file within the root of this repository. The recommendation for development is to do this inside a dedicated virtual environment. All of these steps can be done using the commands below:

```shell
git clone https://github.com/chbh-opensource/mri-on-bear
cd mri-on-bear
python -m venv ./.venv
source ./.venv/bin/activate
pip install -r requirements.txt
```

### Building

To build the documentation, simply use:

```shell
mkdocs build
```

### Testing

To test whether the documentation is building correctly, and whether all (internal) links are correct, use:

```shell
mkdocs build --strict
```

This command will exit with a non-zero exit code if `mkdocs` produces any errors or warnings.

### Previewing

To see a local preview of the rendered documentation in your browser, use

```shell
mkdocs serve
```

or in the off chance that you are already running a `localhost`, use:

```shell
mkdocs serve -a localhost:XXXX
```

and click the link that is provided, for example:

```shell
INFO     -  Documentation built in 0.24 seconds
INFO     -  [17:52:07] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO     -  [17:52:07] Serving on http://127.0.0.1:8000/
```

This preview of the rendered documentation will automatically refresh when the documentation sources are updated!

### Pushing the changes using git

After you have made your changes, you can then push them to the `main` branch:

```shell
git status # check your changes here
git add .
git commit -m "brief description of your changes"
git push origin main
```

We will then review your changes and merge them if we deem them worthy!

### Issues

If you have an idea for the website, or have highlighted a bug, but would prefer that we did the work, feel free to open an issue!

## LICENSE

All content in this repository is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0) license. See LICENSE for more details.