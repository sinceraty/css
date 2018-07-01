# css
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
