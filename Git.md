# Git

## Repositories
- `git init` - Start a new repo in existing folder  
- `git init foo` - Create a new repo 
- `rm -r my_project/.git` - Remove the repo (from inside the porject fodler) Just remove the .git folder, it’s the brains

## Adding Code
- `git add filename.txt` - Add files to track
- `git add -A` - Add all files in the folder to track 

## Branches

### List

- `git branch` - List local branches
- `git branch -r` - List remote branches
- `git branch -a` - List all branches  
- `git ls-remote --heads <remote-name>` - List remote branches (If remote name is `origin`, you can skip referncing it since it's the default)  
- `git ls-remote [url]` - List remote branches (so you don't have to clone it first)
- `git branch --list "*/foo"` List branch by pattern matching (all branches ending in foo)
- `git branch --list "test/*"` List branch by pattern matching (all branches starting with test)
- `gitk --branches="*/foo"` List branch by pattern matching

### Checkout
- `git checkout foo` - Checkout a branch
- `git checkout -b foo` - Create and Checkout a branch  

### Delete
- `git branch -d foo` - delete local branch
- `git push origin --delete foo` - delete remote branch
- `git branch -D foo` - use -D to force deletion without checking merged status

### Rename
- `git branch -m <newname>` - Rename the current branch (local)
- `git branch -m <oldname> <newname>` - Rename a local branch
- `git push <remote> <remote>/<old_name>:refs/heads/<new_name> :<old_name>` - Rename remote branch [href][1]
- Rename a remote branch
```bash
git branch -m <oldname> <newname>     # Rename branch locally    
git push origin --delete <oldname>    # Delete the old branch    
git push -u origin <newname>          # Push the new branch, set local branch to track the new remote
```

Links
---
- [TLDR Dev Notes: Git Basics](http://tldrdevnotes.com/git-basics/)
- [StackOverflow: List all remote branches](http://stackoverflow.com/questions/3471827/how-do-i-list-all-remote-branches-in-git-1-7)
- [StackOverflow: Delete branch both locally and remotely](http://stackoverflow.com/questions/2003505/how-to-delete-a-git-branch-both-locally-and-remotely)
- [StackOverflow: git branch naming best practices](http://stackoverflow.com/questions/273695/git-branch-naming-best-practices)
- [StackOverflow: Rename local branch](http://stackoverflow.com/questions/6591213/how-to-rename-a-local-git-branch)

[1]: http://stackoverflow.com/a/21302474/890814
