---
title: SSL Tunneling
date: 2019-09-19 10:55:21
categories:
tags:
---

https://www.youtube.com/watch?v=AtuAdk4MwWw

"Local" Port Forwarding or "Local" Tunneling
ssh -L 8181:192.168.0.135:3389 pi@192.168.0.135

"Dynamic" Port Forwarding or "Dynamic" Tunneling
ssh -D 8181 pi@192.168.0.135

"Reverse" Port Forwarding
ssh -R 8181:localhost:3389 pi@192.168.0.135

/etc/ssh/sshd_config
AllowTcpForwarding yes
GatewayPorts yes
