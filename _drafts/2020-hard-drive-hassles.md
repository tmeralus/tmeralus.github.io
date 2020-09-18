---
layout: post
title:  "Hard Drive Hassles"
date:   2020-09-12
excerpt: "First time Linux failed me"
tags: [ ]
comments: true
---
 
## The wild wild west with western digital 

Linux is the swiss army knife for hacking, building, and repairing a majority of issues 
found on the internet. When it comes to fixing hard drives, whether it be formating, partitioning, 
resizing, or recovering data, Linux and open source software like GParted will normally do the trick. 
I have been using these tools 

3tb external not working 
checking if drive is listed 
listed as NTFS first 
then unlisted 
not working properly. 
shows up on gparted. 
shows run checkdisk -f to repair 
partition block not recognized. 
switch to windows. 
drive shows up 
plug and unplug drive does not show up but windows oop up shows up 

switch to linux fdisk check
found nothing. 
unplug and replug
mount drive. 
lsblk to check again. 

Fdisk Error Message
https://unix.stackexchange.com/questions/530703/fdisk-error-message

An error message appears after you enter the fdisk command with the absolute path of the disk (1010009)
https://kb.vmware.com/s/article/1010009

Gparted resize of an extended partition fails with error “can't have overlapping partitions”.
https://askubuntu.com/questions/145554/gparted-resize-of-an-extended-partition-fails-with-error-cant-have-overlappin

