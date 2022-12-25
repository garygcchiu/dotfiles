# Dev Env of Peace

## Terminal

https://fig.io
```
brew install --cask fig
```

Enable `Use PowerShell glyphs`: 
![CleanShot 2022-12-24 at 22 25 45](https://user-images.githubusercontent.com/19521762/209456067-a42dd595-69dd-4c7b-b805-32680bbb3d61.png)


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
