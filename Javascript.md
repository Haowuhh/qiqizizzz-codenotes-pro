# 一、基础

## 1.JavaScript 基础

**1.对代码行进行折行**

您可以在文本字符串中使用反斜杠对代码行进行换行。下面的例子会正确地显示：

```js
document.write("你好 \
世界!");
```

**知识点**：JavaScript 是脚本语言，浏览器会在读取代码时，逐行地执行脚本代码。而对于传统编程来说，会在执行前对所有代码进行编译。

**2.注释和结束符**

注释的两种写法

```javascript
/这是一行文字/
/*这是多行文字
这是多行文字
*/
```

结束符`;`可写可不写，最好不写。

**3.typeof**

可以返回该字段的类型

```js
document.getElementById("demo").innerHTML = "carName 的类型是：" +  typeof "你好";
```

**4.作用域**

你的全局变量，或者函数，可以覆盖 window 对象的变量或者函数。 局部变量，包括 window 对象可以覆盖全局变量和函数。

在 JavaScript 中，函数内部的局部变量通常不可以直接被外部作用域访问，但有几种方式可以将函数内的局部变量暴露给外部作用域，具体如下：

- **通过全局对象：**在函数内部，可以通过将局部变量赋值给 window 对象的属性来使其成为全局可访问的。例如，使用 **`window.a = a;`** 语句，可以在函数外部通过 **`window.a`** 访问到这个局部变量的值。
- **定义全局变量：**在函数内部不使用 **var、let** 或 **const** 等关键字声明变量时，该变量会被视为全局变量，从而可以在函数外部访问。但这种做法通常不推荐，因为它可能导致意外的副作用和代码难以维护。
- **返回值：**可以通过在函数内部使用 **return** 语句返回局部变量的值，然后在函数外部接收这个返回值。这样，虽然局部变量本身不会被暴露，但其值可以通过函数调用传递到外部。
- **闭包：**JavaScript 中的闭包特性允许内部函数访问外部函数的局部变量。即使外部函数执行完毕后，其局部变量仍然可以被内部函数引用。
- **属性和方法：**定义在全局作用域中的变量和函数都会变成 window 对象的属性和方法，因此可以在调用时省略 window，直接使用变量名或函数名。

**5.字符串长度**

可以使用内置属性 **length** 来计算字符串的长度：

```js
<script>
var txt = "Hello World!";
document.write("<p>" + txt.length + "</p>");
var txt="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
document.write("<p>" + txt.length + "</p>");
</script>
```

**6.特殊字符**

在 JavaScript 中，字符串写在单引号或双引号中。

因为这样，以下实例 JavaScript 无法解析：

```js
 "We are the so-called "Vikings" from the north."
```

字符串 "We are the so-called " 被截断。

如何解决以上的问题呢？可以使用反斜杠 (\) 来转义 "Vikings" 字符串中的双引号，如下:

```js
 "We are the so-called \"Vikings\" from the north."
```

 反斜杠是一个**转义字符**。 转义字符将特殊字符转换为字符串字符：

转义字符 (\) 可以用于转义撇号，换行，引号，等其他特殊字符。

下表中列举了在字符串中可以使用转义字符转义的特殊字符：

| 代码 | 输出        |
| :--- | :---------- |
| `\'` | 单引号      |
| `\"` | 双引号      |
| `\\` | 反斜杠      |
| `\n` | 换行        |
| `\r` | 回车        |
| `\t` | tab(制表符) |
| `\b` | 退格符      |
| `\f` | 换页符      |

**7.字符串相关函数**

## 字符串方法

