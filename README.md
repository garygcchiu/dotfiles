# Dev-Env-Setup


## Git

**git add commit and push**

Add to `.zshrc`:
```
function gitu() {
    git add .
    git commit -a -m "$1"
    git push
}
```

**Alias `git st` for `git status`**:
```
git config --global alias.st status
```
