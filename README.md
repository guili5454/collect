#HTML 和 CSS

###移动端页面 需要哪些<meta>标签 分别是干什么的

```
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=0, minimum-scale=1.0, maximum-scale=1.0"/>  
```

禁缩放

```
<meta name="apple-mobile-web-app-capable" content="yes"/>
```

IOS中 去掉拨号连接

```
<meta name="apple-mobile-web-app-status-bar-style" content="black"/>
```
```
<meta name="format-detection" content="telephone=no"/> 
```

IOS中 让网页内容以应用程序风格显示，并使状态栏透明
###CSS引入的方式有哪些，都有什么区别
链接样式：```<link rel="stylesheet" type="text/css" href="css/style.css">``` ，这是使用频率最高，最实用的方式，实现了页面框架HTML代码与美工CSS代码的完全分离，使得前期制作和后期维护都十分方便

内部样式：就是把样式表放到页面的<head>区里 ```<style></style>```，如果一个网站有很多页面，每个文件都会变大，后期维护也大，如果文件很少，CSS代码也不多，这种方式还是很不错的

行内样式：直接写到标签上，这种方式，最好不用，因为导致HTML页面不够纯净，文件体积过大，从而导致后期维护成本高

导入样式：```@import url('css/style.css')```，导入样式和链接样式比较相似，采用import方式导入CSS样式表


###CSS中的position属性有几种取值，分别说下它们的作用

absolute 绝对定位，元素将按照包含它的元素的位置进行调整，比如它嵌套在另一个绝对定位的元素中，那么就相对于那个元素定位。

relative 相对定位，元素将按照静态定位时的位置进行调整

fixed 固定定位，元素位置相对浏览器保持不变，但是ie还不支持

static 静态定位，这是默认取值，只有在你想覆盖以前的定义时才需要显示指定
###CSS的盒子模型
margin border padding content
###块元素与行内元素的区别
块元素:

- 总是在新行上开始 
- 高，行高，外边距以及内边距都可以设置
- 宽度是它的容器的100%，除非设置一个宽
- 可以容纳行内元素和其它块元素

行内元素:

- 和其它元素都在一行上
- 高，行高，外边距以及内边距不可改变
- 宽度就是它的文字或图片的宽度，不可改变
- 能容纳文本或其它行内元素
	
###img标签的title属性和alt属性的区别
title属性：提示性文字

alt属性：没有加载成功时的提示
###less与Sass
Sass是一种动态样式语言，语法跟css一样(但多了些功能)，比css好写，而且更容易阅读，用意就是为了快速写Html和Css。

Less一种动态样式语言. 将CSS赋予了动态语言的特性，如变量，继承，运算， 函数.  既可以在客户端上运行 (支持IE 6+, Webkit, Firefox)，也可一在服务端运行 (借助 Node.js)。

#jQuery
	
###jQuery选择器
:first 选取第一个元素

:last 选取最后一个元素

:not(selector) 去除所有给定选择器匹配的元素 

:even 选取索引为偶数的所有元素

:odd 选取索引为奇数的所有元素

:eq(index) 选取索引等于index的所有元素

:gt(index) 选取索引大于index的所有元素

:lt(index) 选取索引小于index的所有元素

:header 选取所有的标题元素

:animated 选取当前正在执行动画的所有元素

:focus 选取当前获取焦点的元素

:contains(text) 选取含有文本内容为text的元素 

:empty 选取不包含子元素或者文本的空元素

:has(selector) 选取含有选择器所匹配的元素的元素

:parent 选取含有子元素或者文本的元素

:hidden 选取所有不可见的元素

:visible 选取所有可见的元素

:first-child 选取每个父元素的第一个子元素

:last-child 选取每个父元素的最后一个子元素

:only-child 如果某个元素是它父元素中唯一的子元素，那么将会被匹配

:nth-child(index/even/odd) 选取每个父元素下的第index个子元素或者奇偶元素

:enabled 选取所有可用元素

:disabled 选取所有不可用元素

:checked 选取所有被选中的元素(单选框，复选框)

:selected 选取所有被选中的元素(下拉列表)

###Ajax
Ajax的优势:

- 不需要插件支持
- 优秀的用户体验
- 提高Web程序的性能
- 减轻服务器和带宽的负担

Ajax的不足:

- 浏览器对XMLHttpRequest对象的支持度不足
- 破坏浏览器前进,“后退”按钮的正常功能
- 对搜索引擎的支持的不足
- 开发和调试工具的缺乏

###$.bind()，$live()和$delegate()的区别
bind() 是直接把处理程序绑定到各个元素上，它不能把处理程序绑定到还未存在于页面中的元素之上

live() 是通过冒泡的方式来绑定到元素上,此live方法有一个非常大的缺点，那就是它仅能针对直接的CSS选择器做操作，这使得它变得非常的不灵活

delegate()仅查找并保存$(document)元素，它速度快
###如何解决Ajax跨域问题
1. iframe方法：这个适合同一主域名的二级域及主域名之间的相互访问。比如:www.a.com和blog.a.com之间的ajax交互，在两个域下的页面都加上document.domain = "a.com"就可以了。

2. 两个完全不同域名下的互访，可以利用iframe的hash属性来调用，本方法有一定局限性，不做多介绍，更多的内容可以搜索一些参考资料看看。

3. 通过中间桥梁过渡，也可以称为代理访问。比如www.a.com下一个test.html页面要访问www.b.com/data.rss数据，由于 data.rss在b.com域名下，在a下不能直接访问，但asp/php/jsp/.net等程序可以请求远程文件，这些后台程序就可以成为ajax 的桥梁了，我们先用后台动态程序请求远程数据，获取后再传递给test.html，由于这些后台程序和test.html在同一域名下，所以就可以直接访问了，跨域问题解决了。 

4. 通过```<script```>标签来解决，此方法原理就是利用```<script></script>```可以调用跨域的js文件，比如www.a.com下的文件访问www.b.com下的js文件，```<script language="javascript" scr="http://www.b.com/data.js"></script>```，在b域名下的data.js就是充当数据源的，js里保存变量和数组，此js文件的主要功能就是传递数据，不做处理用
###cookie是什么？在使用cookie的时候有哪些需要注意的地方?