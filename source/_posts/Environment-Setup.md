---
title: Environment Setup
date: 2018-02-22 15:15:40
tags:
---
# Windows (Git Bash)

## Download and Install Node.js

[Node.js](https://nodejs.org/en/)

### Install hexo

``` bash
npm install hexo-cli -g
```

### Setup Environemt Variables, add node.js to Path

| Variable name | Variable path |
|:-------------:|:-------------:|
| node.js       | %APPDATA%\npm |
| Path          | %node.js%     |

### Clone Github repo and checkuot source branch

``` bash
git clone git@github.com:Baternest/baternest.github.io.git -b souce --recursie

npm install hexo --save
npm install hexo-deployer-git --save
```

### Create a new post

``` bash
hexo new "My New Post"
```

### Deploy the blog

``` bash
npm i -S hexo-deployer-git
hexo deploy
```