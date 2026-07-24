# Lesson 02: Git Configuration

## Overview

After installing Git, the next step is configuring your identity and preferences. Git uses this information to identify who made each commit and to determine how it should behave on your machine.

This lesson explains Git configuration, configuration scopes, and how Git decides which settings to use.

---

## Learning Objectives

After completing this lesson, you will be able to:

* Configure your Git identity
* Understand System, Global, and Local configuration
* View and modify Git settings
* Understand configuration precedence
* Verify your configuration

---

## Prerequisites

* Git installed
* Basic terminal knowledge
* Completed Lesson 01

---

# Why Configuration Matters

Every commit in Git stores information about its author.

A commit contains metadata such as:

* Author Name
* Author Email
* Date and Time
* Commit Message
* Commit Hash

Without configuration, Git cannot correctly identify who created a commit.

---

# Git Configuration Levels

Git supports three configuration levels.

| Level  | Scope              | Location             |
| ------ | ------------------ | -------------------- |
| System | Entire computer    | System configuration |
| Global | Current user       | User profile         |
| Local  | Current repository | `.git/config`        |

---

## System Configuration

Applies to every user on the computer.

Example:

```bash
git config --system user.name "John Doe"
```

This level is mainly used by system administrators.

---

## Global Configuration

Applies to all repositories owned by the current user.

Example:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

This is the configuration most developers use.

---

## Local Configuration

Applies only to the current repository.

```bash
git config --local user.name "Project User"
git config --local user.email "project@example.com"
```

Local settings override global settings.

---

# Configuration Priority

When Git looks for a configuration value, it checks in this order:

```text
Local
   ↓
Global
   ↓
System
```

The first value found is used.

For example:

System:

```
John
```

Global:

```
Musthafa
```

Local:

```
Git Learning
```

Git will use:

```
Git Learning
```

because local configuration has the highest priority.

---

# Configure Your Identity

Configure your name:

```bash
git config --global user.name "Your Name"
```

Configure your email:

```bash
git config --global user.email "your-email@example.com"
```

---

# Verify Configuration

View your name:

```bash
git config --global user.name
```

View your email:

```bash
git config --global user.email
```

View all settings:

```bash
git config --global --list
```

Show where each configuration comes from:

```bash
git config --global --show-origin --list
```

---

# Local Configuration Example

Navigate to a repository:

```bash
cd git-learning
```

Set a repository-specific username:

```bash
git config --local user.name "Git Learning"
```

Verify it:

```bash
git config --local --list
```

Only this repository uses the local configuration.

---

# How Git Uses Your Identity

When you create a commit:

```bash
git commit -m "Initial commit"
```

Git automatically records:

* Your configured name
* Your configured email
* Commit timestamp
* Commit hash
* Commit message

You don't need to provide your name and email every time.

---

# Common Commands

Set global username:

```bash
git config --global user.name "Your Name"
```

Set global email:

```bash
git config --global user.email "your-email@example.com"
```

List all settings:

```bash
git config --list
```

Unset a value:

```bash
git config --global --unset user.name
```

Edit configuration manually:

```bash
git config --global --edit
```

---

# Common Mistakes

* Forgetting to configure name and email.
* Using the wrong email address.
* Confusing local and global configuration.
* Editing configuration files manually without understanding the changes.

---

# Best Practices

* Configure your global identity once after installing Git.
* Use local configuration only when a repository requires a different identity.
* Verify your configuration before making your first commit.
* Keep your email consistent across repositories unless there is a specific reason to use a different one.

---

# Practice Exercises

1. Configure your global username.
2. Configure your global email.
3. Verify your configuration.
4. Create a local configuration for a test repository.
5. Compare global and local settings.
6. Remove the local configuration and verify that Git falls back to the global configuration.

---

# Interview Questions

1. What is Git configuration?
2. What is the difference between system, global, and local configuration?
3. Which configuration has the highest priority?
4. Where does Git store local configuration?
5. How can you display all Git configuration values?
6. How do you edit Git configuration?

---

# Summary

In this lesson, you learned:

* Why Git configuration is required
* How Git stores configuration
* The three configuration scopes
* Configuration precedence
* How to configure your identity
* How to verify and manage Git settings

Your Git environment is now properly configured and ready for creating and managing repositories.

---

# Next Lesson

**Lesson 03: Git Fundamentals**

In the next lesson, you'll learn what version control is, why Git was created, how distributed version control works, and the core concepts that every Git user should understand before using Git commands.
