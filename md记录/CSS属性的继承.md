### css的继承

* CSS中有些属性是可继承的，何为属性的继承？
  * 一个元素如果没有设置某属性的值，就会跟随**父元素**的值
  * 当然，一个元素如果有设置某属性的值，就使用自己设置的值

* 比如 **color**，**font-size**等属性都是可以继承的
* 究竟哪些属性可以继承，自己随时查文档
* 不能继承的属性，一般可以使用**inherit**值强制继承

#### 继承的注意点

* CSS属性继承的是**计算值**,并不是当初编写属性时的指定值（字面值）

~~~~html
<head>
    <style>
        .box1 {
            font-size: 60px;
        }
        .box2 {
            font-size: 0.5em; // 相当于 30px
        }
    </style>
</head>
<body>
    <div class="box1">
        <div class="box2"><span>這是span內容</span></div>
    </div>
</body>
~~~~

![image-20200608110359800](C:\Users\wupeng\AppData\Roaming\Typora\typora-user-images\image-20200608110359800.png)

![image-20200608110622114](C:\Users\wupeng\AppData\Roaming\Typora\typora-user-images\image-20200608110622114.png)

> 当前span的font-size = 30px  而且inherited from div.box2 ,不是基础的0.5em ,而是 30px
>
> 所以继承是继承的计算值

### CSS属性的层叠

* CSS允许多个相同名字的CSS属性层叠同在一个元素上
  * 层叠后的结果是：只有一个CSS属性会生效

* 浏览器的开发者工具非常清晰地显示了哪个CSS属性会生效

* 哪个CSS属性会生效，取决于CSS属性所处环境的**优先级高低**

#### css属性的优先级

* 按照经验，为了方便比较CSS属性的优先级，可以给CSS属性所处的环境定义一个权重值
  * !important : 10000
  * 内联样式： 1000
  * id选择器：100
  * 类选择器、属性选择器、伪类：10
  * 元素选择器、伪元素：1
  * 通配符：0