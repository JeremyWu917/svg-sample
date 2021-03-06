# `SVG` 放射性渐变
> `SVG` 渐变必须在 `<defs>` 标签中进行定义

## 放射性渐变
`<radialGradient>` 用来定义放射性渐变。
`<radialGradient>` 标签必须嵌套在 `<defs>` 中。`<defs>` 标签是 `definitions` 的缩写，它允许对诸如渐变等特殊元素进行定义

```svg
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<defs>
<radialGradient id="grey_blue" cx="50%" cy="50%" r="50%"
fx="50%" fy="50%">
<stop offset="0%" style="stop-color:rgb(200,200,200);
stop-opacity:0"/>
<stop offset="100%" style="stop-color:rgb(0,0,255);
stop-opacity:1"/>
</radialGradient>
</defs>

<ellipse cx="230" cy="200" rx="110" ry="100"
style="fill:url(#grey_blue)"/>


<defs>
<radialGradient id="grey_blue" cx="20%" cy="40%" r="50%"
fx="50%" fy="50%">
<stop offset="0%" style="stop-color:rgb(200,200,200);
stop-opacity:0"/>
<stop offset="100%" style="stop-color:rgb(0,0,255);
stop-opacity:1"/>
</radialGradient>
</defs>

<ellipse cx="230" cy="200" rx="110" ry="100"
style="fill:url(#grey_blue)"/>


</svg>
```

**代码解释**：
`<radialGradient>` 标签的 `id` 属性可为渐变定义一个唯一的名称，`fill:url(#grey_blue)` 属性把 `ellipse` 元素链接到此渐变，`cx`、`cy` 和 `r` 属性定义外圈，而 `fx` 和 `fy` 定义内圈 渐变的颜色范围可由两种或多种颜色组成。每种颜色通过一个 `<stop>` 标签来规定。`offset` 属性用来定义渐变的开始和结束位置。


