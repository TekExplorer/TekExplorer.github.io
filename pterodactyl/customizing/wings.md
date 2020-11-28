---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Customize Wings
subtitle: How to apply changes made to wings
---
{: .box-note}
**ℹ️ Note:** You do not have to do this on your production server, and I would recommend making your changes on a separate system.
# Make changes
First, clone the wings repo and enter it
```bash
git clone https://github.com/pterodactyl/wings
cd wings
```
{: .box-note}
You may now make your changes. Once you are done, you will need to build wings.

# Build Wings
You must have golang installed to build wings.
* The official installation method is linked here: [https://golang.org/doc/install](https://golang.org/doc/install)

Run this to build wings
```bash
go build
```
You should now have a `wings` binary file in your wings directory.
## Install the new binary
1. Delete the current wings install.
```bash
systemctl stop wings # stop the wings service
rm /usr/local/bin/wings # delete the current wings binary. you can also choose to move it instead if you want to be able to restore it quickly
```
2. Upload or move your new wings binary to its new home and make it executable.
```bash
# for example
mv /some/path/to/wings /usr/local/bin/ # move wings
chmod u+x /usr/local/bin/wings # make wings executable
```
3. Run wings manually to ensure it works correctly
```bash
# example commands
wings
wings --debug
wings diagnostics
```
4. Enable the wings service once again
```bash
systemctl start wings
```
### Notes
   - You can use an sftp client to upload the binary.
   - If you have permission issues with uploading the file, you can upload it to a different location and copy it over using `cp` or move it with `mv` as root afterwards
   - If you have permission issues with any of the above commands, you can try adding `sudo` to the front of the command or switch to the `root` user with `sudo su`

