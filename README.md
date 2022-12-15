# JavaScript- 初级学习笔记 概述



JavaScript 用来实时更新网页中的内容，例如从服务器获取数据并更新到网页中，修改某些标签的样式或其中的内容等

ECMA-262 标准主要规定了这门语言的语法、类型、语句、关键字、保留字、操作符、对象等几个部分

目前 ECMAScript 的最新版是 ECMAScript6（简称 'ES6'）



一个完整的 JavaScript 是由以下三个部分组成：

- 核心 (ECMA Script)：提供语言的语法和基本对象

- 文档对象模型 (DOM)：提供处理网页内容的方法和接口

- 浏览器对象模型 (BOM)：提供与浏览器进行交互的方法和接口



JS的特点:

`解释型`语言

- 使用JS编写的代码不需要编译，可以直接运行

`弱类型`

- 弱类型可以理解成，对使用的数据类型没有严格的要求，代表我们可以将一个变量初始化为任意类型，也可以随时改变这个变量的类型。

`动态性`

- 不需要借助 Web 服务器就可以对用户的输入做出响应，例如我们在访问一个网页时，通过滑鼠在网页中进行点击或滚动窗口时，JS 可以直接对这些事件做出响应。



Node.js简介

09年以前的JS只能运行在浏览器中，自从有了 Node.js 以后，JS 就可以脱离浏览器，像其它编程语言一样直接在电脑上使用。

Node.js 不是一门新的编程语言，也不是一个 JS 框架，它是一套 JS 运行环境，用来支持 JS 代码的执行。<br>
用编程术语来讲，Node.js 是一个 JS ==运行时（Runtime）==。



现在的 JavaScript 除了用于 Web 前端编程（网页编程），还能干很多事情，比如：

- 开发网站后台，这原本是 PHP、Java、Python、Ruby 等编程语言擅长的；
- 开发 GUI 程序，也就是我们常说的带界面的电脑软件，比如 QQ、360、迅雷等；
- 手机 APP，包括 Android APP、iOS APP；
- CLI 工具，也就是不带界面的命令行程序。
***

## #1 运行时(Runtime)：

所谓运行时，就是程序在运行期间需要依赖的一系列组件或者工具；把这些工具和组件打包在一起提供给程序员，程序员就能运行自己编写的代码了。

对于 JS 来说，它在运行期间需要依赖以下组件：

- `解释器`

JS 是一种脚本语言，需要一边解释一边运行，用到哪些源代码就编译哪些源代码，整个过程由解释器完成。没有解释器的话，JavaScript 只是一堆纯文本文件，不能被电脑识别。

- `标准库`

在 JS 代码中会调用一些内置函数，这些函数不是我们自己编写的，而是标准库自带的。

- `本地模块`

所谓本地模块，就是已经被提前编译好的模块，它们是二进制文件，和可执行文件在内部结构上没有什么区别，只是不能单独运行而已。这些本地模块其实就是动态链接库（在 Windows 下是 .dll 文件）



## JS 执行序：

浏览器在解析 HTML 文档时，将根据文档流从上到下逐行解析和显示。JavaScript 代码也是 HTML 文档的组成部分，因此 JavaScript 脚本的执行顺序也是根据 <&nbsp;script> 标签的位置来确定的。



## 标识符(Identifier)：

- 第一个字符必须是`字母`、`下划线（_）`或`美元符号（$）`。
- 除了第一个字符外，其他位置可以使用 Unicode 字符。一般建议仅使用 ASCII 编码的字母，不建议使用双字节的字符。
- 不能与 JavaScript 关键字、保留字重名。
- 可以使用 Unicode 转义序列。例如，字符 a 可以使用“\u0061”表示。



## 区分大小写

建议采用小写编写代码，特殊情况另议 如:

### 1.构造函数的首字母建议大写，构造函数不同于普通函数

下面示例调用预定义的构造函数 Date()，创建一个时间对象，然后把时间对象转换为字符串显示出来。

```js
d = new Date(); //获取当前日期与时间
document.write(d.toString()); //显示日期
```

### 2.如果标识符由多个单词组合而成，则推荐使用驼峰命名法

```js
typeof();
printEmployeePaychecks();
//print employee paychecks
```

以上不强制，但约定成俗。



## 注释规则

`//` 单行注释

`/* */` 多行注释


