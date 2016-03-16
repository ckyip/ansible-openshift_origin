## Overview 

A class assignment where we were required to modify existing ansible playbook 
at https://github.com/maxamillion/ansible-openshift_origin
to do the following:


## About

This playbook installs OpenShift M4 for
* Single Broker
* Multi Nodes

## Requirements

Broker & Node
* Centos 6.7
* Dual homed (eth0 = internal, eth1 = external)

Deploy Host
* Ansible 2.1.0 (w/python-netaddr package installed)



## Configuration

1. Place Internal IP for Broker & Node in /etc/ansible/hosts 


Example:

    [brokers]
    192.168.1.100

    [nodes]
    192.168.1.101
    192.168.1.102

2. Please change default role settings at ansible-openshift_origin/group_vars/all
   (i.e. login password and keys)


## Installation
* ansible-playbook ansible-openshift_origin/site.yml

## Post-Installation
* Please follow step 12 in OpenShift Comprehensive Guide

## Other
* See included pdf file for more detail
* Written for course: https://scs.senecac.on.ca/~raymond.chan/ops635/1601/
* Student: Colin Yip
