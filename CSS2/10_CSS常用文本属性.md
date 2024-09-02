# `CSS`常用文本属性

## 一、文本颜色

- 属性名：`color`

- 可选值：

	1. 颜色名
	2. `rgb` 或 `rgba`
	3. `HEX` 或 `HEXA`（十六进制）
	4. `HSL` 或 `HSLA`

	> 开发中常用的是：`rgb`/`rgba` 或 `HEX`或`HEXA`（十六进制）

- 举例：

	```css
	div {
	    color: rgb(112,45,78);
	}
	```

	

## 二、文本间距

- 字母间距：`letter-spacing`
- 单词间距：`word-spacing`（通过空格识别词）

- 属性值为像素（`px`），正值让间距增大，负值让间距减小

- 举例：

	```css
	        .funny1 {
	            /* 字母间距 单个汉字也会被认为是字母 */
	            letter-spacing: 20px;
	        }
	        .funny2 {
	            /* 单词间距 汉字不会被拉开间距 */
	            word-spacing: 20px;
	        }
	```

	

## 三、文本修饰

- 属性名：`text-decoration`（`decoration`装饰）

- 可选值：

	1. `none`：无修饰线（常用）

	2. `underline`：下划线（常用）

	3. `overline`：上划线

	4. `line-through`：删除线

	可搭配如下值使用：

	1. `dotted`(点缀)：虚线
	2. `wavy`(波浪)：波浪线
	3. 也可指定颜色

- 举例：

	```css
	        .fun1 {
	            /* 上划的红色虚线 */
	            text-decoration: overline dotted red;
	        }
	        .fun2 {
	            /* 下划的黄色波浪线 */
	            text-decoration: underline wavy yellow;
	        }
	        .fun3 {
	            /* 删除线 */
	            text-decoration: line-through;
	        }
	        .fun4 {
	            /* 没有任何样式 */
	            text-decoration: none;
	        }
	```

	

## 四、文本缩进

- 属性名：`text-indent`（`indent`缩进）

- 属性值：`css`中的长度单位，例如`px`，`em`

- 举例：

	```css
	div {
	    text-indent: 40px;
	}
	 .fun1 {
	    text-indent: 2em;
	}
	```

> 后面我们会学习`css`中的一些新的长度单位，目前我们只知道像素（`px`）



## 五、文本对齐--水平

- 属性名：`text-align`（`align`对齐）

- 常用值：

	- `left`：左对齐（默认值）
	- `right`：右对齐
	- `center`：居中对齐

- 举例：

	```css
	div {
	    text-align: center;
	}
	```




## 六、文本对齐--垂直

- **顶部**：无需任何属性，在垂直方向上，默认就是顶部对齐

- **居中**：对于单行文字，让`height = line-height`即可

	> 问题：多行文字垂直居中怎么办？——后面我们用定位去做

- **底部**：对于单行文字，目前一个临时方式：

	让`line-height`=`（height*2）` - `font-size` - `x`

	备注：`x`是根据字体族，动态决定的一个值

	> 问题：垂直方向上的底部对齐，更好的解决方法是什么？——后面我们用定位去做



## 七、文本行高

- 属性名：`line-height`

- 可选值：

	1. `normal`：由浏览器根据文字大小决定的一个默认值
	2. 像素（`px`）
	3. 数字：参考自身`font-size`的倍数（很常用）
	4. 百分比：参考自身`font-size`的百分比

- 备注：由于字体设计原因，文字在一行中，并不是绝对垂直居中，若一行中都是文字，不太会影响观感

- 举例：

	```css
	        .fun1 {
	            /* 第一种写法，值为像素 */
	            line-height: 60px;
	            /* 第二种写法，值为normal */
	            line-height: normal;
	            /* 第三种写法，值为数值 */
	            line-height: 1.5;
	            /* 第四中写法，值为百分比 */
	            line-height: 150%;
	}
	```


- 行高注意事项：

	> 1. `line-height`过小会怎样？——文字产生重叠，且最小值是0，不能为负数
	> 2. `line-height`是可以继承的，且为了能更好的呈现文字，最好写数值
	> 3. `line-height`和`height`是什么关系
	> 	- 设置了`height`，那么高度就是`height`的值
	> 	- 不设置`height`的时候，会根据`line-height`计算高度（`line-height`*行数）

- 应用场景：

	- 对于多行文字：控制行与行之间的距离

	- 对于单行文字：让`height`等于`line-height`，可以实现文字垂直居中

		> 备注：由于字体设计原因，靠上述办法实现的居中，并不是绝对的垂直居中，但如果一行中都是文字，不会太影响观感





## 八、文本对齐--垂直（细说`vertical-align`用法）

- 属性名：`vertical-align`

- 作用：用于指定**同一行元素之间**，或**表格单元格**内文字的**垂直对齐方式**

- 常用值：

	1. `baseline`（默认值）：使元素的基线与父元素的基线对齐
	2. `top`：使元素的顶部与其所在行的顶部对齐
	3. `middle`：使元素的中部与其父元素的基线加上父元素字母`x`的一半对齐
	4. `bottom`：使元素的底部与其所在行的底部对齐

	> 特别注意：`vertical-align`不能控制块元素

























  
