---
title: OpenWrt LEDE
date: 2018-06-01 15:50:57
categories:
tags:
---
# To upgrade all of the packages, LEDE recommends,

``` ash
  opkg list-upgradable | cut -f 1 -d ' ' | xargs opkg upgrade 
```


opkg install kmod-usb-storage
opkg install usbutils
lsusb -t

opkg install block-mount
block info | grep "/dev/sd"

opkg install kmod-fs-ext4
block detect > /etc/config/fstab

# Install Samba
``` ash
opkg update
opkg install samba36-server luci-app-samba
```

# DHCP Client DNS
``` ash
cat /tmp/resolv.conf.auto
```