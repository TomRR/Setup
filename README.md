# Setup

Get new fonts for your terminal [Nerdfont](https://www.nerdfonts.com/font-downloads)
install the font you want and set it for you terminal


## set up zsh-shell
```
sudo apt install zsh -y
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
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



* p10k configure
