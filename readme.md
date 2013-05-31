# HTML and CSS

## What is HTML?

HTML stands for HyperText Markup Language. Hypertext means "text with links in it."
A markup language is a programming language used to make text do more than just sit on a page

In simplest terms, html is the skeleton of a webpage. Gives structure to the data the page presents.

## Tags
Things inside of `<>`s are called tags. E.g., `<html>` and `</html>`. Think of tags as parentheses. Whenever you open one, you should close it.
Everthing in html happens inside of the `<html>` and `</html>` tags. For a html document to be valid, it needs a `<head>`, `<body>`, and `<title>`.

There are lots of html tags: `<div>`, `<img>`, `<p>`, `<h1>`, `<span>`, etc.. Each one serves a different purpose.

### Attributes
Every tag has attributes. E.g., `class`, `id`, `src`. Attributes identify, store metadata, and depict how elements should behave.


Let's add a heading, paragraph, and some gifs to our blank html page.

## What is CSS?
CSS stands for Cascading Style Sheets. Styles that cling onto html.

CSS is a language for applying rules to html tags. An example css style would like as so:

```css
p {
    font-size: 14px;
}
```
This rule causes all p tags to have a font-size of 14px. You can also select by `class` or `id`. `classes help group similar elements together. `id`s are used to mark unique elements on the page. You should rarely need to use `id`s since there are usually aren't very many unique elements on a page.

Add `id`s and `classes` like so:
```html
<div id="content"></div>
<div class="container"></div>
```

You can now specify unique styles for these two elements like this:
```css
#content {
    background-color: black;
}
.container {
    background-color: blue;
}
```

Let's play around with adding `classes` and `id`s to our example html page.

### Specificity
Specificity is the means by which a browser decides which property values are the most relevant to an element and gets to be applied. I.e., If an element has two styles from two different rules, the selector that's more specific will be applied.

How do I specificity?
Basic element selectors such as:
```css
p { color: blue; }
```
are less specific than:
```css
p.title { color: red; }
```
which is less specific than:
```css
div#content p.title { color: purple; }
```

ID selectors have a higher specificity than attribute selectors.
You should always try to use IDs to increase the specificity.
A class selector beats any number of element selectors.

Let's add some goofy styles.

## CSS Inheritance
Inheritance is a way of propagating property values from parent elements to their children.

Some CSS properties are inherited by the children of elements by default. For example, if you set the body tag of a page to a specific font, that font will be inherited by other elements, such as headings and paragraphs, without you having to specifically write as much. This is the magic of inheritance at work.


# Box Model
In html, each `tag`/`element` is represented as a rectangular box. Determining the size, properties — like its color, background, borders aspect — and the position of these boxes is the goal of the rendering engine (browser).
![Box Model](https://developer.mozilla.org/files/72/boxmodel%20(1).png)

Refer to [this](https://developer.mozilla.org/en-US/docs/Web/CSS/box_model)

# Web Inspector
Throme web inspector is an engineer's best friend. It allows you pick apart the internals of any web page. Via the web inspector, you can test out new styles, move things around, delete html, etc..

Let's play around with it.

# But wait..
This is all cool except for the fact that we don't know how to put anything anywhere.

In CSS there are lots of ways to position things but let's focus on `positioning` and `floating`.

## Position
In css, elements can be positioned `relative`, `absolute`, or `fixed`. Each one of these positioning rules accepts `top`, `left`, `bottom`, and `right` rules.

### Absolute
Position it at a specified position relative to its closest positioned ancestor or to the containing block. Emphasis on relative to its closest positioned ancestor.
### Relative
Lay out all elements as though the element were not positioned, and then adjust the element's position, without changing layout (and thus leaving a gap for the element where it would have been had it not been positioned
### Fixed
Position it at a specified position relative to the screen's viewport and doesn't move when scrolled.

Let's take a look at positioning.html. Let's move the absolutely positioned element halfway down the screen.

## Float
The float CSS property specifies that an element should be taken from the normal flow and placed along the left or right side of its container, where text and inline elements will wrap around it.

Refer to [this](http://css-tricks.com/all-about-floats/).

Let's float some stuff.

