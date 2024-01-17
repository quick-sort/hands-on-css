# 继承

## 可以继承的属性

* azimuth
* border-collapse
* border-spacing
* caption-side
* color
* cursor
* direction
* empty-cells
* font-family
* font-size
* font-style
* font-variant
* font-weight
* font
* letter-spacing
* line-height
* list-style-image
* list-style-position
* list-style-type
* list-style
* orphans
* quotes
* text-align
* text-indent
* text-transform
* visibility
* white-space
* widows
* word-spacing


## 如何明确继承和控制继承

* inherit 关键字, 使任何属性继承其父项的计算值。使用此关键字的实用方法是创建例外情况。
* initial 关键字, CSS 中的每个属性都有一个默认值。initial 关键字会将属性设置回初始默认值。
* unset 关键字, 无论是否默认继承了某个属性，unset 属性的行为都会有所不同。如果属性在默认情况下是继承的，则 unset 关键字将与 inherit 相同。如果默认情况下不继承该属性，则 unset 关键字等于 initial。