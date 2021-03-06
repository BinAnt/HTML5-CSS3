# Typora 使用教程

### 1.基本操作

#### 1.1 内容目录

----

* 语法

  `[toc]`

#### 1.2 标题

* 语法

  ~~~~
  # 		一级标题
  ## 		二级标题
  ### 	三级标题
  #### 	四级标题
  ##### 	五级标题
  ###### 	六级标题
  ~~~~

#### 1.3 引用

* 语法

  ~~~~
  > 引用内容1
  > 引用内容2
  >> 引用内容3
  ~~~~

* 效果

  > 引用内容1
  > 引用内容2
  >
  > > 引用内容3

### 2.代码

#### 2.1 单行代码

----

* 语法

  > ```dart
  > `String str1 = "hello";`
  > ```

* 效果

  `String str1 = "hello"`

#### 2.2 多行代码

----

* 语法

  > ~~~~
  > ​~~~~
  > 、、、、
  > ​~~~~java
  > 、、、c
  > ~~~~



* 效果

  ~~~~js
  let a = 10
  let b = 20
  ~~~~

  

### 3.列表

#### 3.1 无序列表

----

* 语法

  ~~~~tex
  * 无序列表1
  + 无序列表2
  - 无序列表3
  ~~~~

* 效果
* 无序列表1
* 无序列表2
* 无序列表3

#### 3.2 多行无序列表

----

* 语法

  ~~~~text
  * 多行无序列表1
  TAB * 多行无序列表2
  TAB TAB * 多行无序列表3
  ~~~~

* 效果

* 多行无序列表1
  * 多行无序列表2
  * 多行无序列表3

#### 3.3 有序列表

----

* 语法

  ~~~~text
  1. 有序列表1
  2. 有序列表2
  3. 有序列表3
  ~~~~

* 效果
  1. 有序列表1
  2. 有序列表2
  3. 有序列表3

#### 3.4 多行有序列表

----

* 语法

  ~~~~text
  1. 多行有序列表1
  2. 多行有序列表2
      1. 多行有序列表2-1
      2. 多行有序列表2-2
  3. 多行有序列表3
      1. 多行有序列表3-1
      2. 多行有序列表3-2
  ~~~~

  

* 效果

  1. 多行有序列表1
  2. 多行有序列表2
      1. 多行有序列表2-1
      2. 多行有序列表2-2
  3. 多行有序列表3
      1. 多行有序列表3-1
      2. 多行有序列表3-2

#### 3.5 任务列表

----

* 语法

  ~~~~text
  -[] 抽烟
  -[x] 喝酒
  -[] 烫头
  ~~~~

  

* 效果

-[] 抽烟
-[x] 喝酒
-[] 烫头

#### 3.6 表格

----

* 语法

  ~~~~text
  |姓名|性别|年龄|手机号|
  |:---|:--:|:--:|---:|
  |张三|男|21|18975346876|
  |李四|女|23|17789548964|
  |王五|男|25|15876513546|
  ~~~~

  

* 效果

| 姓名 | 性别 | 年龄 |      手机号 |
| :--- | :--: | :--: | ----------: |
| 张三 |  男  |  21  | 18975346876 |
| 李四 |  女  |  23  | 17789548964 |
| 王五 |  男  |  25  | 15876513546 |

### 4.链接

#### 4.1 图片

* 语法1（本地图片）

  ~~~~text
  [图片上传失败...(image-61fd19-1520850984854)]
  ~~~~

* 语法2 （网络图片）

  ~~~~text
  ![typora.jpg](https://upload-images.jianshu.io/upload_images/1538862-d91e815790b81e4a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
  ~~~~

* 效果2

  ![typora.jpg](https://upload-images.jianshu.io/upload_images/1538862-d91e815790b81e4a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

  #### 4.2 超链接

  ----

* 语法1 （行内链接）

  ~~~~text
  [百度][https://www.baidu.com/]
  ~~~~

  

* 效果1

[百度][https://www.baidu.com/]

* 语法2（参考式链接）

  ~~~~text
  [CSDN][CSDN网址]
  [CSDN网址]:https://www.csdn.net/
  ~~~~

* 效果2

  [CSDN][CSDN网址]

  [CSDN网址]:https://www.csdn.net/

* 语法3

  ~~~~text
  <https://github.com/>
  ~~~~

  

* 效果3

<https://github.com/>

### 5.其他

#### 5.1斜体

----

* 语法

  ~~~~text
  *斜体*
  _斜体_
  ~~~~

  

* 效果

*斜体*
_斜体_

#### 5.2 加粗

----

* 语法

  ~~~~text
  **加粗**
  __加粗__
  ~~~~

  

* 效果

  **加粗**

  __加出__

#### 5.3 下划线

----

* 语法

  ~~~~text
  <u>下划线</u>
  ~~~~

* 效果

  <u>下划线</u>

#### 5.4 删除线

----

* 语法

  ~~~~text
  ~~删除线~~
  ~~~~

  

* 效果

  ~~删除线~~

#### 5.5 分割线

* 语法

  ~~~~text
  ***
  ---
  ___
  ~~~~

  

* 效果

  ***

  ---

  ___

#### 5.6 注脚

---

* 语法

  ~~~~text
  Typora[^1]
  [^1]A markdown editor
  ~~~~

* 效果

  Typora[^1]
  [^1]A markdown editor

#### 5.7 上下标

---

* 语法

  ~~~~text
  $3^2=9$
  $3^{(3-1)}=9$
  $H_2SO_4$
  $H_{2SO_4}$
  ~~~~

* 效果

  $3^2=9$
  $3^{(3-1)}=9$
  $H_2SO_4$
  $H_{2SO_4}$

#### 5.8 符号的输入

---

* 语法

  ~~~~text
  \\   反斜线
  \`   反引号
  \*   星号
  \_   底线
  \{ \}  花括号
  \[ \]  方括号
  \( \)  括弧
  \#   井字号
  \+   加号
  \-   减号
  \.   英文句点
  \!   惊叹号
  ~~~~

* 效果

  \\   反斜线
  \`   反引号
  \*   星号
  \_   底线
  \{ \}  花括号
  \[ \]  方括号
  \( \)  括弧
  \#   井字号
  \+   加号
  \-   减号
  \.   英文句点
  \!   惊叹号

#### 5.9 特殊符号

---

* 语法

  ~~~~text
  &copy;      版权      
  &reg;       注册商标
  &trade;     商标
  &nbsp;      空格
  &amp;       和号
  &quot;      引号
  &apos;      撇号
  &lt;        小于号
  &gt;        大于号
  &ne;        不等号
  &le;        小于等于
  &ge;        大于等于
  &cent;      分
  &pound;     磅
  &euro;      欧元
  &yen;       元
  &sect;      节
  &times;     乘号
  &divide;    除号
  &plusmn;    正负号
  ~~~~

* 效果

  &copy;      版权      
  &reg;       注册商标
  &trade;     商标
  &nbsp;      空格
  &amp;       和号
  &quot;      引号
  &apos;      撇号
  &lt;        小于号
  &gt;        大于号
  &ne;        不等号
  &le;        小于等于
  &ge;        大于等于
  &cent;      分
  &pound;     磅
  &euro;      欧元
  &yen;       元
  &sect;      节
  &times;     乘号
  &divide;    除号
  &plusmn;    正负号