#!/bin/bash

#Dando permissões nas pastas
sudo chown -R apache:apache /var/www/html/
sudo chmod -R 755 /var/www

#Criando pastas do Apache
sudo mkdir /etc/httpd/sites-available
sudo mkdir /etc/httpd/sites-enabled

#Criando VHOST e Criando Link Simbolico
echo "
<VirtualHost *:80>
    ServerName www.testecodedeploy.com.br
    ServerAlias testecodedeploy.com.br
    DocumentRoot /var/www/site/
</VirtualHost>" > /etc/httpd/sites-available/site.conf

sudo ln -s /etc/httpd/sites-available/site.conf /etc/httpd/sites-enabled/site.conf

#Restartando Apache
sudo systemctl restart httpd.service

echo Prontinho
