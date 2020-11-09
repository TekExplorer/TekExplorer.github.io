---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: How to use Mounts
subtitle: This is a short guide on how to use pterodactyl v1 mounts
--- 

Lets say I want to use `/mnt/second_drive/mount/` as my mount, and should show up in my servers as the `host_folder` folder.

# How to make a mount
1. In your panel's admin page, go to the `mounts` section.
2. In there, set **Name** and **Description** to whatever you want.
3. Now to make the mount, set your **Source** to `/mnt/second_drive/mount` (or your own) and your **Target** to `/home/container/host_folder` (or your own, with `/home/container` being the root directory of your container)
4. Now you have 2 options.
   * `Read Only` means that the files cant be changed in the container
   * `User Mountable` means that users can mount it themselves and gain access to its files. Be careful with setting both to true.
5. Hit `Create`
6. Now, you can set what eggs and nodes have the option to use the mount
   * setting only the paper egg, for example, will allow only servers using that egg to gain access to the mount.
   * setting only node 4, for example, means only servers on that node can use that mount.
Now my paper servers on node 4 can see the `host_folder`!

### Do I need to update wings?
No! Wings will be automatically updated with the new mounts.
