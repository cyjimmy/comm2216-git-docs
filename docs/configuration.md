---
layout: default
title: Instruction 1
nav_order: 2
---

# Setting up Git
{: .no_toc }

After this setup, users should have a functional git with an attached username and email.
\_config.yml file.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. Windows setup
2. Mac (OSX) setup
{:toc}

---

View this site's [\_config.yml](https://github.com/just-the-docs/just-the-docs/tree/main/_config.yml) file as an example.

## Windows Setup

1. Download the 64-bit version of the Git Windows setup using the following link:
https://git-scm.com/download/win


```yaml
Note: If you're using a 10-year-old system or older, consider using the 32-bit Windows Setup. The 64-bit version may not be compatible with your system.
```

2. Open the installer and accept all the defaults *except* for the default editor "Vim". Vim is hard to use and not recommended for beginners. I'd recommend selecting Notepad++.
   
```yaml
Note: If you don't have Notepad++ already, download it with the prompt from the installer and install it with default settings.

Once Notepad++ is done installing, press "Back" on the Git installer and "Next" again to refresh the option to continue.
```

3. Once the installer is finished, launch git by right-clicking on an empty space on your desktop or window and selecting "Git Bash here"

4. In the console, type the following to edit your name and email:

```yaml
Username:
git config --global user.name "Adam Savage"
(replace Adam Savage with your name)

Email:
git config --global user.email "adam@hotmail.ca"
(replace adam@hotmail.ca with your email)
```

5. Verify your information by type the following:
```yaml
git config --list
```
and look at the user.name and user.email field to double-check that they've been set properly.

## Mac (OSX) Setup

1. Press Command-space to launch Spotlight and type "Terminal" then double click the search result.

2. In the terminal, type the following to install Git:

```yaml
brew install git
```
3. Once the operation is complete, type the following to verify the installation.

```yaml
git version
```

4. In the console, type the following to edit your name and email:

```yaml
Username:
git config --global user.name "Adam Savage"
(replace Adam Savage with your name)

Email:
git config --global user.email "adam@hotmail.ca"
(replace adam@hotmail.ca with your email)
```

5. Verify your information by type the following:
```yaml
git config --list
```
and look at the user.name and user.email field to double-check that they've been set properly.