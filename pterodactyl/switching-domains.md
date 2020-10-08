---
layout: page
cover-img: https://live.staticflickr.com/4844/45489311404_0567577113_b.jpg
title: Switching Domains
subtitle: For when you need to configure a new domain or ip for your panel
---
<div class="panel panel-warning">
**Warning**
{{: .panel-heading}}
  <div class="panel-body">
When switching domains, you will need to re-create any SSL certificates you may have been using, otherwise, your panel will be using an invalid certificate.
See [Creating SSL Certificates](https://github.com/pterodactyl/documentation/blob/master/tutorials/creating_ssl_certificates.html) documentation page for how to create these certificates before continuing.
  </div>
</div>

## The Panel
You must edit the `APP_URL` in the panel's `.env` file
You will also need to edit the domain in your Webserver Configuration. See  [0.7 Webserver Configuration](https://pterodactyl.io/panel/0.7/webserver_configuration.html) or [1.0 Webserver Configuration](https://pterodactyl.io/panel/1.0/webserver_configuration.html) and edit the `<domain>` fields as appropriate.
## The Daemon/Wings
You must change the url for every node you wish to convert to the new domain in the panel's node settings (the `FQDN` field)
### 0.6 Daemon
Recopy the `core.json` or manually edit the `base_url` field in the existing file to match the panel's new url
### 1.0 Wings
Recopy the `config.yml` or manually edit the `base_url` field in the existing file to match the panel's new url
