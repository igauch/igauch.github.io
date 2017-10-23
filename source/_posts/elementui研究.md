---
title: element-ui研究记录
date: 2017-10-15 12:15:23
---

出于**不要重复造轮子**的伟大忠告，同时团队也已经编写完成了一套简单的组件库，着实没有必要浪费时间和精力、为了学习再去重头写一个组件库，更何况还写不出😂   
我们先直奔主题，研究[elementUi](https://github.com/ElemeFE/element)     
## 开始
* 惯例链接[Element UI 贡献指南](https://github.com/ElemeFE/element/blob/master/.github/CONTRIBUTING.zh-CN.md)
* 下载完成打开项目你会看见这么几个文件夹或文件
    * build 用于构建等的一些文件
    * example 用于构建本地文档的
    * packages 组件原代码
    * src 包含了入口文件和组件公用的部分
    * components.json 完整组件列表    
* 在[localhost:8085](localhost:8085)运行`npm run dev`
* 打包`npm run dist`

## 起因
因果，不同的因就有不同的果，首先我想告诉你我为什么要研究element，准确来说是：在基于element做二次开发时遇到的问题 
* 不能直接通过

## package.json
这个文件大家都很熟悉，包含了项目的很多重要信息，所以我们先从这里开始   
