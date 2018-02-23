---
title: Environment Setup
date: 2018-02-22 15:15:40
tags:
---
# Windows (Git Bash)

## Download and Install Node.js

[Node.js](https://nodejs.org/en/)

## Install hexo

``` bash
npm install hexo-cli -g
```

## Clone GitHub repo and checkuot source branch

``` bash
git clone git@github.com:Baternest/baternest.github.io.git -b source --recursive
cd baternest.github.io.git
npm install hexo --save
```

## Set author info

``` bash
git config user.name "Luo ZhengHong"
git config user.email "baternest@gmail.com"
```

### Create a new post

``` bash
hexo new "My New Post"
```

### Generate and Deploy the blog

``` bash
hexo generate
hexo deploy
```