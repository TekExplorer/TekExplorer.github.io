---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Getting Started
subtitle: What you need to have to make changes
---
# Step 1: Make your changes
# Step 2: Rebuild panel assets 
## Install Dependencies
In your panel directory [`/var/www/pterodactyl`] do the following:
```bash
apt install -y nodejs # installs nodejs (needed for yarn)
npm i -g yarn # installs yarn
yarn # Installs dependencies (must be in directory mentioned above)
```
## Build Panel
Run this in your panel directory (mentioned above) to apply changes:
```bash
yarn build --production # Build panel
```
