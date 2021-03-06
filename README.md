# Data

#### 如何通过饿了么Node.js面试

***

阅读了饿了么Node.js面试第一篇js-基础篇.在这里了解到作为前端方向,在不同的工作经验下都需要掌握到什么知识点,要求我们作为工程师要不间断地跟新自己的知识.并且在不同的阶段自己的代码对于代码的有效维护,不同的写法会对内存性能有影响.

#### js基础问题

> 与前端 Js 不同, 后端是直面服务器的, 更加偏向内存方面.

* 类型判断
* 作用域
* 引用传递
* 内存释放
*  ES6 新特性



##### 类型判断

***

js六大数据类型：number、string、object、Boolean、null、undefined

string： 由单引号或双引号来说明，如"string"

number：什么整数啊浮点数啊都叫数字，你懂的~

Boolean: 就是true和false

undefined：未定义，就是你创建一个变量后却没给它赋值~

null: 故名思久，null就是没有，什么也不表示

object: 这个我也很难解释的说。就是除了上面五种之外的类型



##### 作用域

***

在面试时, 作用域并不是一个很好问的知识点, 一般会问的是 `es6 中 let 与 var 的区别`, 或者列举代码, 然后通过对代码的解读来看你对作用域的掌握比较方便.

这里讲到了一本书 《你不知道的 Javascript》,对于作用域讲解很到位.



##### 引用传递

***

引用传递和值传递是一个非常简单的问题, 也是理解 Javascript 中的内存方面问题的一个基础. 如果不了解引用可能很难去看很多问题.

面试写代码的话, 可以通过 `如何编写一个 json 对象的拷贝函数` 等类似的问题来考察对引用的了解. 



##### 内存释放

***

引用类型是在没有引用之后, 通过 v8 的 GC 自动回收, 值类型如果是处于闭包的情况下, 要等闭包没有引用才会被 GC 回收, 非闭包的情况下等待 v8 的新生代 (new space) 切换的时候回收.

这里讲到2年以上经验的 Node.js 就要开始注意内存问题了,v8与GC是要了解的,并且基础的内存释放一定有概念了, 并且要开始注意内存泄漏的问题了.

```
let arr = [];
while(true)
  arr.push(1);
```

区别

```
let arr = [];
while(true)
  arr.push();
```



##### ES6新特性

***

这里提到阮一峰的《ECMAScript 6 入门》是一本开源的 JavaScript 语言教程，全面介绍 ECMAScript 6 新引入的语法特性。

[![cover](http://es6.ruanyifeng.com/images/cover_thumbnail.jpg)](http://es6.ruanyifeng.com/images/cover-2nd.jpg)

本书覆盖 ES6 与上一个版本 ES5 的所有不同之处，对涉及的语法知识给予详细介绍，并给出大量简洁易懂的示例代码。

本书为中级难度，适合已经掌握 ES5 的读者，用来了解这门语言的最新发展；也可当作参考手册，查寻新增的语法点。