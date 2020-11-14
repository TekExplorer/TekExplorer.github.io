---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Build Panel
subtitle: How to apply changes made to your panel
---
# Rebuild panel assets 
## Install Dependencies
The following commands will install the necessary dependencies for building your panel
Make sure to be inside your panel directory `/var/www/pterodactyl` 
```bash
apt install -y nodejs # installs nodejs (ubuntu and debian only. if you use centos, google how to install it)
npm i -g yarn # installs yarn
yarn add cross-env # installs necessary yarn module
yarn # Installs panel build dependencies
```
## Build Panel
Run this in your panel directory to apply changes
```bash
yarn build --production # Build panel
```
