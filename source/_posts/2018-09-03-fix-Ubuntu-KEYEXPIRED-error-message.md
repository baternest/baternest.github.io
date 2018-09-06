---
title: fix Ubuntu KEYEXPIRED error message
date: 2018-09-03 15:48:06
categories:
tags:
---

``` bash
sudo apt-get update
W: An error occurred during the signature verification. The repository is not updated and the previous index files will be used. GPG error: http://storage.googleapis.com/bazel-apt stable InRelease: The following signatures were invalid: KEYEXPIRED 1527185977  KEYEXPIRED 1527185977  KEYEXPIRED 1527185977
W: Failed to fetch http://storage.googleapis.com/bazel-apt/dists/stable/InRelease  The following signatures were invalid: KEYEXPIRED 1527185977  KEYEXPIRED 1527185977  KEYEXPIRED 1527185977
W: Some index files failed to download. They have been ignored, or old ones used instead.
```

``` bash

apt-key list | grep expired
$ pub   4096R/48457EE0 2016-05-24 [expired: 2018-05-24]
sudo apt-key adv --recv-keys --keyserver keys.gnupg.net 48457EE0

```
