---
title: ubuntu安装node
date: 2016-11-10 23:19:37
---

使用过Ubuntu的都知道，当我们键入无效命令时会给出提示，除了 `command not found` 外，还有一种推断式的提示，例如，当我们还没安装nodeJS而键入 `node` 命令时，它会给出提示 
```
The program 'node' is currently not installed. You can install it by typing:
apt install nodejs-legacy
```

那么我们是否可以根据这个提示通过apt安装呢？     
这是不推荐的，并且现在是有问题的，遇到问题怎么办？当然问[nodeJS](https://nodejs.org)了，官方给出的命令行方案：   
```
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
sudo apt-get install -y nodejs
```
当然，前提是你已经安装了curl。   
OK，就这样就搞定了！ ✌