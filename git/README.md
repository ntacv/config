
# Git Config for multiple accounts

[Repo](https://github.com/ntacv/Github)

## Steps
1. Prepare a clean architecture
[Usar múltiples usuarios con Git - DEV Community](https://dev.to/equimancho/usar-multiples-usuarios-con-git-1fci)


## Git Config

Add VSCode as default editor for git

    Git config --global core.editor "code --wait"

Open the config file of the repository

    Git config --edit --local



## Connect PC to github via SSH
TODO for each account
[How To Work With Multiple Github Accounts on your PC](https://gist.github.com/rahularity/86da20fe3858e6b311de068201d279e3#file-work-with-multiple-github-accounts-md)
### 1. Create a ssh key
[github-ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
### 2. Add key to ssh-agent
same
### 3. Add the pub to your github accout Settings/SSH
same
### 4. Create the config for multiple account
```.ssh/config```
```
Host ntacv
    HostName github.com
    User git
    AddKeysToAgent yes
    IdentitiesOnly yes
    IdentityFile ~/.ssh/key_github_ntacv
```

### 5. Clone repo


    1. Create a ssh key 
    2. Add key to ssh-agent
    3. Add the pub to your github accout Settings/SSH
    4. Create the config for multiple account
    5. Clone repo Warning
    FROM TO
    git@github.com:username/repo.git
    git@HOST:username/repo.git
