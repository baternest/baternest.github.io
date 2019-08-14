---
title: ubunt-gerrit-daemon
date: 2019-08-14 16:19:43
categories:
tags:
---
$ sudo ln -sfv /srv/gerrit2/bin/gerrit.sh /etc/init.d/gerrit
$ sudo update-rc.d -f gerrit remove
$ sudo update-rc.d gerrit defaults 92
echo "GERRIT_SITE=/srv/gerrti2" > /etc/default/gerritcodereview

https://askubuntu.com/questions/721478/ubuntu-init-d-configuration-not-starting-gerrit-2-11-4-at-boot
http://jhshi.me/2016/08/10/start-gerrit-server-upon-boot-on-ubuntu/index.html