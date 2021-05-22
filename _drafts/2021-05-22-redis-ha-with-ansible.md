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

- name: Install Python dependancies
  pip:
    name: netaddr

- name: check for systemd
  stat:
    path: /etc/systemd
  register: systemd_check

- name: check if firewalld exists
  stat:
    path: /etc/sysconfig/firewalld
  register: firewall_rules

- name: Get list of Redis Masters
  vars:
    data_yaml: |
      #!jinja2: lstrip_blocks: True
      {% for host in groups['redis_nodes'] %}
        {% if hostvars[host]['redis_role'] == 'master' %}
        - {{ hostvars[host]['ansible_default_ipv4']['address'] }}
        {% endif %}
      {% endfor %}
  set_fact:
    # Its ugly but this eliminates white spaces and new lines to format the given value into the redis conf files correctly
    redis_masters: "{{ data_yaml | from_yaml | to_nice_yaml | regex_replace('-','') | regex_replace('\n','') | regex_replace('^\\/', '') }}"
