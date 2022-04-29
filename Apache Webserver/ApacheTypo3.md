# Typo3 with Apache 2.x, MariaDB, Letsencrypt and Ubuntu 20.04
## Install Apache 2.x
```bash
sudo apt-get install apache2
```
### Enable mod-rewrite and headers
```bash
sudo a2endmod rewrite
sudo a2enmod headers
``` 
### Settings in php.ini
```
max_execution_time = 240
max_input_vars = 2000
memory_limit = 512M
```
## PHP 8.1
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install software-properties-common && sudo add-apt-repository ppa:ondrej/php -y
sudo apt update
sudo apt upgrade -y
sudo apt-get install libapache2-mod-php8.1 -y
sudo apt-get install php8.1-cli -y
sudo apt-get install php8.1-common -y
sudo apt-get install php8.1-curl -y
sudo apt-get install php8.1-gd -y
sudo apt-get install php8.1-gmagick -y
sudo apt-get install php8.1-intl -y
sudo apt-get install php8.1-mbstring -y
sudo apt-get install php8.1-mysql -y
sudo apt-get install php8.1-opcache -y
sudo apt-get install php8.1-readline -y
sudo apt-get install php8.1-xml -y
sudo apt-get install php8.1-zip -y
sudo apt-get install php8.1 -y

sudo apt-get install graphicsmagick -y
```
## MariaDB
```bash
sudo apt-get install mariadb-server
sudo apt-get install mariadb-client
```
## Certbot for Letsencrypt
### Install
```bash
sudo snap install core; sudo snap refresh core
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
```
### Create virtual host for Apache
```bash
sudo certbot --apache -d {domain}
```