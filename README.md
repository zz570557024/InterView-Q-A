# 准备一份面经

## TypeScript和ES6的区别

TypeScript是一种由微软开发的自由和开源的编程语言。而且本质上向这个语言添加了可选的静态类型和基于类的面向对象编程。安德斯·海尔斯伯格，C#的首席架构师，已工作于TypeScript的开发。TypeScript 是 JavaScript 的超集。TypeScript是为大型应用之开发而设计。TypeScript 是JavaScript 类型化子集，它会被编译成原生的JavaScript。
TypeScript 不是「强类型」，是「静态类型检查」的「弱类型」。

TS最大的价值是引入了 接口、类、继承的编程思想，TypeScript 在 ES2015 之外还提供了

1.类型

2.接口

3.未来的 ES2016+ 特性 (比如注解/装饰器以及异步/等待)

我们可以使用类似 Gulp，Grunt，WebPack，SystemJS 和 JSPM 这些工具反编译成 Babel 或者 TypeScript。

ES2015 是 ES5 的改进。

## 如何理解html语义化

1. 什么是HTML语义化？
根据内容的结构化（内容语义化），选择合适的标签（代码语义化）便于开发者阅读和写出更优雅的代码的同时让浏览器的爬虫和机器很好地解析。

2. 为什么要语义化？
* 为了在没有CSS的情况下，页面也能呈现出很好地内容结构、代码结构:为了裸奔时好看；
* 用户体验：例如title、alt用于解释名词或解释图片信息、label标签的活用；
* 有利于SEO：和搜索引擎建立良好沟通，有助于爬虫抓取更多的有效信息：爬虫依赖于标签来确定上下文和各个关键字的权重；
* 方便其他设备解析（如屏幕阅读器、盲人阅读器、移动设备）以意义的方式来渲染网页；
* 便于团队开发和维护，语义化更具可读性，是下一步吧网页的重要动向，遵循W3C标准的团队都遵循这个标准，可以减少差异化。

3. 写HTML代码时应注意什么？

* 尽可能少的使用无语义的标签div和span；
* 在语义不明显时，既可以使用div或者p时，尽量用p, 因为p在默认情况下有上下间距，对兼容特殊终端有利；
* 不要使用纯样式标签，如：b、font、u等，改用css设置。
* 需要强调的文本，可以包含在strong或者em标签中（浏览器预设样式，能用CSS指定就不用他们），strong默认样式是加粗（不要用b），em是斜体（不用i）；
* 使用表格时，标题要用caption，表头用thead，主体部分用tbody包围，尾部用tfoot包围。表头和一般单元格要区分开，表头用th，单元格用td；
* 表单域要用fieldset标签包起来，并用legend标签说明表单的用途；
* 每个input标签对应的说明文本都需要使用label标签，并且通过为input设置id属性，在lable标签中设置for=someld来让说明文本和相对应的input关联起来。

## HTML5新增了哪些语义标签

- section
`表示文档中的一个区域（或节），比如，内容中的一个专题组，一般来说会有包含一个标题（heading）。一般通过是否包含一个标题 (<h1>-<h6> element) 作为子节点来辨识每一个<section>。一般来说，一个 <section> 应该出现在文档大纲中。`
-artical
`<article>元素表示文档、页面、应用或网站中的独立结构，其意在成为可独立分配的或可复用的结构，如在发布中，它可能是论坛帖子、杂志或新闻文章、博客、用户提交的评论、交互式组件，或者其他独立的内容项目。`
- canvas
`<canvas> 标签定义图形，比如图表和其他图像。
<canvas> 标签只是图形容器，您必须使用脚本来绘制图形。`

`<canvas> 标记和 SVG 以及 VML 之间的差异
<canvas> 标记和 SVG 以及 VML 之间的一个重要的不同是，<canvas> 有一个基于 JavaScript 的绘图 API，而 SVG 和 VML 使用一个 XML 文档来描述绘图。
这两种方式在功能上是等同的，任何一种都可以用另一种来模拟。从表面上看，它们很不相同，可是，每一种都有强项和弱点。例如，SVG 绘图很容易编辑，只要从其描述中移除元素就行。
要从同一图形的一个 <canvas> 标记中移除元素，往往需要擦掉绘图重新绘制它。`

