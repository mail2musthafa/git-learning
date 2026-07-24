# Lesson 23: GitHub CLI (`gh`)

## Overview

While Git manages your local repository and communicates with remote repositories, many GitHub-specific tasks—such as creating repositories, opening Pull Requests, managing issues, and reviewing code—are traditionally performed through the GitHub website.

The **GitHub CLI (`gh`)** brings these GitHub features directly into your terminal, allowing you to perform common GitHub operations without leaving the command line.

> **Important:** `gh` is **not part of Git**. It is a separate tool developed by GitHub.

---

## Learning Objectives

After completing this lesson, you will be able to:

- Understand what GitHub CLI is
- Differentiate between Git and GitHub CLI
- Install and authenticate GitHub CLI
- Create and manage repositories
- Work with Pull Requests
- Manage Issues
- View repository information
- Follow GitHub CLI best practices

---

## Prerequisites

- Lessons 01–22
- Git installed
- GitHub account
- Internet connection

---

# Git vs GitHub vs GitHub CLI

Many beginners confuse these three tools.

| Git | GitHub | GitHub CLI (`gh`) |
|------|---------|-------------------|
| Version Control System | Repository Hosting Platform | Command-line interface for GitHub |
| Tracks file history | Stores repositories online | Controls GitHub from the terminal |
| Works offline | Cloud service | Requires GitHub authentication |
| Created by Linus Torvalds | Owned by Microsoft | Official GitHub tool |

Remember:

- **Git** manages version control.
- **GitHub** hosts repositories.
- **GitHub CLI** interacts with GitHub services.

---

# Installing GitHub CLI

## macOS

```bash
brew install gh
```

---

## Windows

```powershell
winget install GitHub.cli
```

---

## Ubuntu

```bash
sudo apt install gh
```

If your package manager doesn't include the latest version, refer to the official GitHub CLI installation instructions.

---

# Verify Installation

```bash
gh --version
```

Example:

```text
gh version 2.80.0
```

---

# Authenticate

Login:

```bash
gh auth login
```

Typical flow:

1. Choose GitHub.com.
2. Select HTTPS.
3. Authenticate through the browser.
4. Complete login.

Check authentication:

```bash
gh auth status
```

Example:

```text
Logged in to github.com as musthafa
Git operations for github.com configured to use HTTPS.
```

---

# Create a Repository

Public repository:

```bash
gh repo create my-project --public
```

Private repository:

```bash
gh repo create my-project --private
```

Interactive mode:

```bash
gh repo create
```

---

# Clone a Repository

```bash
gh repo clone owner/repository
```

Example:

```bash
gh repo clone mail2musthafa/git-learning
```

---

# View Repository Information

Current repository:

```bash
gh repo view
```

Specific repository:

```bash
gh repo view owner/repository
```

Open it in the browser:

```bash
gh repo view --web
```

---

# List Your Repositories

```bash
gh repo list
```

Limit results:

```bash
gh repo list --limit 10
```

---

# Create a Pull Request

```bash
gh pr create
```

Interactive prompts help you:

- Select the base branch
- Select the compare branch
- Enter a title
- Enter a description

---

# List Pull Requests

```bash
gh pr list
```

View a specific Pull Request:

```bash
gh pr view 15
```

Open it in the browser:

```bash
gh pr view --web
```

---

# Check Out a Pull Request

```bash
gh pr checkout 15
```

GitHub CLI automatically fetches and switches to the PR branch.

---

# Merge a Pull Request

```bash
gh pr merge 15
```

Available merge strategies include:

```bash
gh pr merge --merge
gh pr merge --squash
gh pr merge --rebase
```

---

# Working with Issues

Create an issue:

```bash
gh issue create
```

List issues:

```bash
gh issue list
```

View an issue:

```bash
gh issue view 12
```

Close an issue:

```bash
gh issue close 12
```

---

# Releases

Create a release:

```bash
gh release create v1.0.0
```

List releases:

```bash
gh release list
```

View a release:

```bash
gh release view v1.0.0
```

---

# Open GitHub in Your Browser

Repository:

```bash
gh browse
```

Specific Pull Request:

```bash
gh pr view --web
```

Specific Issue:

```bash
gh issue view --web
```

---

# Useful Commands

| Command | Purpose |
|----------|----------|
| `gh auth login` | Authenticate |
| `gh auth status` | View authentication status |
| `gh repo create` | Create repository |
| `gh repo clone` | Clone repository |
| `gh repo view` | View repository |
| `gh repo list` | List repositories |
| `gh pr create` | Create Pull Request |
| `gh pr list` | List Pull Requests |
| `gh issue create` | Create issue |
| `gh release create` | Create release |

---

# Real-World Workflow

A common workflow might look like this:

```bash
git switch -c feature/login

git add .
git commit -m "Add login feature"

git push -u origin feature/login

gh pr create
```

A reviewer approves the Pull Request:

```bash
gh pr merge --squash
```

Delete the merged branch:

```bash
git branch -d feature/login
git push origin --delete feature/login
```

---

# Best Practices

- Authenticate once using `gh auth login`.
- Keep GitHub CLI updated.
- Use descriptive Pull Request titles.
- Verify the current repository before creating a Pull Request.
- Review changes before merging.

---

# Common Mistakes

- Confusing `git` commands with `gh` commands.
- Running `git repo list` instead of `gh repo list`.
- Forgetting to authenticate.
- Creating Pull Requests from the wrong branch.
- Merging without reviewing changes.

---

# Practice Exercises

1. Verify GitHub CLI installation.
2. Authenticate with GitHub.
3. Create a new repository.
4. Clone a repository.
5. View repository details.
6. Create a feature branch.
7. Push the branch.
8. Create a Pull Request using GitHub CLI.
9. List Pull Requests.
10. View a release.

---

# Interview Questions

1. What is GitHub CLI?
2. How is `gh` different from Git?
3. How do you authenticate GitHub CLI?
4. How do you create a Pull Request using GitHub CLI?
5. How do you list repositories?
6. Can GitHub CLI replace Git?

---

# Summary

In this lesson, you learned:

- What GitHub CLI is
- The difference between Git and GitHub CLI
- Installing and authenticating `gh`
- Managing repositories
- Creating and managing Pull Requests
- Working with Issues and Releases
- Best practices for using GitHub CLI

GitHub CLI streamlines GitHub workflows by bringing repository management, collaboration, and automation directly into the terminal, making it an essential productivity tool for modern developers.

---

## Next Lesson

**Lesson 24: Git Hooks**