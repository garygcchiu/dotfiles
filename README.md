# Dev Env of Peace

## Terminal

### iTerm 2
https://iterm2.com 

Set Left Option key as Esc+:
![image](https://user-images.githubusercontent.com/19521762/215343012-1e0af2a5-891e-42d1-8abf-0daba69e35f9.png)

Enable `Use built-in Powerline glyphs`: 
![image](https://user-images.githubusercontent.com/19521762/215342979-46437437-565f-4aee-84c8-ae42f0d4a2cd.png)

Set Key Bindings to Natural Text Editing:
<img width="1005" alt="image" src="https://user-images.githubusercontent.com/19521762/213565597-7ad7dff8-979b-481e-a3ea-9d672c6091b9.png">

### Zsh Config:

Install [Oh My Zsh](https://github.com/ohmyzsh/ohmyzsh):

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Enable the following plugins in `.zshrc`:

```
plugins=(
    zsh-syntax-highlighting
)
```

Install [Spaceship-Prompt](https://spaceship-prompt.sh):

```
brew install spaceship
echo "source $(brew --prefix)/opt/spaceship/spaceship.zsh" >>! ~/.zshrc
```

Copy `.spaceshiprc.zsh` to `~`.

Install [Fig](https://fig.io) for their autocomplete:

```
brew install fig
```

### IDE

Launch current directory in GoLand via the command line (i.e. `goland .`)

```
echo '
#!/bin/sh
open -na "GoLand.app" --args "$@"
' >> /usr/local/bin/goland;
chmod +x /usr/local/bin/goland;
```

**What it should all look after**:

![CleanShot 2023-01-28 at 15 52 16](https://user-images.githubusercontent.com/19521762/215290624-cd7e7dcf-d955-443d-810f-0351dedbe980.png)

![CleanShot 2023-01-29 at 13 22 30](https://user-images.githubusercontent.com/19521762/215347655-fd021327-83ac-4a64-84a2-a7c68aaf04ed.png)

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

Alias `git st` for `git status`:
```
git config --global alias.st status
```

Alias `git unstage` for `git reset HEAD --` [file]
```
git config --global alias.unstage 'reset HEAD --'
```

Automatically setup remote tracking:
```
git config --global push.autoSetupRemote true
```


## Misc Apps

Contexts

CleanShot X