## 垂直居中的实现
* 方法1：table-cell

html结构：

`<div class="box box1">
        <span>垂直居中</span>
</div>`
css：

.box1{
    display: table-cell;
    vertical-align: middle;
    text-align: center;        
}

* 方法2：display:flex

.box2{
    display: flex;
    justify-content:center;
    align-items:Center;
}

* 方法3：绝对定位和负边距
.box3{position:relative;}
.box3 span{
    position: absolute;
    width:100px;
    height: 50px;
    top:50%;
    left:50%;
    margin-left:-50px;
    margin-top:-25px;
    text-align: center;
}

## React和Vue的区别

React 和 Vue 有许多相似之处，它们都有：

* 使用 Virtual DOM
* 提供了响应式 (Reactive) 和组件化 (Composable) 的视图组件。
* 将注意力集中保持在核心库，而将其他功能如路由和全局状态管理交给相关的库。

区别：

* 运行时性能
在 Vue 应用中，组件的依赖是在渲染过程中自动追踪的，所以系统能精确知晓哪个组件确实需要被重渲染。

* HTML & CSS/模板语法 VS JSX
Vue 的整体思想是拥抱经典的 Web 技术，并在其上进行扩展。
任何合乎规范的 HTML 都是合法的 Vue 模板
Vue 设置样式的默认方法是单文件组件里类似 style 的标签。单文件组件让你可以在同一个文件里完全控制 CSS，将其作为组件代码的一部分。

* 规模
两者另一个重要差异是，Vue 的路由库和状态管理库都是由官方维护支持且与核心库同步更新的。React 则是选择把这些问题交给社区维护，因此创建了一个更分散的生态系统。但相对的，React 的生态系统相比 Vue 更加繁荣。

* 原生渲染
React Native 能使你用相同的组件模型编写有本地渲染能力的 APP (iOS 和 Android)。能同时跨多平台开发，对开发者是非常棒的。

Weex 允许你使用 Vue 语法开发不仅仅可以运行在浏览器端，还能被用于开发 iOS 和 Android 上的原生应用的组件。

*创造前端的富应用
Virtual DOM
改变真实的DOM状态远比改变一个JavaScript对象的花销要大得多。
当有变化产生时，一个新的Virtual DOM对象会被创建并计算新旧Virtual DOM之间的差别。之后这些差别会应用在真实的DOM上。*

## localStorage和cookie的区别
Web Storage的概念和cookie相似，区别是它是为了更大容量存储设计的，cookie的大小是受限的，并且每次请求一个新的页面的时候cookie都会被发送过去，这样无形中浪费了带宽，另外cookie还需要指定作用域，不可跨域调用。 
除此之外，web storage拥有setItem,getItem,removeItem,clear等方法，不像cookie需要前端开发者自己封装setCookie，getCookie。 
但是cookie也是不可或缺的，cookie的作用是与服务器进行交互，作为http规范的一部分而存在的，而web Storage仅仅是为了在本地“存储”数据而生 
sessionStorage、localStorage、cookie都是在浏览器端存储的数据，其中sessionStorage的概念很特别，引入了一个“浏览器窗口”的概念，sessionStorage是在同源的同窗口中，始终存在的数据，也就是说只要这个浏览器窗口没有关闭，即使刷新页面或进入同源另一个页面，数据仍然存在，关闭窗口后，sessionStorage就会被销毁，同时“独立”打开的不同窗口，即使是同一页面，sessionStorage对象也是不同的

Web Storage带来的好处： 
1、减少网络流量：一旦数据保存在本地之后，就可以避免再向服务器请求数据，因此减少不必要的数据请求，减少数

据在浏览器和服务器间不必要的来回传递 
2、快速显示数据：性能好，从本地读数据比通过网络从服务器上获得数据快得多，本地数据可以及时获得，再加上网

页本身也可以有缓存，因此整个页面和数据都在本地的话，可以立即显示 
3、临时存储：很多时候数据只需要在用户浏览一组页面期间使用，关闭窗口后数据就可以丢弃了，这种情况使用sessionStorage非常方便

## HTTP状态码/200和304实现缓存的区别

