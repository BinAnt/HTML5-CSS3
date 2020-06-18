# 认识flex布局

* flex布局是目前web开发中使用最多的布局方案：
  * flex布局（Flexible布局， 弹性布局）
  * 目前特别流在移动端用的最多，目前PC端也是用越来越多了
* 两个重要概念：
  * 开始了flex布局的元素叫flex container
  * flex container里面的直接子元素叫做flex items
* 设置display属性为flex或inline-flex可以成为flex container
  * flex：flex container 以block-level形式存在
  * inline-flex：flex container 以inline-level形式存在



## flex相关的属性

#### 应用在flex container上的CSS属性

* flex-flow
* flex-direction
* flex-wrap
* justify-content
* align-items
* align-content

#### 应用在flex items上的CSS属性

* flex
* flex-grow
* flex-basis
* flex-shrink
* order
* align-self