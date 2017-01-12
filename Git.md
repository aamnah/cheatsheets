# Git

## Repositories
- `git init` - Start a new repo in existing folder  
- `git init foo` - Create a new repo 
- `rm -r my_project/.git` - Remove the repo (from inside the porject fodler) Just remove the .git folder, it’s the brains

## Adding Code
- `git add filename.txt` - Add files to track
- `git add -A` - Add all files in the folder to track 

## Commits



## Branches

### List

- `git branch` - List local branches
- `git branch -r` - List remote branches
- `git branch -a` - List all branches  
- `git ls-remote --heads <remote-name>` - List remote branches (If remote name is `origin`, you can skip referncing it since it's the default)  
- `git ls-remote [url]` - List remote branches (so you don't have to clone it first)

### Checkout
- `git checkout foo` - Checkout a branch
- `git checkout -b foo` - Create and Checkout a branch  

### Delete
- `git branch -d foo` - delete local branch
- `git push origin --delete foo` - delete remote branch
- `git branch -D foo` - use -D to force deletion without checking merged status
