# Welcome to Hack@UCF Private Cloud Wiki

Anyone is welcome to contribute guides, documentation, video, etc.

[MkDocs Docs](https://www.mkdocs.org/) | [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)

# How to Contribute

## Prerequisites

Before contributing, make sure you have the following:

- **Git**: Installed on your local machine.
- **[uv](https://docs.astral.sh/uv/)**: The Python package manager used by this project.
- **Text Editor**: Any text editor of your choice (e.g., VS Code, Sublime Text).

### Installing uv

```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## Steps to Contribute

### 1. Fork the Repository

- Make a fork of this repo by clicking the "Fork" button on GitHub to create your own copy.

### 2. Clone the Repository

- Clone your forked repository to your local machine:

```sh
git clone https://github.com/your-username/pcv2-wiki.git
cd pcv2-wiki
```

### 3. Create a New Branch

- Create a new branch to work on your changes:

```sh
git checkout -b your-branch-name
```

### 4. Install Dependencies

- Install the required dependencies using `uv`:

```sh
uv sync
```

This will automatically create a virtual environment and install all dependencies from `uv.lock`.

### 5. Make Your Changes

- Open the project in your text editor.
- Edit or add new Markdown files in the `docs` directory.
- Update the `mkdocs.yml` configuration file if necessary.

### 6. Preview Your Changes

- Run the MkDocs development server to preview your changes locally:

```sh
uv run mkdocs serve
```

- Open your browser and go to `http://localhost:8000` to see your changes in real-time.

### 7. Commit Your Changes

- After making sure everything looks good, commit your changes:

```sh
git add .
git commit -m "Description of the changes you made"
```

### 8. Push to GitHub

- Push your changes to your forked repository:

```sh
git push origin your-branch-name
```

### 9. Create a Pull Request

- Go to the original repository on GitHub.
- Click "New Pull Request" and select your branch from the dropdown menu.
- Add a meaningful description and submit the pull request.

### 10. Address Feedback

- Maintain communication and address any feedback from the repository maintainers.

### 11. Done!

- Once your pull request is approved and merged, your changes will be part of the wiki!