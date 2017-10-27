---
title: JS原型链和继承     
date: 2017-06-15 12:15:23
---

原型链在JS中是个神奇的存在，因为我们很少去用，但即便只是面试初中级人员，面试官也总会问问你关于原型链的认识和相关问题，但是事实是：掌握原型链确实能让你再上一个台阶，所以我们开始吧！ 
# 原型链   
## [[prototype]]和prototype和__proto__  
请注意！上面标题的第一个prototype外面有两层[]包裹！`[[prototype]] !== prototype`！  
`[[prototype]]`是对象的私有属性，而`prototype`却是只有函数才有的属性！    
**`__proto__`是JS的非标准但许多浏览器实现的属性，即`[[prototype]]`**，也就是`someObject.[[Prototype]] === someObject.__proto__`，当然如果你在控制台操作的话会报错，因为浏览器并没有实现`someObject.[[Prototype]]`这样的操作，所以你如果非要验证的话请使用ES6支持的`Object.getPrototypeOf()`方法，即`Object.getPrototypeOf(someObject) === someObject.__proto__`  

## 