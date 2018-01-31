---
title: Webmin Panel on Ubuntu 16.04
categories:
  - Linux
tags:
  - linux
  - server
  - webmin
  - panel
  - ubuntu
toc: true
gallery:
  - url: /assets/images/Webmin/pkg-manager.png
    image_path: /assets/images/Webmin/pkg-manager.png
    alt:
    title: "Package Manager"
  - url: /assets/images/Webmin/dashboard.png
    image_path: /assets/images/Webmin/dashboard.png
    alt: 
    title: "Dashboard"
  - url: /assets/images/Webmin/file-manager.png
    image_path: /assets/images/Webmin/file-manager.png
    alt:
    title: "File Manager"   
---
---
<span class="firstcharacter">W</span>ebmin is a web-based system administration tool for Unix-like systems. It provides a straightforward alternative to command line system administration and can be used to manage numerous aspects of a system, such as users and services, through the utilization of the provided Webmin modules. 

If you wish to manage your own server however you're uncomfortable with the command line, Webmin could be a smart tool to assist you get started.

Webmin also gives you a file manager, package updater, user control and much more to view and edit your files. 

{% include gallery caption="Some Webmin features." %}


---
## Installation

Install and update Webmin via APT, edit the /etc/apt/sources.list file on your system and add the line :

`deb http://download.webmin.com/download/repository sarge contrib`

You should also fetch and install the GPG key with which the repository is signed, with the commands :

```bash
cd /root
wget http://www.webmin.com/jcameron-key.asc
apt-key add jcameron-key.asc
```
You will now be able to install with the commands :

```bash
apt-get update
apt-get install apt-transport-https
apt-get install webmin
```


All dependencies should be resolved automatically.
___
### Accessing Webmin Panel

Webmin panel can be accessed via any browser. 

Open this URL in your web browser (substitute the IP address): 

`https://ip-address-of-server:10000`

You will be prompted with a warning that claims your server's SSL certificate isn't trustworthy. This is because Webmin generates and installs an SSL certificate upon installation. This SSL certificate wasn't issued by a certificate authority that's trusted by your pc. Although your pc cannot verify the validity of the certificate, you know that you are, in fact, accessing your own server. It's fine to proceed.

Instruct your browser to trust the certificate. 

If you're using Chrome, click the Advanced link, then click the Proceed to server_IP_address (unsafe) link. 

If you're using Firefox, click I understand the Risks, then the Add Exception... button, then the confirm Security Exception button. 

The login window looks like this - 

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/Webmin/canvas.png){: .align-center}
 

The login credentials are the same as your Ubuntu server's username and password. 

Log in and explore the unknown territory that is known as Webmin. 

---


