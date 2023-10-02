# Update the linux
Ubuntu and other linux distros
```
sudo apt update
```
Termux
```
apt update
```

**Note: Depending on the platform commands may vary**
# Download zsh and Oh-my-zsh 
Ubuntu and other linux distros
```
sudo apt install zsh
```
Termux
```
pkg install zsh
```
## Now download Oh-my-zsh
For do more info visit [Oh-my-zsh](https://ohmyz.sh/) 
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Once done it would ask if you want to set it as default enter y and Oh-my-zsh would be set as default terminal 
# Download the required fonts
```
git clone https://github.com/ibnYusrat/my-linux-setup.git
```
Once done navigation to the powerline-fonts directory and copy the fonts to `~/$HOME/.fonts` directory 
# Download Oh-my-zsh theme
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
Once done set 
`ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`.
Source thr `.zshrc` file to see the changes 
Go through the installation and choose the customisation that you need 