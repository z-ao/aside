## 箭头
三角形箭头在页面使用比愈发变大,制做也比较简单.

### 三角形
做一个三角形可以使用渐变或边框.

#### 边框
因为边框是有四个三角形构成的.<br/>
可以把两个边框设置为0.<br/>
另外设置背景色是透明.<br/>
最后一个设置想要的三角.

```
			border: 15px solid #f00000;
			border-top: 0;
			border-left: 0;
			border-right: 15px solid transparent;
```

#### 渐变
设置高宽,可用这属性把角度设为45deg<br/>
然后再把容器的一半背景色设置为透明.

```
			height: 15px;
			width: 15px;
			background: linear-gradient(45deg, #f00 50%,transparent 50%);
```

三角是为做箭头做铺垫

### 箭头
在三角设置伪类,然后做定位.或设置背景色为透明,在设边框.
```
		.arrow-border{
			position: relative;
			border: 15px solid #f00000;
			border-top: 0;
			border-right: 15px solid transparent;
			border-left: 0;	
		}

		.arrow-border::after{
			content: "";
			position: absolute;
			left: 3px;
			top: 2px;
			border: 10px solid #fafafa;
			border-top: 0;
			border-right: 10px solid transparent;
			border-left: 0;
		}
```
背景 and 边框
```
.arrow-bg{
			width: 10px;
			height: 10px;
			background-color: transparent;
			border: 2px solid #f00000;
			border-left: 0;
			border-top: 0;
		}
```
