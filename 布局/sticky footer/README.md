## 贴紧底部
信息高度是无法预定的,有可能溢出window高度,也可能少于window高度,但底部部分,当信息高度少于window高度,要固定在底部.可是开发者必须跨越的难点.可以使用定位or弹性盒子.
### 定位
```
	<style type="text/css">
		.page{
			position: absolute;
			width: 100%;
		}

		.content{
			width: 100%;
			min-height: 100%;
			box-sizing: border-box;
			padding-bottom: 100px;
		}

		.foot{
			height: 100px;
			background-color: #f00000;
			margin-top: -100px;
		}
	</style>

<body>
	<div class="page">
		<div class="content"></div>
		<div class="foot"></div>
	</div>
</body>
```
在父容器设绝对定位,在设高度为100%,当信息高度少于window高度,这样容器的高就和屏幕的高相等.<br/>
把内容容器设为最小高度为100%,怪异盒子,在设置底填充.<br/>
最后底部容器定位在内容容器的填充里.

### 弹性盒子
```
		.page{
			position: absolute;
			width: 100%;
			min-height: 100%;
			display: flex;
			flex-direction: column;
		}

		.content{
			flex: 1;
		}

		.foot{
			flex: 0 0 100px;
			height: 100px;
			background-color: #f00000;
		}
 ```
 在父容器绝对定位后设最小高度100%,当信息高度少于window高度,它的高就与屏幕的高相同.<br/>
 在把弹性布局设为上到下方向
