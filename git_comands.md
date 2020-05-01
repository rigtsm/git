git log --oneline --graph --all
git checkout


## Create a branch an checkout on it
git checkout -b <branch_name>


## Delete a branch
git branch -d <branch_name>
git branch -D <branch_name>


## For undoing a branch delete execute
git reflog
git checkout -b <branch_name> [SHA-1 YOU COPIED]

## Fast Forward Merge: Only if no new commits on the master. Just move the HEAD to the beginning of the branch
- Checkout master
- merge branch, FF is the defaul merge
- delete the branch label

	git checkout master
	git merge feature2
	# delete the branch label
	git branch -d feauture2

## Merge Commit: combines the commits at the tips of the merged branches, places the result in the merge commit. Has multiple parents.

	git checkout master
	git merge featureX
	git branche -d featurex
	# performing a Merge commit instead of an FF merge
	git merge --no-ff featurex
	
## Merge Conclicts
- checkout the master 
- merge featureX 
	- Conflict: both modified the same "hunk" fileA.txt
- fix conflict fileA
- stage fileA 
- commit the merge commit
- delete the branch label 

## Tracking Branches
- are local branches that represent remote branches
- are named <remote>/<branch>, for example origin/master
- can become out of synch with local branches
- updated with network commands like, clone, fetch, pull and push






















