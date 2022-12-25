# Dev Env of Peace

## Terminal

iTerm 2
https://iterm2.com 

Set Left Option key as Esc+:
![CleanShot 2022-12-24 at 22 38 11](https://user-images.githubusercontent.com/19521762/209456226-08979ba5-a59d-409b-bb11-02f6fb2daed3.png)


https://fig.io
```
brew install --cask fig
```

Plugins:

![CleanShot 2022-12-24 at 22 36 29](https://user-images.githubusercontent.com/19521762/209456205-770dc080-ea54-41e2-8348-ba6c917a4779.png)


Enable `Use built-in Powerline glyphs`: 
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
