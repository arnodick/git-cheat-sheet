## COMMIT
#### EVERYTHING
 `git commit -a -m "message"`
		
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
		
#### DELETE LOCAL
 `git branch -d branchname`
 
#### DLETE REMOTE
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
