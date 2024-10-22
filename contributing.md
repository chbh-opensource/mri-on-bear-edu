# Contributing to MRI in Cognitive Neuroscience Course Website

We welcome contributions to improve and expand the course content. This guide will walk you through the process of setting up your environment, making changes, and submitting them for review.

## Setting Up Your Environment

1. Fork the repository on GitHub.

2. Clone your fork locally:
```bash
git clone https://github.com/your-username/mri-on-bear.git
cd mri-on-bear
```

3. Set up a remote to the original repository:
`git remote add upstream https://github.com/original-owner-username/mricn.git`

4. Create and activate a virtual environment:

On macOS and Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

On Windows:
```bash
python -m venv venv
venv\Scripts\activate
```

5. Install the required packages:
`pip install -r requirements.txt`

## Making Changes

1. Ensure your main branch is up-to-date:
```bash
git checkout main
git pull upstream main
```

2. Create a new branch for your changes:
`git checkout -b your-branch-name`

3. Make your changes to the Markdown files in the `docs/` directory.

4. To preview your changes locally, run:
`mkdocs serve`then open `http://localhost:8000` in your web browser. The site will automatically update as you save changes to the files.

5. Once you're satisfied with your changes, stage and commit them:
```bash
git add .
git commit -m "Description of your changes"
```

## Submitting Your Changes

1. Push your branch to your fork on GitHub:
`git push origin your-branch-name`

2. Go to the original repository on GitHub and create a new pull request from your branch.
3. Fill out the pull request template, describing your changes in detail.
4. Submit the pull request for review.
5. If requested, make any necessary changes and push them to your branch. The pull request will update automatically.

## After Your Pull Request is Merged

1. Switch back to your main branch:
`git checkout main`

2. Delete your local branch:
`git branch -d your-branch-name`

3. Update your main branch:
`git pull upstream main`

4. Push the changes to your fork:
`git push origin main`

# Making Changes to Content and Structure

This guide explains how to modify content, add new pages, and change the structure of the website.

## Modifying Existing Content

1. Navigate to the appropriate markdown file in the `docs/` directory.
2. Open the file in a text editor.
3. Make your changes, using Markdown syntax.
4. Save the file.
5. Preview your changes using `mkdocs serve`.

## Adding New Content

1. Create a new markdown file in the appropriate subdirectory of `docs/`.
2. Add your content to the new file, using Markdown syntax.
3. Update the `mkdocs.yml` file to include the new page in the nav section.

Example: If you've added a file `docs/week4/new-topic.md`:

```yaml
nav:
  - Week 4 - Basic MRI Skills:
    - Different MRI file formats: week4/mri-file-formats.md
    - Visualizing MRI data with fsleyes: week4/visualizing-mri-data.md
    - Atlases, masks and regions of interest: week4/atlases-masks-roi.md
    - New Topic: week4/new-topic.md  # Add this line
```

## Changing the Name of a Section or File

Rename the markdown file in the docs/ directory.
Update all internal links in other markdown files that pointed to the old filename.
Update the mkdocs.yml file to reflect the new filename.

Example: If you're renaming docs/week4/mri-file-formats.md to docs/week4/mri-formats.md:

```yaml
nav:
  - Week 4 - Basic MRI Skills:
    - Different MRI formats: week4/mri-formats.md  # Update this line
    - Visualizing MRI data with fsleyes: week4/visualizing-mri-data.md
    - Atlases, masks and regions of interest: week4/atlases-masks-roi.md
```

## Reorganizing the Structure

- Move markdown files to their new locations in the docs/ directory.
- Update the mkdocs.yml file to reflect the new structure.
- Update all internal links in the markdown files to point to the correct new locations.

Example: If you're moving some week 4 content to a new "Advanced Topics" section:
```yaml
nav:
  - Week 4 - Basic MRI Skills:
    - Different MRI formats: week4/mri-formats.md
    - Visualizing MRI data with fsleyes: week4/visualizing-mri-data.md
  - Advanced Topics:
    - Atlases, masks and regions of interest: advanced/atlases-masks-roi.md  # Moved file
```

### Adding Images

Place image files in the `docs/images/` directory.
Reference images in your markdown files using relative paths:

`![Image Description](../images/your-image.png)`