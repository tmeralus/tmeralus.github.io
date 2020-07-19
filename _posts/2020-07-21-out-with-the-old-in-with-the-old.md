---
layout: post
title: "Out with the old, in with the Nagios?"
date: 2020-07-17
excerpt: "Setting up Nagios"
tags:
---
## Taking a modern day approach to managing a classic application

I have to admit I learned about Nagios about a decade after its initial release. In a sprint of learning new technologies in my previous job I had to learn how to navigate through Nagios and understand why it was being used and what it was being used for.
To understand what Nagios core is: Nagios provides enterprise-class Open Source IT monitoring, network monitoring, server and applications monitoring.

To break things down it is the essential server monitoring tool created in 2002. It has been "replaced" by many other tools that have plenty of features and options for backups, data manipulation, and others... but Nagios works. For the services provided with Nagios core, it works for many modern day networking practices. We were able to check connection settings and availability of servers using nagios and alert us via text or email if servers crashed or went down.
In the midst of learning that I was tasked to move the Nagios platform from a redhat 6 server to a centos 7 server. My first thoughts when building it out were 1. There has got to be a better way to migrate all of this without breaking things 2. There has got to be a plan for the next upgrade cycle. 3. There must be a way to save the config files. My answer became a multipart solution. Using git to save personal config files, using Ansible to deploy it to a new server, and running Ansible playbooks to maintain nagios.

Git is the perfect tool to save the config files and manage the changes of the files to make sure that, if your monitoring server crashes and cant be restored, there is a location where the files are saved.

Ansible allowed me to manage the OS arc and deployment steps on downloading the proper dependancies, nagios plugins, and other requirement for setting up a nagios container. [This playbook](https://github.com/tmeralus/ansible-role-nagios-server) was a helpful start to show how others setup and deploy nagios through Ansible. The original playbook was forked from [here](https://github.com/sadsfae/Ansible-nagios) and thus became its own monster. In the short amount of time I had I chose to tweak the playbook to my liking. Using Ansible allowed me to make changes to Nagios hosts or contact settings in nagios without having to go into the Nagios server itself.  Managing Nagios and restarting or stopping it to configure the changes could now be done running an Ansible playbook saved in github.

Now instead of worrying about all the possible locations or connected config files in a linux server I knew where they all were. Years from now if we have to upgrade from CentOS 7 to 8 or to a debian based Ubuntu distro I'm less worried about rsyncing data from one box to another and more focused on running the playbook and getting going in no time.

Using the knowledge I had with Ansible and git allowed me to take an old Nagios platform and use with a more modern day approach. The old approach of pulling the tar file from nagios and trying to untar and configure the perl scripts from scratch is now a thing of the past. Managing Nagios has become easier than ever.
