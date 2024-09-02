# `CSS`伪类选择器

- 作用：选中特殊状态的元素

	> "伪"？——虚假的，不是真的
	>
	> "伪类"？——像类（`class`），但不是类，是元素的一种特殊状



## 一、动态伪类

- `:link`超链接==未被访问==的状态
	`:visited`超链接==被访问==的状态
	`:hover`鼠标==悬停==在元素的状态
	`:active`元素==激活==的状态

	> 什么是激活？——按下鼠标不松开
	>
	> 注意点：遵循`LVHA`的顺序，即：`link`、`visited`、`hover`、`active`

	`:focus`获取==焦点==的元素

	> 表单元素才能使用`:focus`伪类
	>
	> 当用户：点击元素、触摸元素、或通过键盘“`tab`”键等方式，选择元素时，就是获取焦点

- 举例：

	```css
	        /* 选中的是没有被访问过的a元素 */
	        a:link {
	            color:aquamarine
	        }
	        /* 选中的是访问过的a元素 */
	        a:visited {
	            color:gray
	        }
	        /* 选中的是鼠标悬浮的a元素 */
	        a:hover {
	            color: yellow;
	        }
	        /* 选中的是激活的a元素 */
	        a:active {
	            color:red
	        }
	        /* 选中的是鼠标悬浮的span元素 */
	        span:hover {
	            color: yellow;
	        }
	        /* 选中的是激活的span元素 */
	        span:active {
	            color:red
	        }
	        /* 选中的是获取焦点的input和select元素 */
	        input:focus,
			select:focus {
	            color: aquamarine;
	            background-color: blueviolet;
	        }
	```

	```html
	    <a href="https://www.baidu.com">去百度</a>
	    <a href="https://www.jd.com">去京东</a>
	    <span>你好</span>
	    <br>
	    <input type="text">
	    <input type="text">
	    <!-- 下拉框 -->
	    <select>
	        <option value="吃">汉堡</option>
	        <option value="喝">可乐</option>
	        <option value="玩">游乐园</option>
	    </select>
	```



## 二、结构伪类

### 1、常用结构伪类

- 常用的：

	- `:first-child` 所有儿子元素中的==第一个==
	- `:last-child`所有儿子元素的==最后一个==
	- `:nth-child(n)`所有儿子元素中的==第n个==
	- `:first-of-type`所有==同类型==儿子元素中==第一个==
	- `:last-of-type`所有==同类型==儿子元素的==最后一个==
	- `:nth-of-type(n)`所有==同类型==儿子元素的==第n个==

- 关于n的值：

	> ​        1、0或不写：什么都没选中   ——几乎不用
	>
	> ​        2、`n`：选中所有子元素     ——几乎不用
	>
	> ​        3、1~正无穷的整数，选中对应序号的子元素
	>
	> ​        4、`2n` 或 `enve` ：选中序号为偶数的子元素
	>
	> ​        5、`2n+1` 或 `odd` ：选中序号为奇数的子元素
	>
	> ​        6、`-n+3` ：选中前三个 （只能写成`an+b`的形式，例如写成`3-n`则不生效）

- 举例：

	```css
	        /* 选中的是div第一个儿子p元素 */
	        div>p:first-child {
	            color: red;
	        }
	        /* 选中的是div的后代p元素，且p的父亲是谁无所谓，但p必须是其父亲的第一个儿子 */
	        div p:first-child {
	            color:red;
	        }
	        /* 选中的是p元素，且p的父亲是谁无所谓，但p必须是其父亲的第一个儿子 */
	        p:first-child {
	            color: red;
	        }
	
	        /* 选中的是div最后一个儿子p元素 */
	        div>p:last-child {
	            color: red;
	        }
	        /* 选中的是div第n个儿子p元素 */
	        div>p:nth-child(3) {
	            color: red;
	        }
	        /* 选中的是div偶数个儿子p元素 */
	        div>p:nth-child(2n) {
	            color: red;
	        }
	
	        /* 选中的是div第一个p这种类型的儿子p元素（必须是同类型的儿子元素） */
	        div>p:first-of-type {
	            color: red;
	        }
	        /* 选中的是div最后个儿子p元素（必须是同类型的儿子元素） */
	        div>p:last-of-type {
	            color: red;
	        }
	        /* 选中的是div第n个儿子p元素（必须是同类型的儿子元素） */
	        div>p:nth-of-type(3) {
	            color: red;
	        }
	```




