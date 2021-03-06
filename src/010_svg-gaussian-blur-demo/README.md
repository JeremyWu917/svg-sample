# `SVG` 滤镜
> `SVG` 滤镜用来向形状和文本添加特殊的效果

## `SVG` 滤镜
Params|
-|-
`feBlend`|
`feColorMatrix`|
`feComponentTransfer`|
`feComposite`|
`feConvolveMatrix`|
`feDiffuseLighting`|
`feDisplacementMap`|
`feFlood`|
`feGaussianBlur`|
`feImage`|
`feMerge`|
`feMorphology`|
`feOffset`|
`feSpecularLighting`|
`feTile`|
`feTurbulence`|
`feDistantLight`|
`fePointLight`|
`feSpotLight`|
**注释**：可以在每个`SVG`元素上使用多个滤镜！

## `SVG` 高斯模糊
> 必须在 `defs` 标签中定义 `SVG` 滤镜

- `<filter>` 标签用来定义 `SVG` 滤镜。
- `<filter>` 标签使用必需的 `id` 属性来定义向图形应用哪个滤镜？
- `<filter>` 标签必须嵌套在 `<defs>` 标签内。
- `<defs>` 标签是 `definitions` 的缩写，它允许对诸如滤镜等特殊元素进行定义。

```svg
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

<svg width="100%" height="100%" version="1.1"
xmlns="http://www.w3.org/2000/svg">

<defs>
<filter id="Gaussian_Blur">
<feGaussianBlur in="SourceGraphic" stdDeviation="3" />
</filter>
</defs>

<ellipse cx="200" cy="150" rx="70" ry="40"
style="fill:#ff0000;stroke:#000000;
stroke-width:2;filter:url(#Gaussian_Blur)"/>

</svg>
```
**代码解释**：
- `<filter>` 标签的 `id` 属性可为滤镜定义一个唯一的名称（同一滤镜可被文档中的多个元素使用）
- `filter:url` 属性用来把元素链接到滤镜。当链接滤镜 `id` 时，必须使用 # 字符
- 滤镜效果是通过 `<feGaussianBlur>` 标签进行定义的。`fe` 后缀可用于所有的滤镜
- `<feGaussianBlur>` 标签的 `stdDeviation` 属性可定义模糊的程度
- `in="SourceGraphic"` 这个部分定义了由整个图像创建效果

