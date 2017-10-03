# git-cheat-sheet
### Most used
Checkout existing branch
`git checkout <branchname>`
Create a new branch out of the one you're on right now 
`git checkout -b <newbranch>`
Pull & update local branch
`git pull`
Fetch changes (Note: this doesn't pull or update local branches)
`git fetch --all`
View current branch, staged, local commits..etc
`git status`

See the differences introduced in the staged files (before staging)
`git diff`
Stage changes
`git add --all` or `git add .`
Unstage changes
`git reset`
Commit changes
`git commit -m "my commit message"`
Stage and commit
`got commit -a -m "my commit message"`
See previous commits
`git log`
See last commit
`git log -1`

Push changes
`git push`
Push and set upstream
`git push --set-upstream origin <branchname>`

See all local branches
`git branch`
See all local & remote branches
`git branch --all`

### Advanced
Reverting a commit
`git revert <commitid>`
