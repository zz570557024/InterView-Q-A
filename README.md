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
以下为文档原话：
ECMAScript实现继承的方式不止一种。
这是因为 JavaScript 中的继承机制并不是明确规定的，而是通过模仿实现的。这意味着所有的继承细节并非完全由解释程序处理。
作为开发者，你有权决定最适用的继承方式。

在JavaScript中实现继承的方法：
1. 对象冒充
2. call()  call()方法是与经典的对象冒充方法最相似的方法。【第一个参数】用作 this 的对象。【其他参数】直接传递给函数自身。
3. apply()  apply() 方法有两个参数，第一个参数：【用作 this 的对象】，第二个参数：【要传递给函数的参数的数组】
4. 原型链（prototype chaining）
/*注意：
1、原型链和对象冒充不同，原型链除了继承prototype的内容也能继承ClassA函数内的方法（注意：如果方法中含有this的引用，会出现undefined，可以通过对象冒充来解决该问题）
2、原型链不能像 call和apply一样将父类对象this改为子类对象this
3、如果要使用原型链，那么前提是父类是使用原型定义的*/
5. 混合方式
6. es6`class,extend`

## 如何写一个CSS库,要注意哪些东西?
主要有以下几点：
1. 有人可能会这样想：“我 CSS 基础这么好，让我用别人写的？闹呢！”；
2. 别人的库可能有很多冗余的、自己用不到的样式，白白增加项目体积；
3. 别人的库需要学习成本，自己写的不仅符合自己的 css 书写习惯，起的类名也是自己最好记的。

## XHR具体底层原理和API
**XHR 是什么？**
XMLHttpRequest 对象用于在后台与服务器交换数据。

XMLHttpRequest 对象是开发者的梦想，因为您能够：

- 在不重新加载页面的情况下更新网页
- 在页面已加载后从服务器请求数据
- 在页面已加载后从服务器接收数据
- 在后台向服务器发送数据

所有现代的浏览器都支持 XMLHttpRequest 对象。

XHR传数据会base64编码

## Latex怎么解析
TeX特别适合于科技论文和书籍的排版，利用它可以在计算机上生成与印刷品几乎完全一样的作品，目前在国外已经被广泛地用于编排书籍、档案、学位论文和私人信件，以及各种复杂的公式、目录、索引和参考文献等。

## node多线程实现/优点

## MD5摘要算法其他用途

* 概述
MD5即Message-Digest Algorithm 5（信息-摘要算法5），用于确保信息传输完整一致。是计算机广泛使用的杂凑算法之一（又译摘要算法、哈希算法），主流编程语言普遍已有MD5实现。将数据（如汉字）运算为另一固定长度值，是杂凑算法的基础原理，MD5的前身有MD2、MD3和MD4。
1991年，Rivest开发出技术上更为趋近成熟的md5算法。它在MD4的基础上增加了"安全-带子"（safety-belts）的概念。虽然MD5比MD4复杂度大一些，但却更为安全。这个算法很明显的由四个和MD4设计有少许不同的步骤组成。在MD5算法中，信息-摘要的大小和填充的必要条件与MD4完全相同。Den boer和Bosselaers曾发现MD5算法中的假冲突（pseudo-collisions），但除此之外就没有其他被发现的加密后结果了。

* 原理
对于MD5算法可以简要的概括为：MD5是以512位分组来处理输入信息，且每一分组又被划分为16个32位子分组，经过了一系列的处理后，算法的输出由四个32位分组组成，将这四个32位分组级联后将生成一个128位散列值。

  * 填充
  在MD5算法中，首先需要对信息进行填充，使其位长对512求余的结果等于448，并且填充必须进行，即使其位长对512求余的结果等于448。因此，信息的位长（Bits Length）将被扩展至`N*512+448`，N为一个非负整数，N可以是零。

  * 初始化变量
  * 处理分组数据

* MD5应用
**一致性验证** 
MD5的典型应用是对一段信息（Message）产生信息摘要（Message-Digest），以防止被篡改。比如，在Unix下有很多软件在下载的时候都有一个文件名相同，文件扩展名为.md5的文件，在这个文件中通常只有一行文本，大致结构如：
　　MD5 (tanajiya.tar.gz) = 38b8c2c1093dd0fec383a9d9ac940515
　　这就是tanajiya.tar.gz文件的数字签名。MD5将整个文件当作一个大文本信息，通过其不可逆的字符串变换算法，产生了这个唯一的MD5信息摘要。为了让读者朋友对MD5的应用有个直观的认识，笔者以一个比方和一个实例来简要描述一下其工作过程：　　
　　大家都知道，地球上任何人都有自己独一无二的指纹，这常常成为司法机关鉴别罪犯身份最值得信赖的方法；与之类似，MD5就可以为任何文件（不管其大小、格式、数量）产生一个同样独一无二的“数字指纹”，如果任何人对文件做了任何改动，其MD5值也就是对应的“数字指纹”都会发生变化。

　　我们常常在某些软件下载站点的某软件信息中看到其MD5值，它的作用就在于我们可以在下载该软件后，对下载回来的文件用专门的软件（如Windows MD5 Check等）做一次MD5校验，以确保我们获得的文件与该站点提供的文件为同一文件。
　　具体来说文件的MD5值就像是这个文件的“数字指纹”。每个文件的MD5值是不同的，如果任何人对文件做了任何改动，其MD5值也就是对应的“数字指纹”就会发生变化。比如下载服务器针对一个文件预先提供一个MD5值，用户下载完该文件后，用我这个算法重新计算下载文件的MD5值，通过比较这两个值是否相同，就能判断下载的文件是否出错，或者说下载的文件是否被篡改了。
　　利用MD5算法来进行文件校验的方案被大量应用到软件下载站、论坛数据库、系统文件安全等方面。

