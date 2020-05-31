# CSS

### 什么是CSS？

* CSS的作用：可以给网页中的每一个元素设置样式（“化妆”、排版布局），让网页更加精美
* 完全没有使用CSS的网页：基本就是一堆从上到下、从左到右挨在一起的文字和图片
* CSS的全称是Cascading Style Sheets，**层叠样式表**

### 如何将CSS样式应用到元素上？

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

    