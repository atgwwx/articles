#js，dom事件

在浏览器端经常碰到事件，同时作为观察者模式，事件更是在应用中必不可少，现在谈谈事件的强大之处。可以分为3类：

## js自定义事件
。。。

## dom事件
dom事件包括，鼠标操作，键盘操作，BOM自带事件，这些事件的特点是，我们使用的时候只需要注册（addEventListener||attachEvent）就可以了，事件会在特定的时候触发，然后执行我们注册的函数。

## 伪dom事件
这类事件特点是，我们照常可以使用事件注册的方法进行注册，但触发，就需要手动去创建事件了。

创建事件方法：document.createEvent(eventType);[详细见w3c](http://www.w3school.com.cn/xmldom/met_document_createevent.asp)。eventType的取值可以如下：

* HTMLEvents
* MouseEvents
* UIEvents

创建完事件，则需要对事件进行初始，[详细见w3c](http://www.w3school.com.cn/xmldom/met_event_initevent.asp).

event.initEvent(eventType, canBubble, cancelable);

最后一步，就是dom触发事件了，使用dom.dispatchEvent(event);

##参考
* [张鑫旭博客](http://www.zhangxinxu.com/wordpress/2012/04/js-dom%E8%87%AA%E5%AE%9A%E4%B9%89%E4%BA%8B%E4%BB%B6/)