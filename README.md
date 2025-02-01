My personal local development setup. Contains my shell setup, tools, scripts, aliases, quality of life improvements, etc. 

## Terminal

### Warp
https://warp.dev


Add [`kubectx` and `kubens`](https://github.com/ahmetb/kubectx) for quick k8s context and namespace switching:

```
brew install kubectx
```


Add the following to your `.zshrc`: 
```
alias k=kubectl
alias ls='ls --color'
function ksh {
    kubectl exec -it "$1" -- sh
}
function get-pod-named {
    kubectl get pod -o name | grep -m1 "$1" | cut -d '/' -f 2
}
function kgp {
    kubectl get pod "$@"
}
```

Install [bat](https://github.com/sharkdp/bat):
```
brew install bat
```

- .zshrc:
```
alias cat='bat'
```


## IDE

Launch current directory in GoLand via the command line (i.e. `goland .`)

```
echo '
#!/bin/sh
open -na "GoLand.app" --args "$@"
' >> /usr/local/bin/goland;
chmod +x /usr/local/bin/goland;
```

or add to `~/.zshrc`:
```
function goland { 
    open -na "GoLand.app" --args "$@"
}
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
# graphite
function gtu {
        gt cc -a -m "$1"
        gt ss
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

Alias `git co` for `git checkout`: 
```
git config --global alias.co checkout
```

Automatically setup remote tracking:
```
git config --global push.autoSetupRemote true
```

Set `vim` to be default editor:
```
git config --global core.editor "vim"
```

Use `master` as default branch when running `git init`:
```
git config --global init.defaultBranch master
```

## Misc Apps

[Warpd](https://github.com/rvaiya/warpd)
- Install from source
- Move `warpd.config` to `~/.config/warpd/config`

[Contexts](https://contexts.co) 

[CleanShot X](https://cleanshot.com)
- Seems like 1 license per device though. Honestly might be worth, really sweet app.  

[Cron](https://cron.com)
- Mostly use to have my upcoming meetings right in the menu bar. 

[Graphite](https://graphite.dev/cli)
- Git wrapper that helps with branch stacking

[z](https://github.com/rupa/z?tab=readme-ov-file)
- Jump around the terminal, regex to frequently used directories easily