客户端在请求一个文件的时候，发现自己缓存的文件有 Last Modified ，那么在请求中会包含 If Modified Since ，这个时间就是缓存文件的 Last Modified 。因此，如果请求中包含 If Modified Since，就说明已经有缓存在客户端。服务端只要判断这个时间和当前请求的文件的修改时间就可以确定是返回 304 还是 200 。

第一次访问 200
按F5刷新（第二次访问） 304
按Ctrl+F5强制刷新 200

## 实现跨域的方式

**同源策略**
只有当协议、端口、和域名都相同的页面，则两个页面具有相同的源。只要网站的 协议名protocol、 主机host、 端口号port 这三个中的任意一个不同，网站间的数据请求与传输便构成了跨域调用，会受到同源策略的限制。
同源策略限制从一个源加载的文档或脚本如何与来自另一个源的资源进行交互。这是一个用于隔离潜在恶意文件的关键的安全机制。浏览器的同源策略，出于防范跨站脚本的攻击，禁止客户端脚本（如 JavaScript）对不同域的服务进行跨站调用（通常指使用XMLHttpRequest请求）。

1. nginx反向代理
2. JSONP跨域
JSONP是一种跨域数据交互的协议，使用JSONP方法获取到的仍然是json格式的数据。
说白了，用JSON来传数据，靠JSONP来跨域。

`JSONP（JSON with Padding）是数据格式JSON的一种“使用模式”，可以让网页从别的网域要数据。根据 XmlHttpRequest 对象受到同源策略的影响，而利用 <script>元素的这个开放策略，网页可以得到从其他来源动态产生的JSON数据，而这种使用模式就是所谓的 JSONP。用JSONP抓到的数据并不是JSON，而是任意的JavaScript，用 JavaScript解释器运行而不是用JSON解析器解析。所有，通过Chrome查看所有JSONP发送的Get请求都是js类型，而非XHR。 `
缺点：

只能使用Get请求
不能注册success、error等事件监听函数，不能很容易的确定JSONP请求是否失败
JSONP是从其他域中加载代码执行，容易受到跨站请求伪造的攻击，其安全性无法确保

3. CORS
​ Cross-Origin Resource Sharing（CORS）跨域资源共享是一份浏览器技术的规范，提供了 Web 服务从不同域传来沙盒脚本的方法，以避开浏览器的同源策略，确保安全的跨域数据传输。现代浏览器使用CORS在API容器如XMLHttpRequest来减少HTTP请求的风险来源。与 JSONP 不同，CORS 除了 GET 要求方法以外也支持其他的 HTTP 要求。服务器一般需要增加如下响应头的一种或几种：

Access-Control-Allow-Origin: *
Access-Control-Allow-Methods: POST, GET, OPTIONS
Access-Control-Allow-Headers: X-PINGOTHER, Content-Type
Access-Control-Max-Age: 86400

跨域请求默认不会携带Cookie信息，如果需要携带，请配置下述参数：

"Access-Control-Allow-Credentials": true
// Ajax设置
"withCredentials": true

4. 代理

## HTTP 原理

超文本传输协议.

**URI和URL的区别**
URI，是uniform resource identifier，统一资源标识符，用来唯一的标识一个资源。
Web上可用的每种资源如HTML文档、图像、视频片段、程序等都是一个来URI来定位的
URI一般由三部组成：
①访问资源的命名机制
②存放资源的主机名
③资源自身的名称，由路径表示，着重强调于资源。
URL是uniform resource locator，统一资源定位器，它是一种具体的URI，即URL可以用来标识一个资源，而且还指明了如何locate这个资源。
URL是Internet上用来描述信息资源的字符串，主要用在各种WWW客户程序和服务器程序上，特别是著名的Mosaic。
采用URL可以用一种统一的格式来描述各种信息资源，包括文件、服务器的地址和目录等。URL一般由三部组成：
①协议(或称为服务方式)
②存有该资源的主机IP地址(有时也包括端口号)
③主机资源的具体地址。如目录和文件名等
URN，uniform resource name，统一资源命名，是通过名字来标识资源，比如`mailto:java-net@java.sun.com`。
URI是以一种抽象的，高层次概念定义统一资源标识，而URL和URN则是具体的资源标识的方式。URL和URN都是一种URI。笼统地说，每个 URL 都是 URI，但不一定每个 URI 都是 URL。这是因为 URI 还包括一个子类，即统一资源名称 (URN)，它命名资源但不指定如何定位资源。

