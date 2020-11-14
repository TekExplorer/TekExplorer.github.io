---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Build Wings
subtitle: How to apply changes made to wings
---
{: .box-note}
**ℹ️ Note:** You do not have to do this on your production server, and I would recommend making your changes on a separate system.
# Make changes
First, clone the wings repo and enter it
```git
git clone https://github.com/pterodactyl/wings
cd wings
```
Make your changes as you wish.
# Build Wings
You must have golang installed to build wings.
* The official installation method is linked here: https://golang.org/doc/install
Run this to build wings
```bash
go build
```
You should now have a `wings` binary file in your wings directory.
## Install the new binary
1. The new binary you just built should be placed in the [`/usr/local/bin/`] directory on your server.
   - If wings is already there, delete it first.
   - You can use an sftp client to upload the file.
   - If you have permission issues, you can upload it to a different location and copy it over using `cp` or move it with `mv` as root afterwards
2. Make the new wings executable
```bash
chmod u+x /usr/local/bin/wings
```
3. Restart wings with `systemctl restart wings`
