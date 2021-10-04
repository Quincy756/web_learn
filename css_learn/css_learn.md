
目录
- [五类CSS选择器](#五类css选择器)
  - [简单选择器](#简单选择器)
  - [组合器选择器](#组合器选择器)
  - [伪类选择器](#伪类选择器)
  - [伪元素选择器](#伪元素选择器)
  - [属性选择器](#属性选择器)
- [插入css样式的方法](#插入css样式的方法)
  - [优先级排序](#优先级排序)
  - [具体代码](#具体代码)
- [注释](#注释)
- [颜色](#颜色)
  - [颜色名](#颜色名)
  - [rgb](#rgb)
  - [hex](#hex)
  - [hsl](#hsl)
- [背景](#背景)
- [边框](#边框)
  - [样式](#样式)
  - [宽度](#宽度)
  - [圆角](#圆角)
- [边距](#边距)
  - [内外边距](#内外边距)
  - [合并外边距](#合并外边距)
- [宽高](#宽高)
- [轮廓](#轮廓)
- [文本](#文本)
- [字体](#字体)
- [图标](#图标)
- [链接](#链接)
- [列表](#列表)
# [五类CSS选择器](https://www.w3school.com.cn/css/css_selectors.asp)
## 简单选择器
根据名称、id、类来选取元素，类名、id名不能以数字开头

    [标签名]+[.#*]
    .: 类选择
    #: id选择
    *: 全部选择
    ,: 作为一个组都被选择
    p.center: 选择class=center 的p
    p#center: 选择id=center 的p
    p*: 选择所有p标签，设置其为该样式，该样式优先级最低
    p, h: 选择p, h标签
典例

    h, p.m2;
    h, p,.m2;
    h.m2, p.m2;
    h, p .m2;
    h, p#m2;
    h, p*;
    h, p, *;
    ......

## 组合器选择器
根据它们之间的特定关系来选取元素
    后代选择器 (空格)
    子选择器 (>)
    相邻兄弟选择器 (+)
    通用兄弟选择器 (~)

## 伪类选择器
[伪类](https://www.w3school.com.cn/css/css_pseudo_classes.asp)用于定义元素的特殊状态, 不同状态不同样式，根据特定状态选取元素。

    标签 + : + 伪类名
    div : hover   悬停状态的div
    div : lang    不同语言定义不同规则

## 伪元素选择器
选取元素的一部分并设置其样式

    标签 + :: + 伪类名
    div :: first-letter   div首字母
    div :: first-line   div首行

## 属性选择器
[根据属性或属性值来选取元素](https://www.w3school.com.cn/css/css_attribute_selectors.asp)
- 标签 + [attribute="value"]
  
    p[class=class_name]=p.class_name
    p[id=id_name]=p.id_name
    div[color="red"]   颜色为red的div
    div[font-family="黑体"]   字体为黑体的div

- 标签 + [attribute~="value"]

    选择属性名中含有value的标签

- 标签 + [attribute|="value"]
- 标签 + [attribute^="value"]
- 标签 + [attribute$="value"]
- 标签 + [attribute*="value"]

# 插入css样式的方法
## 优先级排序

  - 行内样式（在 HTML 元素中）
  - 外部和内部样式表（在 head 部分）
  - 浏览器默认样式
## 具体代码
- 外部 
  ```html
  <link rel="stylesheet" type="text/css" href="mystyle.css">
  ```
- 内部
  ```html
    <style>
      div{}
    </style>
  ```
- 标签内
  ```html
    <div style="color=redbackground-color=blue">
    </div>
  ```

# 注释
```css
/*这是css注释*/
```
```html
<!-- 这是html注释 -->
```
# 颜色
## 颜色名
color: red
## rgb
(255, 0, 0)
## hex
\#ff0000
## hsl
...

# 背景
- background-color
- background-image
    ```background-image: url("*.png");```
- background-repeat
    沿水平或竖直方向平铺图像
    ``` background-repeat: repeat-x;```
    ``` background-repeat: repeat-y;```
    ``` background-repeat: no-repeat;```
- background-attachment
    指定滚动界面背景是否移动
    ``` background-attachment: fixed;```
    ``` background-attachment: scroll;```
- background-position
    ``` background-position: right top;```
- opacity(不透明度)
- backkground
    简写，要按顺序
    ``` background: red url("*.png") right top;```

# 边框
## 样式
border-style 属性可以设置一到四个值（用于上边框、右边框、下边框和左边框）
<span id="border-style">
```border-style: dotted solid double dashed;```
- dotted - 定义点线边框
- dashed - 定义虚线边框
- solid - 定义实线边框
- double - 定义双边框
- groove - 定义 3D 坡口边框。效果取决于 border-color 值
- ridge - 定义 3D 脊线边框。效果取决于 border-color 值
- inset - 定义 3D inset 边框。效果取决于 border-color 值
- outset - 定义 3D outset 边框。效果取决于 border-color 值
- none - 定义无边框
- hidden - 定义隐藏边框
</span>
## 宽度
<span id="border-width">
border-width 属性可以设置一到四个值（用于上边框、右边框、下边框和左边框）
- 基本单位以 px、pt、cm、em 计
- 预设值: thin、medium、thick
    ```border-width: 10px 20px 30px thin;```
</span>
## 圆角
border-radius 属性可以设置一到四个值（用于上边框、右边框、下边框和左边框）
```border-radius: 5px 2px 8px 10px;```

# 边距
## 内外边距
外边距可简写为
```margin: 5px 2px 8px 10px;```
- margin-top
- margin-right
- margin-bottom
- margin-left
- auto 
- inherit 继承自父类元素
    
内边距可简写为
```padding: 5px 2px 8px 10px;```
- padding-top
- padding-right
- padding-bottom
- padding-left
- auto 
- inherit 继承自父类元素

## 合并外边距
[具体见](https://www.w3school.com.cn/css/css_margin_collapse.asp)


# 宽高
height 和 width 属性不包括内边距、边框或外边距。它设置的是元素内边距、边框以及外边距内的区域的高度或宽度。可设置如下值:
- auto     默认浏览器计算高度和宽度。
- length   以 px、cm 等定义高度/宽度。
- %        以包含块的百分比定义高度/宽度。
- initial  将高度/宽度设置为默认值。
- inherit  从其父值继承高度/宽度。

max-height, min-height
max-width, min-width
![css模型图](resources\css模型.png)


# 轮廓
outline, 轮廓与边框不同！轮廓是在元素边框之外绘制的，并且可能与其他内容重叠。同样，轮廓也不是元素尺寸的一部分；元素的总宽度和高度不受轮廓线宽度的影响。
- outline-style: 同[border-style](#border-style)
- outline-color
- outline-width: 同[border-width](#border-width)
- outline-offset: 在元素的轮廓与边框之间添加空间, 元素及其轮廓之间的空间是透明的。
- outline

# 文本
- background-color
- color
- text-align: center, justify, top, right...
- direction
- unicode-bidi
- vertical-align: 设置元素的垂直对齐方式。
- text-decoration 装饰, 值: none, overline, underline... 
- text-transform 属性用于指定文本中的大写和小写字母。它可用于将所有内容转换为大写或小写字母，或将每个单词的首字母大写。
    ```css
    text-transform: lowercase;
    text-transform: capitalize;
    text-transform: uppercase; 
    ```
间距
- text-indent 指定文本第一行的缩进
- letter-spacing 指定文本中字符之间的间距
- line-height 指定行之间的间距
- word-spacing 指定文本中单词之间的间距
- white-space 指定元素内部空白的处理方式

# 字体
 
- font-family: "Times New Roman", Times, serif;
- font-style 属性主要用于指定斜体文本。
  normal - 文字正常显示
  italic - 文本以斜体显示
  oblique - 文本为“倾斜”（倾斜与斜体非常相似，但支持较少）
- font-weight
  bold, normal
- font-size
  1em 等于当前字体大小。浏览器中的默认文本大小为 16px。因此，默认大小 1em 为 16px。
  可以使用这个公式从像素到 em 来计算大小：pixels/16=em。
  %, px

# 图标
```<i class=...> </i>```
- Font Awesome 图标
  ```<script src="https://kit.fontawesome.com/yourcode.js"></script>```
- Bootstrap 图标
  ```<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">```
- Google 图标
  ```<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">```

# 链接
```<a><\a>```
- a:link  正常的，未访问的链接
- a:visited  用户访问过的链接
- a:hover  用户将鼠标悬停在链接上时
- a:active  链接被点击时

# 列表







  无序 ```<ul> </ul>```
  有序 ```<ol> </ol>```
- list-style-type 属性指定列表项标记的类型, circle, square, 
- list-style-image 属性指定列表项标记为一个图像

