| 方法                  | 描述                                                         |
| :-------------------- | :----------------------------------------------------------- |
| `charAt()`            | 返回指定索引位置的字符                                       |
| `charCodeAt()`        | 返回指定索引位置字符的 Unicode 值                            |
| `concat()`            | 连接两个或多个字符串，返回连接后的字符串                     |
| `fromCharCode()`      | 将 Unicode 转换为字符串                                      |
| `indexOf()`           | 返回字符串中检索指定字符第一次出现的位置                     |
| `lastIndexOf()`       | 返回字符串中检索指定字符最后一次出现的位置                   |
| `localeCompare()`     | 用本地特定的顺序来比较两个字符串                             |
| `match()`             | 找到一个或多个正则表达式的匹配                               |
| `replace()`           | 替换与正则表达式匹配的子串                                   |
| `search()`            | 检索与正则表达式相匹配的值                                   |
| `slice()`             | 提取字符串的片断，并在新的字符串中返回被提取的部分           |
| `split()`             | 把字符串分割为子字符串数组                                   |
| `substr()`            | 从起始索引号提取字符串中指定数目的字符                       |
| `substring()`         | 提取字符串中两个指定的索引号之间的字符                       |
| `toLocaleLowerCase()` | 根据主机的语言环境把字符串转换为小写，只有几种语言（如土耳其语）具有地方特有的大小写映射 |
| `toLocaleUpperCase()` | 根据主机的语言环境把字符串转换为大写，只有几种语言（如土耳其语）具有地方特有的大小写映射 |
| `toLowerCase()`       | 把字符串转换为小写                                           |
| `toString()`          | 返回字符串对象值                                             |
| `toUpperCase()`       | 把字符串转换为大写                                           |
| `trim()`              | 移除字符串首尾空白                                           |
| `valueOf()`           | 返回某个字符串对象的原始值                                   |

## 2.JavaScript用法

HTML 中的 `Javascript` 脚本代码必须位于 **`<script>`** 与 **`</script>`** 标签之间。

`Javascript` 脚本代码可被放置在 HTML 页面的 **`<body>`** 和 **`<head>`** 部分中。

**1.`<script> `标签**

如需在 HTML 页面中插入 JavaScript，请使用 `<script>` 标签。

`<script>` 和 `</script>` 会告诉 JavaScript 在何处开始和结束。

`<script>` 和 `</script>` 之间的代码行包含了 JavaScript:

```javascript
<script> alert("我的第一个 JavaScript"); </script>
```

**2.`<body>` 中的 JavaScript**

在本例中，JavaScript 会在页面加载时向 HTML 的 `<body>` 写文本：

```javascript
<!DOCTYPE html>
<html>
<body>
.
.
<script>
document.write("<h1>这是一个标题</h1>");
document.write("<p>这是一个段落</p>");
</script>
.
.
</body>
</html>
```

> 您只能在 HTML 输出流中使用 **`document.write`**。 如果您在文档已加载后使用它（比如在函数中），会覆盖整个文档。

**3.`head`中的 JavaScript**

也可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。

外部 JavaScript 文件的文件扩展名是 `.js`。

如需使用外部文件，请在 `<script>` 标签的 "`src`" 属性中设置该 `.js` 文件：

