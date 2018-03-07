# Basic Commands

## Branching
##### See all local branches
`git branch`

##### See all local & remote branches
`git branch --all`

##### Checkout existing branch
`git checkout <branchname>`

##### Force checkout
`git checkout --force` **warning** this may overwrite some uncommitted changes

##### Create a new branch out of the one you're on right now 
`git checkout -b <newbranch>`

##### Pull & update local branch
`git pull`

##### Fetch changes (Note: this doesn't pull or update local branches)
`git fetch --all`


## Making changes
##### View current branch, staged, local commits..etc
`git status`

##### See the differences introduced in the staged files (before staging)
`git diff`

##### Stage changes
`git add --all` or `git add .`

##### Unstage changes
`git reset`

##### Commit changes
`git commit -m "my commit message"`

##### Stage and commit
`got commit -a -m "my commit message"`

##### See previous commits
`git log`

##### See last commit
`git log -1`

##### See changes in last commit
`git log -p -1`

##### Push changes
`git push`

##### Push and set upstream
`git push --set-upstream origin <branchname>`

## Merging
##### Merging two branches
`git merge <branchname>`

## Undoing
##### Reverting a commit
`git revert <commitid>`

##### Reverting a merge to original parent
`git revert <commitid> -m 1`

##### Reverting a change in a particular file
`git checkout path/to/file`

##### Reverting a change in a particular file to a particular commit
`git checkout <commitid> path/to/file`

##### Reset uncommitted changes
`git reset --hard` **warning** this will remove all tracked but uncommitted changes

##### Resolving conflicts
`git mergetool` **prerequesit** having a merge tool installed & setup with git, check [this article](https://www.linkedin.com/pulse/git-bash-tips-tricks-naguib-ihab/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_post_details%3BH1ylzOTFQ5ex6cw1yhOwTg%3D%3D) for setting up kdfif3

## Cleaning up
##### Deleting a branch
`git branch -d <branchname>`

##### Deleting all branches but keeping master
`git branch | grep -v "master" | xargs git branch -d`