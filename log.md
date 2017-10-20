# `git log`

### Limit
```
git log -1
```

### Show diff
```
git log -p
```

### Summarise the logs by author
It groups each commit by author and displays the first line of each commit message. 
```
git shortlog
```

### Showing a graph of the branches structure
Also check UnGit below
```
git log --graph --oneline --decorate
```

### Filter by date
```
git log --after="2017-10-10" --before="2017-10-20"
```
Or
```
git log --after="yesterday"
```
Or
```
git log --since=2.weeks
```

### Filter by author
```
git log --author="nick@anideaforanapp.com"
```

### Filter by message
```
git log --grep="SV-1110"
```

### Filter by file
```
git log -- Gruntfile.js
```

### Filter by content
```
git log -S "console.log"
```

### Filter by range between commits
```
git log <commit1>..<commit2>
```

### Filter by range between branches
That will show all the commits that are in `<branch2>` but aren't in `<branch1>`
```
git log <branch1>..<branch2>
```
### Filter merge commits
Filtering out merge commits
```
git log --no-merges
```
Filtering out non-merge commits
```
git log --merges
```

### See all code introcuded by a `nick@anideaforanapp.com` on `master` in the past `2.weeks`
```
git diff -p `git rev-list -n1 --since=2.weeks master --author=nick@anideaforanapp.com` --stat
```

### See all the commits introduced by the user `nick@anideaforanapp.com` on all branches in the past `1.weeks`
```
git log --branches=* --author=nick@anideaforanapp.com --since=1.weeks --oneline --reverse
```


---

# Decorating the log

#### A better looking git log
![git-lg](https://raw.githubusercontent.com/naguibihab/git-cheat-sheet/master/assets/git-lg.png)

`git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"`

Then type `git lg` to get the log

Credits: [https://coderwall.com/p/euwpig/a-better-git-log](https://coderwall.com/p/euwpig/a-better-git-log)


#### UnGit: A nice GUI for git on node.js: [https://github.com/FredrikNoren/ungit](https://github.com/FredrikNoren/ungit)
![git-lg](https://raw.githubusercontent.com/naguibihab/git-cheat-sheet/master/assets/ungit.png)

---

##### Good references:
- Atlassian: [https://www.atlassian.com/git/tutorials/git-log](https://www.atlassian.com/git/tutorials/git-log)