### 2、不常用结构伪类

- 了解即可

	- `:nth-last-child(n)`所有儿子元素的==倒数第n个==
	- `:nth-last-of-type(n)`所有==同类型==儿子元素的==倒数第n个==
	- `:only-child`选择没有兄弟的元素（独生子女）
	- `:only-of-type`选择没有==同类型==兄弟的元素
	- `:root`根元素（一般指`html`）
	- `:empty`内容为空元素（空格也算内容）

- 举例：

	```css
	        /* 选中的是div倒数第n个儿子p元素 */
	        div>p:nth-last-child(2) {
	            color: red;
	        }
	        /* 选中的是div倒数第n个儿子p元素（必须是同类型的儿子元素） */
	        div>p:nth-last-of-type(4) {
	            color: red;
	        }
	
	        /* 选中的是div中没有兄弟的span元素 */
	        div>span:only-child {
	            color: red;
	        }
	        /* 选中的是div中没有同类型span兄弟的span元素 */
	        div>span:only-of-type {
	            color: red;
	        }
	
	        /* 选中的是根元素 */
	        :root {
	            background-color: aqua;
	        }
	
	        /* 选中的是没有任何内容的div元素 */
	        div:empty {
	            width: 100px;
	            height: 100px;
	            background-color: red;
	        }
	```

	

## 三、否定伪类

`:not(选择器)`排除满足括号中条件的元素

```css
        /* 选中的是div儿子p元素，但排除的是类名为fun的p元素 */
        div>p:not(.fun) {
            color: aquamarine;
        }

        /* 选中的是div儿子p元素，但排除的是title属性值以“u”结尾的 */
        div>p:not([title$="u"]) {
            color: aqua;
        }

        /* 选中的是div儿子p元素，但排除第一个儿子p元素（同类型的） */
        div>p:not(:first-of-type) {
            color: aqua;
        }
```

```html
        <p>李华</p>
        <p>张三</p>
        <p>小明</p>
        <p>李四</p>
        <p class="fun" title="wangwu">王五</p>
        <p class="fun" title="zhaoliu">赵六</p>
```



## 四、`UI`伪类

1. `:checked`被选中的复选框或单选按钮
2. `:enabled`可用的表单元素（没有`disabled`属性）
3. `:disabled`不可用的表单元素（有`disabled`属性）

```css
        /* 选中的是勾选的复选框或单选按钮 */
        input:checked {
            width: 100px;
            height: 100px;
        }
        /* 选中的是被禁用的文本框 */
        input:disabled {
            background-color: gray;
        }
        /* 选中的是可用的文本框 */
        input:enabled {
            background-color: aqua;
        }

```

```html
    <input type="checkbox">
    <input type="radio" name="gender">
    <input type="radio" name="gender">

    <input type="text">
    <input type="text" disabled>
```



## 五、目标伪类

`:target`选中锚点指向的元素

```css
        div {
            height: 300px;
            background-color: aquamarine;
        }
		/* 选中被锚点指向的div */
        div:target {
            background-color: bisque;
        }
```

```html
    <a href="#one">看第1个</a>
    <a href="#two">看第2个</a>
    <a href="#three">看第3个</a>

    <div id="one">第1个</div>
    <div id="two">第2个</div>
    <div id="three">第3个</div>
```



## 六、语言伪类

`:lang()`根据指定的语言选择元素（本质是看`lang`属性的值）

```css
        /* 选中语言为英文的div元素 */
        div:lang(en) {
            color: aqua;
        }
        /* 选中语言为简体中文的所有元素 */
        :lang(zh-CN) {
            color: blanchedalmond;
        }
```

```html
    <div>张三</div>
    <div lang="en">lisi</div>
    <p>王五</p>
    <span>赵六</span>
```

















































