# Lesson 01: Installation and Setup

## Overview

Before using Git, you need to install it on your operating system and configure your identity. This lesson covers the installation process, verifies the installation, and introduces the tools commonly used with Git.

---

## Learning Objectives

After completing this lesson, you will be able to:

* Understand what Git is
* Install Git on different operating systems
* Verify the Git installation
* Install GitHub CLI
* Verify GitHub CLI installation
* Understand the difference between Git and GitHub
* Understand the tools required for Git development

---

## Prerequisites

No prior Git knowledge is required.

You should have:

* A computer running Windows, macOS, or Linux
* Administrator access to install software
* A terminal or command prompt

---

## What is Git?

Git is a **distributed version control system (DVCS)** created by Linus Torvalds in 2005.

It helps developers:

* Track changes
* Maintain project history
* Collaborate with teams
* Manage different versions of code
* Recover previous versions when needed

Unlike traditional version control systems, every Git repository contains the complete project history.

---

## Why Learn Git?

Git is one of the most important tools used in software development.

It is used by:

* Software Engineers
* Data Engineers
* Machine Learning Engineers
* DevOps Engineers
* Data Scientists
* Cloud Engineers

Almost every software company expects developers to know Git.

---

## Required Tools

| Tool               | Purpose                           |
| ------------------ | --------------------------------- |
| Git                | Version Control System            |
| GitHub             | Remote code hosting platform      |
| GitHub CLI (`gh`)  | Command-line interface for GitHub |
| Visual Studio Code | Code editor                       |
| Terminal           | Execute Git commands              |

---

## Installing Git

### Windows

Download Git from:

https://git-scm.com/downloads

Run the installer using the default settings.

---

### macOS

Using Homebrew:

```bash
brew install git
```

Or download Git from:

https://git-scm.com/downloads

---

### Linux

Ubuntu/Debian:

```bash
sudo apt update
sudo apt install git
```

Fedora:

```bash
sudo dnf install git
```

---

## Verify Git Installation

```bash
git --version
```

Example output:

```text
git version 2.51.0
```

---

## Installing GitHub CLI

### macOS

```bash
brew install gh
```

### Windows

```bash
winget install GitHub.cli
```

### Linux

Refer to the official GitHub CLI installation guide for your distribution.

---

## Verify GitHub CLI

```bash
gh --version
```

---

## Git vs GitHub

| Git                    | GitHub                                |
| ---------------------- | ------------------------------------- |
| Version Control System | Cloud hosting platform                |
| Installed locally      | Runs on the web                       |
| Tracks project history | Hosts Git repositories                |
| Works offline          | Requires internet for synchronization |

Git and GitHub are related, but they are different technologies.

---

## Verify Everything

Run the following commands:

```bash
git --version
gh --version
```

If both commands return version information, your development environment is ready.

---

## Common Mistakes

* Git is installed but not added to the system PATH.
* Confusing Git with GitHub.
* Forgetting to verify the installation.
* Installing GitHub Desktop instead of Git.

---

## Best Practices

* Install the latest stable version of Git.
* Keep Git updated.
* Use the terminal regularly to become comfortable with Git commands.
* Verify installations before continuing.

---

## Summary

In this lesson, you learned:

* What Git is
* Why Git is important
* How to install Git
* How to install GitHub CLI
* How to verify the installation
* The difference between Git and GitHub

Your development environment is now ready for the next lesson.

---

## Next Lesson

**Lesson 02: Git Configuration**

In the next lesson, you'll configure Git with your name and email, understand configuration scopes (system, global, and local), and verify your setup.
