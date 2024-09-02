# 一、html注释

```html
<!--这里的内容运行不会显示-->
```

注释快捷键：ctrl+/

<!--xxxx-->

注释不可以嵌套



# 二、文档声明

```html
<!DOCTYPE html>
<html>
    <head></head>
    <body></body>
</html>
```

<!DOVTYPE html>

文档声明作用：告诉浏览器我用的是 H5 标准来写的网页
一种标记，仅此而已



doctype

doc:document 文档 

type：类型 



# 三、字符编码

存数据：编码

读数据：解码



UTF-8：万国码

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>html字符编码</title>
    </head>
    <body>
        <input type="text">
    </body>
</html>
```



需要提前声明 ==解码== 用的字符集

UTF-8（不区分大小写）

<meta charset="UTF-8">

charset：字符集

浏览器默认也是UTF-8字符集



# 四、设置语言

  ```html
  <!DOCTYPE html>
  <html lang="en">
      <head>
          <meta charset="UTF-8">
          <title>
              hhhhh 
          </title>
      </head>
      <body>
          <marquee>hhhhhh</marquee>
      </body>
  </html>
  ```



<html lang="en">

lang="en"：英文

lang="en-US"：英语-美国

lang="en-GB"：英语-英国

lang="zh"：中文

lang="zh-CN"：简体中文（中国大陆）

lang="zh-TW"：繁体中文（中国台湾地区）



lang：language语言



具体可参考下面链接

[w3school](http://www.w3school.com.cn/)







































