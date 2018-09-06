---
title: Ubuntu Server 16.04 in VM for Gerrit server
date: 2018-03-29 10:25:17
categories: Ubuntu
tags: Server
---
# Install Ubuntu Server 16.04 in VMware Workstation 14 Player

## Install Packages

```bash
sudo apt-get update
sudo apt-get install openssh-server
sudo apt-get install open-vm-tools
```

```bash
sudo mkdir /mnt/hgfs
sudo vmhgfs-fuse .host:/$(vmware-hgfsclient) /mnt/hgfs/ -o allow_other
```

### Mount

```bash
vmhgfs-fuse .host:/$(vmware-hgfsclient) ~/some_mountpoint
sudo mount -t fuse.vmhgfs-fuse .host:/ /mnt/hgfs -o allow_other
```

### Mount

```bash
.host:/ /mnt/hgfs fuse.vmhgfs-fuse allow_other 0 0
```

```bash
sudo apt-get install default-jre
sudo apt-get install apache2 postgresql
```

```bash
sudo su postgres
createuser --username=postgres -RDIElPS gerrit2
createdb --username=postgres -E UTF-8 -O gerrit2 reviewdb
```

```bash
java -jar gerrit.war init -d /path/to/your/gerrit_application_directory
```