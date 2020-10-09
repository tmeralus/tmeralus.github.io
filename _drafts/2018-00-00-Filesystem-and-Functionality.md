---
layout: post
title:  "Page Title "
date:   2017-10-04
excerpt: "minimal description of page"
project: true
tags: [add, tags, here,]
comments: true
---

![Image Title Name](/assets/img/blog/<image-name>)
{:class="img-responsive"}


 extr4 vs btrfs and the differences between the two.  

Ext4 vs. Btrfs: Which Linux File System Should You Use?
https://www.makeuseof.com/tag/ext4-btrfs-making-switch-linux/


Review EXT4 vs. Btrfs vs. XFS
https://www.unixmen.com/review-ext4-vs-btrfs-vs-xfs/


Ext4 vs. Btrfs: Which Linux File System Should You Use?
By Bertel King
Mar 18, 2020

Not sure which Linux file system to choose? These days, the smart choice is btrfs versus ext4... but which one should YOU use?
linux-file-system

Quite honestly, not enough people consider which file system to use for their computers.

Windows and macOS users have little reason to look, since they really have only one choice for their system---NTFS and HFS+, respectively. Linux, on the other hand, has plenty of different file system options, with the current default being the Fourth Extended Filesystem (ext4).

There's an ongoing push to change the default file system to the B-Tree File System (btrfs). But is btrfs better, and when will we see distributions making the change?
What Do File Systems Do?
File cabinet
Image Credit: Maksym Kaharlytskyi/Unsplash

Like physical filing systems such as folders and cabinets, digital file systems manage files. They control how your operating system stores data that isn't in use, what other information (known as metadata) is attached to the data, who or what has access to data, and so on.

File systems operate in the background. Like the rest of an operating system's kernel, they're largely invisible in everyday use. File managers, the applications that you use to manage files, mostly operate in the same way regardless of which file system is running underneath.

File systems are incredibly complex to code. Developers continually revise these systems to include more functionality while becoming more efficient.
Why Switch File Systems?

No code is good for all use cases, and that applies to file systems as well. Some file systems excel for different reasons. The File Allocation Table (FAT) file system is one that nearly every modern operating supports.

USB flash drives and SD cards use the FAT system so that your computer can read them regardless of if you're running Linux, Windows, macOS, or some other operating system.

But these days, FAT isn't as reliable or powerful as some of the other file systems that have since been developed. So while you will see FAT on portable media, you won't see it managing the data on your hard drive.

Apple, perhaps unsurprisingly, is known for making file systems that only work with its devices.
mac-file-system-external
Which Mac File System Is Best for an External Drive?

Formatting a hard drive for use with your Mac? Here are your macOS file system options and how to pick the best one for you.
Linux's Current File System

Most versions of desktop Linux (known as distributions, or "distros" for short) default to the ext4 file system. ext4 has been an improvement to the ext3 file system, which was an improvement over the ext2 file system before it.

ext4 has proven to be a very robust file system, but it is made from an aging code base. Some Linux users seek features which ext4 does not handle on its own. There is software that takes care of some of those desire, but being able to do those things on the file system level would provide better performance. Hence the desire for btrfs.
Understanding ext4: Pros and Cons
GNOME Disks displaying ext4 formatting option

Ext4's limits remain pretty impressive. The largest volume/partition you can make with ext4 is 1 exbibyte---the equivalent of roughly 1,152,921.5 terabytes. The maximum file size is 16 tebibytes---or roughly 17.6 terabytes, which is much bigger than any hard drive a regular consumer can currently buy.

Ext4 is known to bring speed improvements over ext3 by using multiple different techniques. Like most modern file systems, it is a journaling file system, which means that it keeps a "journal" of where files are located on the disk and of any other changes to the disk.

Despite all of its features, it does not support transparent compression, transparent encryption, or data deduplication. Snapshots are technically supported, but that feature is experimental at best.

Theodore Ts'o, a developer who played a key role in ext4's creation, described ext4 as a stop-gap release based on outdated 1970s technology and believed Btrfs offered a better way forward. That was over a decade ago.
Understanding Btrfs: Pros and Cons
GNOME Disks displaying btrfs formatting option

Btrfs, which can be pronounced as "Butter FS", "Better FS", or "B-Tree FS", is a newer file system remade from scratch. Btrfs exists because the developers wanted to expand the functionality of a file system to include additional functionality such as pooling, snapshots, and checksums.

The project began at Oracle, but other major companies have since played a part in development. The list includes Facebook, Netgear, Red Hat, and SUSE.

While enhancements found in btrfs can benefit general consumers, some of the additional features are of more interest to enterprise use. Such functionality is for more demanding use cases that often require more durable hard drives as well.

For organizations that use very large programs with massive databases, having a seemingly continuous file system across multiple hard drives could make consolidation of data much easier. Data deduplication would reduce the amount of actual space data would occupy, and data mirroring would become easier when there is a single, broad file system that needs to be mirrored.

Of course, you can still choose to create multiple partitions so that you don't have to mirror everything. The maximum partition size of a btrfs file system is 16 exbibytes, and the maximum file size is also 16 exbibytes.

Considering that btrfs will be able to span over multiple hard drives, it's a good thing that it supports 16 times more drive space than ext4.
Have Linux Distros Made the Transition?

Btrfs has been a stable part of the Linux kernel since 2013, and you can reformat your hard drives using the file system today. But btrfs is not by any stretch the default Linux file system. Most distros continue to default to ext4.

Why? Files are the most important bits of data on your hard drive. Personal data is irreplaceable. You can reinstall an OS and redownload apps, but without a backup, lost files are gone for good. That's why it's crucial that a file system be proven reliable before switching millions of people over to using it by default.

Ext4 may be old and arguably crusty, but it has also proven to be resilient and reliable. If the power goes out and your computer goes dark, odds are ext4 will have kept your saved data safe.

For most people, such situations are the single most important factor. It's not about how well a file system performs when things are going well, it's about what happens when things go wrong.

One prominent distro has determined that enough time has passed to make a switch. openSUSE now uses btrfs as the default for the /root partition where the operating system lies. For the /home partition that houses your personal files, however, openSUSE has decided to go with the XFS file system instead.

So no, the transition hasn't gone quite as expected. But as we've seen with the Wayland display server, new technologies sometimes take a long time to proliferate across the Linux landscape.
