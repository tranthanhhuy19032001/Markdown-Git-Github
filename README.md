# Git & GitHub Guide

## Table of Contents

- [I. Introduction](#introduction)
- [II. Markdown Language](#markdown-language)
  - [1. Title Headings](#title-headings)
  - [2. Inserting Links & Images](#inserting-links-images)
  - [3. Bold & Italics](#bold-italics)
  - [4. Inline & Block Quotes](#inline-block-quotes)
  - [5. Bullet Lists](#bullet-lists)
  - [6. Creating Tables](#creating-tables)
  - [Tips for Markdown](#markdown-tips)
- [III. Git & GitHub Operations](#git-github-operations)
  - [1. Initialize Project](#initialize-project)
  - [2. Git Basics](#git-basics)
  - [3. Git Reset](#git-reset)
  - [4. Git Amend](#git-amend)
  - [5. Git Revert](#git-revert)
  - [6. Git Merge](#git-merge)
  - [7. Git Debase](#git-debase)
  - [8. Git Cherry-pick](#git-cherry-pick)
  - [9. Resolving Conflicts](#resolving-conflicts)

---

## I. Introduction

Git and GitHub are essential tools for modern developers. Version control makes managing, sharing, and collaborating on code efficient and safe.

This document provides a concise overview of Git, GitHub, and Markdown, with step-by-step instructions for common operations and useful tips.

---

## II. Markdown Language

Markdown is a simple markup language. For the complete syntax, see [Markdown Syntax](http://daringfireball.net/projects/markdown/syntax).

Below are the core features commonly used:

### <a name="title-headings"></a>1. Title Headings

Use `#` to start headings. More `#` means smaller heading.

Example:

```markdown
# Heading 1
## Heading 2
###### Heading 6
```

Rendered:

# Heading 1
## Heading 2
###### Heading 6

---

### <a name="inserting-links-images"></a>2. Inserting Links & Images

- **Paste a URL for a simple link:**

```markdown
https://github.com
```
https://github.com

- **Shorten links:**

```markdown
[GitHub](https://github.com)
```
[GitHub](https://github.com)

- **Insert images:**

```markdown
<img src="your_image_url">
```

*Tip: For screenshots, use [Lightshot](https://app.prntscr.com/en/index.html) and upload to [Imgur](https://imgur.com/) for direct link.*

---

### <a name="bold-italics"></a>3. Bold & Italics

- **Bold:** `**text**` → **text**
- **Italics:** `*text*` → *text*

Example:

```markdown
**Bold text**
*Italic text*
```

**Bold text**

*Italic text*

---

### <a name="inline-block-quotes"></a>4. Inline & Block Quotes

- **Inline code:** `` `code` `` → `code`
- **Multi-line/code block:**

    ```sh
    auto eth0
    iface eth0 inet static
    ipaddress 10.10.10.10
    netmask 255.255.255.0
    gateway 10.10.10.1
    dns-nameservers 8.8.8.8
    ```

Result:

```sh
auto eth0
iface eth0 inet static
ipaddress 10.10.10.10
netmask 255.255.255.0
gateway 10.10.10.1
dns-nameservers 8.8.8.8
```

---

### <a name="bullet-lists"></a>5. Bullet Lists

```markdown
- First item
  - Indented item
- Second item
```

- First item
  - Indented item
- Second item

---

### <a name="creating-tables"></a>6. Creating Tables

```markdown
| Header 1      | Header 2 | Header 3    | Header 4 |
|---------------|----------|-------------|----------|
| Row 2         | 2 x 1    | 2 x 2       | 2 x 3    |
| Row 3         | 3 x 1    | 3 x 2       | 3 x 3    |
| Row 4         | 4 x 1    | 4 x 2       | 4 x 3    |
```

| Header 1      | Header 2 | Header 3    | Header 4 |
|---------------|----------|-------------|----------|
| Row 2         | 2 x 1    | 2 x 2       | 2 x 3    |
| Row 3         | 3 x 1    | 3 x 2       | 3 x 3    |
| Row 4         | 4 x 1    | 4 x 2       | 4 x 3    |

---

### <a name="markdown-tips"></a>Tips for Markdown

> - **Preview Live:** Use [Markdown Live Preview](http://markdownlivepreview.com/) to see and edit your Markdown instantly.
> - **Reuse Snippets:** Check and borrow formatted markdown from others.
> - Markdown helps make your GitHub repos look professional and organized!

---

## III. Git & GitHub Operations

### <a name="initialize-project"></a>1. Initialize Project

#### 1.1 Create new repository

```sh
echo "# initialize_repository" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/username/your-repository.git  # Change to your repository URL
git push -u origin main
```

#### 1.2 Push existing repository

```sh
git remote add origin https://github.com/username/your-repository.git
git branch -M main
git push -u origin main
```

---

### <a name="git-basics"></a>2. Git Basics

_Basic commands and daily workflow. See [Pro Git](https://git-scm.com/book/en/v2) for more._

---

### <a name="git-reset"></a>3. Git Reset

#### 3.1 Reset to a specific commit

- **Hard Reset:** _Resets HEAD and deletes all changes in working directory_
    ```sh
    git reset --hard [commit_id]
    ```
- **Soft Reset:** _Keeps changes staged_
    ```sh
    git reset --soft [commit_id]
    ```

#### 3.2 Push changes after reset

```sh
git push --force origin your_branch    # after --hard
git push origin your_branch            # after --soft
```

---

### <a name="git-amend"></a>4. Git Amend

#### 4.1 Keep commit message:
```sh
git commit --amend --no-edit
```

#### 4.2 Write new commit message:
```sh
git commit --amend -m "A new comment"
```

---

### <a name="git-revert"></a>5. Git Revert

_Revert a specific commit:_

```sh
git revert <commit-hash>
```

_Revert latest commit:_

```sh
git revert HEAD
```

---

### <a name="git-merge"></a>6. Git Merge

```sh
git checkout destination_branch
git merge source_branch
```

---

### <a name="git-debase"></a>7. Git Debase

_Refer to [Git Rebase Documentation](https://git-scm.com/docs/git-rebase)._

---

### <a name="git-cherry-pick"></a>8. Git Cherry-pick

- **Single commit:**
    ```sh
    git checkout target_branch
    git cherry-pick <commit-hash>
    ```

- **Multiple commits:**
    ```sh
    git cherry-pick commit_hash1 commit_hash2 commit_hash3
    ```

- **Range of commits:**
    ```sh
    git cherry-pick start_commit^..end_commit
    ```

- **Without committing immediately:**
    ```sh
    git cherry-pick --no-commit <commit-hash>
    # Modify, then
    git add .
    git commit
    ```

**Notes:**
- Resolve conflicts by fixing files, then continue: `git cherry-pick --continue`
- Abort cherry-pick: `git cherry-pick --abort`
- For merge commits, use `-m` or `--mainline`.

---

### <a name="resolving-conflicts"></a>9. Resolving Conflicts

1. **Identify conflicts:**
    ```sh
    git status
    ```

2. **Edit files & remove conflict markers:**
    - Look for `<<<<<<<`, `=======`, `>>>>>>>` and choose your final code
    - Remove the markers, save the file

3. **Stage and commit:**
    ```sh
    git add .
    git commit -m "Resolve merge conflict"
    ```

**Other methods:**  
- Use your IDE’s merge editor for a visual process  
- Rebase for a clean history  
- Resolve through GitHub’s "Resolve conflicts" web interface

---

Enjoy coding and collaborating with a clean, well-documented workflow!
