# 一、基础

## 1.注释和结束符

注释的两种写法

```javascript
/这是一行文字/
/*这是多行文字
这是多行文字
*/
```

结束符`;`可写可不写，最好不写。

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

如需使用外部文件，请在 `<script>` 标签的 "`src`" 属性中设置该 .js 文件：

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

