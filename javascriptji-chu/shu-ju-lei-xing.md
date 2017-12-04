# 数据类型

#### 本节学习目标

* 了解JS中的七种数据类型

#### 本节内容

在上一节中我们提到每一种编程语言都有不同的数据类型，也就是我们的“盒子”里面存储的是字符串、还是数字等等。

JavaScript 是一种**弱类型**或者说**动态**语言。这意味着不用提前声明变量的类型，在程序运行过程中，类型会被自动确定。这也意味着可以使用同一个变量保存不同类型的数据：

```JavaScript
var foo = 42;    // foo is a Number now
var foo = "bar"; // foo is a String now
var foo = true;  // foo is a Boolean now
```

最新的JS标准定义了 7 种数据类型，它们分别是：

* 6种原始类型：
  * `Boolean`
  * `Null`

  * `Undefined`
  * `Number`
  * `String`
  * `Symbol(在ES6中新定义，本节暂不讲解)`
* 对象\(`Object`\)类型





