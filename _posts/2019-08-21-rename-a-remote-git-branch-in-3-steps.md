---
published: true
author: Michael
title:  "Rename a remote git branch in 3 steps"
categories: [dev]
tags: [git, branch]
---

# Rename a remote git branch in 3 steps

1. Rename the branch (if you are on the branch)

    `git branch -m <new-name>`

1. Delete old name and push new name

    `git push origin :<old-name> <new-name>`

1. Reset the upstream path for new branch

    `git push origin -u <new-name>`
