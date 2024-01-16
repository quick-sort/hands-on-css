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