# Lesson 04: Creating Your First Repository (`git init`)

## Overview

Before Git can track changes, it needs a repository. In this lesson, you'll learn how to initialize a Git repository, what happens behind the scenes, and why the hidden `.git` directory is the heart of every Git project.

---

## Learning Objectives

After completing this lesson, you will be able to:

* Understand what a Git repository is
* Initialize a new Git repository
* Explain what the `.git` directory contains
* Verify that a repository has been initialized
* Understand why the `.git` directory should not be modified manually

---

## Prerequisites

* Git installed
* Completed Lessons 01–03

---

## What Is a Repository?

A **repository** (often called a **repo**) is a directory that Git uses to track the history of your project.

It stores:

* Project files
* Commit history
* Branch information
* Tags
* Configuration
* References to commits

Without a repository, Git has nowhere to store version history.

---

## The `git init` Command

The `git init` command creates a new Git repository in the current directory.

### Syntax

```bash
git init
```

### Example

```bash
mkdir my-project
cd my-project
git init
```

Typical output:

```text
Initialized empty Git repository in /path/to/my-project/.git/
```

At this point, Git is ready to start tracking changes.

---

## What Happens Internally?

When you run `git init`, Git creates a hidden directory named `.git`.

This directory contains everything Git needs to manage your repository, including:

* Repository configuration
* Branch references
* Commit objects
* Logs
* Hooks
* Index (staging area)

Your project files remain outside the `.git` directory.

---

## Repository Structure

```text
my-project/
├── .git/
├── README.md
├── app.py
└── requirements.txt
```

Only the `.git` folder is managed internally by Git. Your source code stays in the project directory.

---

## Under the Hood

The `.git` directory is the database for your repository.

Some important files and folders include:

```text
.git/
├── HEAD
├── config
├── hooks/
├── objects/
├── refs/
└── logs/
```

You'll learn about each of these in later lessons.

---

## Verify a Repository

To check whether you're inside a Git repository:

```bash
git status
```

If Git reports the repository status, it has been initialized successfully.

---

## Common Mistakes

* Running `git init` in the wrong directory.
* Deleting the `.git` folder accidentally.
* Editing files inside `.git` manually.
* Initializing a repository inside another repository unless you intentionally need nested repositories.

---

## Best Practices

* Initialize Git once at the project root.
* Keep the `.git` directory intact.
* Verify the repository with `git status`.
* Add a `README.md` early in the project.

---

## Practice Exercises

1. Create a new folder named `demo-project`.
2. Initialize it with `git init`.
3. List hidden files using `ls -la`.
4. Locate the `.git` directory.
5. Run `git status`.
6. Create a file named `notes.txt` and observe how Git reports it.

---

## Interview Questions

1. What is a Git repository?
2. What does `git init` do?
3. What is the purpose of the `.git` directory?
4. Can a project exist without `.git`?
5. Why shouldn't you edit files inside `.git` manually?

---

## Summary

In this lesson, you learned:

* What a Git repository is
* How `git init` creates a repository
* What the `.git` directory contains
* How to verify that a repository has been initialized
* Best practices for working with repositories

---

## Next Lesson

**Lesson 05: Understanding the Working Directory, Staging Area, and Repository**

You'll learn how changes move through Git—from editing a file to preparing it for a commit.
