---
title: Modify gerrit's username (NoteDB)
date: 2019-09-02 16:01:32
categories:
tags:
---

https://blog.3skel.com/2019/03/gerrit-converting-from-http-auth-to-ldap/

git clone "ssh://gerrit/All-Users"
git fetch origin refs/meta/external-ids
git checkout -b extid FETCH_HEAD

grep your_id
echo -n "username:your_id" | sha1sum

git mv old
git add
git commit -m
git push origin refs/meta/external-ids