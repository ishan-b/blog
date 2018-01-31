---
title: Nextcloud on Ubuntu 16.04
categories:
  - Linux
tags:
  - linux
  - server
  - media
  - nextcloud
  - ubuntu
toc: true
---
---
<span class="firstcharacter">N</span>extcloud is the one stop solution if you want a simple and yet powerful backup server for your home or work. Nextcloud is similar to dropbox with the difference that former is open source. Also Nextcloud eliminates any third party intrusion, so your data always stays with you and never leaves your server.

Assuming you have Ubuntu 16.04 installed, let's get started. 

---

# Installation

The installation is quite easy as there are automated scripts ready by our great GitHub community. 

The original script by TechAndMe requires 2 GB RAM on your server(which sadly I don't have). So I modified the script a bit for my 1 GB server. You can use whichever script you want.

## Steps

Open an SSH window to your server.

Get the latest install script from master:

> wget https://raw.githubusercontent.com/e-sean/vm/master/nextcloud_install_production.sh

Run the script with:

> sudo bash nextcloud_install_production.sh

Follow the on screen instructions which are quite easy. Read them carefully. 

When the installation finishes, your machine will reboot. This time login with the new user that you created within the script. And the script will install some more components to your server.

If the script does not run after reboot, then type in the command below

> sudo -u <user> sudo bash /var/scripts/nextcloud-startup-script.sh

After everything is finished installing, go to your `server ip/nextcloud` and login to find your new backup server ready.





There is a modified version for RaspberryPi too. So your little Pi can become your data saver!

More info and original script is [here.](https://github.com/nextcloud/vm)



---

