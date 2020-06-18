# Flex container

## 一、Flex-direction

> flex items 默认都是沿着**main axis**（主轴）从**main start** 开始往**main end** 方向排布

**flex-direction决定了main axis的方向**，有4个取值

#### row（默认值）：主轴方向从左到右

<img src="/row.png" style="zoom:50%;" />

#### row-reverse：主轴方向从右向左

<img src="/row-reverse.png" style="zoom: 50%;" />

#### column：主轴方向从上往下



<img src="/column.png" style="zoom:50%;" />

#### column-reverse：主轴的方向从下往上

<img src="/column-reverse.png" style="zoom:50%;" />

## 二、Justify-content

> justify-content决定了**flex items**在**main axis**上的对齐方式

#### 1. flex-start(默认值): 与main start对齐

#### 2. flex-end：与main end对齐

#### 3. center：居中对齐

#### 4. space-between：

* flex items之间的距离相等
* 于main-start、main-end的对齐

#### 5. space-evently:

* flex items之间的距离相等
* flex items与main start，main end 之间的距离等于flex items之间的距离

#### 6. space-around：

* flex items 之间的距离相等
* flex items与main start，main end 之间的距离是flex items之间距离的一半



## 三、align-items

> align-items决定了flex items在cross axis上的对齐方式

#### 1. normal：在弹性布局中，效果和stretch一样

#### 2. stretch：

* 当flex items在cross axis方向的size为auto时，会自动拉伸至填充flex container

#### 3. flex-start：与cross start对齐

#### 4. flex-end： 与cross end对齐

#### 5. center：居中对齐

#### 6. baseline：与基准线对齐



## 四、flex-wrap

> flex-wrap 决定了flex container是单行还是多行

#### 1. nowrap（默认）：单行

#### 2. wrap：多行

#### 3. wrap-reverse：多行（对比wrap，cross start和cross end相反）



## 五、flex-flow

> 缩写属性，是flex-direction，flex-wrap的缩写



## 六、align-centent

> align-content 决定了多行flex items在cross axis上的对齐方式，用法与justify-content类似

stretch（默认值）：与align-items的stretch类似

#### 1.flex-start：与cross start对齐

#### 2.flex-end：与cross end对齐

#### 3.center：居中对齐

#### 4.space-between：

* flex items之间的距离相等
* 与cross start、cross end两端对齐

#### 5.space-around：

* flex items之间的距离相等
* flex items与cross start、cross end之间的距离是flex items之间距离的一半

#### 6.space-evenly：

* flex items之间的距离相等
* flex items与cross start、cross end之间的距离是flex items之间距离相等



# Flex items

### 一、order

> order 决定了flex items的排布顺序

* 可以设置任意整数（正整数、负整数、0），值越小就越排靠前
* 默认值是0

### 二、align-self

> flex items可以通过align-self覆盖flex container设置的align-items

* auto（默认值）：遵从flex container的align-items设置
* stretch、flex-start、flex-end、center、baseline，效果跟align-items一致

### 三、flex-grow

1. flex-grow决定了flex items如果扩展

* 可以设置任意非负数字（正小数、正整数、0），默认值是0
* 当flex container在main axis方向上有剩余size时，flex-grow属性才会有效

2. 如果所有flex items的flex-grow综合sum超过1，每个flex item扩展的size为

* flex container的剩余size* flex-grow/sum

3. 如果所有flex items的flex-grow综合不超过1，每个flex item扩展的size为

* flex container的剩余size*flex-grow

4. flex items扩展后的最终size不能超过max-width\max-height

### 四、flex-shrink

* flex-shrink决定了flex items如何收缩
  * 可以设置任意非负数，默认值是1
  * 当flex items在main axis方向上超过了 flex container的size，flex-shrink才会有效
* 如果所有flex items发flex shrink总和超过1，每个flex item收缩的size为
  * flex items超出flex container的size * 收缩比例/所有flex  items的收缩比例之和
* 如果所有flex items的flex-shrink总和sum不超过1，每个flex item收缩的size为
  * flex items超出flex container的size * sum * 收缩比例/所有flex items的收缩比例之和
  * 收缩比例 = flex-shrink * flex item的base size
  * base size 就是flex item放入flex container之前的size

#### 五、flex-basis

* flex-basis 用来设置flex items在main axis方向上的base size

#### 六、flex

> flex 是flex-grow | flex-shrink | flex-basis的简写，flex属性可以指定1个，2个或3个值。