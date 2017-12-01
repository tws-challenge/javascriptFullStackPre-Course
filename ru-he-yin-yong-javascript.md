# 如何引用JavaScript

#### 本结学习目标

* 能够通过**内部引用**和**外部引用**两种方式在页面中加入JS

#### 本结内容

正如我们之前所了解到的，**HTML**控制页面的**内容**，**CSS**控制页面的**样式**，**JS**控制页面的**行为**。

HTML文档中的一个个标签表达的就是页面中的内容；若想要在HTML文档中加入样式，可以在某一个标签中加入`style`属性同时写上CSS样式即可，如`<p style="font-size:16px"><p/>`，或者将不同选择器的样式写在HTML文档`head`中的`<style>//some css attributes</style>`标签下，也可以在HTML文档中的`head`下加入`link`标签外链CSS文件，如：`<link rel="stylesheet" type="text/css" href="//path to css file">` 。那么我们如何在HTML文档中引入JS呢？

* 内部引用

通过HTML文档内的`script`标签加载JS代码。

示例：

```Javascript
<script type="text/javascript">
  document.write("dreamdu!");
</script>
```

通过此方式就可以在当前页面中引入`script`标签中的JS内容。

在HTML中嵌入JavaScript代码虽然没有问题，但一般认为最好的做法还是尽可能使用外部文件来包含JavaScript代码。不过，并不存在必须使用外部文件的硬性规定，但支持使用外部文件的人多会强调如下优点：

1. **可维护性**：遍及不同HTML页面的JavaScript会造成维护问题。但把所有JavaScript文件都放在一个文件夹中，维护起来就轻松多了。而且开发人员因此也能够在不触及HTML标签的情况下，集中精力编辑JavaScript代码。
2. **可缓存**：浏览器能够根据具体的设置缓存链接的所有外部JavaScript文件。也就是说，如果有两个页面都使用同一个文件，那么这个文件只需下载一次。因此，最终结果就是能够加快页面加载的速度。
3. **适应未来**：统一定义JavaScript代码，方便查看，同时使代码更安全，可以压缩，也可以加密某个JavaScript文件。

* 外部引用

同样是使用script标签，但是使用script标签的src属性，指向外部JS文件的路径。

示例：

```JavaScript
<script type="text/javascript" src="// path to js file" />
```



