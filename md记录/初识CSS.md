# CSS

### 1、什么是CSS？
* CSS的作用：可以给网页中的每一个元素设置样式（“化妆”、排版布局），让网页更加精美
* 完全没有使用CSS的网页：基本就是一堆从上到下、从左到右挨在一起的文字和图片
* CSS的全称是Cascading Style Sheets，**层叠样式表**

### 2、如何将CSS样式应用到元素上？
* CSS提供了3种方法，可以将CSS样式应用到元素上
  * **内联**样式（inline style）
  * **文档**样式表（document style sheet）、**内联**样式表（embed style sheet）
  * **外部**样式表（external style sheet）

* 内联样式

  * 将样式直接写在元素的style属性上

    ~~~~html
    <div style="color:white;background:red;">文字内容</div>
    ~~~~

  * CSS样式之间用分号；隔开，建议每条CSS样式后面都加上分号；
  * 在很多国内资料中，“CSS样式”与“CSS属性”是同义词
    * 样式名 -> 属性名
    * 样式值 -> 属性值

  * 有些人也把inline翻译为“行内”，其实在这里，用“内联”更合适，表示“内部自带”的意思

* 文档样式表

  * 将样式写在**head**元素之内的**style**元素之内

    ~~~~html
    <head>
        <meta charset="UTF-8">
        <title>CSS学习</title>
        <style type="text/css">
            div {
                color: red;
                font-size: 12px;
            }
        </style>
    </head>
    ~~~~

  * style 的type属性 默认就是 “text/css” ，所以可写可不写

* 外部样式表

  * 将样式单独写在css文件

  * 在当前页面的**head**元素中的**link元素**引用

    ~~~~html
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
        <link rel="stylesheet" href="./css/style.css">
    </head>
    ~~~~

### 3、css文件编码和import引入

* 给css文件设置编码

  ~~~~css
  /*设置文件的编码*/
  @charset "utf-8";
  div {
      color: #ff0000;
      font-family: '微软雅黑';
  }
  ~~~~

* import引入css文件

  * 在head元素中的style元素中导入

    ~~~~html
    <style>
        @import url('./css/base.css');
        @import url('./css/style.css');
    </style>
    ~~~~

  * 在css文件中导入另外一个css文件

    ~~~~css
    /*设置文件的编码*/
    @charset "utf-8";
    /*import导入*/
    @import url('./base.css');
    
    h1{
        background-color: #ff0000;
    }
    ~~~~

  > 按浏览器的解析，link引入比import引入更快

### 4、CSS选择器

#### 4.1 元素选择器

~~~~html
 <style>
     p {
         font-size: 25px;
     }
     h2 {
         color: pink;
     }
     div {
         margin: 10px 0;
         color: purple;
     }
</style>
~~~~

#### 4.2 类选择器

~~~~css
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .c-red {
            color: red;
        }
        .c-green {
            color: green;
        }
        .c-gray {
            color: gray;
        }

        .large-font {
            font-size: 25px;
        }
        .litter-font {
            font-size: 14px;
        }
    </style>
</head>
<body>
    <div class="large-font c-red">这是div</div>
    <p class="c-green">这是内容1</p>
    <h2 class="c-gray">这是内容2</h2>
    <div class="large-font">这是内容3</div>
    <div class="litter-font c-green">这是内容4</div>
</body>
~~~~

* 命名准守见名知意的原则
  * “-” 中横线： large-font
  * “_”下横线: large_font
  * 驼峰 : largeFont

* 一个元素可以有多个class，每个class之间用空格隔开

#### 4.3 id选择器

**id名称** 在一个页面中不能重复

~~~~html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #header {
            height: 100px;
            background-color: red;
        }
        #content {
            height: 200px;
            background-color: grey;
        }
        #footer {
            height: 100px;
            background-color: green;
        }
    </style>
</head>
<body>
    <div id="header">头部</div>
    <div id="content">主体内容</div>
    <div id="footer">页面底部</div>
</body>
~~~~

### 5、最常见的CSS属性

* color: 前景色（文字颜色）
* font-size：文字大小
* background-color：背景色
* width：宽度
* height：高度

### 6、常见的文字属性

