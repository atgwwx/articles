# CSS3动画
## transition

* transition-property //过渡效果的css属性名称
	* none 没有属性会得到过渡效果
	* all 所有属性都将得到过渡效果
	* property 过渡效果的css属性

* transition-duration 动画总时长
* transition-timing-function 动画缓动函数
* transition-delay 动画延迟时间

## transform
* transform 向元素应用2D或3D变换
* transform-origin 允许你改变转换元素的位置
* transform-style 规定被嵌套元素如何在3D空间中显示
* perspective 规定3D元素的透视效果
* perspective-origin 规定3D元素的底部位置
* backface-visibility 定义元素在不面对屏幕时是否可见
## animation
* @keyframes 规定动画
* animation 动画所有属性的简写形式
* animation-name 动画名称，对应于keyframes

	* animationname: 定义动画名称
	* keyframes-selector 动画时长的百分比
	* css-styles css样式属性
	
			//demo
			@keyframes mymove
			{
				from {top:0px;} //from等价于0%
				to {top:200px} //to等价于100%
			}

* animation-duration 动画总时长，默认0，即没有效果
		
* animation-delay 延迟时间， 默认0, 单位秒或毫秒计,还可以为负值
	
		//demo
		animation-delay:2s
		animation-delay:2000ms
* animation-timing-function 缓动函数，默认ease
	* linear 直线运动
	* ease 默认。低速开始，然后加快，在结束前变慢
	* ease-in 动画以低速开始
	* ease-out 动画以低速结束
	* ease-in-out 动画以低速开始和结束
	* cubic-bezier(n, n, n, n)三次贝塞尔曲线函数
* animation-iteration-count 动画重复次数,默认1
	* n 动画播放次数
	* infinite 动画应该无限次播放
* animation-direction 定义是否应该轮流反向播放动画，默认normal
	* normal	正常播放
	* alternate 轮流反向播放
* animation-play-state 设定动画是播放或者暂停，IE9及以下不支持,默认running
	* paused 暂停
	* running 播放
* animation-fill-mode 规定动画之外的状态
	* none 不改变默认行为
	* forwards 动画完成后，保持最后一个属性（最后一帧）
	* backwards 保持动画第一帧
	* both 向前向后模式都被应用