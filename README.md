# Git Cheat Sheet
This is a handy list of commonly used commands for git command line. It is meant to help when you can't remember how certain commands work, or when you want to quickly do something without reading the documentation.

Each heading is a thing you can do with git, for example commiting or branching.

Each subheading is a specific way of doing that thing. For example the "everything" subheading under commit shows a command for commiting all the files in a branch.

If there are multiple commands under a subheading, then they are meant to be done in the order presented. For example the "merge" subheading under "branches" has two commands, the first for switching to a branch, the second for merging into that branch from another branch.

> Please note, this isn't meant to be a tutorial or in-depth quide. There are other ways to use many of these commands, and these exact commands may not always be what you're looking for! This cheat sheet also doesn't have any explanations of how or why these things work. Rather, it is meant for people who are already familiar with git and need a quick reference for some common commands.

## COMMIT
#### LIST
 `git reflog`

#### EVERYTHING
 `git commit -a -m "message"`

#### CHANGES
 `git diff hash_of_older_commit..hash_of_newer_commit`
 
#### UNCOMMITTED CHANGES
 `git diff hash_of_older_commit:./ -- filename`
		
#### DELETE LOCAL
 `git reset --hard hash_of_commit_to_go_back_to`
#### DELETE REMOTE
 `git push -f origin hash_of_commit_to_go_back_to:branch_name`

## BRANCHES
#### CREATE LOCAL
 `git checkout -b branchname`
 
#### CREATE REMOTE
 `git push --set-upstream origin new_branch_name`
		
#### SWITCH
 `git checkout branchname`
		
#### MERGE
 `git checkout branch_merge_INTO`
 
 `git merge branch_merge_FROM -m "message"`
 
#### MERGE ABORT (Use when conflicts block a merge)
 `git merge --abort`
		
#### DELETE LOCAL
 `git branch -d branchname`
 
#### DELETE REMOTE
 `git push origin --delete branch_name`
	
## UPDATE
 `git fetch` (update only the branch you're on, but don't merge any changes)
 
 `git remote update` (update all of your branches set to track remote, but doesn't merge any changes)
 
 `git pull` (update and merge any remote changes of the current branch you're on)
	
## TAGS
#### LIST
 `git tag`
	
#### ANNOTATE LOCAL
 `git tag -a v0.9.3.3 hash_to_tag -m "message"`
 
#### ANNOTATE REMOTE
 `git push origin v0.9.3.3`
 
#### ANNOTATE REMOTE
 `git push origin --tags` (pushes all tags)
	
#### DELETE LOCAL
 `git tag -d v0.9.3.3`
 
#### DELETE REMOTE
 `git push origin --delete v0.9.3.3`

## USER

#### STORE CREDENTIALS
 `git config --global credential.helper store` (saves username and password on next signin)