# Project Guide for Mark Stapper's Blog

This guide provides an overview of the project structure, setup, and development workflow for Mark Stapper's Blog. The blog is built using MkDocs and Material for MkDocs, and it hosts articles, workshops, and developer-related content.

---

## Project Overview

### Purpose

This project is a personal blog and knowledge-sharing platform for Mark Stapper. It includes articles, workshops, and insights on software development, Scrum, and developer behavior. The content is written in Markdown and rendered as a static site using MkDocs.

### Key Technologies

- **MkDocs**: Static site generator for documentation.
- **Material for MkDocs**: Theme for MkDocs to enhance the site's appearance.
- **Markdown**: Content is written in Markdown format.
- **Python**: Required for running MkDocs and its plugins.

### High-Level Architecture

The project is structured as a static site generated from Markdown files. The site is organized into categories such as:

- **Developer Stances**: Articles and insights on developer behavior.
- **Connect**: Workshops and activities for team building.
- **Scrum 4 Kids**: Workshops and activities tailored for children.

---

## Getting Started

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git (for version control)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/starkmapper/starkmapper.github.io.git
   cd starkmapper.github.io
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows, use `.venv\Scripts\activate`
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### Running the Site Locally

To serve the site locally for development:

```bash
mkdocs serve
```

This will start a local server at `http://127.0.0.1:8000/`. The site will automatically reload when you make changes to the content.

### Building the Site

To build the static site for deployment:

```bash
mkdocs build
```

The generated site will be placed in the `site` directory.

### Running Tests

Currently, there are no automated tests for this project. However, you can manually verify the site by serving it locally and checking for rendering issues.

---

## Project Structure

### Overview of Directories

- **content/**: Contains all the Markdown files for the blog.
  - **Developer Stances/**: Articles and images related to developer behavior.
  - **Connect/**: Workshops and activities for team building.
  - **Scrum 4 Kids/**: Workshops and activities for children.
- **site/**: Generated static site files (output directory).
- **.venv/**: Python virtual environment (not committed to the repository).
- **docs/**: Symbolic link to the `content` directory (used by MkDocs).

### Key Files

- **mkdocs.yml**: Configuration file for MkDocs, including site settings, theme, and plugins.
- **requirements.txt**: List of Python dependencies required for the project.
- **Readme.md**: Overview of the project and its purpose.

### Important Configuration Files

- **mkdocs.yml**:
  - Defines the site name, URL, and repository.
  - Configures the Material theme with light/dark mode support.
  - Lists Markdown extensions and plugins (e.g., `git-authors`, `tags`).

---

## Development Workflow

### Coding Standards

- Use clear and concise Markdown syntax.
- Follow consistent naming conventions for files and directories.
- Include descriptive titles and headings in your content.
- Adhere to Markdown standards as enforced by `markdownlint`. Ensure your content passes linting checks to maintain consistency and readability.

### Adding New Content

1. Create a new Markdown file in the appropriate directory (e.g., `content/Developer Stances/`).
2. Add metadata (if needed) at the top of the file, such as the title and date.
3. Write your content using Markdown syntax.
4. Add images to the relevant `images` subdirectory and reference them in your content.

### Build and Deployment

- The site is automatically deployed using the `deploy-mkdocs` GitHub Action when changes are pushed to the `main` branch.
- Ensure that the `site` directory is not committed to the repository, as it is generated during the build process.

### Contribution Guidelines

- Fork the repository and create a feature branch for your changes.
- Submit a pull request with a clear description of your changes.
- Ensure that your content adheres to the project's purpose and style.

---

## Key Concepts

### Domain-Specific Terminology

- **Developer Stances**: Roles or behaviors that developers may adopt during their work (e.g., Pragmatist, Perfectionist).
- **Scrum 4 Kids**: Adaptations of Scrum practices for educational purposes.
- **Workshops**: Interactive activities designed to foster learning and collaboration.

### Core Abstractions

- **Markdown Content**: The primary format for all articles and workshops.
- **Static Site Generation**: MkDocs converts Markdown files into HTML for deployment.

### Design Patterns

- **Modular Content**: Content is organized into categories and subdirectories for easy navigation.
- **Reusable Components**: Images and other assets are stored in subdirectories and referenced in the content.

---

## Common Tasks

### Adding a New Article

1. Navigate to the appropriate directory (e.g., `content/Developer Stances/`).
2. Create a new Markdown file (e.g., `Developer Behavior - New Topic.md`).
3. Write your content and save the file.
4. Test the site locally using `mkdocs serve`.

### Adding Images

1. Place images in the relevant `images` subdirectory (e.g., `content/Developer Stances/images/`).
2. Reference the image in your Markdown file:

   ```markdown
   ![Alt text](images/image-name.jpg)
   ```

### Updating the Navigation

The navigation is automatically generated based on the directory structure. Ensure that your files are placed in the correct directories to appear in the navigation menu.

---

## Troubleshooting

### Common Issues

- **Site Not Updating**: Ensure that the MkDocs server is running and that you have saved your changes.
- **Broken Links**: Verify that all links and image paths are correct.
- **Missing Dependencies**: Run `pip install -r requirements.txt` to install all required packages.

### Debugging Tips

- Use `mkdocs serve` to preview changes locally before deploying.
- Check the MkDocs documentation for troubleshooting specific issues.

---

## References

### Links to Relevant Documentation

- [MkDocs Documentation](https://www.mkdocs.org/)
- [Material for MkDocs Documentation](https://squidfunk.github.io/mkdocs-material/)
- [Markdown Guide](https://www.markdownguide.org/)

### Important Resources

- [GitHub Repository](https://github.com/starkmapper/starkmapper.github.io)
- [Mark Stapper's Blog](https://starkmapper.github.io)
- [Mark Stapper's LinkedIn](https://www.linkedin.com/in/markstapper/)

---

## Next Steps

1. Review and edit this guide as needed to reflect your project's specific requirements.
2. Commit the `.continue/rules/CONTINUE.md` file to your repository to share it with your team.
3. Continue will automatically load this file into context when working with the project.

---

**Note**: This guide assumes a basic understanding of MkDocs, Markdown, and static site generation. If you encounter any issues or have questions, refer to the MkDocs documentation or reach out to the project maintainer.
