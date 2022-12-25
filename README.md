# Dev Eng of Peace

## Terminal

https://fig.io
```
brew install --cask fig
```

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

**Alias `git unstage` for `git reset HEAD --` [file]**
```
git config --global alias.unstage 'reset HEAD --'
```


## Misc Apps

Contexts

CleanShot X
