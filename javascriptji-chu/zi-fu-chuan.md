# 字符串

#### 本节学习目标

在JS中，所有的文本数据均被存储为字符串。JS中没有存储单个字符的数据类型，尽管只存储一个字符，也是长度为1的字符串。

字符串可以由双引号（`"`）或者单引号（`'`）表示，因此下面两种字符串的写法都是有效的：
```JavaScript
var firstName = 'Hello';
var lastName = "World";
```
在别的编程语言中，单引号和双引号会影响对字符串的解释方式不同，但是在JS中这两种语法没有什么区别。用双引号表示的字符串和用单引号表示的字符串完全相同。不过，以双引号开头的字符串也必须也双引号结尾，而以单引号开头的字符串必须以单引号结尾。例如：下面这种字符串表示法将会导致语法错误：
```JavaScript
var firstName = 'Hello World"; // 语法错误（左右引号必须匹配）
```

在字符串中，`+`号表示连接，意为将右边的字符串连接在左边的字符串后面，例如：
```JavaScript
var text = 'hello ';
text = text + 'world'; // 也可以用+=表示：text+='world';
console.log(text); // hello world
```
* 字符字面量
在JS中，String数据类型中包含一些特殊的字符字面量，也叫做转义字符，用于表示非打印字符，或者具有其他用途的字符。常用的字符字面量如下所示：
* `\n`: 换行
* `\t`: 制表符
* `\b`: 退格
* `\r`: 回车
* `\\`: 斜杠（\）
* `\'`: 单引号（'）
* `\"`: 双引号（"）
这些字面量可以出现在字符串中的任意位置，而且也将被作为一个字符来解析。如下面例子所示：
```JavaScript
var text = 'Hello \n World';  // 加入了一个换行符(\n)
```
将会打印出如下字符串：
```JavaScript
"Hello 
 World"
```
任何字符串的长度都可以通过访问其`length`属性取得，例如：
```JavaScript
var text = 'Hello ';
console.log(text.length); // 6 （注意Hello后面还有一个空格）
```

* 字符串的特点
在JS中，字符串是不可变的，也就是说，字符串一旦创建，它们的值就不能改变。要改变某个变量保存的字符串，首先要销毁原来的字符串，然后再用另一个包含新值的字符串填充该变量，例如：
```JavaScript
var text = 'tws ';
text = text + 'academy';
```
在这个例子中，变量`text`开始时包含字符串`'tws '`，而在第二行代码把`text`的值重新定义为`'tws '`与`'academy'`的组合，即：`'tws academy'`。在这个过程中，首先会创建一个能容纳11个字符的新字符串，然后在这个字符串中填充`'tws'`和`'academy'`，最后一步是销毁原来的字符串`'tws'`和字符串`'academy'`，因为这两个字符串已经没用了。

* 字符串常用方法
    * 从字符串中取出单个字符
    有两种方法：第一种方法是使用`charAt()`方法，示例：`'cat'.charAt(1); // 'a'`；另一种方法是把字符串当作一个类似数组的对象，其中的每个字符对应一个数值索引，示例：`'cat'[1]; // 'a'`。
    > 这里虽然使用括号访问字符串，但是不可以对其进行删除或添加，因为字符串是不可改变的。
    * `concat()`方法 - 字符串连接
    `concat()`方法将一个或多个字符串与原字符串连接合并，形成一个新的字符串并返回。`concat()`方法并不影响原字符串。示例：
    ```JavaScript
    var hello = "Hello, ";
    console.log(hello.concat("tws", " have a nice day.")); // Hello, tws have a nice day.
    console.log(hello); // Hello, 
    ```
    我们会发现，其实`concat()`方法的作用和`+`，`+=`的作用是一样的。但使用`+`，`+=`会获得更好的性能体验，因此，建议使用赋值操作符（`+`, `+=`）代替`concat()`方法。
    * `includes()`方法 - 字符串搜索
    `includes()`方法用于判断一个字符串是否包含在另一个字符串中，根据情况返回true或false，且该方法是区分大小写的。示例：
    ```JavaScript
    'Blue Whale'.includes('blue'); // false (大小写不同)
    'Blue Whale'.includes('Blue'); // true
    ```
    * `substr()`方法 - 提取子字符串
    `substr()`方法返回一个字符串中从指定位置开始到指定字符数的字符。该方法在调用的时候需要传入两个参数分别为：**开始提取字符的位置**和**提取的字符数长度**（可选）。示例：
    ```JavaScript
    var str = 'abcdefghij';
    str.substr(0,3); // 'abc'
    str.substr(3,3); // 'def'
    str.substr(3); // 'defghij'
    ```
    * `substring()`方法 - 提取子字符串
    `substring()`方法返回一个字符串在开始索引位置到结束索引位置之间的一个子集, 或从开始索引直到字符串的末尾的一个子集。该方法也接受两个参数，第一个参数是**开始提取字符的位置**，但与`substr()`方法不同的是，`substring()`方法的第二个参数是**结束提取字符的位置**（可选）。示例：
    ```JavaScript
    var str = 'abcdefghij';
    str.substring(0,3); // 'abc'
    str.substring(3,3); // ''  (因为从3到3，中间没有字符)
    str.substring(3); // 'defghij'
    str.substring(2,3); // 'c'
    ```