#### 6.1 text-decoration

* text-decoration 用于设置文字的装饰线
  * none：无任何装饰线，可以去除a元素默认的下划线
  * underline：下划线
  * overline：上划线
  * line-through：中划线（删除线）

~~~~html
<head>
    <style>
        a {
            text-decoration: none;
            color: #333333;
        }
        .taobao {
            text-decoration: underline;
        }
        p {
            text-decoration: line-through;
        }
    </style>
</head>
<body>
    <!-- text-decoration 可以消除a标签的下划线 -->
    <a href="">百度一下</a>
    <div>
        <a href="#" class="taobao">淘宝</a>
    </div>
    <!--其他元素 使用装饰线-->
    <p>&yen;998</p>
</body>
~~~~

#### 6.2 letter-spacing

#### 6.3 word-spacing

~~~~html
<head>
    <style>
        /*letter-spacing 默认值为0；修改范围内的字符的间距*/
        .p1 {
            letter-spacing: 10px;
        }
        /*word-spacing: 用于声明单词间距，默认是0*/
        .p2 {
            word-spacing: 20px;
        }
        /*letter-spacing,word-spacing 可以设置负数*/
    </style>
</head>
<body>
    <p class="p1">hello world</p>
    <div>hello world</div>
    <p class="p2">hello world</p>
</body>
~~~~

#### 6.4 text-transform

> 指定如何将元素的文本大写

~~~~html
<head>
    <style>
        .text1 {
            text-transform: capitalize;
        }
        .text2 {
            text-transform: uppercase;
        }
        .text3 {
            text-transform: lowercase;
        }
        .text4 {
            text-transform: none;
        }
    </style>
</head>
<body>
    <div class="text1">hello world</div>
    <div class="text2">hello world</div>
    <div class="text3">hello WoRld</div>
    <div class="text4">hello world</div>
</body>
~~~~

效果：

![image-20200601162514571](C:\Users\wupeng\AppData\Roaming\Typora\typora-user-images\image-20200601162514571.png)

#### 6.5 text-indent

> 能定义一个块元素首行文本内容之前的缩进量

~~~~css
.box {
    text-indent: 2em;
}
~~~~



#### 6.6 text-align

> 定义行内内容（例如文字）如何相对它的块父元素对齐
>
> 并不能控制块元素自己的对齐，只控制它的行内内容的对齐。

#### 6.7 font-size

* 常用值和单位

  * px ：12px 绝对值，12个像素大小

  * em: 2em , 相对于**父元素**的文字的大小。

    ~~~~html
    .box {
    	font-size: 20px;
    }
    
    .box .inner {
    	font-size: .5em; // 当前元素的父元素的字体大小的一半  10px
    	font-size: 2em; // 当前元素的父元素的字体大小的一倍  40px
    }
    ~~~~

#### 6.8 font-family

* ```css
  font-family: "Gill Sans Extrabold", sans-serif;
  ```

#### 6.9 font-weight

> 属性指定了字体的粗细程度。 一些字体只提供 `normal` 和 `bold` 两种值

#### 6.10 font-style

> 允许你选择 [`font-family`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-family) 字体下的 `italic` 或 `oblique` 样式

#### 6.11 line-height

**行高的严格定义是：两行文字基线（baseline）之间的间距**

* 注意区分height和line-height的区别
  * height：元素的整体高度
  * line-height：元素中每一行文字所占据的高度
    * 应用实例：假设div中只有一行文字，如何让这行文字在div内部垂直居中

~~~~html
<head>
    <title>Document</title>
    <style>
        /**
            行高 = 文字高度 + 间距
            间距 = line-height - 文字高度

            1、
            间距 = 26.4px - 20 => 6.4px 再上下平分  => 文字距顶部就是3.2px
            这个时候文本框的高度是200px，而文字距顶是3.2px 所以文字这个时候就是靠顶部的

            2、
            当line-height == 文本框height时，文字可以垂直居中
            间距 = 200px - 20px = 180px / 2 = 90px
            这个时候文字距顶90px + 文字的一半高度 20px/2 = 10px 刚好等于100px = 200px/2
            文字就居中了
        */
        .box {
            height: 200px;
            background-color: green;
            font-size: 20px;
            /* line-height: 26.4px; */
            line-height: 200px;
        }
    </style>
