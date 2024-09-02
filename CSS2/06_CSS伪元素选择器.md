# `CSS`伪元素选择器

- 作用：选中元素中的一些特殊位置
- 常用伪元素：
	- `::first-letter`选中元素中的==第一个文字==
	- `::first-line`选中元素中的==第一行文字==
	- `::selection`选中==被鼠标选中==的内容
	- `::placeholder`选中输入框的==提示文字==
	- `::before`在元素==最开始==的位置，创建一个子元素（必须用`content`属性指定内容）
	- `::after`在元素==最后==的位置，创建一个子元素（必须用`content`属性指定内容）

- 举例：

	```css
	        /* 选中的是div中的第一个文字 */
	        div::first-letter {
	            color: red;
	            font-size: 60px;
	        }
	        /* 选中的是div中的第一行文字 */
	        div::first-line {
	            background-color: aqua;
	        }
	        /* 选中的是div中被鼠标选择的文字 */
	        div::selection {
	            color: orange;
	            background-color: green;
	        }
	        /* 选中的是input元素中的提示文字 */
	        input::placeholder {
	            color: skyblue;
	        }
	        /* 选中的是p元素最开始的位置，随后创建一个子元素 */
	        p::before {
	            content: "￥";
	        }
	        /* 选中的是p元素最后的位置，随后创建一个子元素 */
	        p::after {
	            content: ".00";
	        }
	```

	```html
	    <div>Lorem ipsum dolor sit amet consectetur adipisicing.</div>
	    <input type="text" placeholder="请输入您的用户名">
	    <p>199</p>
	    <p>299</p>
	    <p>399</p>
	```

	













