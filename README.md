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
