---
layout: article
title: 'Setting Up PHP development environment on Ubuntu 9.04'
date: 2010-04-22 09:05:00.000000000 -07:00
type: post
categories: blog
published: true
status: publish
categories: []
tags: []
meta:
  blogger_blog: meraaaj.blogspot.com
  blogger_author: Aman Dogra
  blogger_5b414faa76516d87e0b4b243ad1d0e3b_permalink: '6329491679088895180'
author:
  login: amandogra
  email: amandogra@gmail.com
  display_name: Aman Dogra
  first_name: ''
  last_name: ''
---

I recently setup my Ubuntu machine for PHP development. This is how I did it.
<!--more-->

## INSTALL APACHE
```
sudo aptitude install apache2 apache2.2-common apache2-mpm-prefork apache2-utils libexpat1 ssl-cert

cd /etc/apache2/mods-enabled

sudo ln -s ../mods-available/rewrite.load rewrite.load

cd /etc/apache2/sites-enabled/

sudo ln -s ../sites-available/optimus optimus\
```

## INSTALL PHP

```
 
sudo aptitude install libapache2-mod-php5 php5 php5-common php5-curl php5-dev php5-gd php5-imagick php5-mcrypt php5-memcache php5-mhash php5-mysql php5-pspell php5-snmp php5-sqlite php5-xmlrpc php5-xsl
sudo sed -i 's/memory_limit = 16M/memory_limit = 32M/' /etc/php5/apache2/php.ini
```

## INSTALL MYSQL

```
sudo aptitude install mysql-server mysql-client libmysqlclient15-dev`\
```

keep the username and password as *root* and *root* respectively

## INSTALL JAVA

```
sudo apt-get install sun-java6-jre sun-java6-plugin sun-java6-fontscd /usr/

sudo mkdir java\
```

## INSTALL SVN
```
sudo apt-get install subversion
```

## INSTALL EXTRA REQUIRED PACKAGES
```

sudo apt-get install php-pear

sudo pear channel-update pear.php.net

pear remote-list
sudo apt-get install fop
sudo pear install HTTP\_Upload

sudo pear install MDB2

sudo pear install MDB2\_Driver\_mysql

sudo pear install Structures\_Graph

sudo pear install XML\_Feed\_Parser

sudo pear install XML\_Parser

sudo pear install XML\_fo2pdf

sudo pear channel-discover pear.phpunit.de

sudo pear channel-discover pear.symfony-project.com

sudo pear install Image\_GraphViz

sudo pear install Log

sudo pear channel-discover pear.phpunit.de
```

## INSTALL FLASH
```
sudo apt-get install flash
```

## MAIL SETTINGS
Get the files related to Mail settings and extract them to the user's
home directory

```
cd $homesudo cp Serializer.php /usr/share/php/XML

sudo cp Unserializer.php /usr/share/php/XML

sudo cp Util.php /usr/share/php/XML

sudo mkdir /usr/share/php/Mail

sudo cp -R Mail\_IMAPv2/\* /usr/share/php/Mail/

```

## VIRTUAL HOST ENTRY

```
sudo vi /etc/apache2/sites-available/optimus
```

Please note that file name 'optimus' is configurable. You can choose any name of your choice instead of 'optimus'

Add the following lines and save the file

```
ServerName myapp
DocumentRoot /var/www/app

AllowOverride ALL

sudo vi /etc/hosts

add a line as follows and save the file:
`127.0.1.1       myapp`
```

