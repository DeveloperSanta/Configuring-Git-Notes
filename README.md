# Configuring Git Notes

## Overview

One of my most common things I Google is how to configure and setup git when using a new development computer. This repository includes my consolidated notes on how to setup & configure git, git commands and Visual Studio Code extensions.

These commands work on a Linux based Operating System as well as using the [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/install) on a Windows system.

## Creating an SSH Key

Run the following command (and update it with your email address) to create a new SSH key pair:

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

[Source](https://www.atlassian.com/git/tutorials/git-ssh)

[Section](https://www.atlassian.com/git/tutorials/git-ssh#:~:text=Generate%20an%20SSH%20Key%20on%20Mac%20and%20Linux)

Once you have created the key (assuming you saved it in the default location) copy the contents of the public key `~/.ssh/id_rsa.pub` and create a new SSH key in [GitHub](https://github.com/settings/keys).

## Setting git Author

The first time you attempt to make a commit, you might encounter an error that says `Author identity unknown *** Please tell me who you are.`.

To fix this, run the following commands (and update them with your username and email address):

```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

Then you can run the `git commit` command again.

## Adding git Branch to Bash Terminal

This section is optional and allows you to update your `.bashrc` file to include the name of the branch you are working on in your Terminal.

The snippet of code I use is [here](https://askubuntu.com/questions/730754/how-do-i-show-the-git-branch-with-colours-in-bash-prompt#:~:text=218-,This%20snippet%3A,-%23%20Add%20git%20branch) and the source can be found [here](https://askubuntu.com/questions/730754/how-do-i-show-the-git-branch-with-colours-in-bash-prompt).

## Useful git Commands

| Command                                      | Description                                                                                             |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| git clone [GITHUB REPOSITORY]                | Clone a remote repository to your local computer                                                        |
| git checkout [BRANCH NAME]                   | Checkout to a new branch (local or remote)                                                              |
| git checkout -b [BRANCH NAME]                | Create a new branch from the branch you are currently using                                             |
| git status                                   | Get information of the currently staged & unstaged files and the number of commits your branch is ahead |
| git add --all                                | Stage all files (be careful)                                                                            |
| git add .                                    | Stage all files in the current working directory                                                        |
| git add [FILE NAME]                          | Stage a specific file                                                                                   |
| git commit -m "commit message"               | Commit staged files with a custom message                                                               |
| git push                                     | Push the local branch to the remote branch                                                              |
| git push --set-upstream origin [BRANCH NAME] | If you create a new local branch and run `git push` (for the first time) you will get this command      |
| git pull                                     | Pull down code changes from the remote source                                                           |
| git log                                      | Show an interactive log of all commits                                                                  |
| git log --all --decorate --oneline --graph   | Show a consolidated text based graph of commits                                                         |

[git log adog source](https://stackoverflow.com/questions/1057564/pretty-git-branch-graphs)

[git log adog section](https://stackoverflow.com/questions/1057564/pretty-git-branch-graphs#:~:text=here%20it%20is%3A-,git%20log%20%2D%2Dall%20%2D%2Ddecorate%20%2D%2Doneline%20%2D%2Dgraph,-Not%20everyone%20would)

## Useful Visual Studio Code Extensions

The table below includes some helpful extensions to aid in your development. You can search for these extensions using the `Extension ID` in Visual Studio Code.

| Extension Name      | Extension ID                          | VS Marketplace Link                                                                       |
| ------------------- | ------------------------------------- | ----------------------------------------------------------------------------------------- |
| Code Spell Checker  | streetsidesoftware.code-spell-checker | https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker |
| Docker              | ms-azuretools.vscode-docker           | https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker           |
| Git Graph           | mhutchie.git-graph                    | https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph                    |
| Markdown All in One | yzhang.markdown-all-in-one            | https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one            |
| Prettify JSON       | mohsen1.prettify-json                 | https://marketplace.visualstudio.com/items?itemName=mohsen1.prettify-json                 |
