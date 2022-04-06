---
layout: default title: Git Revert nav_order: 4
---

# Git Revert

{: .no_toc }

## Table of contents

{: .no_toc .text-delta }

1. TOC {:toc}

## What is a Git Revert?

There are a number of ways to undo unintended or incorrect commits that cause something to go wrong
with your repository. The type of Git command you will use will depend on what type of data you want
to revert, and whether your commit has already been published to GitHub.

## Temporarily Switch to a Different Commit

**Purpose:** Temporarily re-visit your previous commit, do testing, make changes, and then to return
to your current commit - unaltered.

1. ***Navigate to your repository on GitHub and copy the commit ID of the commit you want
   re-visit.***

![revert1.png](revert1.png)

```commandline
$ git checkout <commit-id>
```

2. ***To return to where you were before revisiting your old commit, simply use the command line
   statement below.***

```commandline
$ git switch -
```

3. ***To check that you have correctly returned to correct version of your code, use the following
   command line statement and cross-reference it with the most recent commit ID on GitHub.***

```commandline
$ git rev-parse --verify HEAD
```

## Undo Most Recent Unpublished Commit

**Purpose:** You want to undo the most recent un-pushed commit, so you can make changes before 
committing and pushing to GitHub.

1. ***To undo your last unpushed commit, use the following command line statement.***

```commandline
$ git reset --soft HEAD~1
```

## Delete All Unpublished Commits
**Purpose:** You want to completely remove any un-pushed changes from the local directly and 
revert the repository to the last published commit.

1. ***To completely undo any un-pushed changes, use the following command line statement.***

```commandline
git reset --hard
```


## Revert project to previous version on GitHub

1. This is an ordered list following a header.
2. This is an ordered list following a header.
3. This is an ordered list following a header.



