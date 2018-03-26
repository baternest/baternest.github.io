---
title: Monitor Gerrit server error_log size
date: 2018-03-26 16:21:24
categories: Script
tags:
---
# Script

```bash
# Checkout error_log size
file="/home/gerrit2/gerrit-2.14.7/logs/error_log"
maxsize=1000    # 1000 kilobytes
actualsize=$(du -k "$file" | cut -f1)
if [ $actualsize -ge $maxsize ]; then
    echo size is over $maxsize kilobytes
    echo "Gerrit error_log size is over $maxsize kilobytes" | mutt -s "Gerrit error_log size warning!" -c baternest@gmail.com
    exit
else
    echo size is under $maxsize kilobytes
fi
```

## Install package

```bash
sudo apt-get install msmtp
sudo apt-get install mutt
```

### Configuration

```bash
vi /etc/msmtprc
```

```bash
vi ~/.muttrc

set sendmail="/usr/bin/msmtp"
set use_from=yes
set realname="gerrit2@server.vm"
set from=gerrit2@server.vm
set envelope_from=yes

```