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
1. Create remote repository on GitHub<br>
In order to use Git to manage your files, you need to have a remote repository. Follow instructions on this [page](https://docs.github.com/en/get-started/quickstart/create-a-repo) to create your GitHub repository.
2. Link local repository with remote repository<br>
   1. Open desired directory in Command Prompt
      >cd $PATH
      >  
      Replace $PATH with the path of your directory. This line will open the specified directory.<br><br>
      Instead of typing the path of the directory, you can also type cd, then drag the desire directory to Command Prompt.<br><br>
   2. Create a local Git repository
      >git init
      > 
      A local Git repository is a local directory with Git version control enabled.<br><br>
   3. Link your local and remote repository
      >git remote add origin $PATH
      > 
      Replace $PATH with the path of your remote repository.<br><br>
   4. Choose the main branch
      >git branch -M main
      >
      Git also allows users to have branches for their repository. For a new repository, there is only one branch which is main.

## Updating Remote Repository
Now that your repository is created and setup, Git will start tracking any changes made within your local repository.<br>
1. Check if there is any changes made to the local repository
   >git status
   >
   This will show the changes you made locally. Screenshot below shows an example:<br><br>
   ![img.png](img.png)
   In this example, file test.txt was modified and a new file newTest.txt was created.<br><br>
2. Stage files<br>
   Git allows users to choose which file they want to update in version control. This function is called staging. Only the files added to the staging area will be updated.
   >git add $FILE_NAME
   > 
   This will add the specified file to the staging area.
   You can also ask Git to stage all modified and newly created files using:
   >git add .
   >
3. Commit<br>
   In Git, commit is taking a snapshot of your repository. It is the state of your repository with the staged changes.
   >git commit -m "commit message"
   > 
   This commit all the staged changes. Notice there is a "commit message" at the end. This is where you can put message that explain your changes. Putting a non-empty commit message is required, since it is a good practice in development.<br><br>
   
4. Push your commits to remote repository
   >git push
   >
   The push command will update your remote repository with the changes you committed.
   
## Reading Repository
1. Pull


## Deleting Repository
1. Remove from GitHub
2. Remove Local Repository

