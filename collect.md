#HTML

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

###块元素与行内元素的区别
块元素：

	总是在新行上开始 

	高，行高，外边距以及内边距都可以设置

	宽度是它的容器的100%，除非设置一个宽

	可以容纳行内元素和其它块元素

行内元素：

	和其它元素都在一行上

	高，行高，外边距以及内边距不可改变

	宽度就是它的文字或图片的宽度，不可改变

	能容纳文本或其它行内元素
	
#jQuery
	
###jQuery选择器
:first

:last

:not

:even

:odd

:eq

:gt

:lt

:header

:animated

:focus

:contains

:empty

:has

:parent

:hidden

:visible

:first-child

:last-child

:only-child

:nth-child

:enabled

:disabled

:checked

:selected