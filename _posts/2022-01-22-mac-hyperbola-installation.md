---
layout: post
title: Installing Hyperbola GNU/Linux-Libre on a 2008-ish MacBook
---

As a short note, the reason why I title this post with "2008-ish MacBook" is because I couldn't find out the exact model. There are like 3 different MacBook models that were released in the years 2008, 2009
and 2010 and they look pretty much exactly the same.

So a few weeks ago I began looking at alternative OS's. For the most part I've only ever used Windows but I wanted to try give another OS a shot, for educations sake.
I was particularly interested in GNU/Linux distributions because the idea of a libre free system sounded pretty cool to me. I also read that many GNU/Linux distro's give users the ability to change basically everything about them which allows for making fully customised systems.

To practice my OS installing skills, I brought out an old second hand MacBook I've had for a while. I'd never really used the device before so it was a perfect test-bed to practice
partioning disks on. 

I chose to install a distribution called Hyperbola GNU/Linux-Libre. I chose it because I saw that it was endorsed by the Free Software Foundation and also that it would allow me to install a desktop
enviornment from scratch, which is something that I wanted to give a shot.

Installing the distro did have some challenges and I ran into a few things that I haven't really seen before. Firstly, the way they distribute downloads for the OS is by a torrent file. There is
no direct download source. Instead you have to download the torrent and use a torrent client to "seed" from other peers. I'd never really torrented anything in the past and I just assumed torrents were only used for pirating software but I learned that it's a very popular choice for distributing Linux OS's. I'm guessing the advantage is that you could potentially torrent the file faster than a direct download as well as the distro owners not needing to have to pay to host the file in a heap of different countries.

After having successfully gotten my hands on the ISO image, I used a software called Rufus on my main Windows machine to create a bootable USB with the ISO image. Rufus makes this process as simple as clicking
a couple of buttons. After having done that I just plugged it into the Mac and booted it up.

I found booting up a seperate drive on a Mac pretty similar to how it's done on a Window's machine. While the system is starting up you have to hold a special key to enter a boot option menu. The special key in my instance was the "option" key. 

I attempted to install the OS several times, each time having failed. I didn't realise that the instructions on the Hyperbola website were designed for a computer using a MBR disk which mine was not. The Hyperbola guide says to create a Linux partition on one of your disks and toggle it as "bootable", however, since my disk was GPT I didn't have this option. From what I understand, the tutorial was aimed for older computers and nowadays most disks are "GPT". To get around this I discovered that the Arch linux guide has instructions for GPT drives which I used. I found myself swapping between both the Hyperbola and Arch linux guides.

Eventually by following both guides I managed to install the OS successfully. It was pretty cool seeing a MacBook boot up and seeing the console instead of the regular desktop. The next step though will be to install a desktop environment to make the laptop a proper workstation.





