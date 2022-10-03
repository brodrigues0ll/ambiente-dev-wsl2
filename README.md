# Configurações no Windows:
  ## Habilitar WSL e Atualizar para WSL2
  ##### OBS.: Executar powershell como administrador.

  #### 1. Habilitar WSL
  ```sh
  dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
  ```
  #### 2. Habilitar Virtualização

  ```sh
  dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
  ```

  #### 3. Reiniciar o Computador

  #### 4. Baixar e instalar atualização do WSL
  https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

  #### 5. Executar powershell como administrador e executar o código abaixo.
  
  ```sh
  wsl --set-default-version 2
  ```

  <br>

  ## Instalar fonte Go Mono for Powerline
  #### https://github.com/brodrigues0ll/ambiente-dev-wsl2/raw/main/Go%20Mono%20for%20Powerline.ttf

  ## Instalar Ubuntu para WSL
  #### https://apps.microsoft.com/store/detail/ubuntu/9PDXGNCFSCZV?hl=pt-br&gl=br

  ## Instalar e configurar Terminal Windows:
  
  ### 1. Baixar
  #### https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=pt-br&gl=br
  
  ### 2. Adicionar configuração no arquivo JSON
  ### Configuração pronta para copiar e colar: https://github.com/brodrigues0ll/ambiente-dev-wsl2/blob/main/settings.json
  
  <br>
  
  <img src="https://github.com/brodrigues0ll/ambiente-dev-wsl2/blob/main/2022-09-21%2004-19-47.gif" width="800" height="500" />  
  
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

  ## Mudar o arquivo `.zshrc` no diretório `~/`    
  ### Linha `ZSH_THEME=""` passa a ser `ZSH_THEME="agnoster"`  
  <img src="https://github.com/brodrigues0ll/ambiente-dev-wsl2/blob/main/Screenshot_6.png" width="600" height="300" />
  
  
  ### Linha `plugins=(git)` passa a ser `plugins=(git zsh-autosuggestions zsh-syntax-highlighting)`  
  <img src="https://github.com/brodrigues0ll/ambiente-dev-wsl2/blob/main/Screenshot_7.png" width="600" height="300" />
  
  ## Instalar NPM
  ```sh
  sudo apt install nodejs
  ```
  
  ```sh
  sudo apt install npm
  ```
  
  ```sh
  curl -qL https://www.npmjs.com/install.sh | sh
  ```
  
  ## Instalar NVM
  ### 1.

  
  ```sh
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
  ```
  ### 2.
  ```sh
  export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
  ```
  <br>
  
  ## Instalar NODE na versão 16
   ```sh
  sudo nvm install 16
  ```
  
  ```sh
  nvm alias default 16
  ```
  <br>
  
  ## Verificar versões do Node, NPM e NVM
  ```sh
  node -v && npm --version && nvm --version
  ```

