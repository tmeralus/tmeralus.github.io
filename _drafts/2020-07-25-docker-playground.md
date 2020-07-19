---
layout: post
title:  "Simple Site Setup "
date:   2019-01-25
excerpt: "creating your personal piece of the internet"
project: true
tags: [add, tags, here,]
comments: true
---

![Image Title Name](/assets/img/blog/simple-site-setup.png){:class="img-responsive"}


I have to admit I learned about Nagios about a decade after its initial release. In a sprint of learning new technologies in my previous job I had to learn how to navigate through Nagios and understand why it was being used and what it was being used for.
To understand what Nagios core is:Nagios provides enterprise-class Open Source IT monitoring, network monitoring, server and applications monitoring.

To break things down it is the essential server monitoring tool created in 2002. It has been "replaced" by many other tools that have plenty of features and options for backups, data manipulation, and others... but Nagios works. For the services provided with nagios core, it works for many modern day networking practices.
In the midst of learning that I was tasked to move the nagios platform from a redhat 6 server to a centos 7 server. My first thoughts when building it out were 1. There has got to be a better way to do this and 2. There has got to be a plan for the next upgrade cycle. 3. There must be a way to save the config files. My answer became a 3 part solution. Using git to save personal config files, and use Docker to maintain the setup of Nagios.

The nagios server itself
