# css
## flex布局
容器里可以嵌套容器，容器下的元素自动成为项目（同一层容器与项目是否能同时在容器中）
### 容器属性
* flex-direction 主轴的方向，row(默认),row-reverse,coloum,coloum-reverse
* flex-wrap 元素超过轴线怎么排列，nowrap(默认),wrap,wrap-reverse
* flex-flow 前两者的简写 row nowrap
* justify-content 主轴对齐方式，flex-start(默认),center,flex-end,space-between,space-around
* align-items 交叉轴对齐方式，属性与主轴一致
* align-content 暂时不理解，待补充
### 项目属性
* align-self 项目的独特对齐方式，覆盖align-items,默认值为auto
* flex-basic 项目占据的主轴空间，默认值为auto即项目的原本大小
* order 属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。
* flex-grow 属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大
* flex-shrink 属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。
* flex 属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。
### 示例代码
``` html
<!DOCTYPE html>
<html>

  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <title></title>
    <style>
     .box{flex:0 0 auto:;justify-content:space-between;display:flex;margin:16px;padding:4px;background-color:#e7e7e7;width:104px;height:104px;object-fit:contain;box-shadow:inset 0 5px white, inset 0 -5px #bbb, inset 5px 0 #d7d7d7, inset -5px 0 #d7d7d7;border-radius:10%}.item{display:block;width:24px;height:24px;border-radius:50%;margin:4px;background-color:#333;box-shadow:inset 0 3px #111, inset 0 -3px #555}.box1{justify-content:center;align-items:center}.box2 > .item:nth-child(2){align-self:flex-end}.box3 > .item:nth-of-type(2){align-self:center}.box3 > .item:nth-of-type(3){align-self:flex-end}.box4{flex-wrap:wrap}.coloum{display:flex;flex-basis:100%;justify-content:space-between}.box4 > .coloum:nth-of-type(2){align-items:flex-end}.box5{flex-wrap:wrap}.box5 > .coloum:nth-of-type(2){justify-content:center;align-items:center}.box6{flex-wrap:wrap}body{display:flex;justify-content:center;flex-wrap:wrap}
    </style>
  </head>

  <body>
    <div class="box box1">
      <span class="item"></span>
    </div>
    <div class="box box2">
      <span class="item"></span>
      <span class="item"></span>
    </div>
    <div class="box box3">
      <span class="item"></span>
      <span class="item"></span>
      <span class="item"></span>
    </div>
    <div class="box box4">
      <div class="coloum">
        <span class="item"></span>
        <span class="item"></span>
      </div>
      <div class="coloum">
        <span class="item"></span>
        <span class="item"></span>
      </div>
    </div>
    
    <div class="box box5">
      <div class="coloum">
        <span class="item"></span>
        <span class="item"></span>
      </div>
      <div class="coloum">
        <span class="item"></span>
      </div>
      <div class="coloum">
        <span class="item"></span>
        <span class="item"></span>
      </div>
    </div>
    
    <div class="box box6">
      <div class="coloum">
        <span class="item"></span>
        <span class="item"></span>
      </div>
      <div class="coloum">
        <span class="item"></span>
        <span class="item"></span>
      </div>
      <div class="coloum">
         <span class="item"></span>
        <span class="item"></span>
      </div>
    </div>
    
  </body>

</html>
```
## 盒模型
* 标准模型和IE模型
* 标准模型和IE模型的区别
### css如何设置这两种模型
* box-sizing:content-box;(默认)
* box-sizing:border-box;
### js如何设置获取盒模型对应的宽高
* dom.style.width/height;
* dom.currentStyle.width/height(只有IE支持);
* window.getComputedStyle(dom).width/height(兼容chrome等其他游览器)；
* dom.getBoundingClientRect().width/height;
### 根据和模型解释边距重叠
 
### BFC（解决方案）