</head>
<body>
    <div class="box">hello world!</div>
</body>
~~~~

#### 6.12 font

> `font` 属性可以用来作为 [`font-style`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-style), [`font-variant`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-variant), [`font-weight`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-weight), [`font-size`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-size), [`line-height`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/line-height) 和 [`font-family`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/font-family) 属性的简写，或将元素的字体设置为系统字体

~~~~html
<head>
    <style>
        div {
            /* font-style: italic;
            font-variant: small-caps;
            font-size: 30px;
            font-weight: 700;
            line-height: 50px;
            font-family: serif; */

              		/* style variant weight size/line-height family*/
            /* font: italic small-caps bold 30px/50px '宋体'; */

            /* style variant weight 这三项可以位置可以互换，也可以省略*/
            /* font: 30px/50px '宋体'; */

            /*line-height也可以省略*/
            font: 30px '宋体';

            background-color: green;
            height: 100px;
        }
    </style>
</head>
<body>
    <div>
        这是一个div
    </div>
</body>
~~~~

### 7、其他选择器

#### 7.1 属性选择器

~~~~html
<head>
    <style>
        /*选中全部有title属性的元素*/
        [title] {
            color: red;
        }
        /*划掉title='p元素 one'的元素*/
        [title="p元素 one"] {
            text-decoration: line-through;
        }
        /*title中包含'one'*/
        [title*="one"] {
            font-size: 30px;
        }
        /*以one结尾的title*/
        [title$="one"] {
            font-weight: bold;
        }
        /*以one开头的title*/
        [title^="one"] {
            font-weight: 400;
        }
    </style>
</head>
<body>
    <p title="p元素 one">这是p元素</p>
    <span title="span元素">这是span</span>
    <div title="one div元素">这是div元素</div>
    <p>这又是一个p元素</p>
</body>
~~~~

#### 7.2 后代选择器

* div 元素里面的span元素（包括直接、间接子元素）

  ~~~~html
  div span {
  	color: red;
  }
  
  <div>
      <span>这是span</span>
      <p>
          <span>这又是一个span</span>
      </p>
  </div>
  <span>这是第三个span</span>
  ~~~~

#### 7.3 子选择器（child combinators）

> div 元素里面的直接span子元素（不包括间接子元素）

~~~~html
<span>文字内容1</span>
<div>
    <span>文字内容2</span>
    <p>
        <span>文字内容3</span>
    </p>
</div>
<div>
    <span>文字内容4</span>
</div>
~~~~

~~~~css
div>span {
    color: red;
}

div > span {
    color: red;
}

/*
	文字内容2,文字内容4 才能选中
*/
~~~~

### 8、css属性

#### 8.1 visibility

* visibility,能控制元素的可见性，有2个常用值
  * visible: 显示元素
  * hidden: 隐藏元素
* visibility:hidden 和 display:none的区别
  * visibility:hidden 虽然元素看不见，但元素的框依旧还留着，还会占着原来的位置
  * display:none 不仅元素看不见，而且元素的框也会被移除，不会占着任何位置

#### 8.2 overflow

~~~~html
<head>
    <style>
        .box {
            margin: 0 auto;
            width: 200px;
            height: 200px;

            /* 溢出的内容照样可见 */
            /* overflow: visible; */

            /* 溢出的部分直接裁剪 */
            /* overflow: hidden; */

            /* 溢出的内容被裁剪，但可以滚动机制查看 */
            /* overflow: scroll; */

            /* 自动根据内容是否溢出来决定是否提供滚动机制 */
            /* overflow: auto; */

            /* 还有overflow-x,overflow-y 两个属性可以分别设置水平垂直方向
            建议还是直接使用overflow，因为overflow-x、overflow-y还没有成为标准，浏览器可能不支持 */
            overflow: hidden;
            /* overflow-x: scroll; */
            overflow-y: scroll;
        }
        .box img {
            width: 400px;
        }
    </style>
</head>
<body>
    <div class="box">
        <img src="../img/370262860.gif" alt="">
    </div>
</body>
~~~~

