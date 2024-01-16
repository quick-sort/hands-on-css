# 选择器

使用 CSS 选择器查找该特定元素，并应用 CSS 规则，如下所示。CSS 规则的组成部分
```css
article p:first-of-type {
  color: red;
  font-size: 1.5em;
}
```

## 选择器类型
* 通用选择器

匹配所有元素
```css
* {
  color: hotpink;
}
```

* 类型选择器
```css
section {
  padding: 2em;
}
```

* 类选择器
```html
<div class="my-class"></div>
<button class="my-class"></button>
<p class="my-class"></p>
```
```css
.my-class {
  color: red;
}
```
```html
<div class="my-class another-class some-other-class"></div>
```

* ID 选择器
```css
#rad {
  border: 1px solid blue;
}
```

匹配元素
```html
<div id="rad"></div>
```

* 属性选择器
```css
[data-type='primary'] {
  color: red;
}
```

```html
<div data-type="primary"></div>
```

```css
[data-type] {
  color: red;
}
```

```html
<div data-type="primary"></div>
<div data-type="secondary"></div>
```

* 分组选择器
```
strong,
em,
.my-class,
[lang] {
  color: red;
}
```

* 伪类
HTML 元素会处于各种状态，这可能是因为它们进行了互动，或者其中一个子元素处于特定状态。例如，用户可以将鼠标指针悬停在 HTML 元素上，或者，用户也可以将子元素悬停。对于这些情况，请使用 :hover 伪类。
```
/* Our link is hovered */
a:hover {
  outline: 1px dotted green;
}

/* Sets all even paragraphs to have a different background */
p:nth-child(even) {
  background: floralwhite;
}
```

* 伪元素

伪元素与伪类不同，因为它们不会响应平台状态，而是像是在通过 CSS 插入新元素一样。伪元素在语法上也与伪类不同，因为我们使用的是双冒号 (::)，而不是使用单冒号 (:)。

```
.my-element::before {
  content: 'Prefix - ';
}
```

不过，伪元素不限于插入内容。您也可以使用它们来定位元素的特定部分。例如，假设您有一个列表。使用 ::marker 设置列表中的每个项目符号（或编号）样式

```
/* Your list will now either have red dots, or red numbers */
li::marker {
  color: red;
}
::selection {
  background: black;
  color: white;
}
```

* 后代组合符
后代组合符可用于定位子元素。以下代码使用空格 () 指示浏览器查找子元素：
```
p strong {
  color: blue;
}
```

* 下一个同级组合符
您可以在选择器中使用 + 字符，查找紧跟在另一个元素的元素。

* 后续 - 同级组合符
后续组合器与下一个同级选择器非常相似。不过，请使用 ~ 字符，而不是 + 字符。其区别在于，只要一个元素只需跟随父元素相同的另一个元素，而不必跟随父元素一起变为下一个元素。

* 子组合符
子组合器（也称为“直接后代”）可让您更好地控制组合器选择器附带的递归。通过使用 > 字符，您可以将组合器选择器限制为仅应用于直接子级。