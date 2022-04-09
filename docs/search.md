---
layout: default
title: Troubleshooting
nav_order: 6
---

# Troubleshooting

---

| Symptoms                                                                          | Probable cause                                                       | Action                                                                                                      |
|:----------------------------------------------------------------------------------|:---------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| Get `git: command not found` message in Command Prompt when using any Git command | The PATH enviornment is not set properly                             | ???????????                                                                                                 |
| Can not run `sudo` command with newly created user                                | User not on root user when creating and assigning group privilege    | Change to root user with the command `sudo su -`                                                            |
| Process not showing up when using `pgrep processname`                             | The process name does not exist                                      | Verify that the correct keyword is input                                                                    |
| You cannot see a directory that you create                                        | The `touch` command was mistakenly used                              | Verify you input the `mkdir` command                                                                        
| Can not modify contents of a file                                                 | Tried to modify non-existent file or used wrong command              | Verify that `>` is part of the input when you use the `cat > filename` command                              
| Could not move my file into a different directory                                 | User tried to move file to non-existent directory or to another file | Verify that the directory exists and is not a file with an extension. Correct syntax is `mv file directory` 
{: style="width: 1000px" }