状态代码有三位数字组成，第一个数字定义了响应的类别，共分五种类别:
1xx：指示信息--表示请求已接收，继续处理
2xx：成功--表示请求已被成功接收、理解、接受
3xx：重定向--要完成请求必须进行更进一步的操作
4xx：客户端错误--请求有语法错误或请求无法实现
5xx：服务器端错误--服务器未能实现合法的请求

**HTTP工作原理**

HTTP协议定义Web客户端如何从Web服务器请求Web页面，以及服务器如何把Web页面传送给客户端。HTTP协议采用了请求/响应模型。客户端向服务器发送一个请求报文，请求报文包含请求的方法、URL、协议版本、请求头部和请求数据。服务器以一个状态行作为响应，响应的内容包括协议的版本、成功或者错误代码、服务器信息、响应头部和响应数据。

以下是 HTTP 请求/响应的步骤：

1. 客户端连接到Web服务器
一个HTTP客户端，通常是浏览器，与Web服务器的HTTP端口（默认为80）建立一个TCP套接字连接。例如，`http://www.oakcms.cn`。

2. 发送HTTP请求
通过TCP套接字，客户端向Web服务器发送一个文本的请求报文，一个请求报文由请求行、请求头部、空行和请求数据4部分组成。

3. 服务器接受请求并返回HTTP响应
Web服务器解析请求，定位请求资源。服务器将资源复本写到TCP套接字，由客户端读取。一个响应由状态行、响应头部、空行和响应数据4部分组成。

4. 释放连接TCP连接
若connection 模式为close，则服务器主动关闭TCP连接，客户端被动关闭连接，释放TCP连接;若connection
 模式为keepalive，则该连接会保持一段时间，在该时间内可以继续接收请求;

5. 客户端浏览器解析HTML内容
客户端浏览器首先解析状态行，查看表明请求是否成功的状态代码。然后解析每一个响应头，响应头告知以下为若干字节的HTML文档和文档的字符集。客户端浏览器读取响应数据HTML，根据HTML的语法对其进行格式化，并在浏览器窗口中显示。

例如：在浏览器地址栏键入URL，按下回车之后会经历以下流程：

1. 浏览器向 DNS 服务器请求解析该 URL 中的域名所对应的 IP 地址;
2. 解析出 IP 地址后，根据该 IP 地址和默认端口 80，和服务器建立TCP连接;
3. 浏览器发出读取文件(URL 中域名后面部分对应的文件)的HTTP 请求，该请求报文作为 TCP
 三次握手的第三个报文的数据发送给服务器;
4. 服务器对浏览器请求作出响应，并把对应的 html 文本发送给浏览器;
5. 释放 TCP连接;
6. 浏览器将该 html 文本并显示内容; 

GET和POST请求的区别

你轻轻松松的给出了一个“标准答案”：


GET在浏览器回退时是无害的，而POST会再次提交请求。

 

GET产生的URL地址可以被Bookmark，而POST不可以。

 

GET请求会被浏览器主动cache，而POST不会，除非手动设置。

 

GET请求只能进行url编码，而POST支持多种编码方式。

 

GET请求参数会被完整保留在浏览器历史记录里，而POST中的参数不会被保留。

 

GET请求在URL中传送的参数是有长度限制的，而POST么有。

 

对参数的数据类型，GET只接受ASCII字符，而POST没有限制。

 

GET比POST更不安全，因为参数直接暴露在URL上，所以不能用来传递敏感信息。

 

GET参数通过URL传递，POST放在Request body中。

（本标准答案参考自w3schools）

GET和POST本质上就是TCP链接，并无差别。但是由于HTTP的规定和浏览器/服务器的限制，导致他们在应用过程中体现出一些不同。 

GET产生一个TCP数据包；POST产生两个TCP数据包。

## XSS攻击

