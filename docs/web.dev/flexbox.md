# Flexbox

## 使用 Flex 布局执行哪些操作？

* 表格可以显示为行或列。
* 并遵循文档的写入模式。
* 默认情况下，它们是单行，但也可以要求换行。
* 可以在视觉上对布局中的各个项进行重新排序，使其脱离它们在 DOM 中的顺序。
* 空间可以在项内分布，因此它们会根据父级中的可用空间变大或变小。
* 您可以使用 Box Alignment 属性在封装布局中的项和 Flex 线条周围分配空间。
* 项目本身可以在横轴上对齐。

## 主轴和交叉轴

主轴是您的 flex-direction 属性设置的轴。如果值为 row，则主轴沿行，如果为 column，则主轴沿列。
* row：各项内容以行的形式排列。
* row-reverse:，这些项从 Flex 容器末尾排列成一行。
* column：各项内容以列的形式排列。
* column-reverse：这些项从弹性容器末端的一列开始排列。

## 写入模式和方向
```
direction: rtl;
writing-mode: vertical-rl;
```

## 自动换行
```
flex-wrap: nowrap/wrap;
```

## flex-flow 简写形式
简写形式 flex-flow 设置 flex-direction 和 flex-wrap 属性。
```
.container {
  display: flex;
  flex-flow: column wrap;
}
```

## 控制 flex 内容内的空间
* flex-grow: 0：项不会变大。
* flex-shrink: 1：项可以缩小到小于其 flex-basis。
* flex-basis: auto：项的基本大小为 auto。

## flex item 重新排序

```
order: 3;
```

## Flexbox 对齐方式概述

分配空间的属性包括：
* justify-content：主轴上的空间分布情况。
* align-content：横轴上的空间分布情况。
* place-content：设置上述两个属性的简写形式。

用于对齐的属性：
* align-self：在交叉轴上对齐单个项。
* align-items：将所有项作为一个组在交叉轴上对齐。

justify-content 可用的值
* flex-start：与交叉轴的起点对齐。
* flex-end：与交叉轴的终点对齐。
* center：与交叉轴的中点对齐。
* space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
* space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
* space-evenly：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。

align-content可用值多一个：
* stretch（默认值）：轴线占满整个交叉轴。

align-self 可用值
* flex-start
* flex-end
* center
* stretch
* baseline

align-items可用值
* stretch
* flex-start
* flex-end
* center

[flex game](https://flexboxfroggy.com/)