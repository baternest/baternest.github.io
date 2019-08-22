---
title: Automate EV code signing
date: 2019-08-20 17:39:07
categories:
tags:
---

Windows API:
https://stackoverflow.com/a/26126701

https://www.sorinmustaca.com/sign-files-unattended-in-batch-mode-while-having-an-etoken-no-password-popup/
signtool sign /f mycert.cer /csp "eToken Base Cryptographic Provider" /k "[{{TokenPasswordHere}}]=KeyContainerNameHere" myfile.exe
signtool sign /f EVCode.cer /csp "eToken Base Cryptographic Provider" /k "[{{PIN }}]=CONTAINER_NAME " /t http://timestamp.digicert.com unsign.exe

