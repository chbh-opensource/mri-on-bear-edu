# MRI-on-BEAR

![Documentation Status](https://img.shields.io/badge/docs-passing-brightgreen) [![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/) ![GitHub contributors](https://img.shields.io/github/contributors/chbh-opensource/mri-on-bear-edu) ![GitHub last commit](https://img.shields.io/github/last-commit/chbh-opensource/mri-on-bear-edu) 

![GitHub stars](https://img.shields.io/github/stars/chbh-opensource/mri-on-bear-edu) ![GitHub repo size](https://img.shields.io/github/repo-size/chbh-opensource/mri-on-bear-edu)

> 🎯 **Purpose:** A freely available resource for the 'Magnetic Resonance Imaging in Cognitive Neuroscience' course at the Centre for Human Brain Health

Welcome to the MRI-on-BEAR website, a freely available resource created by researchers at the [Centre for Human Brain Health](https://www.birmingham.ac.uk/research/centre-for-human-brain-health), University of Birmingham. The website is made for students on the 'Magnetic Resonance Imaging in Cognitive Neuroscience' course, but may also be useful to external students and researchers. However, please BEAR in mind that the course materials were designed to run on computing resources at the University of Birmingham!

This README is primarily for students, and will help you navigate the course materials and get started with the practical workshops.

## Table of contents

- [Course Overview](#course-overview)
- [Getting Started](#getting-started)
- [Support and Contact](#support-and-contact)
  - [Course-related Issues](#-course-related-issues)
  - [IT Support](#-it-support)
  - [Website Support](#-website-support)
- [Contributing](#-contributing)
  - [Development Setup](#-development-setup)
  - [Building](#building)
  - [Testing](#testing)
  - [Previewing](#previewing)
  - [Pushing the changes using git](#pushing-the-changes-using-git)
  - [Issues](#issues)
- [License](#license)

--- 

## Course Overview

The series of workshops collectively provide <b>a comprehensive introduction to Magnetic Resonance Imaging (MRI) techniques in cognitive neuroscience, including the analysis of diffusion and functional magnetic resonance imaging (fMRI) data</b>. In doing so, you will also learn how to access the BEAR Portal, BlueBEAR and basic programming skills required for working with neuroimaging data (e.g., Linux commands and bash scripting). 

Workshops will be held at Computer Room G19, Gisbert Kapp, at the School of Psychology.

## Getting Started

> ⚠️ **Important:** Before the first workshop, it is important that you have access to the BlueBEAR system. Instructions on how do do so can be found on the website (see the 'Getting Started' page). 

Whilst not mandatory, additional resources related to the course can also be found on the website (see the 'Resources' page).

## Support and contact

If you encounter any issues or have questions please contact the following:

### 📚 Course-related Issues
- **Dr Magda Chechlacz** (Module Lead)
  - 📧 [m.chechlacz@bham.ac.uk](mailto:m.chechlacz@bham.ac.uk)

### 💻 IT/Computing Support
- **Charnjit Sidhu** (Lead Computing Officer, CHBH)
  - 📧 [c.sidhu@bham.ac.uk](mailto:c.sidhu@bham.ac.uk)

### 🌐 Website/GitHub enquiries
- **Aamir Sohail** (Module Teaching Assistant)
  - 📧 [axs2210@bham.ac.uk](mailto:axs2210@bham.ac.uk)

> ⏰ Please contact us during working hours (9am-5pm)!

## 🛠️ Contributing (for CHBH staff)

If you teach on the course, or are staff member at the CHBH and could like to contribute to the website, please follow the instructions below.

### 🔧 Development Setup

You will firstly need to re-create the website locally. The website is built using [MkDocs](https://www.mkdocs.org/), which is nice and easy to work with. After cloning the repository, to install all the required `mkdocs` Python packages, use the provided `requirements.txt` file within the root of this repository. The recommendation for development is to do this inside a dedicated virtual environment. 

All of these steps can be done using the commands below:

```shell
git clone https://github.com/chbh-opensource/mri-on-bear
cd mri-on-bear
python -m venv ./.venv
source ./.venv/bin/activate
pip install -r requirements.txt
```

This assumes that you have push access. If you do not, you will need to `git clone` from your own GitHub account:

`git clone https://github.com/YOUR-USERNAME/mri-on-bear`

The subsequent steps remain the same.

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

After you have made your changes, you can then push them to the `main` branch.

If you have direct push access:

```shell
git status # check your changes here
git add .
git commit -m "brief description of your changes"
git push origin main
```

If you do not have direct push access:

```shell
git checkout -b feature/your-feature-name
git status
git add .
git commit -m "brief description of your changes"
git push origin feature/your-feature-name
```

You will then need to create a pull Request:

1) Go to the original repository at https://github.com/chbh-opensource/mri-on-bear
2) Click "Pull Requests" > "New Pull Request"
3) Click "compare across forks"
4) Select your fork and branch
5) Click "Create Pull Request"
6) Fill in the description of your changes
7) Submit the pull request

We will then review your changes and merge them if we deem them worthy! 👀 ✨

### Issues

If you (e.g., students, externals) have an idea for the website, or have highlighted a bug, but would prefer that we did the work, feel free to open an issue!

## LICENSE

All content in this repository is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/) (CC BY-SA 4.0) license. See the `LICENSE` for more details.