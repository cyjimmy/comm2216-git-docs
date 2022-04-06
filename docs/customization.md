---
layout: default
title: CRUD Operation
nav_order: 3
---

# CRUD Operation
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## What is CRUD?
CRUD is an acronym which stands for Create, Read, Update and Delete. These are the basic functions that present in most storage system including Git.

As a modern source-code management software, Git makes CRUD simple and fast to perform.

## Creating New Repository
1. Create online repository on GitHub<br>
In order to use Git to manage your files, you need to have an online repository. Follow instructions on this [page](https://docs.github.com/en/get-started/quickstart/create-a-repo) to create your GitHub repository.
2. Link local repository with online repository<br>
   1. Open desired directory in Command Prompt
      >cd "C:\Users\Dummy\Demo"
      >  
      This line, for example, will open the Demo directory under user Dummy. Instead of typing the path of the directory, you can also type cd, then drag the desire directory to Command Prompt.<br>
   2. Create a local Git repository
      >git init
      > 
      A local Git repository is a local directory with Git version control enabled.
   3. Link your local and online repository
      >git remote add origin $PATH
      > 
      Replace $PATH with the path of your online repository.
   4. Choose the main branch
      >git branch -M main
      >
      Git also allows users to have branches for their repository. For a new repository, there is only one branch which is main.
## Updating Repository
1. Stage
2. Commit
3. Push

## Reading Repository
1. Pull


## Deleting Repository
1. Remove from GitHub
2. Remove Local Repository

