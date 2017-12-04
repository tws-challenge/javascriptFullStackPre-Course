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

##### 原始值

在JS中除 Object 以外的所有类型都是不可变的（值本身无法被改变），我们称这些类型的值为“原始值”。

* 布尔类型：`Boolean`

布尔表示一个逻辑实体，意为真、假，可以有两个值：`true`和`false`。

* Null类型：`null`

Null 类型只有一个值：`null`，表示空值，表示没有被呈现。

* Undefined类型：`Undefined`

一个没有被赋值的变量会有个默认值`undefined`。

* 数字类型：`Number`

在JS里，数字类型能够代表的范围是**\(-\(2的63次方-1\) ~ \(2的63次方-1\)**。除了具体的数值，在JS中还有一些带符号的值：`+Infinity`，`-Infinity`和`NaN`\(非数值，Not-a-Number\)，分别代表正无穷、负无穷和非数值。例如：

```JavaScript
19 / +0; // Infinity
19 / -0; // -Infinity
```

* 字符串类型：`String`

JavaScript的字符串类型用于表示文本数据。在字符串中的每个元素占据了字符串的位置。第一个元素的索引为0，下一个是索引1，依此类推。字符串的长度是它的元素的数量。

JavaScript 字符串是不可更改的。这意味着字符串一旦被创建，就不能被修改。但是，可以基于对原始字符串的操作来创建新的字符串。例如：

* 获取一个字符串的子串可通过选择个别字母或者使用`String.substr()`。
* 两个字符串的连接使用连接操作符 \(`+`\) 或者`String.concat()`。
  .



