---
title: Environment Setup
date: 2018-02-22 15:15:40
categories: Blog
tags: Hexo
---
# Setup environment for write down note (Windows)

## Prerequisite

- Install [Git for Windows](https://git-scm.com/download/win) (Git Bash)

- Install [Node.js](https://nodejs.org/en/) (not necessary, but recommended)

- Install [Visual Studio Code](https://code.visualstudio.com/download) as markdown editor

## Install hexo (if node.js installed)

``` bash
npm install hexo-cli -g
```

## Clone GitHub repository and checkout source branch

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

or create markdown file into source/_post folder

### Just commit and push to GitHub

``` bash
git add
git commit
git push
```

[Travis-CI](https://travis-ci.org/Baternest/baternest.github.io) wll auto generate and deploy to https://baternest.github.io