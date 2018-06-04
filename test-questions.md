Questions
=========

HTML
----

* Which HTML5 element is equivalent with the ARIA landmark role role="complementary"?

https://www.w3.org/TR/wai-aria-practices/examples/landmarks/complementary.html  ASIDE
http://html5doctor.com/aside-revisited/
`` For content that is not the primary focus of an article (or page) but is still related to the article (or page), aside is what you need, regardless of its visual design.``

* In HTML5 you can't use multiple `<header>` elements. Is it true?
Yes, but with a catch. The W3 documents state that the tags represent the header and footer areas of their nearest ancestor section. I would recommend having as many as your want, but only 1 of each for each "section" of your page, i.e. body, section etc.  there are 5 types of "sectioning" elements: <body>, <nav>, <section>, <article>, and <aside>. Each sectioning element can only have one <header> and one <footer> associated with it.
    
* How can you change the direction of HTML text?

https://www.w3.org/International/questions/qa-html-dir 
Add dir="rtl" to the html tag any time the overall document direction is right-to-left. This sets the base direction for the whole document.

No dir attribute is needed for documents that have a base direction of left-to-right, since this is the default.

`<!DOCTYPE html>
<html dir="rtl" lang="ar">
<head>
<meta charset="utf-8">
...`

* If I do not put `<!DOCTYPE html>` will HTML5 work?


The declaration must be the very first thing in your HTML document, before the tag. The declaration is not an HTML tag; it is an instruction to the web browser about what version of HTML the page is written in. A lot of IDE's allow users to leave this out and simply default to a certain HTML style, but leaving it out does pose a potential threat in browser compatibility and the use of older versions of HTML.

For example: new features & tags in HTML5 such as ``< article >,< footer >, < header >, < nav >, < section >`` may not be supported if the Doctype is not declared.
Additionally, the browser may decide to automatically go into Quirks or Strict Mode.

* Setting an element's tabindex to negative value (eg. -1) has the following result...
When tabindex is set to a negative integer like -1, it becomes programmatically focusable but it isn’t included in the tab order. In other words, it can’t be reached by someone using the tab key to navigate through content, but it can be focused on with scripting.
https://developer.paciellogroup.com/blog/2014/08/using-the-tabindex-attribute/

* How will affect an element if the attribute hidden is present? Is it valid?

It is valid, the element becames invisible. So why use the hidden attribute?  It's more semantically correct and should more efficiently aid screen readers.  You'll even save a few characters on the display:none CSS!

* Are there any semantic differencies between `<strong>` and `<b>`?

The `<b>` tag is for "offset text conventionally styled in bold". If you read deeper into the details you'll see it adds, "without conveying any extra emphasis or importance".

`<strong>` is different. It "represents a span of text with strong importance." There is semantic meaning of importance here. In fact, a `<strong>` tag within another `<strong>` tag has even more importance. There is nested importance. 

* Is the `canvas` resolution idependent?

(probably not) https://coderwall.com/p/vmkk6a/how-to-make-the-canvas-not-look-like-crap-on-retina


CSS
---

* Which of the following order of precedence is valid (ordering is >, left side is the strongest)
  (inline styles, embedded styles, external styles, user-agent styles)
* CSS image replacement is a technique
* Which property can be used to control the main axis, direction of the items in a flex container?
* What does ’above the fold CSS’ mean?
* HTML data- attributes can be used as a content value?
* Using `display: none;` will speed up rendering, because...
* `position: fixed;` is positioned relative to
* When do background images in css downloaded?
* In regards to the CSS box model, where is the margin property located?
* Are CSS properties case sensitive?
* Z-index only effects elements that have a position value other than static. Is it true?
* Stacking context is affected by opacity. Is it true?
* If an element has a set width and height, what CSS command could you use to make padding apply inside of the element instead of defaulting to expand the element with padding?
* What is the difference between a Sass mixin and function?
* What does '%' stand for in this Sass definition %foo {}
* Why it is a good practice to combine Sass placeholder styles with extend?

JavaScript
----------

* What is the arity of a function?
* What is the "closure" in Javascript
* What is the "variable hoisting" in Javascript
* What keyword / symbol do you preface a variable declaration with?
* What is the attribute to get the quantity of objects stored in a ’Set’ object?
* What is JWT?

Riddles
=======

* Which of the following data attributes is invalid? (data-Values="foo,bar")

* Which of these selectors is not a valid one? (`E:only-child`, `E:parent`, `E:empty`)
* What is the meaning of the following selector: `.cont .wrapper:first-child h3:not(:last-child):before {}`

* What is the output?

```
// 1
console.log(~~3.14);
```

```
// 2
var y = 5;
var x = ++y;
console.log(x);
```

```
// 3
const KEY = 'white_rabbit';
if (true) {
  const KEY = 'ginger_rabbit';
}
console.log(KEY);
```

```
// 4
let x = 42;
if (true) {
  let x = 1337;
}
console.log(x);
```

```
// 5
let x, { x: y = 1 } = { x }; y;
```

```
// 6
[...[...'...'], '...'].length
```

```
// 7
var x = `foo ${y}`,
    y = `bar ${x}`;
console.log(x);
```

```
// 8
var score = [12, 7, 14];
Math.max(...score);
```