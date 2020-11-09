---
layout: page
#cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Using S3 for backups
subtitle: For when you would rather upload backups to the cloud
---

If you wish to use S3 for your backups, the following ENV variables may be considered for your `.env` file [`/var/www/pterodactyl/.env`]
```environment
# Sets your panel to use s3 for backups
APP_BACKUP_DRIVER=s3

# Info to actually use s3
AWS_DEFAULT_REGION=

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=

AWS_BACKUPS_BUCKET=

AWS_ENDPOINT=

# Dunno what these are but maybe you do?
AWS_USE_PATH_STYLE_ENDPOINT=false
AWS_BACKUPS_USE_ACCELERATE=false
```
Hopefully i've pointed you in the right direction
