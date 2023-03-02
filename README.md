My personal local development setup. Contains my shell setup, tools, scripts, aliases, quality of life improvements, etc. 

## Terminal

### iTerm 2
https://iterm2.com 

Set Left Option key as Esc+ to skip words with Option+Left or Option+Right or Option+Backspace. 
![image](https://user-images.githubusercontent.com/19521762/215343012-1e0af2a5-891e-42d1-8abf-0daba69e35f9.png)


Enable `Use built-in Powerline glyphs` for prompt icons: 
![image](https://user-images.githubusercontent.com/19521762/215342979-46437437-565f-4aee-84c8-ae42f0d4a2cd.png)

Set Key Bindings to Natural Text Editing for better text navigation:
<img width="1005" alt="image" src="https://user-images.githubusercontent.com/19521762/213565597-7ad7dff8-979b-481e-a3ea-9d672c6091b9.png">

### Zsh:

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

(May need to install it first if not already present)(I prefer to install it via Oh My Zsh as opposed to Fig):
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```


Install [Spaceship-Prompt](https://spaceship-prompt.sh) for their prompt contexts (esp. useful for k8s contexts):

```
brew install spaceship
echo "source $(brew --prefix)/opt/spaceship/spaceship.zsh" >>! ~/.zshrc
```

Copy [.spaceshiprc.zsh](./.spaceshiprc.zsh) to `~`.


Install [Fig](https://fig.io) for their autocomplete:

```
brew install fig
```

Set `[Tab]` to Navigate Down:

![CleanShot 2023-01-29 at 13 24 40](https://user-images.githubusercontent.com/19521762/215347771-4ca39c2e-cdc2-44ee-b53b-8241b443eacf.png)

Disable Telemetry, hide Menu Icon. 

Add [`kubectx` and `kubens`](https://github.com/ahmetb/kubectx) for quick k8s context and namespace switching:

```
brew install kubectx
```


Add the following to your `.zshrc`: 
```
alias k=kubectl
function ksh {
        kubectl exec -it "$1" -- sh
}
```

**What it should all look after**:

![CleanShot 2023-01-29 at 13 28 24](https://user-images.githubusercontent.com/19521762/215347913-1acb8fc5-af84-4125-bcd5-a3dbf9a2261d.png)

![CleanShot 2023-01-29 at 13 27 52](https://user-images.githubusercontent.com/19521762/215347893-01d4d75c-a889-40c6-838c-ac0042848a65.png)


## IDE

Launch current directory in GoLand via the command line (i.e. `goland .`)

```
echo '
#!/bin/sh
open -na "GoLand.app" --args "$@"
' >> /usr/local/bin/goland;
chmod +x /usr/local/bin/goland;
```


## Git

**git add commit and push**

Add to `.zshrc`:
```
function gitu {
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

[Contexts](https://contexts.co) 

[CleanShot X](https://cleanshot.com)
- Seems like 1 license per device though. Honestly might be worth, really sweet app.  

[Cron](https://cron.com)
- Mostly use to have my upcoming meetings right in the menu bar. 

