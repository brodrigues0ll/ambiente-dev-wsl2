# Configurações no Windows:
  ## Habilitar WSL e Atualizar para WSL2
  ##### OBS.: Executar powershell como administrador.

  #### 1
  ```sh
  dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
  ```
  #### 2

  ```sh
  dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
  ```

  #### 3
  ### Reiniciar o Computador

  #### 4
  ### Baixar e instalar atualização do WSL
  https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

  #### 5
  ##### OBS.: Lembrar de executar powershell como administrador.
  ```sh
  wsl --set-default-version 2
  ```

  <br>

  ## Instalar fonte Go Mono for Powerline
  #### https://github.com/brodrigues0ll/ambiente-dev-wsl2/raw/main/Go%20Mono%20for%20Powerline.ttf

  ## Instalar Ubuntu para WSL
  #### https://apps.microsoft.com/store/detail/ubuntu/9PDXGNCFSCZV?hl=pt-br&gl=br

  ## Instalar Terminal Windows
  #### https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=pt-br&gl=br

  <br>
  <br>
  
# Configurações no WSL:  
  ## Executar comandos a seguir para atualizar os pacotes
  ```sh
  sudo apt update -y
  ```
  ```sh
  sudo apt upgrade -y
  ```
  <br>

  ## Instalar e configurar ZSH
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

  ## Instalar Oh-my-zsh! -> https://ohmyz.sh/
  ```sh
  sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  ```
  ```sh
  zsh
  ```
  #### Mudar ~/.zshrc -> ZSH_THEME="agnoster"

  <br>

  ## Instalar Zsh Autosuggestions
  #### https://github.com/zsh-users/zsh-autosuggestions
  ```sh
  git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  ```

  <br>

  ## Instalar Zsh Syntax Highlighting
  #### https://github.com/zsh-users/zsh-syntax-highlighting
  ```sh
  git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  ```

  <br>

  ## Mudar plugins
  ###  ~/.zshrc ~> plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
