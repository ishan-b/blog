---
title: Ubuntu 16.04 Server Installation
categories:
  - Linux
tags:
  - linux
  - server
  - ubuntu
toc: true
---

---

<span class="firstcharacter">R</span>eady to setup your own Home media server? For this installation I’m using Ubuntu 16.04.2 in a Virtual machine on Windows 10. I’ll walk you through the process of installing Ubuntu server. I wrote the important steps of the process and screenshots where ever necessary, so that you can have a Linux server up and running in no time. I’ll be focusing on local access only for the time being.


## Pre-requisites:

* An old computer.
* You need an active internet connection.
* A keyboard.

---
### Step 1: Make a bootable USB

The first thing you must do is download the Ubuntu Server ISO image. Make sure you download **16.04.2 LTS 64 bit** version. Then burn it using **Rufus**. You can refer to the following configuration for Rufus.

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/rufus.png)

* Insert the USB in your server.
* Boot the USB by going into your BIOS settings.

---
### Step 2 : Begin the installation

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (35).png)

* Select Install Ubuntu Server
* Select the language.
* Select the location.
* Select the keyboard layout.

---
### Step 3: Host-name

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (36).png)

Enter any name you like. This host-name is often used to recognize your computer on local networks. If you log on to your router, you can see this name as well as it’s IP address.

---
### Step 4: User configuration

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (37).png)

* Type a full name for the non-root user.
* Type a username for the non-root user.
* Enter and confirm a password for the non-root user.

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (38).png)

When asked if you want to *“configure your home directory for encryption”*, please choose **NO**.

If you really want to encrypt it then you’ll have to log onto your server before you can run any processes (eg. cron jobs) which needs access your home directory. This is because your home directory is only decrypted once you’ve logged onto the server.

---
### Step 5: Disk Partition

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (40).png)

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (41).png)

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (42).png)

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (43).png)

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (44).png)

Unless you need to partition your drive in a non-traditional manner, I highly recommend selecting one of the Guided options.
I also recommend selecting one of the LVM (Logical Volume Management) options here, as it will make managing partitions quite a bit easier.

---
### Step 6: Proxy Settings

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (47).png)

Next you’ll be asked if a proxy is necessary to access the outside world. If your company is behind a proxy, enter it here. I use my server locally, so I have never used proxies before.

---
### Step 7: System Update

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (49).png)

The next step requires you to select how the system will be updated. You have three choices:

* No Automatic Updates
* Install Security Updates Automatically
* Manage System With Landscape

What you select will depend upon how you plan on managing the server. The default choice is No Automatic Updates.

---
### Step 8: Package selection

> Caution : Use space-bar to select options.

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (50).png)

The package selection process uses the tasksel tool. If you’re unsure which packages you want to install, you can always go back once the installation is complete and run tasksel from the terminal and install any packages necessary.
I recommend installing **OpenSSH** server and standard system utilities. We will need them further.

---
### Step 9: Boot loader

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (51).png)

The final step before rebooting is to install the **GRUB bootloader**. Unless you’ve selected a non-traditional partitioning scheme, select Yes, and the boot loader will be installed to the master boot record.
When prompted, reboot the system, and log in as the user you set up during installation.

![Setup](/img/2017-07-13-Ubuntu 16.04 Server Installation/Screenshot (52).png)

Congratulations! You have successfully installed Ubuntu Server on your system.

*P.S. If you are doing this for the first time, you will feel like a hacker. Well, maybe not.*

---