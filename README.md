# wsl ubuntu for development
```
wsl.exe --install
wsl.exe --update
\\wsl$\Ubuntu\home\shah
```
# link for wsl1 to wsl 2
```
https://learn.microsoft.com/en-us/windows/wsl/basic-commands#set-wsl-version-to-1-or-2
https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-2---check-requirements-for-running-wsl-2
```
# wsl 2
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
wsl --set-default-version 2
wsl.exe --set-version Ubuntu 2

wsl -l -v
```
# ubuntu release
```
lsb_release -a
```
# php
```
sudo apt update
sudo add-apt-repository ppa:ondrej/php
sudo apt update
```
# for apache
```
sudo apt install php8.2 -y
```
# for nginx
```
sudo apt install php8.2-fpm
sudo systemctl status php8.2-fpm
```
# install PHP Extensions
```
php --version
sudo apt-get install -y php8.2-cli php8.2-common php8.2-fpm php8.2-mysql php8.2-zip php8.2-gd php8.2-mbstring php8.2-curl php8.2-xml php8.2-bcmath
```
# zsh
```
sudo apt install curl zip unzip
sudo apt install zsh
sudo nano .zshrc
export PATH="$PATH:$HOME/.config/composer/vendor/bin"
```
