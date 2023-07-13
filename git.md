# git

### Update your branch with `main`
```
git checkout my_branch
git fetch origin main
git merge origin/main
```
Resolve conflicts, if any, then stage, commit, and push changes

### Bring a file in from another branch to your current one
`git checkout source_branch -- path/to/file`

Resolve conflicts, if any, then stage, commit, and push changes

### Stash it
1. Stash changes if you are having issues: `git stash`
2. Check which stash you want to apply using: `git stash list`
3. Remove from stash and apply: `git stash pop stash@{n}`
4. Keep in stash and apply: `git stash apply stash@{n}`
