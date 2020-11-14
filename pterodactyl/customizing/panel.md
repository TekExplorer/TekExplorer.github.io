---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Panel
subtitle: How to apply changes made to your panel
---
# Rebuild panel assets 
## Install Dependencies
The following commands will install the necessary dependencies for building your panel
```bash
apt install -y nodejs # installs nodejs
npm i -g yarn # installs yarn

cd /var/www/pterodactyl # go to your panel directory; needed for the following command
yarn # Installs panel build dependencies
```
## Build Panel
Run this in your panel directory to apply changes
```bash
yarn build --production # Build panel
```