**数字签名**
MD5的典型应用是对一段Message(字节串)产生fingerprint(指纹），以防止被“篡改”。举个例子，你将一段话写在一个叫 readme.txt文件中，并对这个readme.txt产生一个MD5的值并记录在案，然后你可以传播这个文件给别人，别人如果修改了文件中的任何内容，你对这个文件重新计算MD5时就会发现（两个MD5值不相同）。如果再有一个第三方的认证机构，用MD5还可以防止文件作者的“抵赖”，这就是所谓的数字签名应用。

**安全访问认证**
MD5还广泛用于操作系统的登陆认证上，如Unix、各类BSD系统登录密码、数字签名等诸多方面。如在Unix系统中用户的密码是以MD5（或其它类似的算法）经Hash运算后存储在文件系统中。当用户登录的时候，系统把用户输入的密码进行MD5 Hash运算，然后再去和保存在文件系统中的MD5值进行比较，进而确定输入的密码是否正确。通过这样的步骤，系统在并不知道用户密码的明码的情况下就可以确定用户登录系统的合法性。这可以避免用户的密码被具有系统管理员权限的用户知道。MD5将任意长度的“字节串”映射为一个128bit的大整数，并且是通过该128bit反推原始字符串是困难的，换句话说就是，即使你看到源程序和算法描述，也无法将一个MD5的值变换回原始的字符串，从数学原理上说，是因为原始的字符串有无穷多个，这有点象不存在反函数的数学函数。所以，要遇到了md5密码的问题，比较好的办法是：你可以用这个系统中的md5（）函数重新设一个密码，如admin，把生成的一串密码的Hash值覆盖原来的Hash值就行了。

* MD5特点
MD5算法具有以下特点：
1. 压缩性：任意长度的数据，算出的MD5值长度都是固定的。
2. 容易计算：从原数据计算出MD5值很容易。
3. 抗修改性：对原数据进行任何改动，哪怕只修改1个字节，所得到的MD5值都有很大区别。
4. 强抗碰撞：已知原数据和其MD5值，想找到一个具有相同MD5值的数据（即伪造数据）是非常困难的。
MD5的作用是让大容量信息在用数字签名软件签署私人密钥前被"压缩"成一种保密的格式（就是把一个任意长度的字节串变换成一定长的十六进制数字串）。除了MD5以外，其中比较有名的还有sha-1、RIPEMD以及Haval等。

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
仅在同级的vnode间做diff，递归地进行同级vnode的diff，最终实现整个DOM树的更新。

逐个遍历newVdom的节点，找到它在oldVdom中的位置，如果找到了就移动对应的DOM元素，如果没找到说明是新增节点，则新建一个节点插入。遍历完成之后如果oldVdom中还有没处理过的节点，则说明这些节点在newVdom中被删除了，删除它们即可。

**vue**
（一）、优先处理特殊场景
一方面一些不需要做移动的DOM得到快速处理，另一方面待处理节点变少，缩小了后续操作的处理范围，性能也得到提升
（二）、“原地复用”
Vue在判断更新前后指针是否指向同一个节点，其实不要求它们真实引用同一个DOM节点，实际上它仅判断指向的是否是同类节点（比如2个不同的div，在DOM上它们是不一样的，但是它们属于同类节点），如果是同类节点，那么Vue会直接复用DOM，这样的好处是不需要移动DOM。

**整体视图**
（1）、第一部分是一个循环，循环内部是一个分支逻辑，每次循环只会进入其中的一个分支，每次循环会处理一个节点，处理之后将节点标记为已处理（oldVdom和newVdom都要进行标记，如果节点只出现在其中某一个vdom中，则另一个vdom中不需要进行标记），标记的方法有2种，当节点正好在vdom的指针处，移动指针将它排除到未处理列表之外即可，否则就要采用其他方法，Vue的做法是将节点设置为undefined。
（2）、循环结束之后，可能newVdom或者oldVdom中还有未处理的节点，如果是newVdom中有未处理节点，则这些节点是新增节点，做新增处理。如果是oldVdom中有这类节点，则这些是需要删除的节点，相应在DOM树中删除之整个过程是逐步找到更新前后vdom的差异，然后将差异反应到DOM树上（也就是patch），特别要提一下Vue的patch是即时的，并不是打包所有修改最后一起操作DOM（React则是将更新放入队列后集中处理），朋友们会问这样做性能很差吧？实际上现代浏览器对这样的DOM操作做了优化，并无差别。

## http2.0/https

**http与https区别**

**HTTP**：是互联网上应用最为广泛的一种网络协议，是一个客户端和服务器端请求和应答的标准（TCP），用于从WWW服务器传输超文本到本地浏览器的传输协议，它可以使浏览器更加高效，使网络传输减少。

**HTTPS**：是以安全为目标的HTTP通道，简单讲是HTTP的安全版，即HTTP下加入SSL层，HTTPS的安全基础是SSL，因此加密的详细内容就需要SSL。

HTTPS协议的主要作用可以分为两种：一种是建立一个信息安全通道，来保证数据传输的安全；另一种就是确认网站的真实性。

超文本传输协议HTTP协议被用于在Web浏览器和网站服务器之间传递信息，HTTP协议以明文方式发送内容，不提供任何方式的数据加密，如果攻击者截取了Web浏览器和网站服务器之间的传输报文，就可以直接读懂其中的信息，因此，HTTP协议不适合传输一些敏感信息，比如：信用卡号、密码等支付信息。

安全套接字层超文本传输协议HTTPS，为了数据传输的安全，HTTPS在HTTP的基础上加入了SSL协议，SSL依靠证书来验证服务器的身份，并为浏览器和服务器之间的通信加密。

HTTPS和HTTP的区别主要如下：

1. https协议需要到ca申请证书，一般免费证书较少，因而需要一定费用。

2. http是超文本传输协议，信息是明文传输，https则是具有安全性的ssl加密传输协议。

3. http和https使用的是完全不同的连接方式，用的端口也不一样，前者是80，后者是443。

4. http的连接很简单，是无状态的；HTTPS协议是由SSL+HTTP协议构建的可进行加密传输、身份认证的网络协议，比http协议安全。

### http2.0
HTTP 2.0是在SPDY（An experimental protocol for a faster web, The Chromium Projects）基础上形成的下一代互联网通信协议。HTTP/2 的目的是通过支持请求与响应的多路复用来较少延迟，通过压缩HTTPS首部字段将协议开销降低，同时增加请求优先级和服务器端推送的支持。
* 二进制分帧层，是HTTP 2.0性能增强的核心。
HTTP 1.x在应用层以纯文本的形式进行通信，而HTTP 2.0将所有的传输信息分割为更小的消息和帧，并对它们采用二进制格式编码。这样，客户端和服务端都需要引入新的二进制编码和解码的机制。
**帧（frame）**
HTTP 2.0通信的最小单位，包括帧首部、流标识符、优先值和帧净荷等。
**消息（message）**
消息是指逻辑上的HTTP消息（请求/响应）。一系列数据帧组成了一个完整的消息。比如一系列DATA帧和一个HEADERS帧组成了请求消息。
**流（stream）**
流是连接中的一个虚拟信道，可以承载双向消息传输。每个流有唯一整数标识符。为了防止两端流ID冲突，客户端发起的流具有奇数ID，服务器端发起的流具有偶数ID。 
所有HTTP 2. 0 通信都在一个TCP连接上完成， 这个连接可以承载任意数量的双向数据流Stream。 相应地， 每个数据流以 消息的形式发送， 而消息由一 或多个帧组成， 这些帧可以乱序发送， 然后根据每个帧首部的流标识符重新组装。
二进制分帧层保留了HTTP的语义不受影响，包括首部、方法等，在应用层来看，和HTTP 1.x没有差别。同时，所有同主机的通信能够在一个TCP连接上完成。

### 多路复用共享连接
基于二进制分帧层，HTTP 2.0可以在共享TCP连接的基础上，同时发送请求和响应。HTTP消息被分解为独立的帧，而不破坏消息本身的语义，交错发送出去，最后在另一端根据流ID和首部将它们重新组合起来。
性能对比，高下立见。HTTP 2.0成功解决了HTTP 1.x的队首阻塞问题（TCP层的阻塞仍无法解决），同时，也不需要通过pipeline机制多条TCP连接来实现并行请求与响应。减少了TCP连接数对服务器性能也有很大的提升。

### 请求优先级
客户端明确指定优先级，服务端可以根据这个优先级作为依据交互数据，比如客户端优先级设置为.css>.js>.jpg（具体可参见《高性能网站建设指南》）， 服务端按优先级返回结果有利于高效利用底层连接，提高用户体验。 
然而，也不能过分迷信请求优先级，仍然要注意以下问题：

* 服务端是否支持请求优先级
* 会否引起队首阻塞问题，比如高优先级的慢响应请求会阻塞其他资源的交互。

### 服务端推送
### 首部压缩
HTTP 1.x每一次通信（请求/响应）都会携带首部信息用于描述资源属性。HTTP 2.0在客户端和服务端之间使用“首部表”来跟踪和存储之前发送的键-值对。首部表在连接过程中始终存在，新增的键-值对会更新到表尾，因此，不需要每次通信都需要再携带首部。

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

* 输入地址
* 浏览器查找域名的 IP 地址
* 这一步包括 DNS 具体的查找过程，包括：浏览器缓存->系统缓存->路由器缓存...
* 浏览器向 web 服务器发送一个 HTTP 请求
* 服务器的永久重定向响应（从 `http://example.com` 到 `http://www.example.com`）
* 浏览器跟踪重定向地址
* 服务器处理请求
* 服务器返回一个 HTTP 响应
* 浏览器显示 HTML
* 浏览器发送请求获取嵌入在 HTML 中的资源（如图片、音频、视频、CSS、JS等等）
* 浏览器发送异步请求

## tcp三次握手/tcp VS udp

**TCP握手协议**
所谓三次握手（Three-Way Handshake）即建立TCP连接，就是指建立一个TCP连接时，需要客户端和服务端总共发送3个包以确认连接的建立。在socket编程中，这一过程由客户端执行connect来触发 
在TCP/IP协议中,TCP协议提供可靠的连接服务,采用三次握手建立一个连接.

* 第一次握手：建立连接时,客户端发送syn包(syn=j)到服务器,并进入SYN_SEND状态,等待服务器确认； 
SYN：同步序列编号(Synchronize Sequence Numbers)
* 第二次握手：服务器收到syn包,必须确认客户的SYN（ack=j+1）,同时自己也发送一个SYN包（syn=k）,即SYN+ACK包,此时服务器进入SYN_RECV状态； 
* 第三次握手：客户端收到服务器的SYN＋ACK包,向服务器发送确认包ACK(ack=k+1),此包发送完毕,客户端和服务器进入ESTABLISHED状态,完成三次握手.

完成三次握手,客户端与服务器开始传送数据。

**四次挥手**
三次握手耳熟能详，四次挥手估计就，所谓四次挥手（Four-Way Wavehand）即终止TCP连接，就是指断开一个TCP连接时，需要客户端和服务端总共发送4个包以确认连接的断开。在socket编程中，这一过程由客户端或服务端任一方执行close来触发

由于TCP连接时全双工的，因此，每个方向都必须要单独进行关闭，这一原则是当一方完成数据发送任务后，发送一个FIN来终止这一方向的连接，收到一个FIN只是意味着这一方向上没有数据流动了，即不会再收到数据了，但是在这个TCP连接上仍然能够发送数据，直到这一方向也发送了FIN。首先进行关闭的一方将执行主动关闭，而另一方则执行被动关闭，上图描述的即是如此。
（1）第一次挥手：Client发送一个FIN，用来关闭Client到Server的数据传送，Client进入FIN_WAIT_1状态。
（2）第二次挥手：Server收到FIN后，发送一个ACK给Client，确认序号为收到序号+1（与SYN相同，一个FIN占用一个序号），Server进入CLOSE_WAIT状态。
（3）第三次挥手：Server发送一个FIN，用来关闭Server到Client的数据传送，Server进入LAST_ACK状态。
（4）第四次挥手：Client收到FIN后，Client进入TIME_WAIT状态，接着发送一个ACK给Server，确认序号为收到序号+1，Server进入CLOSED状态，完成四次挥手。

## 几种双向绑定方法
1. 发布者-订阅者模式（backbone.js）
2. 脏值检查（angular.js）
angular.js 是通过脏值检测的方式比对数据是否有变更，来决定是否更新视图，最简单的方式就是通过 setInterval() 定时轮询检测数据变动，当然Google不会这么low，angular只有在指定的事件触发时进入脏值检测，大致如下：

DOM事件，譬如用户输入文本，点击按钮等。( ng-click )

XHR响应事件 ( $http )

浏览器Location变更事件 ( $location )

Timer事件( $timeout , $interval )

执行 $digest() 或 $apply()

3. 数据劫持（vue.js）

数据劫持:  vue.js 则是采用数据劫持结合发布者-订阅者模式的方式，通过Object.defineProperty()来劫持各个属性的setter，getter，在数据变动时发布消息给订阅者，触发相应的监听回调。

## mvvm/vue原理

**要实现mvvm的双向绑定，就必须要实现以下几点：**

* 实现一个数据监听器Observer，能够对数据对象的所有属性进行监听，如有变动可拿到最新值并通知订阅者

* 实现一个指令解析器Compile，对每个元素节点的指令进行扫描和解析，根据指令模板替换数据，以及绑定相应的更新函数

* 实现一个Watcher，作为连接Observer和Compile的桥梁，能够订阅并收到每个属性变动的通知，执行指令绑定的相应回调函数，从而更新视图

* mvvm入口函数，整合以上三者

**实现Compile**
compile主要做的事情是解析模板指令，将模板中的变量替换成数据，然后初始化渲染页面视图，并将每个指令对应的节点绑定更新函数，添加监听数据的订阅者，一旦数据有变动，收到通知，更新视图
因为遍历解析的过程有多次操作dom节点，为提高性能和效率，会先将跟节点el转换成文档碎片fragment进行解析编译操作，解析完成，再将fragment添加回原来的真实dom节点中

**实现Watcher**
Watcher订阅者作为Observer和Compile之间通信的桥梁，主要做的事情是:
1、在自身实例化时往属性订阅器(dep)里面添加自己
2、自身必须有一个update()方法
3、待属性变动dep.notice()通知时，能调用自身的update()方法，并触发Compile中绑定的回调，则功成身退。

**为什么建立连接是三次握手，而关闭连接却是四次挥手呢？**
这是因为服务端在LISTEN状态下，收到建立连接请求的SYN报文后，把ACK和SYN放在一个报文里发送给客户端。而关闭连接时，当收到对方的FIN报文时，仅仅表示对方不再发送数据了但是还能接收数据，己方也未必全部数据都发送给对方了，所以己方可以立即close，也可以发送一些数据给对方后，再发送FIN报文给对方来表示同意现在关闭连接，因此，己方ACK和FIN一般都会分开发送。

## 异步原理/promise原理

* [Promise类实现]
* 构造函数传入一个fn，有两个参数，resolve：成功回调; reject：失败回调;
* state: 状态存储
* doneList: 成功处理函数列表
* failList: 失败处理函数列表
* done: 注册成功处理函数
* fail: 注册失败处理函数
* then: 同时注册成功和失败处理函数
* always: 一个处理注册到成功和失败，都会调用
* resolve: 更新state为：RESOLVED，并且执行成功处理队列
* reject: 更新state为：REJECTED，并且执行失败处理队列

promise有3种状态：pending（待解决，这也是初始化状态），fulfilled（完成），rejected（拒绝）。

## apply,bind和call有什么区别?

javaScript权威指南上的解释是： call() 、apply()可以看作是某个对象的方法，通过调用方法的形式来间接调用函数。bind() 就是将某个函数绑定到某个对象上。

在JS中，这三者都是用来改变函数的this对象的指向的

三者的相似之处：
1. 都是用来改变函数的this对象的指向的。
2. 第一个参数都是this要指向的对象。
3. 都可以利用后续参数传参。

区别：
1. 对于call可以这样：xw.say.call(xh);
2. 对于apply可以这样：xw.say.apply(xh);
3. 而对于bind来说需要这样：xw.say.bind(xh)();
**call和apply都是对函数的直接调用，而bind方法返回的仍然是一个函数，因此后面还需要()来进行调用才可以。**
**call后面的参数与say方法中是一一对应的，而apply的第二个参数是一个数组，数组中的元素是和say方法中一一对应的，这就是两者最大的区别。由于bind返回的仍然是一个函数，所以我们还可以在调用的时候再进行传参。**

## ES6 模块与 CommonJS 模块的差异

* CommonJS 模块输出的是一个值的拷贝，ES6 模块输出的是值的引用。
* CommonJS 模块是运行时加载，ES6 模块是编译时输出接口。

第二个差异是因为 CommonJS 加载的是一个对象（即module.exports属性），该对象只有在脚本运行完才会生成。而 ES6 模块不是对象，它的对外接口只是一种静态定义，在代码静态解析阶段就会生成。

ES6 模块的运行机制与 CommonJS 不一样。JS 引擎对脚本静态分析的时候，遇到模块加载命令import，就会生成一个只读引用。等到脚本真正执行时，再根据这个只读引用，到被加载的那个模块里面去取值。换句话说，ES6 的import有点像 Unix 系统的“符号连接”，原始值变了，import加载的值也会跟着变。因此，ES6 模块是动态引用，并且不会缓存值，模块里面的变量绑定其所在的模块。

## canvas监听点击事件

HTML中只能为元素/标签绑定监听函数； 
Canvas绘图中只有一个元素-canvas，每一个图形/图像都不是元素，不能直接进行事件绑定。

**解决办法：“事件委托”——让canvas监听所有的事件，计算事件发生坐标点，是否处于某个图形/图像的范围内。**

Canvas事件
* 鼠标事件
```bash
canvas.onmousedown = function(e ) {
  #React to the mouse down event 
};

canvas.addEventListener('mousedown', function(e ) { 
  #React to the mouse down event
});
```
上面一种方法看起来更简单一些，但是，如果需要向某个鼠标事件注册多个监听器的话，那么用addEventListener()方法会更合适。

浏览器通过事件对象传递给监听器的鼠标坐标，是窗口坐标（window coordinate），而不是相对与canvas自身的坐标。而大部分情况下，开发者需要知道的是发生鼠标事件的点相对于canvas的位置，而不是在整个窗口中的位置，所以有必要进行坐标变换。

* 键盘事件
canvas是一个不可获取焦点的元素，所以，在canvas上新增键盘事件监听器是徒劳的。如果想要检测键盘事件的话，你应该在document或window对象上新增键盘事件监听器才对。
* 触摸事件
移动端触摸事件与桌面平台的鼠标事件有两个主要的不同点

1. 鼠标光标只有一个i额，而触摸点可能有很多
2. 鼠标光标可以悬停（hover），而触摸点则不行
* 手指缩放
对于类型为touchstart及touchmove的触摸事件，如果发现有两个点同时在触摸设备，而且它们中至少有一个位置发生了变化，那么就判定用户在pinch屏幕。如果程序发现用户正在pinch屏幕，用于处理touchstart事件的方法会计算两个触摸点之间的距离，以及当前放大倍数与该距离的比值。在touchmove事件的方法也会计算当前两个触摸点之间的距离，并且将该值乘以刚才计算好的比值，就可以得到新的放大倍数。
```bash
let canvas = document.getElementById('mycanvas'),
    ctx = canvas.getContext('2d')
```

## 路由实现
## 无线性能优化
## Tap事件,Touch
`一、click 和 tap 比较
两者都会在点击时触发，但是在手机WEB端，click会有 200~300 ms，所以请用tap代替click作为点击事件。
singleTap和doubleTap 分别代表单次点击和双次点击。`

三、touch事件touch是针对触屏手机上的触摸事件。

## CSS盒模型/box-sizing
盒子模型分为上述两种，W3C盒子模型也就是W3C的标准。 
这两个模型的唯一区别是计算width和height时，IE盒子模型包含padding和border, W3C盒子模型则不包括。为了使页面在不同浏览器下呈现相同的效果，必须统一盒子模型，因为设置width或者height一般是必须用到的。
那么必须设置浏览器的渲染模式是标准模式，在标准模式下，IE6+和其他现代浏览器会以W3C盒子模型渲染。
box-sizing属性可以指定盒子模型种类，content-box指定盒子模型为W3C，后者为IE盒子模型。
这是CSS3属性，IE8+和其他现代浏览器支持，详见文档。

* box-sizing：content-box
默认值，标准的盒模型，width和height只包括内容（content）的宽度和高度，不包括border，padding，margin，这些都是盒子的外部。

* box-sizing：border-box
这个模式下，当我们设置了盒子宽度和高度的时候，其包括：content+padding+border，但是不包括margin。

## DOM事件中target和currentTarget的区别

接收顺序（事件流方式），需要我们了解：
1. 事件捕获：什么叫捕获，其实不用扯那么多一句话从最不具体的到最具体的
2. 事件冒泡：什么叫冒泡，正好和上面相反，从最具体的到最不具体的
3. 为什么会有两种事件流方式呢？历史原因，ie提出的是事件冒泡，而w3c提出的是事件捕获。
4. 现代浏览器高级了，那。。。。。嗯，我知道你要问啥，你一定要问浏览器内部是如何解析这两种事件流的，它的执行顺序：事件捕获-》目标阶段-》事件冒泡，一句话就是先捕获后冒泡

先诉重点理论：
1. target:触发事件的某个具体对象，只会出现在事件流的目标阶段（谁触发谁命中，所以肯定是目标阶段）
2. currentTarget:绑定事件的对象，恒等于this，可能出现在事件流的任意一个阶段中
3. 通常情况下terget和currentTarget是一致的，我们只要使用terget即可，但有一种情况必须区分这三者的关系，那就是在父子嵌套的关系中，父元素绑定了事件，单击了子元素（根据事件流，在不阻止事件流的前提下他会传递至父元素，导致父元素的事件处理函数执行），这时候currentTarget指向的是父元素，因为他是绑定事件的对象，而target指向了子元素，因为他是触发事件的那个具体对象

currentTarget（其事件处理程序当前正在处理事件的那个元素），
target(事件的目标)。

通过自己写的demo,我对这两个属性的理解是，
currentTarget(你绑定事件的那个元素), 
target(触发事件的那个目标)

点击button的时候由于事件处理程序注册于button之上，所以处理事件的目标也是button。
如果只是在div上注册点击事件处理程序，虽然事件是由button出发的，但是它本身并没有注册这个事件处理程序，所以会向上冒泡，找到div元素。

## 深拷贝的实现原理

对于字符串类型，浅复制是对值的复制，对于对象来说，浅复制是对对象地址的复制，并没 有开辟新的栈，也就是复制的结果是两个对象指向同一个地址，修改其中一个对象的属性，则另一个对象的属性也会改变，而深复制则是开辟新的栈，两个对象对应两个不同的地址，修改一个对象的属性，不会改变另一个对象的属性。深复制实现代码如下：
可以从两个方法进行解决。
第一种方法、通过递归解析解决：
```bash
var china = { nation : '中国', birthplaces:['北京','上海','广州'], skincolr :'yellow', friends:['sk','ls'] } 
#深复制，要想达到深复制就需要用递归 
function deepCopy(o,c){ var c = c || {} for(var i in o){ 
if(typeof o[i] === 'object'){ 
#要考虑深复制问题了 
if(o[i].constructor === Array){ 
#这是数组 
c[i] =[] }else{ 
#这是对象 
c[i] = {} } 
deepCopy(o[i],c[i]) }else{ c[i] = o[i] } } return c } 
var result = {name:'result'} 
result = deepCopy(china,result) 
console.dir(result)
```
第二种方法：通过JSON解析解决
```bash
var test ={ name:{ xing:{ first:'张', second:'李' }, ming:'老头' }, age :40, friend :['隔壁老王','宋经纪','同事'] } 
var result = JSON.parse(JSON.stringify(test)) 
result.age = 30 
result.name.xing.first = '往' 
result.friend.push('fdagldf;ghad') 
console.dir(test) 
console.dir(result)
```
## 编写webpack的loader
loader 用于对模块的源代码进行转换。loader 可以使你在 import 或"加载"模块时预处理文件。因此，loader 类似于其他构建工具中“任务(task)”，并提供了处理前端构建步骤的强大方法。

vue-loader 是一个 Webpack 的 loader，可以将指定格式编写的 Vue 组件转换为 JavaScript 模块。

我们知道了webpack的强大依托于一个个强大的 loader（当然还有plugin，本文就不介绍了）。如果想真的玩溜webpack，我们就必须掌握loader的使用。在我们使用它们前，我们得知道自己需要什么loader。如果想编译less，可以用less-loader；想加载html文件并打包它内链的静态文件，可以使用html-loader。只要我们想对文件进行处理时，我们都可以去找想对应的loader。

**编写一个 loader**
loader 是导出为一个函数的 node 模块。该函数在 loader 转换资源的时候调用。给定的函数将调用 loader API，并通过 this 上下文访问。

匹配(test)单个 loader，你可以简单通过在 rule 对象设置 path.resolve 指向这个本地文件
匹配(test)多个 loaders，你可以使用 resolveLoader.modules 配置，webpack 将会从这些目录中搜索这些 loaders。例如，如果你的项目中有一个 /loaders 本地目录

**简单用法**
当一个 loader 在资源中使用，这个 loader 只能传入一个参数 - 这个参数是一个包含包含资源文件内容的字符串

同步 loader 可以简单的返回一个代表模块转化后的值。在更复杂的情况下，loader 也可以通过使用 this.callback(err, values...) 函数，返回任意数量的值。错误要么传递给这个 this.callback 函数，要么扔进同步 loader 中。

loader 会返回一个或者两个值。第一个值的类型是 JavaScript 代码的字符串或者 buffer。第二个参数值是 SourceMap，它是个 JavaScript 对象。

**复杂用法**
当链式调用多个 loader 的时候，请记住它们会以相反的顺序执行。取决于数组写法格式，从右向左或者从下向上执行。

最后的 loader 最早调用，将会传入原始资源内容。
第一个 loader 最后调用，期望值是传出 JavaScript 和 source map（可选）。
中间的 loader 执行时，会传入前一个 loader 传出的结果。
所以，在接下来的例子，foo-loader 被传入原始资源，bar-loader 将接收 foo-loader 的产出，返回最终转化后的模块和一个 source map（可选）

**用法准则(Guidelines)**
编写 loader 时应该遵循以下准则。它们按重要程度排序，有些仅适用于某些场景，请阅读下面详细的章节以获得更多信息。

* 简单易用。
* 使用链式传递。
* 模块化的输出。
* 确保无状态。
* 使用 loader utilities。
* 记录 loader 的依赖。
* 解析模块依赖关系。
* 提取通用代码。
* 避免绝对路径。
* 使用 peer dependencies。

查阅node与webpack文档，我们可以通过loader-utils来获取loader的配置项。通过node的fs.readFileSync去加载文件

## babel把ES6转成ES5或者ES3之类的原理
* Babel的包构成
**核心包**
* babel-core：babel转译器本身，提供了babel的转译API，如babel.transform等，用于对代码进行转译。像webpack的babel-loader就是调用这些API来完成转译过程的。
* babylon：js的词法解析器
* babel-traverse：用于对AST（抽象语法树，想了解的请自行查询编译原理）的遍历，主要给plugin用
* babel-generator：根据AST生成代码

* babel的工作原理
babel是一个转译器，感觉相对于编译器compiler，叫转译器transpiler更准确，因为它只是把同种语言的高版本规则翻译成低版本规则，而不像编译器那样，输出的是另一种更低级的语言代码。
但是和编译器类似，babel的转译过程也分为三个阶段：parsing、transforming、generating，以ES6代码转译为ES5代码为例，babel转译的具体过程如下：

> ES6代码输入 ==》 babylon进行解析 ==》 得到AST==》 plugin用babel-traverse对AST树进行遍历转译 ==》 得到新的AST树==》 用babel-generator通过AST树生成ES5代码

babel只是转译新标准引入的语法，比如ES6的箭头函数转译成ES5的函数；而新标准引入的新的原生对象，部分原生对象新增的原型方法，新增的API等（如Proxy、Set等），这些babel是不会转译的。需要用户自行引入polyfill来解决

**plugins**

插件应用于babel的转译过程，尤其是第二个阶段transforming，如果这个阶段不使用任何插件，那么babel会原样输出代码。
我们主要关注transforming阶段使用的插件，因为transform插件会自动使用对应的词法插件，所以parsing阶段的插件不需要配置。

**polyfill**
polyfill是一个针对ES2015+环境的shim，实现上来说babel-polyfill包只是简单的把core-js和regenerator runtime包装了下，这两个包才是真正的实现代码所在（后文会详细介绍core-js）。
使用babel-polyfill会把ES2015+环境整体引入到你的代码环境中，让你的代码可以直接使用新标准所引入的新原生对象，新API等，一般来说单独的应用和页面都可以这样使用。
**使用方法**
先安装包： npm install --save babel-polyfill
要确保在入口处导入polyfill，因为polyfill代码需要在所有其他代码前先被调用
代码方式： import "babel-polyfill"
webpack配置： module.exports = { entry: ["babel-polyfill", "./app/js"] };
如果只是需要引入部分新原生对象或API，那么可以按需引入，而不必导入全部的环境，具体见下文的core-js

**runtime**
polyfill和runtime的区别
直接使用babel-polyfill对于应用或页面等环境在你控制之中的情况来说，并没有什么问题。但是对于在library中使用polyfill，就变得不可行了。因为library是供外部使用的，但外部的环境并不在library的可控范围，而polyfill是会污染原来的全局环境的（因为新的原生对象、API这些都直接由polyfill引入到全局环境）。这样就很容易会发生冲突，所以这个时候，babel-runtime就可以派上用场了。

**通过core-js实现按需引入polyfill或runtime**
但是polyfill和runtime都是整体引入的，不能做细粒度的调整，如果我们的代码只是用到了小部分ES6而导致需要使用polyfill和runtime的话，会造成代码体积不必要的增大（runtime的影响较小）。所以，按需引入的需求就自然而然产生了，这个时候就得依靠core-js来实现了。

**core-js的组织结构**
首先，core-js有三种使用方式：

默认方式：require('core-js')
这种方式包括全部特性，标准的和非标准的
库的形式： var core = require('core-js/library')
这种方式也包括全部特性，只是它不会污染全局名字空间
只是shim： require('core-js/shim')或var shim = require('core-js/library/shim')
这种方式只包括标准特性（就是只有polyfill功能，没有扩展的特性）

## rax
* What is Rax
A universal React-compatible render engine.

官方描述：一个通用的跨容器的渲染引擎。

关键词：
* universal：跨容器（Browser/Native/Node）
* React-compatible：React语法基本兼容

* Why use Rax

`Weex本身是Vue@1.x的语法糖`，如果你和你的团队的技术栈之前就是React，并没有Vue，那么Rax将是一个不错的选择。

由于Rax基于React DSL，所以天生就享有React社区所带来的一些资源，比如：Redux。

此外，相比于React，它的优势：

渐进渲染模式，白屏时间更短
8.5kb（min+gzip），文件体积更小

* 入门
与react/react-native类似，Rax同样是由两个库组成：rax和rax-components：

rax – 核心渲染库，提供了React-compatible API
rax-components – 辅助组件库，更准确地说，应该是：元件，提供了UI跨平台的能力
所以：一般来说，基于元件编写的复合组件，是可以同时运行在Native和Web上的。

* 差异点
虽然Rax实现了大部分React-compatible API，可能出于底层需要适配Weex API以及Native性能上的一些考虑，所以在实现细节上，还是会有一些差别，比如：

不支持createClass()方法，更推荐使用ES6 Class替代（Rax并不像React有过多的历史包袱）
向指定container node渲染时，并不会清空当前容器的子节点，而是直接采用appendChild的方式
setState()方法是同步的，不再支持批处理更新（batchedUpdates），而React是异步的。
…

**前面开篇里提到过，使用Rax/Weex构建的是：一个移动端·跨平台应用。**

那么，从样式编写的角度，该如何看待移动端和跨平台这两个Rax/Weex特性？

* 移动端：宽高/边距，甚至是字体大小等样式，需要能够适配不同屏幕尺寸的手机
* 跨平台：同一份样式代码需要能够同时在Web/IOS/Android平台上运行
面对上述的问题，其实在以往的Web App实践中，已经有了一些类似的经验沉淀：

通过**「rem」**和**「flexbox」**可以做到手机屏幕适配
通过**「css in js」**的方式，让JS拥有描述样式的能力，从而做到将同一份代码运行在不同的JS Engine里（抛弃了原来Web固有的CSS样式表）
Rax/Weex也正是基于类似上述的思路实现了对应样式API，接下来主要以Rax为例介绍如何编写样式。

**关于适配**
在传统的Web中，根据手机屏幕宽度的值，动态改变html font-size，再结合rem单位对不同尺寸的手机屏幕进行适配（对于样式数值的转换，往往会通过sass/less来进行预编译）。

而在Weex/Rax中，同样是根据手机屏幕宽度，由于样式已经通过「css in js」的方式引入，所以动态转换用户传递参数（样式数值）就可以达到适配的目的（这里的数值转换，与之前的不同，因为发生在javascript运行时）。

**关于布局**
在Weex/Rax中，不再支持float布局，取而代之的是flexbox布局（对于移动端而言，理应如此）。

###高阶
事实上，在项目开发过程中，如果将所有的样式代码都写在JS文件里，会发现代码看起来很臃肿，或许我们更习惯于：分离样式代码。

Webpack的诞生，推动了前端自动化工具的发展的同时，也加速了我们对前端的认知，不用再去一直等待标准规范的完全实现，有很多这样的例子：

babel-loader：jsx/es6/es7转换成es5
sass/less-loader：sass/less转换成css
vue-loader：实现了SFC（Single File Components）
weex-loader：实现了SFC的同时，还注入了__weex_require__（可以引用Native Module）
所以，代码的写法已经不受太多约束，因为可以有很多插件去支撑一个靠谱的想法。

同样的，Rax也提供了这么一个Webpack插件 – 「stylesheet-loader」，让我们能够在Rax应用中通过CSS写样式。

除了样式代码的分离，少写几个引号之外，stylesheet-loader的好处还在于：

对于Weex不支持的样式，能快速给予友好的warning提示
可以跟sass/less-loader结合，使用变量、mixin、嵌套等预编译功能

## javascript的变量的存储方式--栈（stack）和堆（heap）/ javascript值传递与址传递

* 栈：自动分配内存空间，系统自动释放，里面存放的是基本类型的值和引用类型的地址
* 堆：动态分配的内存，大小不定，也不会自动释放。里面存放引用类型的值。

基本类型与引用类型最大的区别实际就是传值与传址的区别
* 值传递：基本类型采用的是值传递。
* 址传递：引用类型则是地址传递，将存放在栈内存中的地址赋值给接收的变量。

## nodejs加载原生的包与自己定义的包路径如何查找
## css性能优化，就动画效果，如何从js、css角度减少回流
## 强制使用硬件加速 （通过 GPU 来提高动画性能）
在浏览器中用css开启硬件加速，使GPU (Graphics Processing Unit) 发挥功能，从而提升性能吗？
**在桌面端和移动端用CSS开启硬件加速**
Chrome, FireFox, Safari, IE9+和最新版本的Opera都支持硬件加速，当它们检测到页面中某个DOM元素应用了某些CSS规则时就会开启，最显著的特征的元素的3D变换。

原生的移动端应用(Native mobile applications)总是可以很好的运用GPU，这是为什么它比网页应用(Web apps)表现更好的原因。硬件加速在移动端尤其有用，因为它可以有效的减少资源的利用(麦时注：移动端本身资源有限)。

## webpack的plugin与loader区别
## 原型链与作用域链
## 七层网络协议，每层干嘛用
OSI是一个开放性的通信系统互连参考模型，他是一个定义得非常好的协议规范。OSI模型有7层结构，每层都可以有几个子层。 OSI的7层从上到下分别是 7 应用层 6 表示层 5 会话层 4 传输层 3 网络层 2 数据链路层 1 物理层 ；其中高层（即7、6、5、4层）定义了应用程序的功能，下面3层（即3、2、1层）主要面向通过网络的端到端的数据流。

* 应用层
与其它计算机进行通讯的一个应用，它是对应应用程序的通信服务的。例如，一个没有通信功能的字处理程序就不能执行通信的代码，从事字处理工作的程序员也不关心OSI的第7层。但是，如果添加了一个传输文件的选项，那么字处理器的程序员就需要实现OSI的第7层。示例：TELNET，HTTP，FTP，NFS，SMTP等。

* 表示层
这一层的主要功能是定义数据格式及加密。例如，FTP允许你选择以二进制或ASCII格式传输。如果选择二进制，那么发送方和接收方不改变文件的内容。如果选择ASCII格式，发送方将把文本从发送方的字符集转换成标准的ASCII后发送数据。在接收方将标准的ASCII转换成接收方计算机的字符集。示例：加密，ASCII等。

* 会话层
它定义了如何开始、控制和结束一个会话，包括对多个双向消息的控制和管理，以便在只完成连续消息的一部分时可以通知应用，从而使表示层看到的数据是连续的，在某些情况下，如果表示层收到了所有的数据，则用数据代表表示层。示例：RPC，SQL等。

* 传输层
这层的功能包括是否选择差错恢复协议还是无差错恢复协议，及在同一主机上对不同应用的数据流的输入进行复用，还包括对收到的顺序不对的数据包的重新排序功能。示例：TCP，UDP，SPX。

* 网络层
这层对端到端的包传输进行定义，它定义了能够标识所有结点的逻辑地址，还定义了路由实现的方式和学习的方式。为了适应最大传输单元长度小于包长度的传输介质，网络层还定义了如何将一个包分解成更小的包的分段方法。示例：IP，IPX等。

* 数据链路层
它定义了在单个链路上如何传输数据。这些协议与被讨论的各种介质有关。示例：ATM，FDDI等。

* 物理层
OSI的物理层规范是有关传输介质的特这些规范通常也参考了其他组织制定的标准。连接头、帧、帧的使用、电流、编码及光调制等都属于各种物理层规范中的内容。物理层常用多个规范完成对所有细节的定义。示例：Rj45，802.3等。


## GraghQL/WebAssembly

### GraghQL

> ask exactly what you want.

GraphQL 是一个用于 API 的查询语言，是一个使用基于类型系统来执行查询的服务端运行时（类型系统由你的数据定义）。GraphQL 并没有和任何特定数据库或者存储引擎绑定，而是依靠你现有的代码和数据支撑。

### WebAssembly
JavaScript是在虚拟机（VM）中执行的，该虚拟机能够最大化地优化代码并压榨每一丝的性能，这也使得JavaScript称为速度最快的动态语言之一。但尽管如此，它还是无法与原生的C/C++代码相媲美。所以，WebAssembly就出现了。
Wasm同样在JavaScript虚拟机中运行，但是它表现得更好。两者可以自由交互、互不排斥，这样你就同时拥有了两者最大的优势——JavaScript巨大的生态系统和有好的语法，WebAssembly接近原生的表现性能。

C到WebAssembly的编译器，推荐使用Emscripten（`https://kripken.github.io/emscripten-site/docs/getting_started/downloads.html`），安装这个工具费时费力费空间，但没办法，这是目前为止最好的选择，请仔细阅读安装说明，需占用约1GB的硬盘空间。