# Instalar fonte Go Mono for Powerline
### link

<br>

# Instalar Terminal Windows
### link

<br>
  
# Executar comandos a seguir para atualizar os pacotes
```sh
sudo apt update -y
```
```sh
sudo apt upgrade -y
```
<br>

# Instalar e configurar ZSH
```sh
sudo apt install zsh -y
```
```sh
chsh -s /bin/zsh
```
```sh
zsh
```

<br>

# Instalar Oh-my-zsh! -> https://ohmyz.sh/
```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
```sh
zsh
```
#### Mudar ~/.zshrc -> ZSH_THEME="agnoster"

<br>

# Instalar Zsh Autosuggestions
### https://github.com/zsh-users/zsh-autosuggestions
```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

<br>

# Instalar Zsh Syntax Highlighting
### https://github.com/zsh-users/zsh-syntax-highlighting
```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

<br>

# Mudar plugins
##  ~/.zshrc ~> plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
