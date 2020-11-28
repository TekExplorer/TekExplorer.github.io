---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Build Panel
subtitle: How to apply changes made to your panel
#https://www.freecodecamp.org/news/how-to-install-node-js-on-ubuntu-and-update-npm-to-the-latest-version/
---
# Rebuild panel assets 
## Install Dependencies
The following commands will install the necessary dependencies for building your panel.
* Make sure to be inside your panel directory `/var/www/pterodactyl` 

### Install NodeJS
**Ubuntu/Debian**
```bash
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
apt install -y nodejs
```
**CentOS**
```
curl -sL https://rpm.nodesource.com/setup_12.x | sudo -E bash -
yum install -y nodejs # CentOS 7
dnf install -y nodejs # CentOS 8
```
By now, you should have NodeJS 12 installed. Make sure this is the case by checking `npm -v`
### Install Yarn Dependencies
```bash
npm i -g yarn # installs yarn
yarn add cross-env # installs necessary yarn module
yarn # Installs panel build dependencies
```
## Build Panel
Run this in your panel directory to apply changes
```bash
yarn build --production # Build panel
```
