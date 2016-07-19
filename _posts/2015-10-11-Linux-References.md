---
layout: post
title: Linux References
categories: [os, linux]
tags: [linux, os]
description: the collection of Linux relate articles.
---

## Administration

### LVM

* [Extending an LVM volume](https://www.turnkeylinux.org/blog/extending-lvm)
* [LVM Partition Resizing](http://www.linuxquestions.org/questions/fedora-35/lvm-partition-resizing-666683/)

### crontab

* [Linux Crontab: 15 Awesome Cron Job Examples](http://www.thegeekstuff.com/2009/06/15-practical-crontab-examples/)

### ssh

* know_hosts
  * [ssh-keyscan](http://linux.about.com/library/cmd/blcmdl1_ssh-keyscan.htm)
  * [Printing the SSH host key fingerprint](http://root42.blogspot.com/2009/12/printing-ssh-host-key-fingerprint.html)
  * [How to disable SSH host key checking](http://linuxcommando.blogspot.com/2008/10/how-to-disable-ssh-host-key-checking.html)
* port fowarding
  * [Command Line SSH Tunnel Port Forwarding](http://www.laurencegellert.com/2011/01/command-line-ssh-tunnel-port-forwarding/)
  * [Run SSH Tunnel in background](http://notepad2.blogspot.com/2012/11/run-ssh-tunnel-in-background.html)
  * [Background SSH Forwarding](http://www.greenend.org.uk/rjk/sshfwd/)

### sudo

* [Sudo: You're Doing It Wrong](http://www.bsdcan.org/2014/schedule/attachments/283_2014-04-29%20sudo%20tutorial%20-%20bsdcan%202014.pdf)

### iptables

* [Make all iptables Rules Persistent](http://docs.mongodb.org/manual/tutorial/configure-linux-iptables-firewall/)

### Tips

#### Diagnose issues

* [Linux Performance Analysis in 60,000 Milliseconds](http://techblog.netflix.com/2015/11/linux-performance-analysis-in-60s.html)
  * `dmesg | tail`
  * `vmstat 1` - display statistics of virtual memory, kernerl threads, disks, system processes, I/O blocks, interrupts, CPU activity and much more.
  * `pidstat 1`
  * `iostat -xz 1`
  * `sar -n DEV 1` - Use this tool to check network interface throughput: rxkB/s and txkB/s, as a measure of workload, and also to check if any limit has been reached. 
  * `sar -n TCP,ETCP 1` - This is a summarized view of some key TCP metrics.
  * `top`
  * `lsof` - display list of all the open files and the processes. The open files included are disk files, network sockets, pipes, devices and processes.
  * `netstat` - monitoring incoming and outgoing network packets statistics as well as interface statistics. 
* [Netflix at Velocity 2015: Linux Performance Tools](http://techblog.netflix.com/2015/08/netflix-at-velocity-2015-linux.html)
