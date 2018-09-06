---
title: Buffalo WZR-HP-G450H + OpenWrt
date: 2018-05-30 16:27:05
categories: router
tags: openwrt
---
# 前言

發現有新版的OpenWrt (LEDE 17.01)，更新時未仔細確認
一時手殘刷掛機器...

救援參考：[Buffalo WZR-HP-G450H 刷 OpenWRT – 比尔盖子 博客](https://tomli.blog/archives/2014/07/1878.html)

# 設定802.1X認證(有線網路)

http://www.cnblogs.com/kkzxak47/archive/2013/03/16/2961964.html

# wget https link

```` sh
# opkg update
# opkg install wget
````

wpa_supplicant -B -i eth0.3 -c /etc/wpa_supplicant/wpa_supplicant.conf -D wired

udhcpc -i eth0.3

remove wpa-mini
install wpad

luci-app-samba
samba36-server