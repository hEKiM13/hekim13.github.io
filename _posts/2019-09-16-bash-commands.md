---
published: true
author: Michael
title:  "Bash commands"
categories: [linux]
tags: [shell]
---

Below are the bash commands I use most frequently and sometimes forget.

# Bash commands

## SSH

| Command | Description |
| ------- | ----------- |
| `ssh-keygen -t rsa -b 4096` | create a new ssh key of type `rsa` and of `4096` bytes |

## SCP

| Command | Description |
| ------- | ----------- |
| `scp <filename> <remote-username>@<remote-server>:<remote-directory>` | secure copy local `<filename>` to remote computer |
| `scp -r <remote-username>@<remote-server>:<remote-directory> <local-path>` | secure copy a remote directory to a local path |

## Network

| Command | Description |
| ------- | ----------- |
| `ip address show` | Show all IP addresses for all network adapters |

## Filesystem

| Command | Description |
| ------- | ----------- |
| `df -h` | check free space on disk |
| `du` | check the size of folders |
| `rm -rf <directory>` | will remove `<directory>` and all files files and folders inside |
| `ls -l <filename>` | displays permissions for `<filename>` |
| `ls -ld <directory>` | displays the permissions for `<directory>` |
| `touch <filename>` | will create a new file at `<filename>` |

## Server management

| Command | Description |
| ------- | ----------- |
| `sudo shutdown -P now` | shutdown server |
| `free -m` | check free and used memory (Displayed in Mb) |
| `crontab -l > <filename>` | will copy your cron jobs to `<filename>` |
