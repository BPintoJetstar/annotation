
# Instalatling LAMP (Linux Ubuntu\ Apache \ MySQL\ PHP)
This tutorial teaches you how to install and setup laravel application on Ubuntu.

## Install Ubuntu
........building.........

## Installing LAMP
This step will install Apache,MySQL and PHP at once.
Make sure your sistem is well-updated.
```
sudo apt-get update

```
Then, exectue the following (do not forget the symbol ^)
```
$ sudo apt-get install lamp-server^

```

## Installing laravel 
Before instaling laravel you need to install Composer.
```  	
$ curl -sS https://getcomposer.org/installer | php
```
After installing Composer you need to change  'composer.phar' file location as following:
```
sudo mv composer.phar /usr/local/bin/composer
```
Then finally install the laravel with this command
```
composer global require "laravel/installer=~1.1"
```
After that you need to set the PATH variable depend on which location your composer is instaled.
```
export PATH="~/.composer/vendor/bin:$PATH" 
```
OR if your composer is located inside the .config directory
```
PATH="~/.config/composer/vendor/bin:$PATH"
```
## Creating your Laravel projecto
```
composer global update
Laravel new nome_projeto
php  artisan 
```
