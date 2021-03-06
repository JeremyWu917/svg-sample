# `SVG` `<rect>`

## `SVG` 形状
> `SVG` 有一些预定义的形状元素，可被开发者使用和操作

- 矩形 `<rect>`
- 圆形 `<circle>`
- 椭圆 `<ellipse>`
- 线 `<line>`
- 折线 `<polyline>`
- 多边形 `<polygon>`
- 路径 `<path>`

## `rect` 标签
> `rect` 标签可用类创建矩形，以及矩形的变种

```svg
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<rect width="300" height="100" x="2" y="2"
style="fill:rgb(0,0,255);stroke-width:1;
stroke:rgb(0,0,0)"/>

<rect x="20" y="200" width="250" height="250"
style="fill:blue;stroke:pink;stroke-width:5;
fill-opacity:0.1;stroke-opacity:0.9"/>

<rect x="360" y="20" width="250" height="250"
style="fill:blue;stroke:pink;stroke-width:5;
opacity:0.9"/>

<rect x="640" y="20" rx="20" ry="20" width="250"
height="100" style="fill:red;stroke:black;
stroke-width:5;opacity:0.5"/>

</svg>
```
**代码解释**
- `rect` 元素的 `width` 和 `height` 属性可定义矩形的高度和宽度
- `style` 属性用来定义 `CSS` 属性
- `CSS` 的 `fill` 属性定义矩形的填充颜色（`rgb` 值、颜色名或者十六进制值）
- `CSS` 的 `stroke-width` 属性定义矩形边框的宽度
- `CSS` 的 `stroke` 属性定义矩形边框的颜色
- `x` 属性定义矩形的左侧位置（例如，x="0" 定义矩形到浏览器窗口左侧的距离是 0px）
- `y` 属性定义矩形的顶端位置（例如，y="0" 定义矩形到浏览器窗口顶端的距离是 0px）
- `CSS` 的 `fill-opacity` 属性定义填充颜色透明度（合法的范围是：0 - 1）
- `CSS` 的 `stroke-opacity` 属性定义笔触颜色的透明度（合法的范围是：0 - 1）
- `CSS` 的 `opacity` 属性定义整个元素的透明值（合法的范围是：0 - 1）
- `rx` 和 `ry` 属性可使矩形产生圆角

