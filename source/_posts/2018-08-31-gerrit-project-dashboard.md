---
title: gerrit project dashboard
date: 2018-08-31 16:12:29
categories:
tags:
---

[Creating Custom Dashboards in Gerrit](http://chris.wang/posts/2016/01/04/gerrit-dashboards)

[Gerrit Code Review - Dashboards](https://gerrit-review.googlesource.com/Documentation/user-dashboards.html)

``` bash
git clone ssh://ZH_Luo@ubuntu:29418/All-Projects
cd All-Projects
```

``` bash
git checkout --orphan custom-dashboards
vim dashboard-file-name
git reset # if needed to make sure other files aren't going to be committed
git add dashboard-file-name # name of the git config file-formatted dashboard file
git commit -m "add dashboard"
git push origin custom-dashboards:refs/meta/dashboards/branch_name
```

``` vim
[dashboard]
  title = Default Dashbord
  description = Most recent open and merged changes.
[section "Open Changes"]
  query = status:open project:${project} limit:15
[section "Merged Changes"]
  query = status:merged project:${project} limit:15
```