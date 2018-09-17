---
title: SSH public-key authentication to connect to a remote machine
date: 2018-09-06 17:00:00
comments: true
tags:
     - ssh
     - bash
     - linux
categories: 
    - linux
---
This article show the steps to connect your laptop to a remote machine like ARC or Ubuntu in the lab.
Before we start, make sure the what is domain name, like for ARC it is like ```jianyuan@cascades.arc.ct.edu```, while for wire-connected ubuntu it is like  ```jianyuan@128.173.93.178```, where the ip4 address could be easily found by google *my ip address*.  
1. connect VPN if you are out of campus.
2. in remote ubuntu, install openssh-server by ```sudo apt-get install openssh-server```. 
3. in local machine, generate public key by ```ssh-keygen -t rsa -b 4096```. By default it should write sth in ```~/.ssh/id_rsa``` and empty passprahse is OK enough.
4. copy the stuff of ```~/.ssh/id_rsa```

For more details about connect to ARC, refer to https://www.arc.vt.edu/2fa/#keys .