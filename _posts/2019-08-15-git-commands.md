---
published: true
author: Michael
title:  "GIT commands"
categories: [dev]
tags: [git]
---

Below are the GIT commands I use most frequently and sometimes forget.

# GIT commands

## Basics

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add -A` | Add all tracked and untracked files to the staging area |
| `git commit -m "<commit-message>"` | Commit changes |

## Branches

| Command | Description |
| ------- | ----------- |
| `git branch` | List all local branches |
| `git branch -a` | List all branches (local and remote) |
| `git checkout <branch-name>` | Switch to `branch-name` |
| `git checkout -b <branch-name>` | Create and switch to `branch-name` |
| `git merge <branch-name>` | Merge `branch-name` into the active branch |
| `git branch -d <branch-name>` | Delete `branch-name` locally |
| `git remote prune origin` | Prune dead remote branches |
| `git fetch -p` | Before fetching remove any dead remote branches |
| `git branch -vv | grep 'origin/.*: gone]' | awk '{print $1}' | xargs git branch -d` | Delete local branches that don't have a remote set |

## History / Log

| Command | Description |
| ------- | ----------- |
| `git log --graph --decorate --oneline` | A pretty printed view of the history |

## Tagging

| Command | Description |
| ------- | ----------- |
| `git tag --delete <tag-name>` | Delete a **shared** `tag-name` locally (Remember to push the change - see command below) |
| `git push origin :refs/tags/<tag-name>` | Push the local `tag-name` changes |
| `git tag -a <tag-name> -m <commit-message>` | Create an annotated tag with a commit |

## Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push` | Push changes to remote repository (remembered branch) |
| `git fetch` | Fetch remote changes |
| `git pull` | Update local repository to the newest commit |
| `git reset HEAD` | Reset the staging area (not working directory) to the commit that HEAD is pointing at |
| `git reset --hard HEAD` | Reset the staging area and the working directory to the commit that HEAD is pointing at |
