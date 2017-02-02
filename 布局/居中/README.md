## 垂直居中
布局居中是开发者的必须跨越的难点,在日常使用频率是个技术里最大的.<br/>
再夸水平居中简单,块状元素可用margin居中,内联元素可text-align居中,但垂直居中呢<br/>
可用定位or表格or弹性布局

### 定位
```
		.layout-center{
			position: absolute;
			top: 50%;
			left: 50%;
			margin: -50px auto 0;
		}
```
注意绝对定位是与其祖先容器那个设相对定位而定位的.

### 表格
```

		.layout-center-child{
			display: table-cell;
			vertical-align: middle;
			text-align: -webkit-center;
		}
```
把容器为表单元素,就可用vertical-align进行居中.

### 弹性盒子
```
		.layout-center-child{
			display: flex;
			align-items: center;
			justify-content: center;
		}
```
万能弹性盒子.
