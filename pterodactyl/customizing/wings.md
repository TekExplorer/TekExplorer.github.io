---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Build Wings
subtitle: How to apply changes made to wings
---
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
2. If wings is already there, delete it first.
3. Make the new wings executable
```bash
chmod u+x /usr/local/bin/wings
```
4. Restart wings with `systemctl restart wings`
