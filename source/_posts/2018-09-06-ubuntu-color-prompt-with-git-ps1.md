---
title: ubuntu color prompt with __git_ps1
date: 2018-09-06 15:20:32
categories:
tags:
---
```bash
vi ~/.bashrc

```

uncomment this line

    #force_color_prompt=yes

add [\033[35m\]$(__git_ps1)

PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[35m\]$(__git_ps1)\[\033[00m\]\$ '
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w                        \[\033[00m\]\$ '