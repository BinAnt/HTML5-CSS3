# CSS

<<<<<<< HEAD
### 1、什么是CSS？
=======
### 什么是CSS？
>>>>>>> 55d0817f9e5d31a462ed12e47bd8cc05b6082fa0

* CSS的作用：可以给网页中的每一个元素设置样式（“化妆”、排版布局），让网页更加精美
* 完全没有使用CSS的网页：基本就是一堆从上到下、从左到右挨在一起的文字和图片
* CSS的全称是Cascading Style Sheets，**层叠样式表**

<<<<<<< HEAD
### 2、如何将CSS样式应用到元素上？
=======
### 如何将CSS样式应用到元素上？
>>>>>>> 55d0817f9e5d31a462ed12e47bd8cc05b6082fa0

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

<<<<<<< HEAD
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
=======
    
>>>>>>> 55d0817f9e5d31a462ed12e47bd8cc05b6082fa0
