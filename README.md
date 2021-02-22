# Setup

Get new fonts for your terminal [Nerdfont](https://www.nerdfonts.com/font-downloads)
install the font you want and set it for you terminal


## set up zsh-shell
```
sudo apt install zsh -y
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Or
```
sudo pacman -S zsh
```
### set ZSH as Default
Open
```
sudo nano ~/.bashrc
```
then add the line below top of the file
```
exec zsh
```

### Install powerlevel10k zsh theme
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```
set the theme in the config file
```
vim ~/.zshrc
or
nano ~/.zshrc
or
code ~/.zshrc
```
change ZSH_THEME=”robbyrussel” with ZSH_THEME=”powerlevel10k/powerlevel10k”. 

[My ZSH Alias](https://github.com/TomRR/Setup/blob/main/zsh-alias)

### install plugins
[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Add Plugins to the zshrc file
```
plugins=(git npm nvm gatsby zsh-autosuggestions zsh-syntax-highlighting)
```

### Config ZSH
If you start the ZSH with the powerlevel10k theme for the first time the config wizzard should start automaticly 
Otherwise tippe
```
p10k configure
```
to start the wizzard
**Also use ```p10k configure``` every time you want change your setup**

## GIT

```sudo apt install git```
or [GIT SCM](https://git-scm.com/)

### Git Konfiguration
```
git config --global user.name "USER"
git config --global user.email "EMAIL"
```
### check for key 
**(git bash on windows)**
```
ls -al ~/.ssh
```
Keys looks like 
* id_rsa.pub
* id_ecdsa.pub
* id_ed25519.pub

### Generating a new SSH key and adding it to the ssh-agent

```
ssh-keygen -t ed25519 -C "EMAIL"
```
*If you are using a legacy system that doesn't support the Ed25519 algorithm, use:*
```
ssh-keygen -t rsa -b 4096 -C "EMAIL"
```
**Start the ssh-agent in the background.**
```
eval "$(ssh-agent -s)"
```
> Agent pid 59566

**Add your SSH private key to the ssh-agent.**
```
ssh-add ~/.ssh/id_ed25519
or
ssh-add ~/.ssh/id_rsa
```

### Adding a new SSH key
```
cat ~/.ssh/id_ed25519.pub
or
cat ~/.ssh/id_rsa.pub
```
And add the key to Github, Gitlab, ...

### Gatsby
```
sudo npm install -g gatsby-cli
```
[Gatsby Tutorial](https://www.gatsbyjs.com/docs/tutorial/part-zero/)

### Node
```
sudo apt-get install -y nodejs
```
```
sudo apt-get install -y npm
```

# Pop OS
## Update and Upgrade
```
sudo apt update
sudo apt full-upgrade
```
OR
Pop Store

## Enable Minimize and Maximize Buttons
```
sudo apt install gnome-tweaks
```
search for **"tweaks"**
[window-titlebar](https://static.techhut.tv/img/archive/5-things-popos/2-window_titlebars.png)
## Install Dash to Dock
[https://extensions.gnome.org/extension/307/dash-to-dock/)](https://extensions.gnome.org/extension/307/dash-to-dock/)

![gnome-exentions](https://static.techhut.tv/img/archive/5-things-popos/3-gnome-exentions.png)
![dash-to-docker](https://static.techhut.tv/img/archive/5-things-popos/4-dash-to-dock.png)
