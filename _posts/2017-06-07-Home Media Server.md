---
title: Home Media Server
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
 <span class="firstcharacter">T</span>he point of this story is to introduce you to (and hopefully teach you how to install everything) the manner I exploit my computers and servers. This is by no means the most effective or correct way to use a bunch of computers, however I have found that it suits most of my (and others) needs. The hardware I exploit is by no means that high-end. I conjointly don’t assume that I exploit my hardware to the utmost, however I don’t need to. Nevertheless, I have yet to find a bottleneck with my server.

My server is just an old computer with a 2nd generation Intel i3 with 2 gigs of RAM. I have installed some old HDD’s on to it, so the total space available for storage is 1.5 TB. All my movies and Anime are stored here. Even I store some of my photos here.

I have a really slow router (150 mbps). But that doesn’t mean I cannot stream in HD. In fact, I can stream 1080p videos without glitch. 4K streaming is what gives me problems. My router cannot handle such high bitrates.

Typically my workflow consists of several steps if I am not using a service like Netflix or Amazon Prime -

* Find a movie
* Download it to a server
* Download it from server down to my local machine for watching.

![Setup](/img/setup.png)
*My home setup*

The last part of this workflow is normally time consuming even though I have a decent internet connection and the process being automated.
 
So a couple of weeks ago I decided to give Plex media server a go.
The advantage of this approach is that the movie is ready for watching the minute it’s done downloading. I just stream it directly from the server. On top of that, I can stream to any device I want, so no copy/paste of videos required.

Also I connected a RaspberryPi to my TV(HDMI) since my TV does not have WiFi. The Pi is connected to WiFi which can stream videos off my server.
You can run Plex through your browser. Enter the IP address of the server and you will see something like this -

![Setup](/img/1.png)
*Plex on Chrome browser*
 
And this is what you see when you open a movie -

![Setup](/img/2.png)
*Plex UI*

Pretty neat, right ? I think so too.

The next cool thing I want to tell is Nextcloud. With this application you can browse through your server files just like you do in Windows Explorer. You can do upload, download, delete, rename or anything you want to.

![Setup](/img/3.png)
*Nextcloud on Chrome*

Nextcloud allows you to create different accounts for family members and share files with them. Nextcloud is available on Android, Windows & iOS.

![Setup](/img/4.png)
*Nextcloud Users*

Here are the steps for you to install this kinda setup-

* Install Ubuntu Server on a server (old PC).
* Install Plex media server on your server.
* Install Plex clients on your laptop and mobile.
* Set up Nextcloud.

---