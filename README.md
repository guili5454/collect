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
