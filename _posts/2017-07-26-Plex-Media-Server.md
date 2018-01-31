---
title: Installing Plex on Ubuntu 16.04
categories:
  - Linux
tags:
  - linux
  - server
  - media
  - plex
  - ubuntu
toc: true

---
---

<span class="firstcharacter">P</span>lex is a feature-rich media library platform that allows you to organize and stream your digital video and audio from virtually anywhere. This guide will show you how to set up the Plex Media Server on your Ubuntu 16.04 LTS, as well as how to connect to your media server from a Plex client application. 

To start, I will assume you understand how to use command line and have a bit of background knowledge of Ubuntu or Debian based operating systems. This install isn’t terribly difficult, but you should know how to install and update applications through terminal.

---
## Plex Installation

Get the latest .deb package using `wget`:


 
>mkdir plextmp
 

 
>cd plextmp
 

 
>wget https://downloads.plex.tv/plex-media-server/1.7.5.4035-313f93718/plexmediaserver_1.7.5.4035-313f93718_amd64.deb
 

 
>sudo dpkg -i plexmediaserver*.deb
 

Start the Plex service


 
>sudo systemctl enable plexmediaserver.service
 


>sudo systemctl start plexmediaserver.service


Open Ports


Plex runs on the port 32400. 
Open the port using the following command:

> sudo iptables -I INPUT -p tcp --dport 32400 -j ACCEPT


---

## Setting up PleX

Open the following link in your browser: 


>http://ip-address:32400/web
 

or


>https://ip-address:32400/web
 

You need a PleX account to continue. So go ahead and Sign Up. 

![Plex](/img/Plexserver/login.png)

Give your server any name you like.

![Plex](/img/Plexserver/1.png)

Add folders where your media files are stored on your server.

![Plex](/img/Plexserver/3.png)

![Plex](/img/Plexserver/4.png)

Select next and you are done.

![Plex](/img/Plexserver/5.png)

![Plex](/img/Plexserver/6.png)

What's Next?

Once the Wizard finishes, the Server will begin scanning your media and creating the Plex Library It can take a little while to completely scan a new Library, depending on how many shows you have. You should also expect some Internet usage while metadata is fetched. You can watch media on a Plex Web App while the Library is building but it's generally better to let the process complete before using the Server.

![Plex](/img/Plexserver/8.png)


For more information you can follow the official PleX documents.
<https://support.plex.tv/hc/en-us/sections/200225647>

There is an official standalone client for Windows. So you don't need to login using browser every time.

![Plex](/img/Plexserver/7.png)


Available on [Plex's official site].
[Plex's official site]: https://www.plex.tv/downloads/

---