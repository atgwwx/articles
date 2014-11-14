# CSS讨论
写CSS并不难，难的是如何写出可维护的CSS。

0. 如何写出select的placeholder效果
	
	select标签是不支持placeholder效果的，想要得到这种效果，需要这样做：
	
	0. 设置select颜色：select{color:#999}, placeholder的默认颜色是#999
	0. 设置select下第一个option:<option value="" disable selected>请选择</option>
	0. 监听select的change事件，当选中option后，将select的颜色修改为#000.
	0. 至此，打工告成。

0. 关于CSS模块化的讨论：[http://blog.jobbole.com/76030/](http://blog.jobbole.com/76030/)
1. 吸收bootstrap的规范：[http://getbootstrap.com/2.3.2/components.html](http://getbootstrap.com/2.3.2/components.html)
1. 国外大神关于CSS的可维护性的讨论：[http://benfrain.com/enduring-css-writing-style-sheets-rapidly-changing-long-lived-projects/](http://benfrain.com/enduring-css-writing-style-sheets-rapidly-changing-long-lived-projects/)