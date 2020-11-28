---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Misc things
subtitle: Some things you may want to change and their locations
--- 
# WIP
## Panel [`/var/www/pterodactyl/`]
* Tab Icon (Favicon)
  * `public/favicons`
* Logos (such as in the login and error screens)
  * `public/assets/svgs`
* `container@Pterodactyl~` *([Requires Rebuilding](../../panel))
  * `resources/scripts/components/server/Console.tsx`
  * line 59
* Colors *([Requires Rebuilding](../../panel))
  * `tailwind.config.js`

## Wings *([Requires Building](../../wings))
* `[Pterodactyl Daemon]:`
  * `server/console.go`
  * line 166
