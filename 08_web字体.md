# `web`字体

## 一、基本用法

可以通过`@font-face`指定字体的具体地址，浏览器会自动下载该字体，这样就不依赖用户电脑上的字体了

- 语法（简写方式）：

	```css
	@font-face {
	    font-family: "手写字体";		//将新引入的字体命名为手写字体
	    src: url("./xxx/xxx.ttf");
	}
	h1 {
	    //调用上面导入的字体
	    font-family: "手写字体";
	}
	```

- 语法（高兼容性写法）

	```css
	@font-face {
	    font-family: "手写字体";
	    font-display: swap;
	    src: url('./font/webfont.eot'); /* IE9 */
	    src: url('./font/webfont.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
	    	url('./font/webfont.woff2') format('woff2'),
	    	url('./font/webfont.woff') format('woff'), /* chrome、firefox */
	     	url('./font/webfont.ttf') format('truetype'), /* chrome、firefox、opera、Safari, Android, iOS 4.2+*/
	    	url('./font/webfont.svg#webfont') format('svg'); /* iOS 4.1- */
	}
	h1 {
	    font-family: "手写字体";
	}
	```



## 二、定制字体

- 中文的字体文件很大，使用完整的字体文件不现实，通常针对某几个文字进行单独定制
- 可使用阿里`Web`字体定制工具：https://www.iconfont.cn/webfont





## 三、字体图标

- 相比图片更加清晰
- 灵活性高，更方便改变大小、颜色、风格等
- 兼容性高，`IE`也支持

> 字体图标的使用方式，每个平台不尽相同，最好参考平台使用指南，这里建议使用最多的是阿里图标库
>
> 阿里图标官网地址：https://www.iconfont.cn/











































