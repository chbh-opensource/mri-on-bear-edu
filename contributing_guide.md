# Contributing to MRI in Cognitive Neuroscience Course Website

We welcome contributions to improve and expand the course content. This guide will walk you through the process of making changes, and submitting them for review.

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

Example: If you've added a file `docs/workshop2/new-topic.md`:

```yaml
nav:
  - Workshop 2 - Basic MRI Skills:
    - Different MRI file formats: workshop2/mri-file-formats.md
    - Visualizing MRI data with fsleyes: workshop2/visualizing-mri-data.md
    - Atlases, masks and regions of interest: workshop2/atlases-masks-roi.md
    - New Topic: workshop2/new-topic.md  # Add this line
```

## Changing the Name of a Section or File

Rename the markdown file in the docs/ directory.
Update all internal links in other markdown files that pointed to the old filename.
Update the mkdocs.yml file to reflect the new filename.

Example: If you're renaming docs/workshop2/mri-file-formats.md to docs/workshop2/mri-formats.md:

```yaml
nav:
  - Workshop 2 - Basic MRI Skills:
    - Different MRI formats: workshop2/mri-formats.md  # Update this line
    - Visualizing MRI data with fsleyes: workshop2/visualizing-mri-data.md
    - Atlases, masks and regions of interest: workshop2/atlases-masks-roi.md
```

## Reorganizing the Structure

- Move markdown files to their new locations in the docs/ directory.
- Update the mkdocs.yml file to reflect the new structure.
- Update all internal links in the markdown files to point to the correct new locations.

Example: If you're moving some Workshop 2 content to a new "Advanced Topics" section:
```yaml
nav:
  - Workshop 2 - Basic MRI Skills:
    - Different MRI formats: workshop2/mri-formats.md
    - Visualizing MRI data with fsleyes: workshop2/visualizing-mri-data.md
  - Advanced Topics:
    - Atlases, masks and regions of interest: advanced/atlases-masks-roi.md  # Moved file
```

## Adding Images

Place image files in the `docs/images/` directory.
Reference images in your markdown files using relative paths:

`![Image Description](../images/your-image.png)`