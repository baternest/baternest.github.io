---
title: KeyStore Explorer
date: 2019-08-15 10:00:41
categories: java
tags: cert
---
# Import self-signed CA  into JAVA cacerts file

Windows path: JAVA_PATH\jre\lib\security

GUI tool: https://keystore-explorer.org/

https://docs.microsoft.com/zh-tw/azure/java/java-sdk-add-certificate-ca-store
keytool -keystore cacerts -importcert -alias bc2025ca -file bc2025.cer
keytool -list -keystore cacerts