XSS是一种经常出现在web应用中的计算机安全漏洞，它允许恶意web用户将代码植入到提供给其它用户使用的页面中。比如这些代码包括HTML代码和客户端脚本。攻击者利用XSS漏洞旁路掉访问控制——例如同源策略(same origin policy)。这种类型的漏洞由于被黑客用来编写危害性更大的网络钓鱼(Phishing)攻击而变得广为人知。对于跨站脚本攻击，黑客界共识是：跨站脚本攻击是新型的“缓冲区溢出攻击“，而JavaScript是新型的“ShellCode”。

XSS的防御措施

（1）编码：对用户输入的数据进行HTML Entity编码
（2）过滤：移除用户上传的DOM属性，如onerror等，移除用户上传的style节点，script节点，iframe节点等
（3）校正：避免直接对HTML Entity编码，使用DOM Prase转换，校正不配对的DOM标签。

## 浏览器工作原理/浏览器解析过程
主流的浏览器主要包括：Firefox、Chrome、Safari、Edge、IE等，这些浏览器基于WebKit，Gecko两种内核。（各种主流浏览器内核介绍）
WebKit包含两个主要部分WebCore渲染引擎（或排版引擎）和JSCore引擎（用于解析JavaScript）。

**浏览器整体框架组成**
1 用户界面 （User Interface） 
用户之间接触的部分，通常包括地址栏、后退/前进按钮、菜单栏等。

2 浏览器引擎 （Browser Engine） 
渲染引擎的查询与操作接口

3 渲染引擎 （Rendering Engine） 
显示请求的内容，即页面

4 网络层 （Networking） 
网络调用，例如HTTP请求，基于具体操作系统平台

5 UI后端 （UI Backend） 
用于绘制图形化组件，利用操作系统的用户接口

6 JavaScript解析器 （JavaScript Interpret） 
解析并执行JavaScript代码

7 数据存储（Data Storage） 
数据持久层，浏览器需要将数据存储在磁盘，例如cookies

**Rendering Engine**
1. 影响浏览器渲染方式的文档模式
每个浏览器都有自己的页面渲染引擎。渲染引擎包括两部分：一部分负责 HTML、CSS 代码的解析（渲染引擎，如 blink 引擎 or 内核），一部分负责 JavaScript 代码的解析（JavaScript 引擎，如 V8 引擎）。

2. HTML 文档的解析过程
2.1 纯 HTML 文档，无 CSS 和脚本
2.2 包含内联样式和内联脚本的 HTML 文档
2.3 包含外部 CSS 和脚本的 HTML 文档

3. JS 解释器的工作原理
3.1 扫描全局变量，确定所有已声明的变量或函数名
3.2 顺序执行所有语句

## Ajax原理
什么是 AJAX ？
AJAX = 异步 JavaScript 和 XML。
AJAX 是一种用于创建快速动态网页的技术。
通过在后台与服务器进行少量数据交换，AJAX 可以使网页实现异步更新。这意味着可以在不重新加载整个网页的情况下，对网页的某部分进行更新。

XMLHttpRequest 是 AJAX 的基础。
所有现代浏览器均支持 XMLHttpRequest 对象（IE5 和 IE6 使用 ActiveXObject）。
所有现代浏览器（IE7+、Firefox、Chrome、Safari 以及 Opera）均内建 XMLHttpRequest 对象。

创建 XMLHttpRequest 对象的语法：variable=new XMLHttpRequest();
```bash
var xmlhttp;
if (window.XMLHttpRequest)
  {// code for IE7+, Firefox, Chrome, Opera, Safari
  xmlhttp=new XMLHttpRequest();
  }
else
  {// code for IE6, IE5
  xmlhttp=new ActiveXObject("Microsoft.XMLHTTP");}

xmlhttp.open("GET","test1.txt",true);
xmlhttp.send();

# 为了避免这种情况，请向 URL 添加一个唯一的 ID：

xmlhttp.open("GET","demo_get.asp?t=" + 
Math.random()
,true);
xmlhttp.send();

# setRequestHeader( header , value )	
# 向请求添加 HTTP 头。

# header : 规定头的名称
# value : 规定头的值
```
异步 - True 或 False？
AJAX 指的是异步 JavaScript 和 XML（Asynchronous JavaScript and XML）。

XMLHttpRequest 对象如果要用于 AJAX 的话，其 open() 方法的 async 参数必须设置为 true.

