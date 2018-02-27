# modern-normalize

「 规范化浏览器的默认样式 」

[![explain](http://llever.com/explain.svg)](https://github.com/chinanf-boy/Source-Explain)
    
Explanation

> "version": "1.0.0"

[github source](https://github.com/sindresorhus/modern-normalize)

~~[english](./README.en.md)~~

---

## 与[`normalize.css`](https://github.com/necolas/normalize.css)不同

-   小
-   仅包括最新的Chrome,Firefox和Safari的标准化
-   [设置 `box-sizing: border-box`](https://www.paulirish.com/2012/box-sizing-border-box-ftw/)
-   [提高了默认字体的一致性](https://github.com/sindresorhus/modern-normalize/issues/3)
-   [设置更可读的标签大小](https://github.com/sindresorhus/modern-normalize/issues/17)

---

> 对于 css 来说, 很多东西更像是`经验之谈`, 我们比较能控制的也就只有实现`效果`, 一般-`css属性本身-实现-`很少涉及

> 所以, 总得来说, 大家理解一下, 问题, 解决-问题, 就够, 当然目标可以是-`css 专家啦`-:P

---

本文解释分三类

比如

``` css
*, 
*::before,
*::after {
	box-sizing: inherit; 
}
```

1. `*` <kbd>css选择器</kbd>

2. `::before` <kbd>css伪类</kbd>

3. `box-sizing` <kbd>css属性</kbd>

---

## package

``` json
	"main": "modern-normalize.css",
```

~~[更多信息](#dev-tool)~~

## > modern-normalize.css

---

### 1. Document

<details>

``` css
*,
*::before,
*::after {
	box-sizing: inherit; 
	/* 继承 box-sizing 属性 */
    /* 
    html {
	box-sizing: border-box;
} */
}
```

#### 1.1 [`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before) 

> [codepen例子](https://developer.mozilla.org/en-US/docs/Web/CSS/::before#Examples)

</details>

---

### 2. html


<details>

``` css
/*! modern-normalize | MIT License | https://github.com/sindresorhus/modern-normalize */

/* Document
   ========================================================================== */

/**
 * Use a better box model (opinionated).
 */

html {
	box-sizing: border-box;
}

/**
 * Correct the line height in all browsers.
 */

html {
	line-height: 1.15;
}


```

#### 2.1 [box-sizing](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing)

> 属性用于更改用于计算元素宽度和高度的默认的 CSS 盒子模型

> 为什么应该 [将所有的元素的box-sizing都设为border-box。](https://css-tricks.com/international-box-sizing-awareness-day/)

#### 2.2 `line-height`

> [它指定元素内行的最小高度-例子>>](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)

</details>

---

### 3. root

<details>

``` css
/**
 * Use a more readable tab size (opinionated).
 */

:root {
	-moz-tab-size: 4;
	tab-size: 4;
}

```

#### 3.1 :root

> :root 这个 CSS 伪类 匹配文档树的根元素。对于 HTML 来说， :root 表示 html 元素，除了 优先级 更高之外，与 html 选择器相同。

#### 3.2 tab-size

> [CSS 属性 tab-size 用于自定义制表符 (U+0009) 的宽度。](https://developer.mozilla.org/en-US/docs/Web/CSS/tab-size)

</details>


---

### 4. Sections

<details>

``` css

/* Sections
   ========================================================================== */

/**
 * Remove the margin in all browsers.
 移除 所有浏览器上 的 margin
 */

body {
	margin: 0;
}

/**
 * 提高所有浏览器中默认字体的一致性
 . (https://github.com/sindresorhus/modern-normalize/issues/3)
 */

body {
	font-family:
		-apple-system,
		BlinkMacSystemFont,
		'Segoe UI',
		Roboto,
		Helvetica,
		Arial,
		sans-serif,
		'Apple Color Emoji',
		'Segoe UI Emoji',
		'Segoe UI Symbol';
}

/**
 修正Chrome，Firefox和Safari中
 
 `section`和`article`上下文中
 
 `h1`元素的字体大小和边距。
 */

h1 {
	font-size: 2em;
	margin: 0.67em 0;
}

``` 

#### 4.1 `-apple-system`

> ios 字体 ？？？

#### 4.2 [`em` 动态计量单位 更多>>](#em)

> 默认 1em = 16px，2em = 32px

</details>

---

### 5. Grouping-content

<details>


```css
/* Grouping content
   ========================================================================== */

/**
 * 在Firefox中添加正确的高度.
 */

hr {
	height: 0;
}

```

#### 5.1 `hr`

> hr 是一个 空元素. 在 `github` 中 markdown 文件 `---` 就是 `<hr>` 

<hr>

> 显示 一条线


</details>

---

### 6. Text-level-semantics

<details>

```css
/* Text-level semantics
   ========================================================================== */

/**
 * 在Chrome，Edge和Safari中
 
 	添加正确的文字修饰。
 */

abbr[title] {
	text-decoration: underline dotted;
}

/**
 * 添加正确的字体粗细 in Chrome, Edge, and Safari.
 */

/*  */
b,
strong {
	font-weight: bolder;
}

/**
 * 1. 提高所有浏览器中默认字体的一致性
 . (https://github.com/sindresorhus/modern-normalize/issues/3)
 * 2.纠正所有浏览器中奇怪的'em`字体大小.
 */

code,
kbd,
samp,
pre {
	font-family: SFMono-Regular, Consolas, 'Liberation Mono', Menlo, Courier, monospace; /* 1 */
	font-size: 1em; /* 2 */
}

/**
 * 在所有浏览器中添加正确的字体大小.
 */

small {
	font-size: 80%;
}

```

#### 6.1 [abbr](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/abbr)

> 使用该 `title` 属性来定义缩写的完整描述。

``` html
<abbr title="Laugh Out Loud">LOL</abbr>
```

<abbr title="Laugh Out Loud">LOL</abbr>

---

#### 6.2 text-decoration

> [指定的文本使用的装饰线条的外观](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration)

---

#### 6.3 code

> 显示其内容在旨在表示该文本是计算机代码的一个短期片段的方式称呼

```html
<code>selectAll()</code>
```
<code>selectAll()</code>

---

#### 6.4 [kbd](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/kbd)

> 代表嵌入式文本从一个键盘，语音输入，或任何其他文本输入设备，表示文本的用户输入的跨度

``` html
<kbd>help mycommand</kbd>
```
<kbd>help mycommand</kbd>

---

#### 6.5 samp

> 用来包围从一个计算机程序，其表示样品嵌入式文本（或引用）的输出

``` html
<samp>Scan complete. Found <em>N</em> results.</samp>
```
<samp>Scan complete. Found <em>N</em> results.</samp>

#### 6.6 pre

> 代表预格式化文本将被准确地呈现写在HTML文件

> 此元素内的空白显示为已写入

``` html
<!-- Some example CSS code -->
<pre>
body {
  color:red;
}
</pre>
```

<pre>
body {
  color:red;
}
</pre>

---

``` css
/**
 * 防止`sub`和`sup`元素影响行中的高度
  所有浏览器。
 */

sub,
sup {
	font-size: 75%;
	line-height: 0;
	position: relative;
	vertical-align: baseline;
}

sub {
	bottom: -0.25em;
}

sup {
	top: -0.5em;
}
```

#### 6.7 [sub](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sub)

> sub 下标

``` html
Mason<sub>1</sub> 
```
Mason<sub>1</sub> 

#### 6.8 [sup](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/sup)

> sup 上标

``` html
<var>E</var>=<var>m</var><var>c</var><sup>2</sup>
```
<var>E</var>=<var>m</var><var>c</var><sup>2</sup>

</details>

---

### 7. Forms

<details>

``` css

/* Forms
   ========================================================================== */

/**
 * 1. 更改所有浏览器中的字体样式.
 * 2. 删除 Firefox 和 Safari 中的边距.
 */

button, 
input,
optgroup,
select,
textarea {
	font-family: inherit; /* 1 */
	font-size: 100%; /* 1 */
	line-height: 1.15; /* 1 */
	margin: 0; /* 2 */
}

/**
 * 删除 Edge 和 Firefox text transform 的继承.
 * 1. 删除 Firefox text transform 的继承.
 */

button,
select { /* 1 */
	text-transform: none;
}

/**
 * 纠正无法在iOS和Safari中设置可点击类型的风格。
 */

button,
[type='button'],
[type='reset'],
[type='submit'] {
	-webkit-appearance: button;
}

/**
 * 在Firefox中删除内部边框和填充.
 */

button::-moz-focus-inner,
[type='button']::-moz-focus-inner,
[type='reset']::-moz-focus-inner,
[type='submit']::-moz-focus-inner {
	border-style: none;
	padding: 0;
}

/**
 * 恢复先前规则未设置的焦点样式.
 */

button:-moz-focusring,
[type='button']:-moz-focusring,
[type='reset']:-moz-focusring,
[type='submit']:-moz-focusring {
	outline: 1px dotted ButtonText;
}


```

#### 7.1 [button](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button)

> 表示一个可点击的按钮

```
<button name="button">Click me</button>
```
<button name="button">Click me</button> 

---

#### 7.2 [input](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

> 使用，以接受来自用户的数据，以创建基于web的表单交互控制。

``` html
<input id="input1" type="text">
```

<input id="input1" type="text">

---

#### 7.3 [`optgroup`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup)

> 该HTML `<optgroup>`元素产生的内选择一组`<select>`元素。

``` html
<select>
  <optgroup label="Group 1">
    <option>Option 1.1</option>
  </optgroup> 
  <optgroup label="Group 2">
    <option>Option 2.1</option>
    <option>Option 2.2</option>
  </optgroup>
  <optgroup label="Group 3" disabled>
    <option>Option 3.1</option>
    <option>Option 3.2</option>
    <option>Option 3.3</option>
  </optgroup>
</select>
```

<select>
  <optgroup label="Group 1">
    <option>Option 1.1</option>
  </optgroup> 
  <optgroup label="Group 2">
    <option>Option 2.1</option>
    <option>Option 2.2</option>
  </optgroup>
  <optgroup label="Group 3" disabled>
    <option>Option 3.1</option>
    <option>Option 3.2</option>
    <option>Option 3.3</option>
  </optgroup>
</select>

---

#### 7.4 [`select`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select)

>HTML `<select>`元素表示，其提供选项菜单的控制：

``` html
<select name="text"> <!--Supplement an id here instead of using 'text'-->
  <option value="value1">Value 1</option> 
  <option value="value2" selected>Value 2</option>
  <option value="value3">Value 3</option>
</select>
```

<select name="text"> <!--Supplement an id here instead of using 'text'-->
  <option value="value1">Value 1</option> 
  <option value="value2" selected>Value 2</option>
  <option value="value3">Value 3</option>
</select>

---

#### 7.5 [`textarea`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea)

> 表示一个多行纯文本编辑控制。

``` html
<textarea name="textarea"
   rows="10" cols="50">Write something here</textarea>
```

<textarea name="textarea"
   rows="10" cols="50">Write something here</textarea>

---

#### 7.6  text-transform

> [CSS属性指定如何利用元素的文本 >>](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)

#### 7.7 [type='button']

> css 匹配 带有 `type` 属性 == `button` 的 element

比如 `<input type="button">`

---

[type="button" jsbin-demo](http://jsbin.com/tujazop/1/edit?html,css,output)

---
> 如上 - 解释 `[type='reset']`


> 如上 - 解释 `[type='submit']`

---

#### 7.8 [`-webkit-appearance`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/-moz-appearance)

>  以基于操作系统主题的平台本地样式显示元素。

#### 7.9 [`::-moz-focus-inner`]

> ???

#### 7.10 [`:-moz-focusring`]

> 非标准: 此功能是非标准的，不在标准轨道上。不要在面向Web的生产站点上使用它：它不适用于每个用户。实现之间也可能存在很大的不兼容性，并且行为在未来可能会发生变化。

> [codepen例子 - 在 firefox 中打开](https://codepen.io/china-boy/pen/gvBjJr)

---



``` css
/**
 * 修正Firefox中的 padding.
 */

fieldset {
	padding: 0.35em 0.75em 0.625em;
}

/**
 * 删除填充，以便在开发人员将它们清零时不会被捕获
 *    `fieldset` elements in all browsers.
 */

legend {
	padding: 0;
}

/**
 * 添加正确的垂直对齐 in Chrome and Firefox.
 */

progress {
	vertical-align: baseline;
}

/**
 *  更正增量和减量按钮的光标风格in Chrome.
 */

[type='number']::-webkit-inner-spin-button,
[type='number']::-webkit-outer-spin-button {
	height: auto;
}

/**
 * 1. 纠正奇怪的外观 in Chrome and Safari.
 * 2. 修正 outline 样式 in Safari.
 */

[type='search'] {
	-webkit-appearance: textfield; /* 1 */
	outline-offset: -2px; /* 2 */
}

/**
 * 在MacOS上删除Chrome和Safari中的内部填充.
 */

[type='search']::-webkit-search-decoration {
	-webkit-appearance: none;
}

/**
 * 1. 纠正无法在iOS和Safari中设置可点击类型的风格.
 * 2. 字体属性更改为“继承” in Safari.
 */

::-webkit-file-upload-button {
	-webkit-appearance: button; /* 1 */
	font: inherit; /* 2 */
}

```

#### 7.11 `fieldset`

> 被用于组数控制以及标签（`<label>`一个web表单内）。

#### 7.12 `legend`

> 代表其父内容的标题`<fieldset>`。

#### 7.13 `progress`

> 显示表示任务的完成进度，通常显示为进度条的指示符。

---

[`fieldset`+`legend`+`progress` jsbin-demo](http://jsbin.com/tujazop/1/edit?html,css,output)

---


#### 7.14 `[type='number']`

> css 匹配 带有 `type` 属性 == `number` 的 element

> [如上解释-`[type='search']`]

---

[jsbin例子](http://jsbin.com/tujazop/2/edit?html,css,output)

---

#### 7.15 [`::-webkit-inner-spin-button`](https://developer.mozilla.org/en-US/docs/Web/CSS/::-webkit-inner-spin-button)

> 用于风格号选择器的输入元件的旋转器按钮的内部部分。h

#### 7.16 `::-webkit-search-decoration`

> 查询详述 ??

#### 7.17 [`::-webkit-file-upload-button`](https://developer.mozilla.org/en-US/docs/Web/CSS/::-webkit-file-upload-button)

> 文件上传按钮, 省略了前缀, 全

``` css
input[type=file]::-webkit-file-upload-button {
  border: 1px solid grey;
  background: #FFFAAA;
}
```

> 这个伪元素是非标准的，并且只支持WebKit / Blink兼容的浏览器，如Chrome，Opera和Safari（用-webkit前缀表示）


</details>



---

### 8. Interactive

<details>

```css

/* Interactive
   ========================================================================== */

/*
 * 添加正确的显示 in Chrome and Safari.
 */

summary {
	display: list-item;
}

```

#### 8.1 summary

> 一个`<details>`元素的一个内容的摘要，标题或图例

正如 `>详细信息`

``` html
<details>
<summary>详细🔎信息</summary>	
</details>
```
<details>
<summary>详细🔎信息</summary>	
</details>

</details>

---

## 	其他

### em

em值的大小是动态的。

定义font-size属性时，em等于适用于所讨论元素的父级的字体大小。

如果您没有在页面上的任何位置设置字体大小，那么它就是浏览器的默认值，通常为16px。所以，默认1em = 16px，2em = 32px。

如果您font-size在body元素上设置了20px，那么1em = 20px和2em = 40px。请注意，值 2 基本上是当前em大小的乘数。

为了计算所需的任何像素值的em等效值，可以使用以下公式：

```
em = 所需要 element 像素 值 / 父 element font-size 「 像素单位 」
```

[mdn-`em`-说明](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size#Possible_approaches)

## dev-tool