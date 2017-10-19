---
title: JS单线程和执行环境    
date: 2016-07-08 22:07:41
---

# 单线程
JS执行是单线程的，人尽皆知，但同时也要知道：现在可以通过一些‘魔法手段’实现多线程  
    
如果在控制台执行如下代码
```
setTimeout(function(){ 
    console.log('hello gauch');
},1000);

while(true){

}
```
你是看不到 `hello gauch` 的输出的。因为while一直在占据着线程，同样的    
```
setTimeout(function () {
    console.log(1);
});
console.log(2);
```
也是先将`2`输出，虽然设置延时为0，更多信息请看下面的执行环境    

# 执行环境  