服务器响应
如需获得来自服务器的响应，请使用 XMLHttpRequest 对象的 responseText 或 responseXML 属性。
responseText	获得字符串形式的响应数据。
responseXML		获得 XML 形式的响应数据。

## 对象继承的实现

## 如何写一个CSS库,要注意哪些东西?

## XHR具体底层原理和API

## Latex怎么解析

## node多线程实现/优点

## MD5摘要算法其他用途

## BFC
一、BFC是什么？
BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。
Box: CSS布局的基本单位
BFC 定义
　　BFC(Block formatting context)直译为"块级格式化上下文"。它是一个独立的渲染区域，只有Block-level box参与， 它规定了内部的Block-level Box如何布局，并且与这个区域外部毫不相干。

在一个Web页面的CSS渲染中，块级格式化上下文 (Block Fromatting Context)是按照块级盒子布局的。W3C对BFC的定义如下：

浮动元素和绝对定位元素，非块级盒子的块级容器（例如 inline-blocks, table-cells, 和 table-captions），以及overflow值不为“visiable”的块级盒子，都会为他们的内容创建新的BFC（块级格式上下文）。
为了便于理解，我们换一种方式来重新定义BFC。一个HTML元素要创建BFC，则满足下列的任意一个或多个条件即可：

1、float的值不是none。
2、position的值不是static或者relative。
3、display的值是inline-block、table-cell、flex、table-caption或者inline-flex
4、overflow的值不是visible

BFC是一个独立的布局环境，其中的元素布局是不受外界的影响，并且在一个BFC中，块盒与行盒（行盒由一行中所有的内联元素所组成）都会垂直的沿着其父元素的边框排列。

BFC布局规则：
* 内部的Box会在垂直方向，一个接一个地放置。
* Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠
* 每个元素的margin box的左边， 与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。
* BFC的区域不会与float box重叠。
* BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。
* 计算BFC的高度时，浮动元素也参与计算

二、哪些元素会生成BFC?

* 根元素
* float属性不为none
* position为absolute或fixed
* display为inline-block, table-cell, table-caption, flex, inline-flex
* overflow不为visible

## 虚拟 DOM 的 diff 算法

## http2.0

## webpack原理
webpack是一个打包模块化js的工具，可以通过loader转换文件，通过plugin扩展功能。

**webpack核心概念**
entry 一个可执行模块或库的入口文件。
chunk 多个文件组成的一个代码块，例如把一个可执行模块和它所有依赖的模块组合和一个 chunk 这体现了webpack的打包机制。
loader 文件转换器，例如把es6转换为es5，scss转换为css。
plugin 插件，用于扩展webpack的功能，在webpack构建生命周期的节点上加入扩展hook为webpack加入功能。

**webpack构建流程**
从启动webpack构建到输出结果经历了一系列过程，它们是：

* 解析webpack配置参数，合并从shell传入和webpack.config.js文件里配置的参数，生产最后的配置结果。
* 注册所有配置的插件，好让插件监听webpack构建生命周期的事件节点，以做出对应的反应。
* 从配置的entry入口文件开始解析文件构建AST语法树，找出每个文件所依赖的文件，递归下去。
* 在解析文件递归的过程中根据文件类型和loader配置找出合适的loader用来对文件进行转换。
* 递归完后得到每个文件的最终结果，根据entry配置生成代码块chunk。
* 输出所有chunk到文件系统。

**打包原理**
把所有依赖打包成一个bundle.js文件，通过代码分割成单元片段并按需加载。
整个打包生成的代码是一个IIFE(立即执行函数)，参数为由模块名和模块文件处理成的函数组成的对象，由此，我们可以猜测 webpack在打包时做了模块文件到函数的转换。

webpack就hack了commonjs代码。

原理还是很简单的，其实就是实现exports和require，然后自动加载入口模块，控制缓存模块，that's all。
通过__webpack_require__(0)启动入口模块。

webpack对于es模块的实现，也是基于自己实现的__webpack_require__ 和__webpack_exports__ ，装换成类似于commonjs的形式。对于es模块和commonjs混用的情况，则需要通过__webpack_require__.n的形式做一层包装来实现。

## url->页面加载完成的整个流程