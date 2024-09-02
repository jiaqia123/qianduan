# `html`全局属性

常用的全局属性

## 1、 `id`

- `id`不能重复，可以比作成人的身份证一样

- 可以让`label`标签与表单控件相关联；也可与`CSS`、`JavaScript`配合使用

- 注：不能在以下`HTML`元素中使用：

	<head>、<html>、<meta>、<script>、<style>、<title>

```html
	<div id="hello1">你好1</div>
    <div id="hello2">你好2</div>

	<input type="radio" name="gender" value="male" id="nan">
    <label for="nan">男</label>
```



## 2、`class`

- 给标签指定签名，进行分类的意思，随后通过`CSS`就可以给标签设置样式
- `class`可重复

```html
	<div class="student">张三</div>
    <div class="student">李四</div>
```



## 3、`style`

- 给标签设置`CSS`样式

```html
	<div style="color: blue">旺财</div>
```



## 4、`dir`

- 表示内容的方向，值：`ltr`(默认)，`rtl`

- 注：不能在以下`HTML`元素中使用：

	<head>、<html>、<meta>、<script>、<style>、<title>

```html
	<bdo dir="rtl">你是年少的欢喜</bdo>
    <div dir="rtl">你是年少的欢喜</div>
```

- 在`bdo`标签中会将文字倒过来显示
	在`div`标签中会将文字右对齐显示



## 5、`title`

- 给标签设置一个文字提示，一般超链接和图片用的比较多

```html
	<div title="英雄联盟">LOL</div>
    <a href="https://www.baidu.com" title="qubaidu">去百度</a>
```



## 6、`lang`

- 给标签指定语言

- 注：不能在以下`HTML`元素中使用：

	<head>、<html>、<meta>、<script>、<style>、<title>



## 7、其他全局属性

[全局属性](https://developer.mozilla.org/zh-CN/docs/Web/HTML)

















































