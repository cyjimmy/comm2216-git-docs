---
layout: default
title: Troubleshooting
nav_order: 6
---

# Troubleshooting

---

| Symptoms                                                        | Probable cause                                                       | Action                                                                                                      |
|:----------------------------------------------------------------|:---------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| Get the `git: command not found` message                        | The PATH environment is not set properly                             | ???                                                                                                         |
| Get the `fatal: not a git repository` message                   | You are not in the correct folder                                    | Go to the root folder using the `cd` command                                                                |
|                                                                 | You forgot to initialize your folder as a git repository             | Go to the root folder and use the `git init` command                                                        |
| Get the `error: failed to push` error when pushing              | The remote repository is in newer version than your local repository | Use the `git merge` command, then stage, commit and push again                                                                                                         
| Get the `git: 'add.' is not a git command` message when staging | You forgot the space between 'add' and '.'                           | Put the correct command `git add .`                             
| Get the `fatal: not a git repository` message                   | ???                                                                  | ??? 
{: style="width: 1000px" }

