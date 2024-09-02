# `CSS`表格属性

## 边框相关属性（其他元素也能用）

![](D:\Huawei Share\Screenshot\capture_20240614141215508.bmp)

> 注意：
>
> 	1. 以上四个边框相关属性，其他元素也能用，这是我们第一次遇见他们
> 	1. 在后面的盒子模型中，我们会详细讲解边框相关的知识

- 举例：

	```css
	        table {
	            /* 边框宽度 */
	            border-width: 2px;
	            /* 边框颜色 */
	            border-color: aqua;
	            /* 边框样式 */
	            border-style: dotted;
	        }
	        th,td {
	            /* 边框复合属性 */
	            border: 3px red solid;
	        }
	        /* border属性不仅可以用在表格上，其他属性也能用 */
	        h2 {
	            border: 3px green dashed;
	        }
	        span {
	            border: 3px purple double;
	        }
	```

	

## 表格独有属性（只有`table`标签才能使用）

![](D:\Huawei Share\Screenshot\capture_20240614144911834.bmp)

> 注：以上5个属性，只有表格才能使用，即`<table>`标签

- 举例：

	```css
	    table {
	        /* 控制表格的列宽 */
	        table-layout: fixed;
	        /* 控制单元格间距(生效前提：相邻单元格边框不能合并) */
	        border-spacing: 0px;
	        /* 合并相邻单元格的边框 */
	        border-collapse: collapse;
	        /* 隐藏没有内容的单元格(生效前提：相邻单元格边框不能合并) */
	        empty-cells: hide;
	        /* 设置表格标题的位置 */
	        caption-side: top;
	    }
	```

	























































