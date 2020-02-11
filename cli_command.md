# Linux
Linux commands 
=========================== start bash  ===========================
#!/bin/bash
# Author:  Yehonatan Tzroyua.
# Created: xxxx-xx-xx.
#Updated: xxxx-xx-xx. 
#Purpose: xxxxxxxxxxxxxxxxxxxxxxxxxx

=========== close tar command ==================

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

 Ulimit -a
 vi /etc/security/limits.conf

* soft nofile 500000

* hard nofile 500000

===============mount=========================
/etc/fstab

mount -t nfs $hostname:/$nameofmount

mount -a

mount /dev/cdrom /root/cdrom 

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

==========file ============================

file xxxx - understand king of file in the system 


=======rpm =======================

rpm -ivh webmin.rpm 

rpm -qa | grep webmin

rpm -e webmin.rpm 

rpm -e --nodeps iptable 

rpm -u filename --- upgrade 

=========firewall =================

service iptable stop 

=========cretae disk ==============
1.fdisk -l ==== list all the disk 
df -h ===== list for all mount disk 
2.fdisk /dev/sdb2
m
n
p
defult
defult ( or +1g)
w =====write to disk 
fdisk -l
3.fsck.ext4 /dev/sdb2 == format the disk 
mkfs /dev/sdb2
4. mkdir xxxx ====== mount the partiton
   mount /dev/sdb2 xxxx
5. /etc/fstab --- save the mount 
   add the mount to file 
==============LVM================= 



=======umask================

change the permission when you are crate file .

umask xxx.txt

locate bashrc 

====================ln -s =================================

ln -s /opt/jboss/T24/jars/t24lib lib
 ln -s /opt/jboss/T24/jars/leumiT24lib leumiT24lib
 ln -s /opt/jboss/T24/jars/gpackjars gpackjars
  ln -s  /opt/jboss/T24/jars/semlib semlib












