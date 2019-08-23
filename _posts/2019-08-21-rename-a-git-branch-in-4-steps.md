1. Rename a local branch (if you are on the branch)
git branch -m <new-name>
 
2. Rename another branch
git branch -m <old-name> <new-name>
 
3. Delete old name and push new name
git push origin :<old-name> <new-name>
 
4. Reset the upstream path for new branch
git push origin -u <new-name>