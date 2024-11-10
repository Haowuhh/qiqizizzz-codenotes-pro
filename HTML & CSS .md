# 0、资料

[前端原生Html免费模板网站总结(带网址)](https://blog.csdn.net/m0_49714202/article/details/125457301)

[HTML教程](https://www.runoob.com/html/html-tutorial.html)

[HTML 参考手册- (HTML5 标准)](https://www.runoob.com/tags/html-reference.html)

 [CSS教程](https://www.runoob.com/css/css-tutorial.html)

[CSS 参考手册](https://www.runoob.com/cssref/css-reference.html)



# 一、基础

## 1.网页

HTML:超文本标记语言，用来制作网页的一门语言。

网页是图片、链接、文字、声音、视频等元素组成，其实就是一个html文件(后缀名为html)。

## 2.Web标准

主要包括结构、表现和行为三个方面。

| 标准 | 说明                                                         |
| ---- | ------------------------------------------------------------ |
| 结构 | 结构用于对网页元素进行整理和分类，现阶段主要学的是HTML。     |
| 表现 | 表现用于设置网页元素的版式、颜色、大小等外观样式，主要指的是CSS |
| 行为 | 行为是指网页模型的定义及**交互**的编写，现阶段主要学的是JavaScript |

## 3.基础语法

### 3.1 HTML 标题

HTML 标题（Heading）是通过`<h1> `- `<h6> `标签来定义的。

```html
<h1>这是一个标题</h1>
<h2>这是一个标题</h2>
<h3>这是一个标题</h3>
```

 `<br>`元素可用于分割内容。区分一下： `<br>`, `<br/> `以及 `<br />`（带有空格）
`<br>` 是 HTML 写法。是 XHTML1.1 的写法, 也是 XML 写法。`<br/>` 是 XHTML 为兼容 HTML 的写法,也是 XML 写法。HTML5 因为兼容 XHTML，所以三种写法都可以使用。
早期发布的 HTML 规范当中，`<br>` 与` <img>` 等元素是不用封闭自身的，但是这种元素造成了 HTML 规范的不严谨，于是在之后发布的 XHTML 语言中，参考了更为严谨的 XML 规范，在这些不用自身封闭的元素后加 `/`来表示自行封闭，在逻辑上来讲等同于`<br>`....`</br>`（但是没有 `</br>` 这种写法），这样一来保证了较少的代码量，二来保证了规范的严谨



可以将注释插入 HTML 代码中，这样可以提高其可读性，使代码更易被人理解。浏览器会忽略注释，也不会显示它们。

注释写法如下:

```html
<!-- 这是一个注释 -->
```

**注释:** 开始括号之后（左边的括号）需要紧跟一个叹号 **!** (英文标点符号)，结束括号之前（右边的括号）不需要，合理地使用注释可以对未来的代码编辑工作产生帮助。



> **标题大小与字体大小的关系:**

1到6号标题与1到6号字体逆序对应，比如1号字体对应6号标题，2号字体对应5号标题。

```html
<h1>这是1号标题</h1>
<font size="6">这是6号字体文本</font>

<h2>这是2号标题</h2>
<font size="5">这是5号字体文本</font>

<h3>这是3号标题</h3>
<font size="4">这是4号字体文本</font>

<h4>这是4号标题</h4>
<font size="3">这是3号字体文本</font>

<h5>这是5号标题</h5>
<font size="2">这是2号字体文本</font>

<h6>这是6号标题</h6>
<font size="1">这是1号字体文本</font>
```

### 3.2 HTML 段落

HTML 段落是通过标签 `<p>` 来定义的。

```html
<p>这是一个段落。</p>
<p>这是另外一个段落。</p>
```

**注意**：浏览器会自动地在段落的前后添加空行。（`</p>` 是块级元素）



### 3.3 HTML 链接

HTML 链接是通过标签 `<a>` 来定义的。

```html
<a href="https://www.runoob.com">这是一个链接</a>
```

- `<a>` 标签：定义了一个超链接（anchor）。它是 HTML 中用来创建可点击链接的主要标签。
- `href` 属性：指定目标 URL，当点击链接时，浏览器将导航到此 URL。



HTML使用标签 **`<a>`** 来设置超文本链接。

超链接可以是一个字，一个词，或者一组词，也可以是一幅图像，您可以点击这些内容来跳转到新的文档或者当前文档中的某个部分。

当您把鼠标指针移动到网页中的某个链接上时，箭头会变为一只小手。

在标签 `<a> `中使用了 **`href`** 属性来描述链接的地址。

默认情况下，链接将以以下形式出现在浏览器中：

- 一个未访问过的链接显示为蓝色字体并带有下划线。
- 访问过的链接显示为紫色并带有下划线。
- 点击链接时，链接显示为红色并带有下划线。

> 注意：如果为这些超链接设置了 CSS 样式，展示样式会根据 CSS 的设定而显示。



#### HTML 链接属性

href 属性描述了链接的目标。

**1、href：定义链接目标。**

这是超链接最重要的属性，用来指定链接的目的地，可以是另一个网页、文件、邮件、电话号码或 JavaScript。

```html
<a href="https://www.example.com">访问 Example</a>
```

**2、target：定义链接的打开方式。**

- `_blank`: 在新窗口或新标签页中打开链接。
- `_self`: 在当前窗口或标签页中打开链接（默认）。
- `_parent`: 在父框架中打开链接。
- `_top`: 在整个窗口中打开链接，取消任何框架。

```html
<a href="https://www.example.com" target="_blank" rel="noopener">新窗口打开 Example</a>
```

 `_self`的话是指在本身这个网页窗口来打开新的网页链接。
`_parent`主要是针对于框架网页中的跳转。
如果你一个页面由两三个框架组成，你要想整个页面跳转到其它网页链接，目标就需要用`_parent`了。如果不用这个，就只会使得那一小块框架区域里的网页跳转。 
而其它的地方则不变`_top`与`_self`差不很大。但是如果你用了`<!--#include file="..."-->`时，就会知道两者的差别了。因为如果你的超链接是做在 `<!--#include file="..."-->`上时。如果用`_self` 点击后的超链接就会在`<!--#include file="..."-->` 这个页面上打开，而页面其它部分不会改变。如果用_top 则会整个窗口一起跳转到新的链接网页。

**3、rel：定义链接与目标页面的关系。**

**nofollow**: 表示搜索引擎不应跟踪该链接，常用于外部链接。

**noopener** 和 **noreferrer**: 防止在新标签中打开链接时的安全问题，尤其是使用 **target="_blank"** 时。

- `noopener`: 防止新的浏览上下文（页面）访问`window.opener`属性和`open`方法。
- `noreferrer`: 不发送referer header（即不告诉目标网站你从哪里来的）。
- `noopener noreferrer`: 同时使用`noopener`和`noreferrer`。例子: `<a href="https://www.example.com" rel="noopener noreferrer">安全链接</a>`

> noopener noreferrer的意思是不会打开其他的网站，因为恶意病毒可能会修改你的浏览器空白页地址。

```html
<a href="https://www.example.com" target="_blank" rel="noopener noreferrer">安全链接</a>
```

**4、download：提示浏览器下载链接目标而不是导航到该目标。**

如果指定了文件名，浏览器会提示下载并保存为指定文件名。

例如：

```html
<a href="file.pdf" download="example.pdf">下载文件</a>
```

**5、title：定义链接的额外信息，当鼠标悬停在链接上时显示的工具提示。**

```html
<a href="https://www.example.com" title="访问 Example 网站">访问 Example</a>
```

**6、id：用于链接锚点，通常在同一页面中跳转到某个特定位置。**

```html
<!-- 链接到页面中的某个部分 -->
<a href="#section1">跳转到第1部分</a>
<div id="section1">这是第1部分</div>
```

**7、hreflang: 指定链接的目标URL的语言**

```html
<a href="https://www.example.com/es" hreflang="es">访问西班牙语网站</a>
```

**8、type: 指定链接资源的MIME类型**

```html
<a href="style.css" type="text/css">样式表</a>
```

**9、class: 用于指定元素的类名（CSS中定义）**

```html
<a href="https://www.example.com" class="external-link">外部链接</a>
```

**10、style: 直接在元素上定义CSS样式**

```html
<a href="https://www.example.com" style="color: red;">红色链接</a>
```

#### 空链接

以下是常见的几种设置空链接的方法，以及它们之间的区别：

| 方法                        | 作用                       | 是否会跳转 | 场景适用性                   |
| :-------------------------- | :------------------------- | :--------- | :--------------------------- |
| `href="#"`                  | 导航到页面顶部             | 是         | 占位符，捕获点击事件         |
| `href="javascript:void(0)"` | 阻止默认行为，不刷新页面   | 否         | 阻止跳转，配合 JS 使用       |
| `href=""`                   | 刷新当前页面               | 是         | 需要页面刷新时               |
| `href="about:blank"`        | 打开空白页面               | 是         | 新窗口打开空白页面           |
| `role="button"`             | 链接表现为按钮，无默认行为 | 否         | 配合 JS 实现按钮功能，无跳转 |



#### 关于创建电子邮件链接时如何发送邮件内容

在进行邮件内容发送时，需要使用关键字：**mailto**

示例如下：

```html
<a href="mailto:zhangrr601@163.com?subject=这是邮件的主题&body=这是邮件的内容" rel="nofollow">发送邮件</a>
```

这样会调启系统默认的邮件程序发送给 `zhangrr601@163.com`并且收件人那里已经填上了我邮箱的地址。

关于创建电子邮件链接时如何进行抄送，密送.

> **抄送：**
>
> 英文名称：Carbon Copy，又简称为 CC。在网络术语中，抄送就是将邮件同时发送给收信人以外的人，用户所写的邮件抄送一份给别人，对方可以看见该用户的 E-mail。同收件人地址栏一样，不可以超过 1024 个字符。一般来说，使用"抄送"服务时，多人抄送的电子邮件地址使用 **;** 分隔。



> **密件抄送：**
>
> 英文名称：Blind Carbon Copy ，又称“盲抄送”，和抄送的唯一区别就是它能够让各个收件人**无法查看**到这封邮件同时还发送给了哪些人。密件抄送是个很实用的功能，假如一次向成百上千位收件人发送邮件，最好采用密件抄送方式，这样一来可以保护各个收件人的地址不被其他人轻易获得，二来可以使收件人节省下收取大量抄送的 E-mail 地址的时间。

在进行抄送时，需要使用关键字：**cc**

在进行密送时，需要使用关键字：**bcc**

示例如下：

```html
<a href="mailto:zhangrr601@163.com?cc=someone@163.com&bcc=somebody@163.com" rel="nofollow">发送邮件</a>
```

参数说明：

| 参数                     | 描述             |
| :----------------------- | :--------------- |
| `mailto:*name@email.com` | 邮件接收地址     |
| `cc=*name@email.com`     | 抄送地址         |
| `bcc=*name@email.com`    | 密件抄送地址     |
| `subject=*subject text`  | 邮件主题         |
| `body=*body text`        | 邮件内容         |
| `?`                      | 第一个参数分隔符 |
| `&`                      | 其他参数分隔符   |

注：多个邮件地址用 **;** 隔开，空格用 **%20** 代替。



### 3.4 HTML 图像

HTML 图像是通过标签 `<img>` 来定义的.

```html
<img src="/images/logo.png" width="258" height="39" />
```

**注意**： 图像的名称和尺寸是以属性的形式提供的。



1、***.html** 文件跟 **1.png** 文件(c盘)在不同目录下：

```html
 <img src="file:///C:/Users/ASUS/Pictures/1.png" width="260" height="260"/>
```

2、***.html** 文件跟 **1.jpg** 图片在相同目录下：

```html
<img src="1.jpg" width="300" height="120"/>
```

3、***.html** 文件跟 **1.jpg** 图片在不同目录下：

```html
a、图片 1.jpg 在 image 文件夹中，1.html 跟 image 在同一目录下：
<img src="image/1.jpg/"width="300" height="120"/>
```

```html
b、图片 1.jpg 在 image 文件夹中，1.html 在 connage 文件夹中，image 跟 connage 在同一目录下：
<img src="../image/1.jpg/"width="300" height="120"/>
```

4、如果图片来源于网络，那么写绝对路径：

```html
<img src="http://static.runoob.com/images/runoob-logo.png" width="300" height="120"/>
```



**html 相对路径的写法：**

-  **./**：代表文件所在的目录（可以省略不写）如果写成image/background就相当于是在html文件下找image文件夹，当然是找不到的
-  **../**：代表文件所在的父级目录
-  **../../**：代表文件所在的父级目录的父级目录
-  **/**：代表文件所在的根目录

> 同一个目录：index2.html 或./index2.html；
> 在子目录：xxx/index2.html；
> 在孙子目录：xxx/xxx/index2.html；
> 在父目录：../index2.html；
> 在爷爷目录：../../index2.html；



# 二、HTML

## 0.HTML速查表

### HTML 基本文档

```html
<!DOCTYPE html>
<html>
<head>
<title>文档标题</title>
</head>
<body>
可见文本...
</body>
</html>
```

### 基本标签

```html
<h1>最大的标题</h1>
<h2> . . . </h2>
<h3> . . . </h3>
<h4> . . . </h4>
<h5> . . . </h5>
<h6>最小的标题</h6>
 
<p>这是一个段落。</p>
<br> （换行）
<hr> （水平线）
<!-- 这是注释 -->
```

### 文本格式化

```html
<b>粗体文本</b>
<code>计算机代码</code>
<em>强调文本</em>
<i>斜体文本</i>
<kbd>键盘输入</kbd> 
<pre>预格式化文本</pre>
<small>更小的文本</small>
<strong>重要的文本</strong>
 
<abbr> （缩写）
<address> （联系信息）
<bdo> （文字方向）
<blockquote> （从另一个源引用的部分）
<cite> （工作的名称）
<del> （删除的文本）
<ins> （插入的文本）
<sub> （下标文本）
<sup> （上标文本）
```

### 链接（Links）

```html
普通的链接：<a href="http://www.example.com/">链接文本</a>
图像链接： <a href="http://www.example.com/"><img src="URL" alt="替换文本"></a>
邮件链接： <a href="mailto:webmaster@example.com">发送e-mail</a>
书签：
<a id="tips">提示部分</a>
<a href="#tips">跳到提示部分</a>
```

### 图片（images）

```html
<img src="URL" alt="替换文本" height="42" width="42">
```

### 样式/区块

```html
<style type="text/css">
h1 {color:red;}
p {color:blue;}
</style>
<div>文档中的块级元素</div>
<span>文档中的内联元素</span>
```

### 无序列表

```html
<ul>
    <li>项目</li>
    <li>项目</li>
</ul>
```

### 有序列表

```html
<ol>
    <li>第一项</li>
    <li>第二项</li>
</ol>
```

### 定义列表

```html
<dl>
  <dt>项目 1</dt>
    <dd>描述项目 1</dd>
  <dt>项目 2</dt>
    <dd>描述项目 2</dd>
</dl>
```

### 表格（Tables）

```html
<table border="1">
  <tr>
    <th>表格标题</th>
    <th>表格标题</th>
  </tr>
  <tr>
    <td>表格数据</td>
    <td>表格数据</td>
  </tr>
</table>
```

### 框架（Iframe）

```html
<iframe src="demo_iframe.htm"></iframe>
```

### 表单（Forms）

```html
<form action="demo_form.php" method="post/get">
<input type="text" name="email" size="40" maxlength="50">
<input type="password">
<input type="checkbox" checked="checked">
<input type="radio" checked="checked">
<input type="submit" value="Send">
<input type="reset">
<input type="hidden">
<select>
<option>苹果</option>
<option selected="selected">香蕉</option>
<option>樱桃</option>
</select>
<textarea name="comment" rows="60" cols="20"></textarea>
 
</form>
```

### 实体（Entities）

```html
&lt; 等同于 <
&gt; 等同于 >
&#169; 等同于 ©
```



## 1.HTML 元素

| 开始标签 *               | 元素内容     | 结束标签 * |
| :----------------------- | :----------- | :--------- |
| `<p>`                    | 这是一个段落 | `</p>`     |
| `<a href="default.htm">` | 这是一个链接 | `</a>`     |
| `<br>`                   | 换行         |            |

*****开始标签常被称为**起始标签（opening tag）**，结束标签常称为**闭合标签（closing tag）**。

> HTML 元素语法

- HTML 元素以**开始标签**起始
- HTML 元素以**结束标签**终止
- **元素的内容**是开始标签与结束标签之间的内容
- 某些 HTML 元素具有**空内容（empty content）**
- 空元素**在开始标签中进行关闭**（以开始标签的结束而结束）
- 大多数 HTML 元素可拥有**属性**



**注意**：不要忘记结束标签,忘记使用结束标签会产生不可预料的结果或错误。

没有内容的 HTML 元素被称为空元素。空元素是在开始标签中关闭的。

**最好使用小写标签！**



## 2.HTML属性

属性是 HTML 元素提供的附加信息。

属性总是以 **name="value"** 的形式写在标签内，**name** 是属性的名称，**value** 是属性的值。

- HTML 元素可以设置**属性**
- 属性可以在元素中添加**附加信息**
- 属性一般描述于**开始标签**
- 属性总是以名称/值对的形式出现，**比如：name="value"**。



**实例：**

HTML 链接由 `<a>` 标签定义。链接的地址在 **href 属性**中指定：

```html
<a href="http://www.runoob.com">这是一个链接</a>
```

### HTML 属性常用引用属性值

属性值应该始终被包括在引号内。

双引号是最常用的，不过使用单引号也没有问题。

在某些个别的情况下，比如属性值本身就含有双引号，那么您必须使用单引号，例如：

```html
name='John "ShotGun" Nelson'
```



## 3.HTML文本格式化

HTML 使用标签 `<b>`("bold") 与 `<i>`("italic") 对输出的文本进行格式, 如：**粗体** or *斜体*

这些HTML标签被称为格式化标签（请查看完整标签参考手册）。

```html
通常标签 <strong> 替换加粗标签 <b> 来使用, <em> 替换 <i>标签使用。
然而，这些标签的含义是不同的：
<b> 与<i> 定义粗体或斜体文本。
<strong> 或者 <em>意味着你要呈现的文本是重要的，所以要突出显示。现今所有主要浏览器都能渲染各种效果的字体。不过，未来浏览器可能会支持更好的渲染效果。
```



## 4.HTML头部

**1. HTML` <head> `元素**

`<head> `元素包含了所有的头部标签元素。在 `<head>`元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。

可以添加在头部区域的元素标签为:` <title>`,` <style>`, `<meta>`, `<link>`, `<script>`, `<noscript>` 和 `<base>`。

**head 标签和 header 标签的不同**

head 标签用于定义文档头部，它是所有头部元素的容器。`<head>` 中的元素可以引用脚本、指示浏览器在哪里找到样式表、提供元信息等等。

如：

```html
<html>
  <head>
     <title>文档标题</title>
  </head>
</html>
```

header 标签用于定义文档的页眉（介绍信息）。

如：

```html
<html>
  <body>
    <header>
        <p>段落</p>
        <h1>一级标题</h1>
    </header>
  </body>
</html>
```

注意千万不要弄混。

**2. HTML `<title>` 元素**

`<title> `标签定义了不同文档的标题。

`<title> `在 HTML/XHTML 文档中是必需的。

`<title>` 元素:

- 定义了浏览器工具栏的标题
- 当网页添加到收藏夹时，显示在收藏夹中的标题
- 显示在搜索引擎结果页面的标题

**2. HTML `<base>` 元素**

`<base>` 标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接:

```html
<head> <base href="http://www.runoob.com/images/" target="_blank"> </head>
```

**3. HTML `<link>` 元素**

`<link>` 标签定义了文档与外部资源之间的关系。

`<link>` 标签通常用于链接到样式表:

```html
<head> <link rel="stylesheet" type="text/css" href="mystyle.css"> </head>
```

**4. HTML `<style>` 元素**

`<style>` 标签定义了HTML文档的样式文件引用地址.

在`<style>` 元素中你也可以直接添加样式来渲染 HTML 文档:

```html
<head>
<style type="text/css">
body {
    background-color:yellow;
}
p {
    color:blue
}
</style>
</head>
```

**5. HTML `<meta>` 元素**

meta标签描述了一些基本的元数据。

```html
<meta> 标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。
```

META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。

元数据可以使用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他Web服务。

```html
<meta> 一般放置于 <head> 区域
```

**`<meta>` 标签- 使用实例**

为搜索引擎定义关键词:

```html
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">
```

为网页定义描述内容:

```html
<meta name="description" content="免费 Web & 编程 教程">
```

定义网页作者:

```html
<meta name="author" content="Runoob">
```

每30秒钟刷新当前页面:

```html
<meta http-equiv="refresh" content="30">
```

**6. HTML `<script>` 元素**

`<script>`标签用于加载脚本文件，如： JavaScript。

## 5.HTML CSS

### 如何使用CSS

CSS 是在 HTML 4 开始使用的,是为了更好的渲染HTML元素而引入的.

CSS 可以通过以下方式添加到HTML中:

- 内联样式- 在HTML元素中使用"style" **属性**
- 内部样式表 -在HTML文档头部 `<head>` 区域使用`<style>` **元素** 来包含CSS
- 外部引用 - 使用外部 CSS **文件**

最好的方式是通过外部引用CSS文件.

### 内联样式

当特殊的样式需要应用到**个别元素**时，就可以使用内联样式。 使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性。以下实例显示出如何改变段落的颜色和左外边距。

```html
<p style="color:blue;margin-left:20px;">这是一个段落。</p>
```

> 1.HTML样式实例 - **背景颜色**

背景色属性（background-color）定义一个元素的背景颜色：

```html
<body style="background-color:yellow;">
<h2 style="background-color:red;">这是一个标题</h2> 
<p style="background-color:green;">这是一个段落。</p> </body>
```

> 2.HTML 样式实例 - **字体, 字体颜色 ，字体大小**

我们可以使用font-family（字体），color（颜色），和font-size（字体大小）属性来定义字体的样式:

```html
<h1 style="font-family:verdana;">一个标题</h1> <p style="font-family:arial;color:red;font-size:20px;">一个段落。</p>
```

> 3.HTML 样式实例 - **文本对齐方式**

使用 text-align（文字对齐）属性指定文本的水平与垂直对齐方式：

```html
<h1 style="text-align:center;">居中对齐的标题</h1> <p>这是一个段落。</p>
```

### CSS 引入外部标签`link`

第一种方式：使用最多，稳定

```html
<link rel="stylesheet" href="标签路径">
```

第二种方式：

```html
<style>
@import url("标签路径")
</style>
```

**扩展知识点:** link 和 import之间的区别?

**差别 1：**

本质的差别：**link** 属于 XHTML 标签，而 **@import** 完全是 CSS 提供的一种方式。

**差别 2：**

**加载顺序的差别：** 当一个页面被加载的时候（就是被浏览者浏览的时候) ，link 引用的 CSS 会同时被加载，而 **@import** 引用的 CSS 会等到页面全部被下载完再被加载。所以有时候浏览 **@import** 加载 CSS 的页面时开始会没有样式(就是闪烁)，网速慢的时候还挺明显。

**差别 3：**

**兼容性的差别:** **@import** 是 CSS2.1 提出的，所以老的浏览器不支持，**@import** 只有在 IE5 以上的才能识别，而 **link** 标签无此问题。

**差别 4：**

使用 dom(document object model文档对象模型 )控制样式时的差别：当使用 javascript 控制 dom 去改变样式的时候，只能使用 link 标签，因为**@import** 不是 dom 可以控制的。



## 6.HTML图像

**1. HTML 图像- 图像标签（ `<img>`）、`alt`属性和源属性（`Src`）**

在 HTML 中，图像由`<img>` 标签定义。

`<img>` 是空标签，意思是说，它只包含属性，并且没有闭合标签。

要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。

**定义图像的语法是：**

```html
<img src="url" alt="some_text">
```

URL 指存储图像的位置。如果名为 "pulpit.jpg" 的图像位于 `www.runoob.com` 的 images 目录中，那么其 URL 为 `http://www.runoob.com/images/pulpit.jpg`。

alt 属性用来为图像定义一串预备的可替换的文本。

替换文本属性的值是用户定义的。

在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。此时，浏览器将显示这个替代性的文本而不是图像。为页面上的图像都加上替换文本属性是个好习惯，这样有助于更好的显示信息，并且对于那些使用纯文本浏览器的人来说是非常有用的。

**2. HTML 图像- 设置图像的高度与宽度**

height（高度） 与 width（宽度）属性用于设置图像的高度与宽度。

属性值默认单位为像素:

```html
<img src="pulpit.jpg" alt="Pulpit rock" width="304" height="228">
```

**提示:** 指定图像的高度和宽度是一个很好的习惯。如果图像指定了高度宽度，页面加载时就会保留指定的尺寸。如果没有指定图片的大小，加载页面时有可能会破坏HTML页面的整体布局。

**3.HTML 图像-网站图标**

[如何在浏览器标题前端显示一张图片](https://blog.csdn.net/ggq53219/article/details/139016760?sharetype=blogdetail&shareId=139016760&sharerefer=APP&sharesource=2301_81250551&sharefrom=link)

使用 Favicon（网站图标）：Favicon 是一个小的图标，通常显示在浏览器标签页的左上角或地址栏旁边。你可以使用 .ico 或 .png 格式的图片作为 Favicon。在 HTML 中，你可以通过 `<link>` 标签的 rel="icon" 属性来引用它。

```html
<link rel="icon" href="image/cs.ico" type="image/x-icon">
```

或者，对于 PNG 格式：

```html
<link rel="icon" type="image/png" size="16x16" href="image/cs.png">
```

## 7.HTML表格

HTML 表格由 **`<table>`** 标签来定义。

HTML 表格是一种用于展示结构化数据的标记语言元素。

每个表格均有若干行（由 `<tr>` 标签定义），每行被分割为若干单元格（由 `<td>` 标签定义），表格可以包含标题行（**`<th>`**）用于定义列的标题。

- **tr**：tr 是 table row 的缩写，表示表格的一行。
- **td**：td 是 table data 的缩写，表示表格的数据单元格。
- **th**：th 是 table header的缩写，表示表格的表头单元格。

数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。

```html
<table>
  <thead>
    <tr>
      <th>列标题1</th>
      <th>列标题2</th>
      <th>列标题3</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>行1，列1</td>
      <td>行1，列2</td>
      <td>行1，列3</td>
    </tr>
    <tr>
      <td>行2，列1</td>
      <td>行2，列2</td>
      <td>行2，列3</td>
    </tr>
  </tbody>
</table>
```

`<table>` 元素表示整个表格，它包含两个主要部分：`<thead>` 和 `<tbody>`。

- `<thead >` 用于定义表格的标题部分: 在 `<thead > `中，使用 `<th>` 元素定义列的标题，以上实例中列标题分别为"列标题1"，"列标题2"和"列标题3"。
- `<tbody >` 用于定义表格的主体部分: 在 `<tbody> `中，使用 `<tr>` 元素定义行，并在每行中使用 `<td>` 元素定义单元格数据，以上实例中有两行数据，每行包含三个单元格。

通过使用 `<th>` 元素定义列标题，可以使其在表格中以粗体显示，与普通单元格区分开来。

HTML 表格还可以具有其他部分，如 `<tfoot>` （表格页脚）和 `<caption>` （表格标题），`<tfoot> `可用于在表格的底部定义摘要、统计信息等内容。 `<caption>` 可用于为整个表格定义标题。

HTML 表格还支持合并单元格和跨行/跨列的操作，以及其他样式和属性的应用，以满足各种需求。

我们也可以使用 CSS 来进一步自定义表格的样式和外观。

### HTML 表格标签

| 标签         | 描述                 |
| :----------- | :------------------- |
| `<table>`    | 定义表格             |
| `<th>`       | 定义表格的表头       |
| `<tr>`       | 定义表格的行         |
| `<td>`       | 定义表格单元         |
| `<caption>`  | 定义表格标题         |
| `<colgroup>` | 定义表格列的组       |
| `<col>`      | 定义用于表格列的属性 |
| `<thead>`    | 定义表格的页眉       |
| `<tbody>>`   | 定义表格的主体       |
| `<tfoot>`    | 定义表格的页脚       |

## 8.HTML列表

HTML 支持有序、无序和定义列表:

### HTML无序列表

无序列表是一个项目的列表，此列项目使用粗体圆点（典型的小黑圆圈）进行标记。

无序列表使用 `<ul>`标签

```html
<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>
```

浏览器显示如下：

- Coffee
- Milk

### HTML 有序列表

同样，有序列表也是一列项目，列表项目使用数字进行标记。 有序列表始于 `<ol>` 标签。每个列表项始于 `<li> `标签。

列表项使用数字来标记。

```html
<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>
```

浏览器中显示如下：

1. Coffee
2. Milk

### HTML 自定义列表

自定义列表不仅仅是一列项目，而是项目及其注释的组合。

自定义列表以 `<dl> `标签开始。每个自定义列表项以 `<dt>` 开始。每个自定义列表项的定义以 `<dd>` 开始。

```html
<dl>
<dt>Coffee</dt>
<dd>- black hot drink</dd>
<dt>Milk</dt>
<dd>- white cold drink</dd>
</dl>
```

浏览器显示如下：

- Coffee

  - black hot drink

- Milk

  - white cold drink

> **注意事项 - 有用提示**

**提示:** 列表项内部可以使用段落、换行符、图片、链接以及其他列表等等。

## 9.HTML区块

### HTML `<div>` 和`<span>`

HTML 可以通过 `<div>` 和 `<span>`将元素组合起来。

###　HTML 区块元素

大多数 HTML 元素被定义为**块级元素**或**内联元素**。

块级元素在浏览器显示时，通常会以新行来开始（和结束）。

实例: `<h1>`, `<p>`, `<ul>`, `<table>`

### HTML 内联元素

内联元素在显示时通常不会以新行开始。

实例: `<b>`, `<td>`, `<a>`, `<img>`

### HTML`<div>` 元素

HTML `<div>`元素是块级元素，它可用于组合其他 HTML 元素的容器。

`<div>` 元素没有特定的含义。除此之外，由于它属于块级元素，浏览器会在其前后显示折行。

如果与 CSS 一同使用，`<div>` 元素可用于对大的内容块设置样式属性。

`<div>` 元素的另一个常见的用途是文档布局。它取代了使用表格定义布局的老式方法。使用 `<table>` 元素进行文档布局不是表格的正确用法。`<table>` 元素的作用是显示表格化的数据。

###　HTML`<span>` 元素

HTML `<span>` 元素是内联元素，可用作文本的容器。

`<span>` 元素也没有特定的含义。

当与 CSS 一同使用时，`<span>` 元素可用于为部分文本设置样式属性。

## 10.HTML布局

网页布局对改善网站的外观非常重要。

请慎重设计您的网页布局。

### 使用`<div>`元素

div 元素是用于分组 HTML 元素的块级元素。

下面的例子使用五个 div 元素来创建多列布局：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>
 
<div id="container" style="width:500px">
 
<div id="header" style="background-color:#FFA500;">
<h1 style="margin-bottom:0;">主要的网页标题</h1></div>
 
<div id="menu" style="background-color:#FFD700;height:200px;width:100px;float:left;">
<b>菜单</b><br>
HTML<br>
CSS<br>
JavaScript</div>
 
<div id="content" style="background-color:#EEEEEE;height:200px;width:400px;float:left;">
内容在这里</div>
 
<div id="footer" style="background-color:#FFA500;clear:both;text-align:center;">
版权 © runoob.com</div>
 
</div>
 
</body>
</html>
```

### 使用`<table>`元素

使用 HTML `<table>` 标签是创建布局的一种简单的方式。

大多数站点可以使用 `<div>` 或者 `<table>` 元素来创建多列。CSS 用于对元素进行定位，或者为页面创建背景以及色彩丰富的外观。

**即使可以使用 HTML 表格来创建漂亮的布局，但设计表格的目的是呈现表格化数据 - 表格不是布局工具！**

下面的例子使用三行两列的表格 - 第一和最后一行使用 colspan 属性来横跨两列：

```html
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>
 
<table width="500" border="0">
<tr>
<td colspan="2" style="background-color:#FFA500;">
<h1>主要的网页标题</h1>
</td>
</tr>
 
<tr>
<td style="background-color:#FFD700;width:100px;">
<b>菜单</b><br>
HTML<br>
CSS<br>
JavaScript
</td>
<td style="background-color:#eeeeee;height:200px;width:400px;">
内容在这里</td>
</tr>
 
<tr>
<td colspan="2" style="background-color:#FFA500;text-align:center;">
版权 © runoob.com</td>
</tr>
</table>
 
</body>
</html>
```

> HTML 布局 - 有用的提示

**Tip:** 使用 CSS 最大的好处是，如果把 CSS 代码存放到外部样式表中，那么站点会更易于维护。通过编辑单一的文件，就可以改变所有页面的布局。

**Tip:** 由于创建高级的布局非常耗时，使用模板是一个快速的选项。通过搜索引擎可以找到很多免费的网站模板（您可以使用这些预先构建好的网站布局，并优化它们）

## 11.HTML表单

HTML 表单用于收集用户的输入信息。

HTML 表单表示文档中的一个区域，此区域包含交互控件，将用户收集到的信息发送到 Web 服务器。

HTML 表单通常包含各种输入字段、复选框、单选按钮、下拉列表等元素。

以下是一个简单的HTML表单的例子：

- `<form>` 元素用于创建表单，`action` 属性定义了表单数据提交的目标 URL，`method` 属性定义了提交数据的 HTTP 方法（这里使用的是 "post"）。
- `<label>` 元素用于为表单元素添加标签，提高可访问性。
- `<input>` 元素是最常用的表单元素之一，它可以创建文本输入框、密码框、单选按钮、复选框等。`type` 属性定义了输入框的类型，`id` 属性用于关联 `<label>` 元素，`name` 属性用于标识表单字段。
- `<select>` 元素用于创建下拉列表，而 `<option>` 元素用于定义下拉列表中的选项。

```html
<form action="/" method="post">
    <!-- 文本输入框 -->
    <label for="name">用户名:</label>
    <input type="text" id="name" name="name" required>

    <br>

    <!-- 密码输入框 -->
    <label for="password">密码:</label>
    <input type="password" id="password" name="password" required>

    <br>

    <!-- 单选按钮 -->
    <label>性别:</label>
    <input type="radio" id="male" name="gender" value="male" checked>
    <label for="male">男</label>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">女</label>

    <br>

    <!-- 复选框 -->
    <input type="checkbox" id="subscribe" name="subscribe" checked>
    <label for="subscribe">订阅推送信息</label>

    <br>

    <!-- 下拉列表 -->
    <label for="country">国家:</label>
    <select id="country" name="country">
        <option value="cn">CN</option>
        <option value="usa">USA</option>
        <option value="uk">UK</option>
    </select>

    <br>

    <!-- 提交按钮 -->
    <input type="submit" value="提交">
</form>
```

表单是一个包含表单元素的区域。

表单元素是允许用户在表单中输入内容，比如：文本域（textarea）、下拉列表（select）、单选框（radio-buttons）、复选框（checkbox） 等等。

我们可以使用 `<form>`标签来创建表单:

```html
<form>
.
input 元素
.
</form>
```



### HTML 表单 - 输入元素

多数情况下被用到的表单标签是输入标签 `<input>`。

输入类型是由 **type** 属性定义。

接下来我们介绍几种常用的输入类型。

**1.文本域（Text Fields）**

文本域通过 **`<input type="text">`** 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域。

```html
<form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>
```

**注意**：表单本身并不可见。同时，在大多数浏览器中，文本域的默认宽度是20个字符。

**2.密码字段**

密码字段通过标签 **`<input type="password">`** 来定义:

```html
<form>
Password: <input type="password" name="pwd">
</form>
```

**注意**：密码字段字符不会明文显示，而是以星号 ***** 或圆点 **.** 替代。

**3.单选按钮（Radio Buttons）**

**`<input type="radio">`** 标签定义了表单的单选框选项:

```html
<form action="">
<input type="radio" name="sex" value="male">男<br>
<input type="radio" name="sex" value="female">女
</form>
```

**4.复选框（Checkboxes）**

**`<input type="checkbox">`** 定义了复选框。

复选框可以选取一个或多个选项：

```html
<form>
<input type="checkbox" name="vehicle[]" value="Bike">我喜欢自行车<br>
<input type="checkbox" name="vehicle[]" value="Car">我喜欢小汽车
</form>
```

**5.提交按钮(Submit)**

**`<input type="submit">`** 定义了提交按钮。

当用户单击确认按钮时，表单的内容会被传送到服务器。表单的动作属性 **action** 定义了服务端的文件名。

**action** 属性会对接收到的用户输入数据进行相关的处理:

```html
<form name="input" action="html_form_action.php" method="get">
Username: <input type="text" name="user">
<input type="submit" value="Submit">
</form>
```

假如您在上面的文本框内键入几个字母，然后点击确认按钮，那么输入数据会传送到 **html_form_action.php** 文件，该页面将显示出输入的结果。

以上实例中有一个 method 属性，它用于定义表单数据的提交方式，可以是以下值：

- **post**：指的是 HTTP POST 方法，表单数据会包含在表单体内然后发送给服务器，用于提交敏感数据，如用户名与密码等。
- **get**：默认值，指的是 HTTP GET 方法，表单数据会附加在 **action** 属性的 URL 中，并以 **?**作为分隔符，一般用于不敏感信息，如分页等。例如：`https://www.runoob.com/?page=1`，这里的 page=1 就是 get 方法提交的数据。

```html
<!-- 以下表单使用 GET 请求发送数据到当前的 URL，method 默认位 GET。 -->
<form>
  <label>Name:
    <input name="submitted-name" autocomplete="name">
  </label>
  <button>Save</button>
</form>

<!-- 以下表单使用 POST 请求发送数据到当前的 URL。 -->
<form method="post">
  <label>Name:
    <input name="submitted-name" autocomplete="name">
  </label>
  <button>Save</button>
</form>

<!-- 表单使用 fieldset, legend, 和 label 标签 -->
<form method="post">
  <fieldset>
    <legend>Title</legend>
    <label><input type="radio" name="radio"> Select me</label>
  </fieldset>
</form>
```

## 12.HTML 框架

通过使用框架，你可以在同一个浏览器窗口中显示不止一个页面。

**iframe语法:**

```html
<iframe src="URL"></iframe>
```

该URL指向不同的网页。

### iframe - 设置高度与宽度

height 和 width 属性用来定义iframe标签的高度与宽度。

属性默认以像素为单位, 但是你可以指定其按比例显示 (如："80%")。

```html
<iframe src="demo_iframe.htm" width="200" height="200"></iframe>
```

### iframe - 移除边框

frameborder 属性用于定义iframe表示是否显示边框。

设置属性值为 "0" 移除iframe的边框:

```html
<iframe src="demo_iframe.htm" frameborder="0"></iframe>
```

### iframe-显示目标链接页面

iframe 可以显示一个目标链接的页面

目标链接的属性必须使用 iframe 的属性，如下实例:

```html
<iframe src="demo_iframe.htm" name="iframe_a"></iframe>
<p><a href="https://www.runoob.com" target="iframe_a" rel="noopener">RUNOOB.COM</a></p>
```



> 出于有些网页不希望被嵌套, 响应头中有一选项:

```
X-Frame-Options
```

他有三个可配置值

```html
DENY：表示该网站页面不允许被嵌套，即便是在自己的域名的页面中也不能进行嵌套。
SAMEORIGIN：表示该页面可以在相同域名页面中被嵌套展示。
ALLOW-FROM uri：表示该页面可以在指定来源页面中进行嵌套展示。
```

## 13.HTML颜色

HTML 颜色由红色、绿色、蓝色混合而成。

HTML 颜色由一个十六进制符号来定义，这个符号由红色、绿色和蓝色的值组成（RGB）。

每种颜色的最小值是0（十六进制：#00）。最大值是255（十六进制：#FF）。

RGBA 的意思是（Red-Green-Blue-Alpha）它是在 RGB 上扩展包括了 **“alpha”** 通道，运行对颜色值设置透明度。

```css
div {

background:rgba(255,0,0,0.5);

}
```

相对于使用 rgb(255,255,0)，使用 rgba(255,255,0,0.5) 可以实现设置颜色透明度的功能，这里的 0.5 表示透明度，范围 0~1，0 表示全透明。

通常我们为了省略一个 0:

```css
div {
    background:rgba(255,0,0,.5);
}
```

实例：

```html
<p style="background-color:rgb(255,255,0)">
通过 rbg 值设置背景颜色
</p>
<p style="background-color:rgba(255,255,0,0.25)">
通过 rbg 值设置背景颜色
</p>
<p style="background-color:rgba(255,255,0,0.5)">
通过 rbg 值设置背景颜色
</p>
<p style="background-color:rgba(255,255,0,0.75)">
通过 rbg 值设置背景颜色
</p>
```

## 14.HTML脚本

### HTML `<script>` 标签

`<script>` 标签用于定义客户端脚本，比如 JavaScript。

`<script>` 元素既可包含脚本语句，也可通过 src 属性指向外部脚本文件。

JavaScript 最常用于图片操作、表单验证以及内容动态更新。

下面的脚本会向浏览器输出"Hello World!"：

```html
<script>
document.write("Hello World!");
</script>
```

### HTML`<noscript>` 标签

`<noscript> `标签提供无法使用脚本时的替代内容，比方在浏览器禁用脚本时，或浏览器不支持客户端脚本时。

`<noscript>`元素可包含普通 HTML 页面的 body 元素中能够找到的所有元素。

只有在浏览器不支持脚本或者禁用脚本时，才会显示 `<noscript>` 元素中的内容：

```html
<script>
document.write("Hello World!")
</script>
<noscript>抱歉，你的浏览器不支持 JavaScript!</noscript>
```

您只能在 HTML 输出流中使用 **document.write**。 如果您在文档已加载后使用它（比如在函数中），会覆盖整个文档。

## 15.HTML字符实体

HTML 中的预留字符必须被替换为字符实体。

一些在键盘上找不到的字符也可以使用字符实体来替换。

### HTML 实体

在 HTML 中，某些字符是预留的。

在 HTML 中不能使用小于号（<）和大于号（>），这是因为浏览器会误认为它们是标签。

如果希望正确地显示预留字符，我们必须在 HTML 源代码中使用字符实体（character entities）。 字符实体类似这样：

```html
&entity_name;

<!-- 或 -->

&#entity_number;
```

如需显示小于号，我们必须这样写：`&lt;` 或`&#60; `  或  `&#060`

**提示**： 使用实体名而不是数字的好处是，名称易于记忆。不过坏处是，浏览器也许并不支持所有实体名称（对实体数字的支持却很好）。

### 不间断空格

HTML 中的常用字符实体是不间断空格(&nbsp;)。

浏览器总是会截短 HTML 页面中的空格。如果您在文本中写 10 个空格，在显示该页面之前，浏览器会删除它们中的 9 个。如需在页面中增加空格的数量，可以用以下转义字符分隔字符

`&nbsp;` , `&ensp;` , `&emsp;` , `&thinsp;` , `&zwnj;` ,`&zwj;`

**1.`&nbsp;`**

`&nbsp;`的宽度，可运行于所有主流浏览器。其他几种空格（ `&ensp;` , `&emsp;` , `&thinsp;` , `&zwnj;` ,`&zwj;`）在不同浏览器中宽度各异。

`&nbsp;`  受font-size影响, 受letter-spacing和word-spacing影响;
另外5个,受font-size影响, 不受letter-spacing和word-spacing影响;

`&nbsp;` 不换行空格,默认四分之一em
全称No-Break Space，它是最常见和我们使用最多的空格，大多数的人可能只接触了&nbsp;，它是按下space键产生的空格。在HTML中，如果你用空格键产生此空格，空格是不会累加的（只算1个）。要使用html实体表示才可累加，该空格占据宽度受字体影响明显而强烈。
`&nbsp;`受css的word-spacing和letter-spacing控制, 其它不受;
`&nbsp;`等效Unicode的不间断空格: 十六进制写法`&#xA0;` , 十进制写法`&#160`;

**2.`&ensp;`**

`&ensp;` 半角空格,半个em
全称是En Space，en是字体排印学的计量单位，为em宽度的一半。根据定义，它等同于字体度的一半（如16px字体中就是8px）。名义上是小写字母n的宽度。
此空格传承空格家族一贯的特性：透明的，
此空格有个相当稳健的特性，就是其 占据的宽度正好是1/2个中文宽度，而且基本上不受字体影响。
受font-size影响, 不受letter-spacing和word-spacing影响;

**3.`&emsp;`**

`&emsp;` 全角空格,一个em
全称是Em Space，em是字体排印学的计量单位，相当于当前指定的点数。例如，1 em在16px的字体中就是16px。
此空格也传承空格家族一贯的特性：透明的，
此空格也有个相当稳健的特性，就是其 占据的宽度正好是1个中文宽度，而且基本上不受字体影响。
受font-size影响, 不受letter-spacing和word-spacing影响;

**4.`&thinsp;`** 

`&thinsp;` 窄空格符,瘦弱空格符,六分之一em
全称是Thin Space。瘦弱空格，就是该空格长得比较瘦弱，身体单薄，占据的宽度比较小。它是em之六分之一宽。
受font-size影响, 不受letter-spacing和word-spacing影响

**5.`&zwnj;`**‌

`&zwnj;`‌零宽不连字符
全称是Zero Width Non Joiner，是一个不打印字符，放在电子文本的两个字符之间，抑制本来会发生的连字，而是以这两个字符原本的字形来绘制。Unicode中的零宽不连字字符映射为“”（zero width non-joiner，U+200C），HTML字符值引用为： ‌
受font-size影响, 不受letter-spacing和word-spacing影响;

**6.`&zwj;`**

`&zwj;` 零宽连字符
全称是Zero Width Joiner，是一个不打印字符，放在某些需要复杂排版语言（如阿拉伯语、印地语）的两个字符之间，使得这两个本不会发生连字的字符产生了连字效果。零宽连字符的Unicode码位是U+200D 。
受font-size影响, 不受letter-spacing和word-spacing影响;




### 结合音标符

发音符号是加到字母上的一个"glyph(字形)"。

一些变音符号, 如 尖音符 ( ̀) 和 抑音符 ( ́) 。

变音符号可以出现字母的上面和下面，或者字母里面，或者两个字母间。

变音符号可以与字母、数字字符的组合来使用。

以下是一些实例:

| 音标符 | 字符 | Construct | 输出结果 |
| :----- | :--- | :-------- | :------- |
| ̀       | a    | `&#768`;  | à        |
| ́       | a    | `&#769`;  | á        |
| ̂       | a    | `&#770`;  | â        |
| ̃       | a    | `&#771`;  | ã        |
| ̀       | O    | `&#768`;  | Ò        |
| ́       | O    | `&#769`;  | Ó        |
| ̂       | O    | `&#770`;  | Ô        |
| ̃       | O    | `&#771`;  | Õ        |

### HTML字符实体

实体名称对大小写敏感！

[HTML ISO-8859-1 参考手册](https://www.runoob.com/tags/ref-entities.html)

## 16.HTML URL

URL 是一个网页地址。

URL可以由字母组成，如`runoob.com`，或互联网协议（IP）地址： `192.68.20.50`。大多数人进入网站使用网站域名来访问，因为名字比数字更容易记住。

### URL - 统一资源定位器

Web浏览器通过URL从Web服务器请求页面。

当您点击 HTML 页面中的某个链接时，对应的 `<a>` 标签指向万维网上的一个地址。

一个统一资源定位器(URL) 用于定位万维网上的文档。

一个网页地址实例: http://www.runoob.com/html/html-tutorial.html 语法规则:

```html
scheme://host.domain:port/path/filename
```

**说明:**

- scheme - 定义因特网服务的类型。最常见的类型是 http

- host - 定义域主机（http 的默认主机是 www）

- domain - 定义因特网域名，比如 runoob.com

- :port - 定义主机上的端口号（http 的默认端口号是 80）

- path - 定义服务器上的路径（如果省略，则文档必须位于网站的根目录中）。

- filename - 定义文档/资源的名称

### 常见的 URL Scheme

以下是一些URL scheme：

| Scheme | 访问               | 用于...                             |
| :----- | :----------------- | :---------------------------------- |
| http   | 超文本传输协议     | 以 http:// 开头的普通网页。不加密。 |
| https  | 安全超文本传输协议 | 安全网页，加密所有信息交换。        |
| ftp    | 文件传输协议       | 用于将文件下载或上传至网站。        |
| file   |                    | 您计算机上的文件。                  |

### URL 字符编码

URL 只能使用 [ASCII 字符集](https://www.runoob.com/tags/html-ascii.html).

来通过因特网进行发送。由于 URL 常常会包含 ASCII 集合之外的字符，URL 必须转换为有效的 ASCII 格式。

URL 编码使用 "%" 其后跟随两位的十六进制数来替换非 ASCII 字符。

URL 不能包含空格。URL 编码通常使用 + 来替换空格。

## 17.HTML 标签简写及全称

下表列出了 HTML 标签简写及全称：

| 标签        | 英文全称                  | 中文说明                       |
| :---------- | :------------------------ | :----------------------------- |
| a           | Anchor                    | 锚                             |
| abbr        | Abbreviation              | 缩写词                         |
| acronym     | Acronym                   | 取首字母的缩写词               |
| address     | Address                   | 地址                           |
| alt         | alter                     | 替用(一般是图片显示不出的提示) |
| b           | Bold                      | 粗体（文本）                   |
| bdo         | Bi-Directional Override   | 文本显示方向                   |
| big         | Big                       | 变大（文本）                   |
| blockquote  | Block Quotation           | 区块引用语                     |
| br          | Break                     | 换行                           |
| cell        | cell                      | 巢                             |
| cellpadding | cellpadding               | 巢补白                         |
| cellspacing | cellspacing               | 巢空间                         |
| center      | Centered                  | 7居中（文本）                  |
| cite        | Citation                  | 引用                           |
| code        | Code                      | 源代码（文本）                 |
| dd          | Definition Description    | 定义描述                       |
| del         | Deleted                   | 删除（的文本）                 |
| dfn         | Defines a Definition Term | 定义定义条目                   |
| div         | Division                  | 分隔                           |
| dl          | Definition List           | 定义列表                       |
| dt          | Definition Term           | 定义术语                       |
| em          | Emphasized                | 加重（文本）                   |
| font        | Font                      | 字体                           |
| h1~h6       | Header 1 to Header 6      | 标题1到标题6                   |
| hr          | Horizontal Rule           | 水平尺                         |
| href        | hypertext reference       | 超文本引用                     |
| i           | Italic                    | 斜体（文本）                   |
| iframe      | Inline frame              | 定义内联框架                   |
| ins         | Inserted                  | 插入（的文本）                 |
| kbd         | Keyboard                  | 键盘（文本）                   |
| li          | List Item                 | 列表项目                       |
| nl          | navigation lists          | 导航列表                       |
| ol          | Ordered List              | 排序列表                       |
| optgroup    | Option group              | 定义选项组                     |
| p           | Paragraph                 | 段落                           |
| pre         | Preformatted              | 预定义格式（文本 ）            |
| q           | Quotation                 | 引用语                         |
| rel         | Reload                    | 加载                           |
| s/ strike   | Strikethrough             | 删除线                         |
| samp        | Sample                    | 示例（文本                     |
| small       | Small                     | 变小（文本）                   |
| span        | Span                      | 范围                           |
| src         | Source                    | 源文件链接                     |
| strong      | Strong                    | 加重（文本）                   |
| sub         | Subscripted               | 下标（文本）                   |
| sup         | Superscripted             | 上标（文本）                   |
| td          | table data cell           | 表格中的一个单元格             |
| th          | table header cell         | 表格中的表头                   |
| tr          | table row                 | 表格中的一行                   |
| tt          | Teletype                  | 打印机（文本）                 |
| u           | Underlined                | 下划线（文本）                 |
| ul          | Unordered List            | 不排序列表                     |
| var         | Variable                  | 变量（文本）                   |



# 三、CSS

## 1.CSS 语法

### CSS实例

CSS声明总是以分号 **;** 结束，声明总以大括号 **{}** 括起来:

```css
p 
{
    color:red;
    text-align:center;
}
```

### CSS 注释

注释是用来解释你的代码，并且可以随意编辑它，浏览器会忽略它。

CSS注释以 **/*** 开始, 以 ***/** 结束, 实例如下:

```css
/*这是个注释*/
p
{
    text-align:center;
    /*这是另一个注释*/
    color:black;
    font-family:arial;
}
```

## 2.CSS id 和 class

如果你要在HTML元素中设置CSS样式，你需要在元素中设置"id" 和 "class"选择器。

### id 选择器

id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。

HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 "#" 来定义。

以下的样式规则应用于元素属性 id="para1":

```css
#para1
{
    text-align:center;
    color:red;
}
```

> ID属性不要以数字开头，数字开头的ID在 Mozilla/Firefox 浏览器中不起作用。

### class 选择器

class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用。

class 选择器在 HTML 中以 class 属性表示, 在 CSS 中，类选择器以一个点 **`.`** 号显示：

在以下的例子中，所有拥有 center 类的 HTML 元素均为居中。

```css
.center {text-align:center;}
```

你也可以指定特定的 HTML 元素使用 class。

在以下实例中, 所有的 p 元素使用 class="center" 让该元素的文本居中:

```css
p.center {text-align:center;}
```

多个 class 选择器可以使用空格分开：

```css
.center { text-align:center; }
.color { color:#ff0000; }
<p class="center color">段落居中，颜色为红色。</p> 
```

## 3.CSS 创建

当读到一个样式表时，浏览器会根据它来格式化 HTML 文档。

**如何插入样式表**

插入样式表的方法有三种:

- 外部样式表(External style sheet)
- 内部样式表(Internal style sheet)
- 内联样式(Inline style)

### 外部样式表

当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 `<link>` 标签链接到样式表。 `<link> `标签在（文档的）头部：

```css
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

浏览器会从文件 mystyle.css 中读到样式声明，并根据它来格式文档。

外部样式表可以在任何文本编辑器中进行编辑。文件不能包含任何的 html 标签。样式表应该以 .css 扩展名进行保存。下面是一个样式表文件的例子：

```css
hr {color:sienna;}
p {margin-left:20px;}
body {background-image:url("/images/back40.gif");}
```

> 不要在属性值与单位之间留有空格（如："margin-left: 20 px" ），正确的写法是 "margin-left: 20px" 。

### 内部样式表

当单个文档需要特殊的样式时，就应该使用内部样式表。你可以使用 `<style>` 标签在文档**头部**定义内部样式表，就像这样:

```css
<head>
<style>
hr {color:sienna;}
p {margin-left:20px;}
body {background-image:url("images/back40.gif");}
</style>
</head>
```

### 行内样式表

> 也叫做内联样式

由于要将表现和内容混杂在一起，内联样式会损失掉样式表的许多优势。请慎用这种方法，例如当样式仅需要在一个元素上应用一次时。

要使用内联样式，你需要在相关的标签内使用样式（style）属性。Style 属性可以包含任何 CSS 属性。本例展示如何改变段落的颜色和左外边距：

```css
<p style="color:sienna;margin-left:20px">这是一个段落。</p>
```

### 多重样式

如果某些属性在不同的样式表中被同样的选择器定义，那么属性值将从更具体的样式表中被继承过来。 

例如，外部样式表拥有针对 h3 选择器的三个属性：

```css
h3
{
    color:red;
    text-align:left;
    font-size:8pt;
}
```

而内部样式表拥有针对 h3 选择器的两个属性：

```css
h3
{
    text-align:right;
    font-size:20pt;
}
```

假如拥有内部样式表的这个页面同时与外部样式表链接，那么 h3 得到的样式是：

```css
color:red;
text-align:right;
font-size:20pt;
```

即颜色属性将被继承于外部样式表，而文字排列（text-alignment）和字体尺寸（font-size）会被内部样式表中的规则取代。

### 多重样式优先级

样式表允许以多种方式规定样式信息。样式可以规定在单个的 HTML 元素中，在 HTML 页的头元素中，或在一个外部的 CSS 文件中。甚至可以在同一个 HTML 文档内部引用多个外部样式表。

一般情况下，优先级如下：

**（内联样式）`Inline style` > （内部样式）`Internal style sheet` >（外部样式）`External style sheet` > 浏览器默认样式**

**注意**：如果外部样式放在内部样式的后面，则外部样式将覆盖内部样式。

[CSS 样式优先级](https://www.runoob.com/w3cnote/css-style-priority.html)



**多重样式优先级深入概念**

优先级是浏览器是通过判断哪些属性值与元素最相关以决定并应用到该元素上的。优先级仅由选择器组成的匹配规则决定的。

优先级就是分配给指定的CSS声明的一个权重，它由匹配的选择器中的每一种选择器类型的数值决定。

**1.优先级顺序**

下列是一份优先级逐级增加的选择器列表：

- 通用选择器（*）
- 元素(类型)选择器
- 类选择器
- 属性选择器
- 伪类
- ID 选择器
- 内联样式

**2.!important 规则例外**

当 !important 规则被应用在一个样式声明中时,该样式声明会覆盖CSS中任何其他的声明, 无论它处在声明列表中的哪里. 尽管如此, !important规则还是与优先级毫无关系.使用 !important 不是一个好习惯，因为它改变了你样式表本来的级联规则，从而使其难以调试。

一些经验法则：

- **Always** 要优化考虑使用样式规则的优先级来解决问题而不是 `!important`
- **Only** 只在需要覆盖全站或外部 css（例如引用的 ExtJs 或者 YUI ）的特定页面中使用 `!important`
- **Never** 永远不要在全站范围的 css 上使用` !important`
- **Never** 永远不要在你的插件中使用 `!important`

**3.CSS 优先级法则：**

-  A 选择器都有一个权值，权值越大越优先；
-  B 当权值相等时，后出现的样式表设置要优于先出现的样式表设置；
-  C 创作者的规则高于浏览者：即网页编写者设置的CSS 样式的优先权高于浏览器所设置的样式；
-  D 继承的CSS 样式不如后来指定的CSS 样式；
-  E 在同一组属性设置中标有“!important”规则的优先级最大；

![CSS优先级](C:\Users\wuqian\Desktop\附录文件和源代码\杂物\壁纸\QQ图片20241027131238.png)

## 4.CSS 背景

CSS 背景属性用于定义HTML元素的背景。

CSS 属性定义背景效果:

- background-color
- background-image
- background-repeat
- background-attachment
- background-position

### 背景颜色

background-color 属性定义了元素的背景颜色.

页面的背景颜色使用在body的选择器中:

```css
body {background-color:#b0c4de;}
```

CSS中，颜色值通常以以下方式定义:

- 十六进制 - 如："#ff0000"
- RGB - 如："rgb(255,0,0)"
- 颜色名称 - 如："red"

### 背景图像

background-image 属性描述了元素的背景图像.

默认情况下，背景图像进行平铺重复显示，以覆盖整个元素实体.

页面背景图片设置实例:

```css
body {background-image:url('paper.gif');}
```

### 背景图像 - 水平或垂直平铺

默认情况下 background-image 属性会在页面的水平或者垂直方向平铺。

一些图像如果在水平方向与垂直方向平铺，这样看起来很不协调

如果图像只在水平方向平铺 (repeat-x), 页面背景会更好些:

```css
body
{
background-image:url('gradient2.png');
background-repeat:repeat-x;
}
```

### 背景图像- 设置定位与不平铺

让背景图像不影响文本的排版

如果你不想让图像平铺，你可以使用 background-repeat 属性:

```css
body
{
background-image:url('img_tree.png');
background-repeat:no-repeat;
}
```

以上实例中，背景图像与文本显示在同一个位置，为了让页面排版更加合理，不影响文本的阅读，我们可以改变图像的位置。

可以利用 background-position 属性改变图像在背景中的位置:

```css
body
{
background-image:url('img_tree.png');
background-repeat:no-repeat;
background-position:right top;
}
```

### 背景- 简写属性

在以上实例中我们可以看到页面的背景颜色通过了很多的属性来控制。

为了简化这些属性的代码，我们可以将这些属性合并在同一个属性中.

背景颜色的简写属性为 "background":

```css
body {background:#ffffff url('img_tree.png') no-repeat right top;}
```

当使用简写属性时，属性值的顺序为:

- background-color
- background-image
- background-repeat
- background-attachment
- background-position

以上属性无需全部使用，你可以按照页面的实际需要使用.

### --CSS 背景属性

| Property              | 描述                                         |
| :-------------------- | :------------------------------------------- |
| background            | 简写属性，作用是将背景属性设置在一个声明中。 |
| background-attachment | 背景图像是否固定或者随着页面的其余部分滚动。 |
| background-color      | 设置元素的背景颜色。                         |
| background-image      | 把图像设置为背景。                           |
| background-position   | 设置背景图像的起始位置。                     |
| background-repeat     | 设置背景图像是否及如何重复。                 |

## 5.CSS 文本

### 文本颜色

颜色属性被用来设置文字的颜色。

颜色是通过CSS最经常的指定：

- 十六进制值 - 如: **＃FF0000**
- 一个RGB值 - 如: **RGB(255,0,0)**
- 颜色的名称 - 如: **red**

参阅 [CSS 颜色值](https://www.runoob.com/cssref/css-colors-legal.html) 查看完整的颜色值。

一个网页的背景颜色是指在主体内的选择：

```css
body {color:red;}
h1 {color:#00ff00;}
h2 {color:rgb(255,0,0);}
```

对于W3C标准的CSS：如果你定义了颜色属性，你还必须定义背景色属性。

### 文本的对齐方式

文本排列属性是用来设置文本的水平对齐方式。

文本可居中或对齐到左或右,两端对齐.

当text-align设置为"justify"，每一行被展开为宽度相等，左，右外边距是对齐（如杂志和报纸）。

```css
h1 {text-align:center;}
p.date {text-align:right;}
p.main {text-align:justify;}
```

### 文本修饰

text-decoration 属性用来设置或删除文本的装饰。

从设计的角度看 text-decoration属性主要是用来删除链接的下划线：

```css
a {text-decoration:none;}
```

也可以这样装饰文字：

```css
h1 {text-decoration:overline;}
h2 {text-decoration:line-through;}
h3 {text-decoration:underline;}
```

我们不建议强调指出不是链接的文本，因为这常常混淆用户。

### 文本转换

文本转换属性是用来指定在一个文本中的大写和小写字母。

可用于所有字句变成大写或小写字母，或每个单词的首字母大写。

```css
p.uppercase {text-transform:uppercase;}
p.lowercase {text-transform:lowercase;}
p.capitalize {text-transform:capitalize;}
```

### 文本缩进

文本缩进属性是用来指定文本的第一行的缩进。

```css
p {text-indent:50px;}
```

### --CSS 文本属性

| 属性                    | 描述                     |
| :---------------------- | :----------------------- |
| color                   | 设置文本颜色             |
| direction               | 设置文本方向             |
| letter-spacing          | 设置字符间距             |
| line-height(类似行间距) | 设置行高                 |
| text-align              | 对齐元素中的文本         |
| text-decoration         | 向文本添加修饰           |
| text-indent             | 缩进元素中文本的首行     |
| text-shadow             | 设置文本阴影             |
| text-transform          | 控制元素中的字母         |
| unicode-bidi            | 设置或返回文本是否被重写 |
| vertical-align          | 设置元素的垂直对齐       |
| white-space             | 设置元素中空白的处理方式 |
| word-spacing            | 设置字间距               |

## 6.CSS 字体

CSS字体属性定义字体，加粗，大小，文字样式。

### CSS字型

在CSS中，有两种类型的字体系列名称：

- **通用字体系列** - 拥有相似外观的字体系统组合（如 "Serif" 或 "Monospace"）
- **特定字体系列** - 一个特定的字体系列（如 "Times" 或 "Courier"）

| Generic family | 说明                                        |
| :------------- | :------------------------------------------ |
| Serif          | Serif字体中字符在行的末端拥有额外的装饰     |
| Sans-serif     | "Sans"是指无 - 这些字体在末端没有额外的装饰 |
| Monospace      | 所有的等宽字符具有相同的宽度                |

### 字体系列

font-family 属性设置文本的字体系列。

font-family 属性应该设置几个字体名称作为一种"后备"机制，如果浏览器不支持第一种字体，他将尝试下一种字体。

**注意**: 如果字体系列的名称超过一个字，它必须用引号，如Font Family："宋体"。

多个字体系列是用一个逗号分隔指明：

```css
p{font-family:"Times New Roman", Times, serif;}
```

### 字体样式

主要是用于指定斜体文字的字体样式属性。

这个属性有三个值：

- 正常 - 正常显示文本
- 斜体 - 以斜体字显示的文字
- 倾斜的文字 - 文字向一边倾斜（和斜体非常类似，但不太支持）

```css
p.normal {font-style:normal;}
p.italic {font-style:italic;}
p.oblique {font-style:oblique;}
```

### 字体大小

font-size 属性设置文本的大小。

能否管理文字的大小，在网页设计中是非常重要的。但是，你不能通过调整字体大小使段落看上去像标题，或者使标题看上去像段落。

请务必使用正确的HTML标签，就`<h1>` - `<h6>`表示标题和`<p>`表示段落：

字体大小的值可以是绝对或相对的大小。

绝对大小：

- 设置一个指定大小的文本
- 不允许用户在所有浏览器中改变文本大小
- 确定了输出的物理尺寸时绝对大小很有用

相对大小：

- 相对于周围的元素来设置大小
- 允许用户在浏览器中改变文字大小

**1.设置字体大小像素**

设置文字的大小与像素，让您完全控制文字大小：

```css
h1 {font-size:40px;}
h2 {font-size:30px;}
p {font-size:14px;}
```

**2.用em来设置字体大小**

为了避免Internet Explorer 中无法调整文本的问题，许多开发者使用 em 单位代替像素。

em的尺寸单位由W3C建议。

1em和当前字体大小相等。在浏览器中默认的文字大小是16px。

因此，1em的默认大小是16px。可以通过下面这个公式将像素转换为em：**px/16=em**

```css
h1 {font-size:2.5em;} /* 40px/16=2.5em */
h2 {font-size:1.875em;} /* 30px/16=1.875em */
p {font-size:0.875em;} /* 14px/16=0.875em */
```

在上面的例子，em的文字大小是与前面的例子中像素一样。不过，如果使用 em 单位，则可以在所有浏览器中调整文本大小。

不幸的是，仍然是IE浏览器的问题。调整文本的大小时，会比正常的尺寸更大或更小。

**3.使用百分比和EM组合**

在所有浏览器的解决方案中，设置 `<body>`元素的默认字体大小的是百分比：

```css
body {font-size:100%;}
h1 {font-size:2.5em;}
h2 {font-size:1.875em;}
p {font-size:0.875em;}
```

### --CSS 字体属性

| Property     | 描述                                 |
| :----------- | :----------------------------------- |
| font         | 在一个声明中设置所有的字体属性       |
| font-family  | 指定文本的字体系列                   |
| font-size    | 指定文本的字体大小                   |
| font-style   | 指定文本的字体样式                   |
| font-variant | 以小型大写字体或者正常字体显示文本。 |
| font-weight  | 指定字体的粗细。                     |

## 7.CSS 链接

不同的链接可以有不同的样式。

### 链接样式

链接的样式，可以用任何CSS属性（如颜色，字体，背景等）。

特别的链接，可以有不同的样式，这取决于他们是什么状态。

这四个链接状态是：

- `a:link` - 正常，未访问过的链接
- `a:visited` - 用户已访问过的链接
- `a:hover` - 当用户鼠标放在链接上时
- `a:active` - 链接被点击的那一刻

```css
a:link {color:#000000;}      /* 未访问链接*/
a:visited {color:#00FF00;}  /* 已访问链接 */
a:hover {color:#FF00FF;}  /* 鼠标移动到链接上 */
a:active {color:#0000FF;}  /* 鼠标点击时 */
```

当设置为若干链路状态的样式，也有一些顺序规则：

- `a:hover` 必须跟在 `a:link` 和 `a:visited`后面
- `a:active` 必须跟在 `a:hover`后面

### 常见的链接样式

根据上述链接的颜色变化的例子，看它是在什么状态。

让我们通过一些其他常见的方式转到链接样式：

**1.文本修饰**

text-decoration 属性主要用于删除链接中的下划线：

```css
a:link {text-decoration:none;}
a:visited {text-decoration:none;}
a:hover {text-decoration:underline;}
a:active {text-decoration:underline;}
```

**2.背景颜色**

背景颜色属性指定链接背景色：

```css
a:link {background-color:#B2FF99;}
a:visited {background-color:#FFFF85;}
a:hover {background-color:#FF704D;}
a:active {background-color:#FF704D;}
```



## 8.CSS列表

CSS 列表属性作用如下：

- 设置不同的列表项标记为有序列表
- 设置不同的列表项标记为无序列表
- 设置列表项标记为图像

在 HTML中，有两种类型的列表：

- 无序列表 **`ul`** - 列表项标记用特殊图形（如小黑点、小方框等）
- 有序列表 **`ol`** - 列表项的标记有数字或字母

使用 CSS，可以列出进一步的样式，并可用图像作列表项标记。

### 不同的列表项标记

list-style-type属性指定列表项标记的类型是：

```css
ul.a {list-style-type: circle;}
ul.b {list-style-type: square;}
 
ol.c {list-style-type: upper-roman;}
ol.d {list-style-type: lower-alpha;}
```

### 作为列表项标记的图像

要指定列表项标记的图像，使用列表样式图像属性：

```css
ul
{
    list-style-image: url('sqpurple.gif');
}
```

### 浏览器兼容性解决方案

同样在所有的浏览器，下面的例子会显示的图像标记：

```css
ul
{
    list-style-type: none;
    padding: 0px;
    margin: 0px;
}
ul li
{
    background-image: url(sqpurple.gif);
    background-repeat: no-repeat;
    background-position: 0px 5px; 
    padding-left: 14px; 
}
```

例子解释：

- ul:
  - 设置列表类型为没有列表项标记
  - 设置填充和边距 0px（浏览器兼容性）
- ul 中所有 li:
  - 设置图像的 URL，并设置它只显示一次（无重复）
  - 您需要的定位图像位置（左 0px 和上下 5px）
  - 用 padding-left 属性把文本置于列表中

### 列表 - 简写属性

在单个属性中可以指定所有的列表属性。这就是所谓的简写属性。

为列表使用简写属性，列表样式属性设置如下：

```css
ul
{
    list-style: square url("sqpurple.gif");
}
```

可以按顺序设置如下属性：

- list-style-type
- list-style-position (有关说明，请参见下面的CSS属性表)
- list-style-image

如果上述值丢失一个，其余仍在指定的顺序，就没关系。

### 移除默认设置

list-style-type:none 属性可以用于移除小标记。默认情况下列表 <ul> 或 <ol> 还设置了内边距和外边距，可使用 `margin:0` 和 `padding:0` 来移除:

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
```

### --CSS 列表属性

| 属性                | 描述                                               |
| :------------------ | :------------------------------------------------- |
| list-style          | 简写属性。用于把所有用于列表的属性设置于一个声明中 |
| list-style-image    | 将图像设置为列表项标志。                           |
| list-style-position | 设置列表中列表项标志的位置。                       |
| list-style-type     | 设置列表项标志的类型。                             |

## 9.CSS 表格

### 表格边框

指定CSS表格边框，使用border属性。

下面的例子指定了一个表格的Th和TD元素的黑色边框：

```css
table, th, td
{
    border: 1px solid black;
}
```

请注意，在上面的例子中的表格有双边框。这是因为表和th/ td元素有独立的边界。

为了显示一个表的单个边框，使用 border-collapse属性。

### 折叠边框

border-collapse 属性设置表格的边框是否被折叠成一个单一的边框或隔开：

```css
table
{
    border-collapse:collapse;
}
table,th, td
{
    border: 1px solid black;
}
```

### 表格宽度和高度

Width和height属性定义表格的宽度和高度。

下面的例子是设置100％的宽度，50像素的th元素的高度的表格：

```css
table 
{
    width:100%;
}
th
{
    height:50px;
}
```

### 表格文字对齐

表格中的文本对齐和垂直对齐属性。

text-align属性设置水平对齐方式，向左，右，或中心：

```css
td
{
    text-align:right;
}
```

垂直对齐属性设置垂直对齐，比如顶部，底部或中间：

```css
td
{
    height:50px;
    vertical-align:bottom;
}
```

### 表格填充

如需控制边框和表格内容之间的间距，应使用td和th元素的填充属性：

```css
td
{
    padding:15px;
}
```

### 表格颜色

下面的例子指定边框的颜色，和th元素的文本和背景颜色：

```css
table, td, th
{
    border:1px solid green;
}
th
{
    background-color:green;
    color:white;
}
```



## 10.CSS 盒子模型

所有HTML元素可以看作盒子，在CSS中，"box model"这一术语是用来设计和布局时使用。

CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：边距，边框，填充，和实际内容。

盒模型允许我们在其它元素和周围元素边框之间的空间放置元素。

不同部分的说明：

- **Margin(外边距)** - 清除边框外的区域，外边距是透明的。
- **Border(边框)** - 围绕在内边距和内容外的边框。
- **Padding(内边距)** - 清除内容周围的区域，内边距是透明的。
- **Content(内容)** - 盒子的内容，显示文本和图像。

为了正确设置元素在所有浏览器中的宽度和高度，你需要知道的盒模型是如何工作的。

### 元素的宽度和高度

当您指定一个 CSS 元素的宽度和高度属性时，你只是设置内容区域的宽度和高度。要知道，完整大小的元素，你还必须添加内边距，边框和外边距。

下面的例子中的元素的总宽度为 450px：

```css
div {
    width: 300px;
    border: 25px solid green;
    padding: 25px;
    margin: 25px;
}
```

最终元素的总宽度计算公式是这样的：

总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距

元素的总高度最终计算公式是这样的：

总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距

### 浏览器的兼容性问题

一旦为页面设置了恰当的 DTD，大多数浏览器都会按照上面的图示来呈现内容。然而 IE 5 和 6 的呈现却是不正确的。根据 W3C 的规范，元素内容占据的空间是由 width 属性设置的，而内容周围的 padding 和 border 值是另外计算的。不幸的是，IE5.X 和 6 在怪异模式中使用自己的非标准模型。这些浏览器的 width 属性不是内容的宽度，而是内容、内边距和边框的宽度的总和。

虽然有方法解决这个问题。但是目前最好的解决方案是回避这个问题。也就是，不要给元素添加具有指定宽度的内边距，而是尝试将内边距或外边距添加到元素的父元素和子元素。

IE8 及更早IE版本不支持设置填充的宽度和边框的宽度属性。

解决IE8及更早版本不兼容问题可以在HTML页面声明 `<!DOCTYPE html>`即可。

## 11.CSS Border(边框)

CSS边框属性允许你指定一个元素边框的样式和颜色。

### 边框样式

边框样式属性指定要显示什么样的边界。

 **border-style**属性用来定义边框的样式

**border-style 值:**

- none: 默认无边框
- dotted: 定义一个点线边框
- dashed: 定义一个虚线边框
- solid: 定义实线边框
- double: 定义两个边框。 两个边框的宽度和 border-width 的值相同
- groove: 定义3D沟槽边框。效果取决于边框的颜色值
- ridge: 定义3D脊边框。效果取决于边框的颜色值
- inset:定义一个3D的嵌入边框。效果取决于边框的颜色值
- outset: 定义一个3D突出边框。 效果取决于边框的颜色值

### 边框宽度

您可以通过 border-width 属性为边框指定宽度。

为边框指定宽度有两种方法：可以指定长度值，比如 2px 或 0.1em(单位为 px, pt, cm, em 等)，或者使用 3 个关键字之一，它们分别是 thick 、medium（默认值） 和 thin。

**注意：**CSS 没有定义 3 个关键字的具体宽度，所以一个用户可能把 thick 、medium 和 thin 分别设置为等于 5px、3px 和 2px，而另一个用户则分别设置为 3px、2px 和 1px。

```css
p.one
{
    border-style:solid;
    border-width:5px;
}
p.two
{
    border-style:solid;
    border-width:medium;
}
```

### 边框颜色

border-color属性用于设置边框的颜色。可以设置的颜色：

- name - 指定颜色的名称，如 "red"
- RGB - 指定 RGB 值, 如 "rgb(255,0,0)"
- Hex - 指定16进制值, 如 "#ff0000"

您还可以设置边框的颜色为"transparent"。

**注意：** border-color单独使用是不起作用的，必须得先使用border-style来设置边框样式。

```css
p.one
{
    border-style:solid;
    border-color:red;
}
p.two
{
    border-style:solid;
    border-color:#98bf21;
}
```

### 边框-单独设置各边

在CSS中，可以指定不同的侧面不同的边框：

```css
p
{
    border-top-style:dotted;
    border-right-style:solid;
    border-bottom-style:dotted;
    border-left-style:solid;
}
```

border-style属性可以有1-4个值：

- border-style:dotted solid double dashed;
  - 上边框是 dotted
  - 右边框是 solid
  - 底边框是 double
  - 左边框是 dashed
- border-style:dotted solid double;
  - 上边框是 dotted
  - 左、右边框是 solid
  - 底边框是 double
- border-style:dotted solid;
  - 上、底边框是 dotted
  - 右、左边框是 solid
- border-style:dotted;
  - 四面边框是 dotted

上面的例子用了border-style。然而，它也可以和border-width 、 border-color一起使用。

### 边框-简写属性

上面的例子用了很多属性来设置边框。

你也可以在一个属性中设置边框。

你可以在"border"属性中设置：

- border-width
- border-style (required)
- border-color

```css
border:5px solid red;
```

### --CSS 边框属性

| 属性                | 描述                                                         |
| :------------------ | :----------------------------------------------------------- |
| border              | 简写属性，用于把针对四个边的属性设置在一个声明。             |
| border-style        | 用于设置元素所有边框的样式，或者单独地为各边设置边框样式。   |
| border-width        | 简写属性，用于为元素的所有边框设置宽度，或者单独地为各边边框设置宽度。 |
| border-color        | 简写属性，设置元素的所有边框中可见部分的颜色，或为 4 个边分别设置颜色。 |
| border-bottom       | 简写属性，用于把下边框的所有属性设置到一个声明中。           |
| border-bottom-color | 设置元素的下边框的颜色。                                     |
| border-bottom-style | 设置元素的下边框的样式。                                     |
| border-bottom-width | 设置元素的下边框的宽度。                                     |
| border-left         | 简写属性，用于把左边框的所有属性设置到一个声明中。           |
| border-left-cololr  | 设置元素的左边框的颜色。                                     |
| border-left-style   | 设置元素的左边框的样式。                                     |
| border-left-width   | 设置元素的左边框的宽度。                                     |
| border-right        | 简写属性，用于把右边框的所有属性设置到一个声明中。           |
| border-right-color  | 设置元素的右边框的颜色。                                     |
| border-right-style  | 设置元素的右边框的样式。                                     |
| border-right-width  | 设置元素的右边框的宽度。                                     |
| border-top          | 简写属性，用于把上边框的所有属性设置到一个声明中。           |
| border-top-color    | 设置元素的上边框的颜色。                                     |
| border-top-style    | 设置元素的上边框的样式。                                     |
| border-top-width    | 设置元素的上边框的宽度。                                     |
| border-radius       | 设置圆角的边框。                                             |

## 12.CSS outline(轮廓)

轮廓（outline）是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用。

轮廓（outline）属性指定元素轮廓的样式、颜色和宽度。

### --CSS 轮廓属性

"CSS" 列中的数字表示哪个CSS版本定义了该属性(CSS1 或者CSS2)。

| 属性          | 说明                           | 值                                                           | CSS  |
| :------------ | :----------------------------- | :----------------------------------------------------------- | :--- |
| outline       | 在一个声明中设置所有的轮廓属性 | *outline-color outline-style outline-width *inherit          | 2    |
| outline-color | 设置轮廓的颜色                 | *color-name hex-number rgb-number *invert inherit            | 2    |
| outline-style | 设置轮廓的样式                 | none dotted dashed solid double groove ridge inset outset inherit | 2    |
| outline-width | 设置轮廓的宽度                 | thin medium thick *length *inherit                           | 2    |

## 13.CSS margin(外边距)

CSS margin(外边距)属性定义元素周围的空间。

margin 清除周围的（外边框）元素区域。margin 没有背景颜色，是完全透明的。

margin 可以单独改变元素的上，下，左，右边距，也可以一次改变所有的属性。

| 值     | 说明                                        |
| :----- | :------------------------------------------ |
| auto   | 设置浏览器边距。 这样做的结果会依赖于浏览器 |
| length | 定义一个固定的margin（使用像素，pt，em等）  |
| %      | 定义一个使用百分比的边距                    |

> Margin可以使用负值，重叠的内容。

### margin - 单边外边距属性

在CSS中，它可以指定不同的侧面不同的边距：

```css
margin-top:100px;
margin-bottom:100px;
margin-right:50px;
margin-left:50px;
```

### margin - 简写属性

为了缩短代码，有可能使用一个属性中margin指定的所有边距属性。这就是所谓的简写属性。

所有边距属性的简写属性是 **margin** :

```css
margin:100px 50px;
```

margin属性可以有一到四个值。

- margin:25px 50px 75px 100px;
  - 上边距为25px
  - 右边距为50px
  - 下边距为75px
  - 左边距为100px
- margin:25px 50px 75px;
  - 上边距为25px
  - 左右边距为50px
  - 下边距为75px
- margin:25px 50px;
  - 上下边距为25px
  - 左右边距为50px
- margin:25px;
  - 所有的4个边距都是25px

### --CSS 边距属性

| 属性          | 描述                                       |
| :------------ | :----------------------------------------- |
| margin        | 简写属性。在一个声明中设置所有外边距属性。 |
| margin-bottom | 设置元素的下外边距。                       |
| margin-left   | 设置元素的左外边距。                       |
| margin-right  | 设置元素的右外边距。                       |
| margin-top    | 设置元素的上外边距。                       |

## 14.CSS padding(填充)

CSS padding（填充）是一个简写属性，定义元素边框与元素内容之间的空间，即上下左右的内边距。

当元素的 padding（填充）内边距被清除时，所释放的区域将会受到元素背景颜色的填充。

单独使用 padding 属性可以改变上下左右的填充。

| 值     | 说明                                |
| :----- | :---------------------------------- |
| length | 定义一个固定的填充(像素, pt, em,等) |
| %      | 使用百分比值定义一个填充            |

### 填充- 单边内边距属性

在CSS中，它可以指定不同的侧面不同的填充

```css
padding-top:25px;
padding-bottom:25px;
padding-right:50px;
padding-left:50px;
```

- 上内边距是 25px
- 右内边距是 50px
- 下内边距是 25px
- 左内边距是 50px

### 填充 - 简写属性

为了缩短代码，它可以在一个属性中指定的所有填充属性。

这就是所谓的简写属性。所有的填充属性的简写属性是 **padding** :

```css
padding:25px 50px;
```

Padding属性，可以有一到四个值。

-  padding:25px 50px 75px 100px;

  - 上填充为25px

  - 右填充为50px

  - 下填充为75px

  - 左填充为100px

-  padding:25px 50px 75px;

  - 上填充为25px

  - 左右填充为50px

  - 下填充为75px

-  padding:25px 50px;

  - 上下填充为25px

  - 左右填充为50px

-  padding:25px;
  - 所有的填充都是25px

### --CSS 填充属性

| 属性           | 说明                                       |
| :------------- | :----------------------------------------- |
| padding        | 使用简写属性设置在一个声明中的所有填充属性 |
| padding-bottom | 设置元素的底部填充                         |
| padding-left   | 设置元素的左部填充                         |
| padding-right  | 设置元素的右部填充                         |
| padding-top    | 设置元素的顶部填充                         |

## 15.CSS 分组和嵌套选择器

### 分组选择器

在样式表中有很多具有相同样式的元素。

```css
h1 {
    color:green;
}
h2 {
    color:green;
}
p {
    color:green;
}
```

为了尽量减少代码，你可以使用分组选择器。

每个选择器用逗号分隔。

在下面的例子中，我们对以上代码使用分组选择器：

```css
h1,h2,p
{
    color:green;
}
```

### 嵌套选择器

它可能适用于选择器内部的选择器的样式。

在下面的例子设置了四个样式：

- **`p{ }`**: 为所有 **p** 元素指定一个样式。
- **`.marked{ }`**: 为所有 **class="marked"** 的元素指定一个样式。
- **`.marked p{ }`**: 为所有 **class="marked"** 元素内的 **p** 元素指定一个样式。
- **`p.marked{ }`**: 为所有 **class="marked"** 的 **p** 元素指定一个样式。

```css
p
{
    color:blue;
    text-align:center;
}
.marked
{
    background-color:red;
}
.marked p
{
    color:white;
}
p.marked{
    text-decoration:underline;
}
```

## 16.CSS  Dimension(尺寸)

CSS 尺寸 (Dimension) 属性允许你控制元素的高度和宽度。同样，它允许你增加行间距。

### --CSS 尺寸属性

| 属性        | 描述                 |
| :---------- | :------------------- |
| height      | 设置元素的高度。     |
| line-height | 设置行高。           |
| max-height  | 设置元素的最大高度。 |
| max-width   | 设置元素的最大宽度。 |
| min-height  | 设置元素的最小高度。 |
| min-width   | 设置元素的最小宽度。 |
| width       | 设置元素的宽度。     |



## 17.CSS Display(显示) 与 Visibility（可见性）

display属性设置一个元素应如何显示，visibility属性指定一个元素应可见还是隐藏。

### 隐藏元素 visibility:hidden

隐藏一个元素可以通过把display属性设置为"none"，或把visibility属性设置为"hidden"。但是请注意，这两种方法会产生不同的结果。

visibility:hidden可以隐藏某个元素，但隐藏的元素仍需占用与未隐藏之前一样的空间。也就是说，该元素虽然被隐藏了，但仍然会影响布局。

```css
h1.hidden {visibility:hidden;}
```

### 隐藏元素 display:none

display:none可以隐藏某个元素，且隐藏的元素不会占用任何空间。也就是说，该元素不但被隐藏了，而且该元素原本占用的空间也会从页面布局中消失。

```css
h1.hidden {display:none;}
```

### Display - 块和内联元素

块元素是一个元素，占用了全部宽度，在前后都是换行符。

块元素的例子：

- `<h1>`
- `<p>`
- `<div>`

内联元素只需要必要的宽度，不强制换行。

内联元素的例子：

- `<span>`
- `<a>`

### 如何改变一个元素显示

可以更改内联元素和块元素，反之亦然，可以使页面看起来是以一种特定的方式组合，并仍然遵循web标准。

下面的示例把列表项显示为内联元素：

```css
li {display:inline;}
```

下面的示例把span元素作为块元素：

```css
span {display:block;}
```

**注意：**变更元素的显示类型看该元素是如何显示，它是什么样的元素。例如：一个内联元素设置为display:block是不允许有它内部的嵌套块元素。

## 18.CSS Position(定位)

position 属性指定了元素的定位类型。

position 属性的五个值：

- static
- relative
- fixed
- absolute
- sticky

元素可以使用的顶部，底部，左侧和右侧属性定位。然而，这些属性无法工作，除非事先设定position属性。他们也有不同的工作方式，这取决于定位方法。

### static 定位

HTML 元素的默认值，即没有定位，遵循正常的文档流对象。

静态定位的元素不会受到 top, bottom, left, right影响。

```css
div.static {
    position: static;
    border: 3px solid #73AD21;
}
```

### fixed 定位

元素的位置相对于浏览器窗口是固定位置。

即使窗口是滚动的它也不会移动：

```css
p.pos_fixed
{
    position:fixed;
    top:30px;
    right:5px;
}
```

**注意**： Fixed 定位在 IE7 和 IE8 下需要描述 !DOCTYPE 才能支持。

Fixed定位使元素的位置与文档流无关，因此不占据空间。

Fixed定位的元素和其他元素重叠。

### relative 定位

相对定位元素的定位是相对其正常位置。

```css
h2.pos_left
{
    position:relative;
    left:-20px;
}
h2.pos_right
{
    position:relative;
    left:20px;
}
```

移动相对定位元素，但它原本所占的空间不会改变。

```css
h2.pos_top
{
    position:relative;
    top:-50px;
}
```

相对定位元素经常被用来作为绝对定位元素的容器块。

### absolute 定位

绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于<html>:

```css
h2
{
    position:absolute;
    left:100px;
    top:150px;
}
```

bsolute 定位使元素的位置与文档流无关，因此不占据空间。

absolute 定位的元素和其他元素重叠。

### sticky 定位

sticky 英文字面意思是粘，粘贴，所以可以把它称之为粘性定位。

**`position: sticky;`** 基于用户的滚动位置来定位。

粘性定位的元素是依赖于用户的滚动，在 **`position:relative`** 与 **`position:fixed`** 定位之间切换。

它的行为就像 **`position:relative;`** 而当页面滚动超出目标区域时，它的表现就像 **`position:fixed;`**，它会固定在目标位置。

元素定位表现为在跨越特定阈值前为相对定位，之后为固定定位。

这个特定阈值指的是 top, right, bottom 或 left 之一，换言之，指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。

**注意**： Internet Explorer, Edge 15 及更早 IE 版本不支持 sticky 定位。 Safari 需要使用 -webkit- prefix (查看以下实例)。

```css
div.sticky {
    position: -webkit-sticky; /* Safari */
    position: sticky;
    top: 0;
    background-color: green;
    border: 2px solid #4CAF50;
}
```

### z-index 重叠的元素

元素的定位与文档流无关，所以它们可以覆盖页面上的其它元素

z-index属性指定了一个元素的堆叠顺序（哪个元素应该放在前面，或后面）

一个元素可以有正数或负数的堆叠顺序：

```css
img
{
    position:absolute;
    left:0px;
    top:0px;
    z-index:-1;
}
```

具有更高堆叠顺序的元素总是在较低的堆叠顺序元素的前面。

**注意**： 如果两个定位元素重叠，没有指定z - index，最后定位在HTML代码中的元素将被显示在最前面。

### --CSS 定位属性

"CSS" 列中的数字表示哪个CSS(CSS1 或者CSS2)版本定义了该属性。

| 属性       | 说明                                                         | 值                                                           | CSS  |
| :--------- | :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| bottom     | 定义了定位元素下外边距边界与其包含块下边界之间的偏移。       | `auto` `length` `%` `inherit`                                | 2    |
| clip       | 剪辑一个绝对定位的元素                                       | `shape` `auto` `inherit`                                     | 2    |
| cursor     | 显示光标移动到指定的类型                                     | `url` `auto` `crosshair` `default` `pointer` `move` `e-resize` `ne-resize ` `nw-resize` `n-resize` `se-resize` `sw-resize` `s-resize` `w-resize` `text` `wait` `help` | 2    |
| left       | 定义了定位元素左外边距边界与其包含块左边界之间的偏移。       | `auto` `length` `%` `inherit`                                | 2    |
| overflow   | 设置当元素的内容溢出其区域时发生的事情。                     | `auto` `hidden` `scroll` `visible` `inherit`                 | 2    |
| overflow-y | 指定如何处理顶部/底部边缘的内容溢出元素的内容区域            | `auto` `hidden` `scroll` `visible` `no-display` `no-content` | 2    |
| overflow-x | 指定如何处理右边/左边边缘的内容溢出元素的内容区域            | `auto` `hidden` `scroll` `visible` `no-display` `no-content` | 2    |
| position   | 指定元素的定位类型                                           | `absolute` `fixed` `relative` `static` `inherit`             | 2    |
| right      | 定义了定位元素右外边距边界与其包含块右边界之间的偏移。       | `auto` `length` `%` `inherit`                                | 2    |
| top        | 定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。 | `auto` `length` `%` `inherit`                                | 2    |
| z-index    | 设置元素的堆叠顺序                                           | `number` `auto` `inherit`                                    | 2    |

## 19.CSS  Overflow(布局)

CSS overflow 属性用于控制内容溢出元素框时显示的方式。

CSS overflow 属性可以控制内容溢出元素框时在对应的元素区间内添加滚动条。

overflow属性有以下值：

| 值      | 描述                                                     |
| :------ | :------------------------------------------------------- |
| visible | 默认值。内容不会被修剪，会呈现在元素框之外。             |
| hidden  | 内容会被修剪，并且其余内容是不可见的。                   |
| scroll  | 内容会被修剪，但是浏览器会显示滚动条以便查看其余的内容。 |
| auto    | 如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。 |
| inherit | 规定应该从父元素继承 overflow 属性的值。                 |

**注意**：overflow 属性只工作于指定高度的块元素上。

**注意**： 在 OS X Lion ( Mac 系统) 系统上，滚动条默认是隐藏的，使用的时候才会显示 (设置 "overflow:scroll" 也是一样的)。

### overflow: visible

默认情况下，overflow 的值为 visible， 意思是内容溢出元素框。

```css
div {
    width: 200px;
    height: 50px;
    background-color: #eee;
    overflow: visible;
}
```

## 20.CSS Float(浮动)

CSS 的 Float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。

Float（浮动），往往是用于图像，但它在布局时一样非常有用。

### 元素怎样浮动

元素的水平方向浮动，意味着元素只能左右移动而不能上下移动。

一个浮动元素会尽量向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。

浮动元素之后的元素将围绕它。

浮动元素之前的元素将不会受到影响。

如果图像是右浮动，下面的文本流将环绕在它左边：

```css
img
{
    float:right;
}
```

### 彼此相邻的浮动元素

如果你把几个浮动的元素放到一起，如果有空间的话，它们将彼此相邻。

在这里，我们对图片廊使用 float 属性：

```css
.thumbnail 
{
    float:left;
    width:110px;
    height:90px;
    margin:5px;
}
```

### 清除浮动 - 使用 clear

元素浮动之后，周围的元素会重新排列，为了避免这种情况，使用 clear 属性。

clear 属性指定元素两侧不能出现浮动元素。

使用 clear 属性往文本中添加图片廊：

```css
.text_line
{
    clear:both;
}
```

### --CSS 浮动属性

"CSS" 列中的数字表示不同的 CSS 版本（CSS1 或 CSS2）定义了该属性。

| 属性  | 描述                               | 值                                     | CSS  |
| :---- | :--------------------------------- | :------------------------------------- | :--- |
| clear | 指定不允许元素周围有浮动元素。     | `left` `right` `both` `none` `inherit` | 1    |
| float | 指定一个盒子（元素）是否可以浮动。 | `left` `right` `none` `inherit`        | 1    |

## 21.CSS对齐

### 元素居中对齐

要水平居中对齐一个元素(如 `<div>`), 可以使用 **`margin: auto;`**。

设置到元素的宽度将防止它溢出到容器的边缘。

元素通过指定宽度，并将两边的空外边距平均分配：

```css
.center {
    margin: auto;
    width: 50%;
    border: 3px solid green;
    padding: 10px;
}
```

**注意**： 如果没有设置 **width** 属性(或者设置 100%)，居中对齐将不起作用。

### 文本居中对齐

如果仅仅是为了文本在元素内居中对齐，可以使用 **`text-align: center;`**

```css
.center {
    text-align: center;
    border: 3px solid green;
}
```

### 图片居中对齐

要让图片居中对齐, 可以使用 **`margin: auto;`** 并将它放到 **`块`** 元素中:

```css
img {
    display: block;
    margin: auto;
    width: 40%;
}
```

### 左右对齐 - 使用定位方式

我们可以使用 **`position: absolute;`** 属性来对齐元素:

```css
.right {
    position: absolute;
    right: 0px;
    width: 300px;
    border: 3px solid #73AD21;
    padding: 10px;
}
```

注释：绝对定位元素会被从正常流中删除，并且能够交叠元素。

**提示**： 当使用 **`position`** 来对齐元素时, 通常 **`<body>`** 元素会设置 **`margin`** 和 **`padding`** 。 这样可以避免在不同的浏览器中出现可见的差异。

当使用 position 属性时，IE8 以及更早的版本存在一个问题。如果容器元素（在我们的案例中是 `<div class="container">`）设置了指定的宽度，并且省略了 !DOCTYPE 声明，那么 IE8 以及更早的版本会在右侧增加 17px 的外边距。这似乎是为滚动条预留的空间。当使用 position 属性时，请始终设置 !DOCTYPE 声明：

```css
body {
    margin: 0;
    padding: 0;
}
 
.container {
    position: relative;
    width: 100%;
}
 
.right {
    position: absolute;
    right: 0px;
    width: 300px;
    background-color: #b0e0e6;
}
```

### 左右对齐 - 使用 float 方式

我们也可以使用 **`float`** 属性来对齐元素:

```css
.right {
    float: right;
    width: 300px;
    border: 3px solid #73AD21;
    padding: 10px;
}
```

当像这样对齐元素时，对 `<body>` 元素的外边距和内边距进行预定义是一个好主意。这样可以避免在不同的浏览器中出现可见的差异。

> 注意：如果子元素的高度大于父元素，且子元素设置了浮动，那么子元素将溢出，这时候你可以使用 "**clearfix**(清除浮动)" 来解决该问题。

我们可以在父元素上添加 overflow: auto; 来解决子元素溢出的问题:

```css
.clearfix {
    overflow: auto;
}
```

当使用 float 属性时，IE8 以及更早的版本存在一个问题。如果省略 !DOCTYPE 声明，那么 IE8 以及更早的版本会在右侧增加 17px 的外边距。这似乎是为滚动条预留的空间。当使用 float 属性时，请始终设置 !DOCTYPE 声明：

```css
body {
    margin: 0;
    padding: 0;
}
 
.right {
    float: right;
    width: 300px;
    background-color: #b0e0e6;
}
```

### 垂直居中对齐 - 使用 padding

CSS 中有很多方式可以实现垂直居中对齐。 一个简单的方式就是头部顶部使用 **`padding`**:

```css
.center {
    padding: 70px 0;
    border: 3px solid green;
}
```

如果要水平和垂直都居中，可以使用 **`padding`** 和 **`text-align: center`**:

```css
.center {
    padding: 70px 0;
    border: 3px solid green;
    text-align: center;
}
```

### 垂直居中 - 使用 line-height

```css
.center {
    line-height: 200px;
    height: 200px;
    border: 3px solid green;
    text-align: center;
}
 
/* 如果文本有多行，添加以下代码: */
.center p {
    line-height: 1.5;
    display: inline-block;
    vertical-align: middle;
}
```

### 垂直居中 - 使用 position 和 transform

除了使用 **`padding`** 和 **`line-height`** 属性外,我们还可以使用 **`transform`** 属性来设置垂直居中:

```css
.center { 
    height: 200px;
    position: relative;
    border: 3px solid green; 
}
 
.center p {
    margin: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```

## 22.CSS 组合选择符

> 组合选择符说明了两个选择器之间的关系。

CSS组合选择符包括各种简单选择符的组合方式。

在 CSS3 中包含了四种组合方式:

- 后代选择器(以空格 ` ` 分隔)
- 子元素选择器(以大于 **`>`** 号分隔）
- 相邻兄弟选择器（以加号 **`+`** 分隔）
- 普通兄弟选择器（以波浪号 **`～`** 分隔）

### 后代选择器

后代选择器用于选取某元素的后代元素。

以下实例选取所有 `<p>` 元素插入到 `<div>` 元素中: 

```css
div p
{
  background-color:yellow;
}
```

### 子元素选择器

与后代选择器相比，子元素选择器（Child selectors）只能选择作为某元素直接/一级子元素的元素。

以下实例选择了`<div>`元素中所有直接子元素 `<p>` ：

```css
div>p
{
  background-color:yellow;
}
```

### 相邻兄弟选择器

相邻兄弟选择器（Adjacent sibling selector）可选择紧接在另一元素后的元素，且二者有相同父元素。

如果需要选择紧接在另一个元素后的元素，而且二者有相同的父元素，可以使用相邻兄弟选择器（Adjacent sibling selector）。

以下实例选取了所有位于 `<div>` 元素后的第一个 `<p>` 元素:

```css
div+p
{
  background-color:yellow;
}
```

### 后续兄弟选择器

后续兄弟选择器选取所有指定元素之后的相邻兄弟元素。

以下实例选取了所有 `<div>` 元素之后的所有相邻兄弟元素 `<p>` :

```css
div~p
{
  background-color:yellow;
}
```

