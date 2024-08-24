# Welcome to Hack@UCF Private Cloud Wiki
Anyone is welcome to contribute guides, documentation, video, etc.

[MKDocs Docs](https://www.mkdocs.org/)

[MKDocs Material](https://squidfunk.github.io/mkdocs-material/)

# How to Contribute 
## I had ChatGPT write this so blame them 
## Prerequisites

Before contributing, make sure you have the following:

- **Git**: Installed on your local machine.
- **Python**: Version 3.6 or higher.
- **MkDocs**: Installed via pip (`pip install mkdocs`).
- **Text Editor**: Any text editor of your choice (e.g., VS Code, Sublime Text).

## Steps to Contribute

### 1. Fork the Repository

- Go to the MkDocs website repository on GitHub.
- Click the "Fork" button to create your own copy of the repository.

### 2. Clone the Repository

- Clone your forked repository to your local machine using Git:

  ```bash
  git clone https://github.com/your-username/repository-name.git
  cd repository-name
  ```

### 3. Create a New Branch

- Create a new branch to work on your changes:

  ```bash
  git checkout -b your-branch-name
  ```

### 4. Install Dependencies

- Install the required dependencies by running:

  ```bash
  pip install -r requirements.txt
  ```

### 5. Make Your Changes

- Open the project in your text editor.
- Edit or add new Markdown files in the `docs` directory.
- Update the `mkdocs.yml` configuration file if necessary.

### 6. Preview Your Changes

- Run the MkDocs development server to preview your changes locally:

  ```bash
  mkdocs serve
  ```

- Open your browser and go to `http://localhost:8000` to see your changes in real-time.

### 7. Commit Your Changes

- After making sure everything looks good, commit your changes:

  ```bash
  git add .
  git commit -m "Description of the changes you made"
  ```

### 8. Push to GitHub

- Push your changes to your forked repository:

  ```bash
  git push origin your-branch-name
  ```

### 9. Create a Pull Request

- Go to the original repository on GitHub.
- Click "New Pull Request" and select your branch from the dropdown menu.
- Add a meaningful description and submit the pull request.

### 10. Address Feedback

- Maintain communication and address any feedback from the repository maintainers.

### 11. Done!

- Once your pull request is approved and merged, your changes will be part of the MkDocs website.
