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

本目录



---

## package

``` json
	"main": "modern-normalize.css",
```

[更多信息](#dev-tool)

## >modern-normalize.css

### 1. *

<details>

``` css
*,
*::before,
*::after {
    box-sizing: inherit; 
    /* 
    html {
	box-sizing: border-box;
} */
}
```

</details>

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

- box-sizing

> 

- line-height

>
</details>

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

- tab-size

>

</details>


### 4. Sections

<details>

``` css

/* Sections
   ========================================================================== */

/**
 * Remove the margin in all browsers.
 */

body {
	margin: 0;
}

/**
 * Improve consistency of default fonts in all browsers. (https://github.com/sindresorhus/modern-normalize/issues/3)
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
 * Correct the font size and margin on `h1` elements within `section` and
 * `article` contexts in Chrome, Firefox, and Safari.
 */

h1 {
	font-size: 2em;
	margin: 0.67em 0;
}
``` 

</details>

### 5. Grouping-content

<details>


```css
/* Grouping content
   ========================================================================== */

/**
 * Add the correct height in Firefox.
 */

hr {
	height: 0;
}

```
</details>

### 6. Text-level-semantics

<details>

```css
/* Text-level semantics
   ========================================================================== */

/**
 * Add the correct text decoration in Chrome, Edge, and Safari.
 */

abbr[title] {
	text-decoration: underline dotted;
}

/**
 * Add the correct font weight in Chrome, Edge, and Safari.
 */

b,
strong {
	font-weight: bolder;
}

/**
 * 1. Improve consistency of default fonts in all browsers. (https://github.com/sindresorhus/modern-normalize/issues/3)
 * 2. Correct the odd `em` font sizing in all browsers.
 */

code,
kbd,
samp,
pre {
	font-family: SFMono-Regular, Consolas, 'Liberation Mono', Menlo, Courier, monospace; /* 1 */
	font-size: 1em; /* 2 */
}

/**
 * Add the correct font size in all browsers.
 */

small {
	font-size: 80%;
}

```


``` css
/**
 * Prevent `sub` and `sup` elements from affecting the line height in
 * all browsers.
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
</details>

### 7. Forms

<details>

``` css

/* Forms
   ========================================================================== */

/**
 * 1. Change the font styles in all browsers.
 * 2. Remove the margin in Firefox and Safari.
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
 * Remove the inheritance of text transform in Edge and Firefox.
 * 1. Remove the inheritance of text transform in Firefox.
 */

button,
select { /* 1 */
	text-transform: none;
}

/**
 * Correct the inability to style clickable types in iOS and Safari.
 */

button,
[type='button'],
[type='reset'],
[type='submit'] {
	-webkit-appearance: button;
}

/**
 * Remove the inner border and padding in Firefox.
 */

button::-moz-focus-inner,
[type='button']::-moz-focus-inner,
[type='reset']::-moz-focus-inner,
[type='submit']::-moz-focus-inner {
	border-style: none;
	padding: 0;
}

/**
 * Restore the focus styles unset by the previous rule.
 */

button:-moz-focusring,
[type='button']:-moz-focusring,
[type='reset']:-moz-focusring,
[type='submit']:-moz-focusring {
	outline: 1px dotted ButtonText;
}

/**
 * Correct the padding in Firefox.
 */

fieldset {
	padding: 0.35em 0.75em 0.625em;
}

/**
 * Remove the padding so developers are not caught out when they zero out
 *    `fieldset` elements in all browsers.
 */

legend {
	padding: 0;
}

/**
 * Add the correct vertical alignment in Chrome and Firefox.
 */

progress {
	vertical-align: baseline;
}

/**
 * Correct the cursor style of increment and decrement buttons in Chrome.
 */

[type='number']::-webkit-inner-spin-button,
[type='number']::-webkit-outer-spin-button {
	height: auto;
}

/**
 * 1. Correct the odd appearance in Chrome and Safari.
 * 2. Correct the outline style in Safari.
 */

[type='search'] {
	-webkit-appearance: textfield; /* 1 */
	outline-offset: -2px; /* 2 */
}

/**
 * Remove the inner padding in Chrome and Safari on macOS.
 */

[type='search']::-webkit-search-decoration {
	-webkit-appearance: none;
}

/**
 * 1. Correct the inability to style clickable types in iOS and Safari.
 * 2. Change font properties to `inherit` in Safari.
 */

::-webkit-file-upload-button {
	-webkit-appearance: button; /* 1 */
	font: inherit; /* 2 */
}

```
</details>

### 8. Interactive

<details>

```css

/* Interactive
   ========================================================================== */

/*
 * Add the correct display in Chrome and Safari.
 */

summary {
	display: list-item;
}

```

</details>

## dev-tool