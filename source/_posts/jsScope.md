---
title: JS作用域
date: 2016-07-19 21:18:33
---

作为JS的系列文章，同样的提醒：我只是把对JS的认识用最粗鄙的语言进行讲解和记录，所以，阅读需谨慎！

这个东西简单、老生常谈，但如果稍不留意还是会经常出错，然而这里我只说几点不直观的演示和讲解
1. 变量提升会先提升函数然后才是变量,见下    
    ```
    fa();//fa
    fb();//Uncaught TypeError: fb is not a function
    //fb()的异常错误代表变量已被声明且作用域判断成功，但因还没定义造成的用方错误
    function fa() {
        console.log('fa');
    }
    var fb=function () {
        console.log('fb');
    };
    ```
    所以，为了避免混乱，也是推荐的规范写法，以后的函数声明还是用变量声明吧。
2. 循环结构和条件结构的用花括号包裹的代码块并不会创建新的作用域，也不是真正的代码块，如下
    ```
    (function(){
        for(var i=0;i<6;i++){
            if(i===3){
                var b=i;
                return false;
            }
            console.log(b);//三次undefined
        }
    })();
    ```
    注意：ES6的`let` `const`已做改进