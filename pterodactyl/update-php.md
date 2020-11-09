---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Update to php 7.4
subtitle: For when you need to configure a new domain or ip for your panel
--- 

# For for anyone with a `Malformed Communication Packet` error in their panel
You need to update php from 7.2 to 7.4.
{: .box-note}
**ℹ️ Note:** Add `sudo` as necessary if you are not `root`
## Upgrade to php 7.4
```bash
# Install php7.4
apt-add-repository ppa:ondrej/php
apt update
apt -y install php7.4 php7.4-{cli,gd,mysql,pdo,mbstring,tokenizer,bcmath,xml,fpm,curl,zip}

# Remove old php 7.2
apt-get purge php7.2*
```
## Update Webserver
### Nginx
```bash
nano /etc/nginx/sites-available/pterodactyl.conf
```
Change `fastcgi_pass unix:/run/php/php7.2-fpm.sock;` to `fastcgi_pass unix:/run/php/php7.4-fpm.sock;`
Note the change from 7.2 to 7.4
```bash
systemctl restart nginx
```
### Apache
```bash
# Enable php 7.4
a2enmod php7.4
# Disable php 7.2 
a2dismod php7.2
```
