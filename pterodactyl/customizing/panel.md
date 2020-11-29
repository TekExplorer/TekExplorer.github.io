---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Build Panel
subtitle: How to apply changes made to your panel
#https://www.freecodecamp.org/news/how-to-install-node-js-on-ubuntu-and-update-npm-to-the-latest-version/
---
The official [BUILDING.md](https://github.com/pterodactyl/panel/blob/develop/BUILDING.md)
# Rebuild panel assets 
## Install Dependencies
The following commands will install the necessary dependencies for building your panel.
### Install NodeJS
***NOTE:*** You may have to add sudo to the following commands if you are not root.
```bash
# Ubuntu/Debian
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
apt install -y nodejs

# CentOS
curl -sL https://rpm.nodesource.com/setup_12.x | sudo -E bash -
yum install -y nodejs # CentOS 7
dnf install -y nodejs # CentOS 8
```
By now, you should have NodeJS 12 installed. Make sure this is the case by checking `npm -v`
### Install Yarn and Panel Dependencies

{: .box-warning}
**⚠️ Warning:** Do not ever run `yarn upgrade`! This will upgrade webpack and screw up your panel!

```bash
npm i -g yarn # Installs yarn
yarn install # Installs panel build dependencies
```
## Build Panel
Run this in your panel directory to apply changes (usually `/var/www/pterodactyl`)
```bash
yarn build:production # Build panel
```
