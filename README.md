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