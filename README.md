# wsl ubuntu for development
```
wsl.exe --install
wsl.exe --update
wsl --install -d ubuntu
\\wsl$\Ubuntu\home\shah
```
## link for wsl 1 to wsl 2
```
https://learn.microsoft.com/en-us/windows/wsl/basic-commands#set-wsl-version-to-1-or-2
https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-2---check-requirements-for-running-wsl-2
```
## wsl 2
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
wsl --set-default-version 2
wsl.exe --set-version Ubuntu 2

wsl -l -v
```
## ubuntu release
```
lsb_release -a
```
## php
```
sudo apt update
sudo add-apt-repository ppa:ondrej/php
sudo apt update
```
## for apache
```
sudo apt install php8.2 -y
```
## for nginx
```
sudo apt install php8.2-fpm
sudo systemctl status php8.2-fpm
```
## install PHP Extensions
```
php --version
sudo apt-get install -y php8.2-cli php8.2-common php8.2-fpm php8.2-mysql php8.2-zip php8.2-gd php8.2-mbstring php8.2-curl php8.2-xml php8.2-bcmath php8.2-intl
```
## zsh
```
sudo apt install curl zip unzip
sudo apt install zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
sudo nano .zshrc
export PATH="$PATH:$HOME/.config/composer/vendor/bin"
```
## mysql
```
sudo apt install mysql-server
ps -ef | grep mysql
kill [the id]
sudo /etc/init.d/mysql restart
sudo /etc/init.d/mysql start
sudo /etc/init.d/mariadb start
 sudo mariadb
sudo  mysql -u root -p
CREATE DATABASE lv;
CREATE USER 'admin'@'localhost' IDENTIFIED BY '123456';
GRANT ALL ON lv.* TO 'admin'@'localhost';
FLUSH PRIVILEGES;
QUIT;
```
## /etc/mysql/my.cnf
```
[mysqld]                                                                                                                
bind-address = 0.0.0.0                                                                                                    
user=root                                                                                                               
pid-file     = /var/run/mysqld/mysqld.pid                                                                                
socket       = /var/run/mysqld/mysqld.sock                                                                               
port         = 3306                                                                                                                                                                                                                              

[client]                                                                                                                
port         = 3306                                                                                                      
socket       = /var/run/mysqld/mysqld.sock
```
## mysql
```
chmod 777 -R /var/run/mysqld
chmod 777 -R /var/lib/mysql
chmod 777 -R /var/log/mysql

mysqld

mysql -uroot -pYourPass
```
## mariadb
```
sudo apt install mariadb-server
mariadb --version
sudo /etc/init.d/mariadb start
sudo /etc/init.d/mariadb status
sudo mariadb
#or
sudo mysql
```
## Where is the Ubuntu file system root directory in Windows Subsystem for Linux and vice versa?
```
%userprofile%\AppData\Local\Packages\Canonical...\LocalState\ext4.vhdx
```
## Where is the kali linux file system root directory in Windows Subsystem for Linux and vice versa?
```
C:\Users\shahmohamadi\AppData\Local\Packages\KaliLinux.54290C8133FEE_ey8k8hqnwqnmg\LocalState\ext4.vhdx
```
## alias
```
nano ~/.zshrc
alias nrd="npm run dev"
```
## change php version
```
sudo update-alternatives --config php
```
## install microsoft store
```
powershell run as administrator
wsreset-i
```
## wsl proxy
```
export http_proxy="http://localhost:2081"
export https_proxy="http://localhost:2081"
export ftp_proxy="http://localhost:2081"

nano ~/.bashrc
```
