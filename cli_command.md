# Linux
Linux commands 
===========================bash ===========================
#!/bin/bash
# Author:  Yehonatan Tzroyua.
# Created: xxxx-xx-xx.
#Updated: xxxx-xx-xx. 
#Purpose: xxxxxxxxxxxxxxxxxxxxxxxxxx

=========== colse tar command ==================

tar -xvf /tmp/yoni.tar.gz -C / my_tar---------- OPEN TAR

==========open tar coomad ============
tar -cvf byoni.tar.gz /opt/jboss 

tar -cvf byoni.tar.gz /opt/jboss--exclude='/opt/jboss/etc/log/*' --exclude='/opt/jboss/etc/tmp/yoni.txt - open tar exculde file or dic


==========copy files with scp ==========

scp /tmp/data/rar root@10.93.0.5:/tmp//

===========copy files with rsync==========

rsync -avze ssh --progress --exclude '/tmp/excludefile.txt/' /jbossusr@10.93.0.5:/opt/jboss

rsync -avze ssh --progress --exclude-from '/tmp/exclude-list.txt/' /jbossusr@10.93.0.5:/opt/jboss

anther example: https://www.tecmint.com/rsync-local-remote-file-synchronization-commands/

=================java and jboss commands=======================

ps -ef | grep java | grep jbossuser

java -version 

sudo vim /etc/init.d/jboss 

sudo vim /home/jbossuser/.bash_profile 

sudo update-alternatives 

=============cpu and memory ======================================


less /proc/cpuinfo | grep "cpu MHz"
lscpu 

less /proc/meminfo | grep "MemFree"

top 

ps -p $PID -o %cpu,%mem

egrep –color ‘Mem|Cache|Swap’ /proc/meminfo

free -h
=============security( fix the issue with premission after mount windows mount )===========================

vi /etc/security/limits.conf

* soft nofile 500000

* hard nofile 500000

===============mount=========================

/etc/fstab

mount -t nfs $hostname:/$nameofmount

mount -a

=============crontab==============

crontab -l ===== for list 
crontab -e =====for edit 

==============password============

passwd

============networks==============

cd /etc/sysconfig/network-scripts/

nano ifcfg-eth0
 
 =============disk space =================

du --max-depth=1 -h

df -h

=============find =======================

find /opt/jboss/\&yoni\& -type f mtime +8 | wc -l 

find /opt/jboss/\&yoni\& -type f mtime +8 | -exec rm {}+

==============version=============================

cat /etc/os-release