```javascript
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

**4.`<head>` 中的 JavaScript 函数**

在本例中，我们把一个 JavaScript 函数放置到 HTML 页面的 `<head>` 部分。

该函数会在点击按钮时被调用：

```javascript
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</head>
<body>
<h1>我的 Web 页面</h1>
<p id="demo">一个段落</p>
<button type="button" onclick="myFunction()">尝试一下</button>
</body>
</html>
```

**5.`<body>` 中的 JavaScript 函数**

在本例中，我们把一个 JavaScript 函数放置到 HTML 页面的 `<body>` 部分。

该函数会在点击按钮时被调用：

```javascript
<!DOCTYPE html>
<html>
<body>
<h1>我的 Web 页面</h1>
<p id="demo">一个段落</p>
<button type="button" onclick="myFunction()">尝试一下</button>
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</body>
</html>
```

**6.外部的 JavaScript**

也可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。

外部 JavaScript 文件的文件扩展名是` .js`。

如需使用外部文件，请在 `<script>` 标签的 "src" 属性中设置该` .js `文件：

```js
<!DOCTYPE html>
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```

你可以将脚本放置于 `<head>` 或者 `<body>`中，放在 `<script> `标签中的脚本与外部引用的脚本运行效果完全一致。

myScript.js 文件代码如下：

```js
function myFunction()
{    
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
```

> 外部脚本不能包含 `<script>` 标签。

## 3.JavaScript 输出

JavaScript 没有任何打印或者输出的函数。

**JavaScript 显示数据**

JavaScript 可以通过不同的方式来输出数据：

- 使用 **`window.alert()`** 弹出警告框。
- 使用 **`document.write()`** 方法将内容写到 HTML 文档中。
- 使用 **`innerHTML`** 写入到 HTML 元素。
- 使用 **`console.log()`** 写入到浏览器的控制台。

------

### **1.使用 `window.alert()`**

你可以弹出警告框来显示数据：

```js
<!DOCTYPE html>
<html>
<body>
<h1>我的第一个页面</h1><p>我的第一个段落。</p>
	
<script>window.alert(5 + 6);
</script>

</body>
</html>
```

### **2.使用`document.write()`**

```js
<!DOCTYPE html>
<html>
<body>

<h1>我的第一个 Web 页面</h1>

<p>我的第一个段落。</p>

<script>
document.write(Date());
</script>

</body>
</html>
```

> 使用 `document.write()` 可以向文档写入内容。

> 如果在文档已完成加载后执行 `document.write`，整个 HTML 页面将被覆盖。

**例如：**

```js
<!DOCTYPE html>
<html>
<body>
<h1>我的第一个 Web 页面</h1>
<p>我的第一个段落。</p>
<button onclick="myFunction()">点我</button>
<script>
function myFunction() {
   	document.write(Date());
}
</script>
</body>
</html>
```

### **3.使用 `innerHTML`**

如需从 JavaScript 访问某个 HTML 元素，您可以使用 `document.getElementById(id)` 方法。

请使用 "id" 属性来标识 HTML 元素，并 `innerHTML` 来获取或插入元素内容：

```js
<!DOCTYPE html><html>
<body>

<h1>我的第一个 Web 页面</h1>

<p id="demo">我的第一个段落</p>

<script>
	document.getElementById("demo").innerHTML = "段落已修改。";
</script>

</body>
</html>
```

以上 JavaScript 语句（在 `<script>` 标签中）可以在 web 浏览器中执行：

**`document.getElementById("demo")`** 是使用 id 属性来查找 HTML 元素的 JavaScript 代码 。

**`innerHTML` = "段落已修改。"** 是用于修改元素的 HTML 内容(`innerHTML`)的 JavaScript 代码。

**4.使用console.log()**

如果您的浏览器支持调试，你可以使用 **console.log()** 方法在浏览器中显示 JavaScript 值。

浏览器中使用 F12 来启用调试模式， 在调试窗口中点击 "Console" 菜单。

```js
<!DOCTYPE html>
<html>
<body>
<h1>我的第一个 Web 页面</h1>
<script>
a = 5;
b = 6;
c = a + b;
console.log(c);
</script>

</body>
</html>
```

## 4.JavaScript 关键字

JavaScript 关键字用于标识要执行的操作。

和其他任何编程语言一样，JavaScript 保留了一些关键字为自己所用。

**var** 关键字告诉浏览器创建一个新的变量：

```js
var x = 5 + 6;
var y = x * 10;
```

JavaScript 同样保留了一些关键字，这些关键字在当前的语言版本中并没有使用，但在以后 JavaScript 扩展中会用到。

以下是 JavaScript 中最重要的保留关键字（按字母顺序）：

| abstract | else       | instanceof | super        |
| -------- | ---------- | ---------- | ------------ |
| boolean  | enum       | int        | switch       |
| break    | export     | interface  | synchronized |
| byte     | extends    | let        | this         |
| case     | false      | long       | throw        |
| catch    | final      | native     | throws       |
| char     | finally    | new        | transient    |
| class    | float      | null       | true         |
| const    | for        | package    | try          |
| continue | function   | private    | typeof       |
| debugger | goto       | protected  | var          |
| default  | if         | public     | void         |
| delete   | implements | return     | volatile     |
| do       | import     | short      | while        |
| double   | in         | static     | with         |



## 5.JavaScript 对象

**1.创建对象**

对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：

```js
var person={firstname:"John", lastname:"Doe", id:5566};
```

上面例子中的对象 (person) 有三个属性：`firstname`、`lastname` 以及 `id`。

空格和折行无关紧要。声明可横跨多行：

```js
var person={
firstname : "John",
lastname : "Doe",
id    : 5566
};
```

对象属性有两种寻址方式：

```js
<script>
var person=
{
	firstname : "John",
	lastname  : "Doe",
	id        :  5566
};
document.write(person.lastname + "<br>");           // 第一种
document.write(person["lastname"] + "<br>");        //第二种
</script>
```

**2.创建对象方法**

```js
methodName : function() {
    // 代码 
}
```

实例：

```js
<script>
var person = {
    name:"qiqizi",
  	age:18,
  	id:720,
    qiqizi : function() 
	{
       return this.firstName + " " + this.lastName;
    }
};
document.getElementById("demo").innerHTML = person.qiqizi();   //返回qiqizi 18 720
document.getElementById("demo").innerHTML = person.qiqizi;    
/*返回函数的定义 即function() { return this.name+" "+this.age+" "+this.id; }*/
</script>
```

## 6.JavaScript 函数

**1.函数基本语法**

函数就是包裹在花括号中的代码块，前面使用了关键词 **`function`**：

```js
function functionname()
{
  // 执行代码
}
```

当调用该函数时，会执行函数内的代码。

可以在某事件发生时直接调用函数（比如当用户点击按钮时），并且可由 JavaScript 在任何位置进行调用。

> JavaScript 对大小写敏感。关键词 function 必须是小写的，并且必须以与函数名称相同的大小写来调用函数。

**2.调用带参数的函数**

在调用函数时，您可以向其传递值，这些值被称为参数。

这些参数可以在函数中使用。

您可以发送任意多的参数，由逗号 (,) 分隔：

```js
myFunction(argument1,argument2)
```

当您声明函数时，请把参数作为变量来声明：

```js
function myFunction(var1,var2)
{
	代码
}
```

变量和参数必须以一致的顺序出现。第一个变量就是第一个被传递的参数的给定的值，以此类推。

**实例：**

```js
<p>点击这个按钮，来调用带参数的函数。</p>
<button onclick="myFunction('qiqizi','zzz')">点击这里</button>
<script>
function myFunction(name,job){
    alert("Welcome " + name + ", the " + job);
}
</script>
```

## 7.JavaScript 事件

HTML 事件是发生在 HTML 元素上的事情。

当在 HTML 页面中使用 JavaScript 时， JavaScript 可以触发这些事件。

HTML 事件可以是浏览器行为，也可以是用户行为。

以下是 HTML 事件的实例：

- HTML 页面完成加载
- HTML input 字段改变时
- HTML 按钮被点击

通常，当事件发生时，你可以做些事情。

在事件触发时 JavaScript 可以执行一些代码。

HTML 元素中可以添加事件属性，使用 JavaScript 代码来添加 HTML 元素。

**1.语法**

单引号:

```js
<some-HTML-element some-event='JavaScript 代码'>
```

双引号:

```js
<some-HTML-element some-event="JavaScript 代码">
```

**2.实例**

> **1.修改`<p>`标签中的字段**

在以下实例中，按钮元素中添加了 onclick 属性 (并加上代码):

```js
<body>

<button onclick="getElementById('demo').innerHTML=Date()">现在的时间是?</button>
<p id="demo"></p>

</body>
//以上实例中，JavaScript 代码将修改 id="demo" 元素的内容。
```

> **2.修改按钮`<button>`内部的字段**

```js
<body>

<button onclick="this.innerHTML=Date()">现在的时间是?</button>

</body>
```

> **3.调用函数执行事件**

```js
<body>

<p>点击按钮执行 <em>displayDate()</em> 函数.</p>
<button onclick="displayDate()">点这里</button>
<script>
function displayDate(){
	document.getElementById("demo").innerHTML=Date();
}
</script>
<p id="demo"></p>

</body>
```

**3.更多**

事件可以用于处理表单验证，用户输入，用户行为及浏览器动作:

- 页面加载时触发事件
- 页面关闭时触发事件
- 用户点击按钮执行动作
- 验证用户输入内容的合法性
- 等等 ...

可以使用多种方法来执行 JavaScript 事件代码：

- HTML 事件属性可以直接执行 JavaScript 代码
- HTML 事件属性可以调用 JavaScript 函数
- 你可以为 HTML 元素指定自己的事件处理程序
- 你可以阻止事件的发生。
- 等等 ...

### 常见的HTML事件

下面是一些常见的HTML事件的列表:

| 事件          | 描述                                 |
| :------------ | :----------------------------------- |
| `onchange`    | HTML 元素改变                        |
| `onclick`     | 用户点击 HTML 元素                   |
| `onmouseover` | 鼠标指针移动到指定的元素上时发生     |
| `onmouseout`  | 用户从一个 HTML 元素上移开鼠标时发生 |
| `onkeydown`   | 用户按下键盘按键                     |
| `onload`      | 浏览器已完成页面的加载               |

## 8.JavaScript字符串模版
