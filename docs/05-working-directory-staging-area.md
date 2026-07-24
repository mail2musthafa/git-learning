# Lesson 05: Understanding the Working Directory, Staging Area, and Repository

## Overview

Git doesn't immediately save every change you make. Instead, changes move through a workflow consisting of three important areas:

1. Working Directory
2. Staging Area
3. Local Repository

Understanding these areas is essential because almost every Git command interacts with one or more of them.

---

## Learning Objectives

After completing this lesson, you will be able to:

* Explain the three Git areas
* Understand how files move through Git
* Describe the purpose of the staging area
* Explain why Git uses snapshots instead of continuously saving files
* Visualize the Git workflow

---

## Prerequisites

* Completed Lessons 01–04
* Basic understanding of Git repositories

---

## The Three Areas of Git

When working with Git, your files move through three distinct areas:

1. Working Directory
2. Staging Area
3. Local Repository

Each area has a different purpose.

---

## Working Directory

The Working Directory is the folder where you actively create and edit files.

Examples:

* Writing code
* Editing documentation
* Creating folders
* Deleting files

At this stage, Git knows the files have changed, but those changes are **not yet prepared for a commit**.

---

## Staging Area

The Staging Area (also called the **Index**) is a temporary area where you choose which changes should be included in the next commit.

Think of it as a packing table before shipping a package.

You decide exactly what goes into the next snapshot of your project.

---

## Local Repository

The Local Repository stores the complete history of your project.

Once changes are committed, they become part of your repository history.

Each commit creates a new snapshot of the project.

---

## Visual Workflow

```mermaid
flowchart LR
    A[Working Directory] -->|git add| B[Staging Area]
    B -->|git commit| C[Local Repository]
    C -->|git push| D[Remote Repository (GitHub)]
```

---

## Real-World Example

Imagine you're writing a book.

* **Working Directory** → Your desk where you're writing and editing pages.
* **Staging Area** → The pages you've selected for today's revision.
* **Local Repository** → The published edition stored safely.
* **Remote Repository** → The copy shared with your publisher (GitHub).

This separation gives you complete control over what becomes part of your project's history.

---

## Why Does Git Have a Staging Area?

Without a staging area, every modified file would be committed automatically.

The staging area lets you:

* Select only the files you want to commit.
* Split unrelated changes into separate commits.
* Create clean, meaningful project history.

This is one of Git's most powerful features.

---

## Common Mistakes

* Thinking that saving a file automatically creates a Git commit.
* Forgetting that `git add` only stages changes; it does not save them permanently.
* Assuming a file reaches GitHub immediately after a commit.

---

## Best Practices

* Review changes before staging them.
* Stage only related changes together.
* Make small, focused commits.
* Commit frequently with meaningful messages.

---

## Practice Exercises

1. Create a new file in your repository.
2. Modify an existing file.
3. Predict which Git area each file is currently in.
4. Explain what happens after running `git add`.
5. Explain what happens after running `git commit`.
6. Explain what happens after running `git push`.

---

## Interview Questions

1. What is the Working Directory?
2. What is the Staging Area?
3. What is the Local Repository?
4. Why does Git use a staging area?
5. What happens after a commit?
6. What is the difference between a commit and a push?

---

## Summary

In this lesson, you learned:

* The three core Git areas
* How changes move through Git
* Why the staging area exists
* How commits are created
* How Git prepares changes before they become part of history

This workflow is the foundation for almost every Git operation.

---

## Next Lesson

**Lesson 06: Checking Repository Status (`git status`)**

You'll learn how to inspect your repository, understand file states, and determine exactly what Git is tracking before making a commit.
