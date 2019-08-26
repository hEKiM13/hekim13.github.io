# My most used git commands

## Basics

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add <file-name.txt>` | Add a file to the staging area |
| `git add -A` | Add all tracked and untracked files to the staging area |
| `git commit -m "<commit-message>"` | Commit changes |

## Branches

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch <branch-name>` | Create a new branch |
| `git branch -d <branch-name>` | Delete a branch |
| `git checkout <branch-name>` | Switch to a branch |
| `git merge <branch-name>` | Merge a branch into the active branch |

## Tagging

| Command | Description |
| ------- | ----------- |
| `git tag --delete <tag-name>` | Delete a **shared** tag locally (Remember to push the change - see command below) |
| `git push origin :refs/tags/<tag-name>` | Push the local tag changes for a specific tag |
| `git tag -a <tag-name> -m <commit-message>` | Create an annotated tag with a commit |

## Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push` | Push changes to remote repository (remembered branch) |
| `git fetch` | Fetch remote changes |
| `git pull` | Update local repository to the newest commit |
