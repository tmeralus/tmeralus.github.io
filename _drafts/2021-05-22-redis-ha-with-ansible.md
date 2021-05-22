---
layout: post
title:  "Redis-HA setup with ansible "
date:   2021-05-21
excerpt: "making things work with jinja2"   
---
https://github.com/tmeralus/ansible-role-redis-sentinel-HA
When working with variables in Ansible, sometimes you don’t need the whole string, just a part of it.

For example, we have a variable like ansible_nodename containing the fqdn: server1.example.org and want to create a label with only the first part: server1

Ansible uses jinja2 for formatting so filters can be applied.

{{  ansible_nodename.split(".")[0] | lower }}
