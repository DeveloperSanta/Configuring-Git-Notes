# Configuring Git Notes

## Overview

One of my most common things I Google is how to configure and setup git when using a new development computer. This repository includes my consolidated notes on how to setup and configure git as well as some helpful commands.

These commands work on a Linux based Operating System as well as using the [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/install) on a Windows system.

## Creating an SSH Key

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

[Source](https://www.atlassian.com/git/tutorials/git-ssh)

[Section](https://www.atlassian.com/git/tutorials/git-ssh#:~:text=Generate%20an%20SSH%20Key%20on%20Mac%20and%20Linux)

Once you have created the key (assuming you saved it in the default location) copy the contents of the public key `~/.ssh/id_rsa.pub` and create a new SSH key in [GitHub](https://github.com/settings/keys).

## Setting git Author

The first time you attempt to make a commit, you might encounter an error that says `Author identity unknown *** Please tell me who you are.`.

To fix this, run the following commands (and update them with your username and email):

```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

Then you can run the `git commit` command again.

## Useful git Commands

| Command                                               | Description                                                                                             |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| git clone [GITHUB REPOSITORY]                         | Clone a remote repository to your local computer                                                        |
| git checkout [BRANCH NAME]                            | Checkout to a new branch (local or remote)                                                              |
| git checkout -b [BRANCH NAME]                         | Create a new branch from the branch you are currently using                                             |
| git status                                            | Get information of the currently staged & unstaged files and the number of commits your branch is ahead |
| git add --all                                         | Stage all files (be careful)                                                                            |
| git add .                                             | Stage all files in the current working directory                                                        |
| git add [FILE NAME]                                   | Stage a specific file                                                                                   |
| git commit -m "commit message"                        | Commit staged files with a custom message                                                               |
| git push                                              | Push the local branch to the remote branch                                                              |
| git push --set-upstream origin [BRANCH NAME]          | If you create a new local branch and run `git push` you will get this command                           |
| git pull                                              | Pull down code changes from the remote source                                                           |
| git log                                               | Show an interactive log of all commits                                                                  |
| git log --all --decorate --oneline --graph            | Show a consolidated text based graph of commits                                                         |

[git log adog source](https://stackoverflow.com/questions/1057564/pretty-git-branch-graphs)

[git log adog section](https://stackoverflow.com/questions/1057564/pretty-git-branch-graphs#:~:text=here%20it%20is%3A-,git%20log%20%2D%2Dall%20%2D%2Ddecorate%20%2D%2Doneline%20%2D%2Dgraph,-Not%20everyone%20would)
