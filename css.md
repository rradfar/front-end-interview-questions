![CSS logo](images/logos/logo-css.png)

# CSS Interview Questions

Q. CSS stands for Cascading Style Sheets. What is Cascading?

<details><summary>Answer</summary>

Cascading is the process of combining several style sheets and resolving conflicts between them.

The rule used is chosen by cascading down from the more general rules to the specific rule required.

Concepts such as **inheritance** and **specificity** are used to decide which styles get applied.  

For instance,  
- a more specific rule will override a less specific rule.
- a rule defined in an external stylesheet is overruled by a style defined in the `<head>` of the document, which, in turn, is overruled by an inline style within the element itself.

</details>

---

Q. What were some new features that were introduced in CSS3? Which ones are your favorite?

<details><summary>Answer</summary>

- Border radius and border images
- Drop shadows, text shadows, linear and radial gradients
- Animations, Transitions, and 3D Transformations
- Flexbox and Grids
- Web fonts
- Media Queries
- New pseudo-classes (e.g. `:nth-child(n)`, `:nth-of-type(n)`, `:last-child`)

Pick your favorite(s) and be able to explain why.

</details>

---

Q. Are you familiar with any CSS methodologies for writing modular and reusable code?

<details><summary>Answer</summary>

The three most popular CSS methodologies are BEM, SMACSS, and OOCSS. See below for summary of each.

The Block, Element, Modifier methodology (BEM) is a popular naming convention for classes in HTML and CSS. Its goal is to help developers better understand the relationship between the HTML and CSS in a given project. E.g.

```html
<a class="btn btn--big btn--shadow" href="https://www.google.com/">
  <span class="btn__price">$8.99</span>
  <span class="btn__text">Subscribe</span>
</a>
```

```css
/* Block component */
.btn {}

/* Element that depends upon the block */ 
.btn__price {}
.btn__text {}

/* Modifier that changes the style of the block */
.btn--big {}
.btn--shadow {}
```

Scalable and Modular Architecture for CSS (SMACSS) is a style guide that focuses on separating CSS rules into five categories of Base, Layout, Module, State, and Theme. SMACSS is less opinionated about naming conventions than BEM.

‎Object Oriented CSS (OOCSS) is based on two major principles: Separation of structure (height, width, margins, etc.) and skin (colors, fonts, etc.), and Separation of container and content (elements such as images, paragraphs and div tags that are nestled within other elements, which serve as containers).

</details>

---

Q. Describe the CSS Box model.

<details><summary>Answer</summary>

All HTML elements can be considered as boxes. The CSS box model is essentially a box that wraps around every HTML element and consists of margins, borders, padding, and the actual content.

![image](images/002.png)

</details>

---

Q. Describe the CSS Box-sizing property

<details><summary>Answer</summary>

The CSS box-sizing property defines whether the width and height of an element should include padding and borders.

**content-box**  
This is the initial and default value as specified by the CSS standard. The width and height properties include the content, but does not include the padding, border, or margin. For example, `.box {width: 350px; border: 10px solid black;}` renders a box that is `370px` wide.

**border-box**  
The width and height properties include the content, padding, and border, but do not include the margin. Note that padding and border will be inside of the box. For example, `.box {width: 350px; border: 10px solid black;}` renders a box that is `350px` wide.

</details>

---

Q. Have you heard of the Block Formatting Context or BFC?

<details><summary>Answer</summary>

A new Block Formatting Context (BFC) is created whenever we use floats, absolutely positioned elements, inline-blocks, table-cells, elements with 'overflow' other than 'visible', etc. Once an element creates a BFC, everything is contained inside it. BFC is used to prevent margins collapsing, text wrapping, or to contain floats.

</details>

---

Q. Are you familiar with CSS Combinators?

<details><summary>Answer</summary>

A CSS combinator explains the relationship between the selectors.

There are four different combinators in CSS:
- The **descendant** selector (`space`) matches all elements that are descendants of a specified element.
- The **child** selector (`>`) matches only those elements matched by the second selector that are the direct children of elements matched by the first.
- The **adjacent sibling** selector (`+`) is used to select something if it is right next to another element at the same level of the hierarchy.
- The **general sibling** selector (`~`) selects siblings of an element even if they are not directly adjacent.

```css
div p {
  background-color: yellow;
}

div > p {
  background-color: yellow;
}

div + p {
  background-color: yellow;
}

div ~ p {
  background-color: yellow;
}
```

</details>

---

Q. What are attribute selectors in CSS?

<details><summary>Answer</summary>

Attribute selectors can be used to style HTML elements that have specific attributes.

```css
a[target="_blank"] {
  /* style rules here */
}

input[type="text"] {
  /* style rules here */
}

[class^="top"] {
  /* style rules here */
}
```
</details>

---

Q. Is it possible to use an image as a border for an element?

<details><summary>Answer</summary>

Yes, we can use the `border-image` CSS property to achieve that. The `border-image` property is a shorthand for five other CSS properties related to border images.

```css
border-image: url(border.png) 30 round;
```

</details>

---

Q. When setting a box shadow in CSS, what is the difference between blur radius and spread radius?

<details><summary>Answer</summary>

```css
box-shadow: (offset-x | offset-y | blur-radius(optional) | spread-radius(optional) | color(optional));
```

`blur radius`: if set to 0 the shadow will be sharp, the higher the number, the more blurred it will be, and the further out the shadow will extend.

`spread radius`: positive values increase the size of the shadow, negative values decrease the size. Default is 0 (the shadow is same size as blur).

</details>

---

Q. What does adding the `inset` keyword to the CSS box-shadow property do?

<details><summary>Answer</summary>

The `inset` keyword changes the shadow from an outer shadow (outset) to an inner shadow.

![image](images/003.png)

</details>

---

Q. What are some of the pros and cons of using CSS animations instead of doing them with JavaScript?

<details><summary>Answer</summary>

CSS animations are preferred when we want to create small, self-contained states for UI elements. JavaScript is usually more appropriate when we want to have a greater control over the animations.

While CSS animations tend to be faster than animation performance of jQuery, newer libraries such as GSAP tend to narrow that gap substantially.

CSS keyframe animations are great for sequencing transitions however they only allow for percentages and not time.

</details>

---

Q. What is the difference between block, inline, and inline-block when displaying elements?

<details><summary>Answer</summary>

**Inline**: An inline element does not start on a new line and only takes up as much width as necessary. Some examples of inline elements are `<span>` , `<strong>`, and `<img>`. You can add space to the left and right of an inline element, but you cannot add height to the top or bottom padding or margin of an inline element. Inline elements can appear within block elements.

**Inline-Block**: Compared to `display: inline`, the major difference is that `display: inline-block` allows to set a width and height on the element. Also, the top and bottom margins/paddings are respected. Compared to `display: block`, the major difference is that `display: inline-block` does not add a line-break after the element, so the element can sit next to other elements. One common use for `display: inline-block` is to display list items horizontally instead of vertically.

**Block**: Unlike inline or inline-block elements, a block-level element always starts on a new line and takes up the full width available.

</details>

---

Q. What are the five possible values that can be assigned to the position property in CSS?

<details><summary>Answer</summary>

`static`: Default value. Static doesn't mean much; it just means that the element will flow into the page as it normally would.

`relative`: An element's original position remains in the flow of the document, just like the static value. But now left/right/top/bottom/z-index will work. So `left: 20px;` adds 20 pixels to the element's left position. Two things to note: Even if we don't set a z-index value, the relatively positioned element will now appear on top of any other statically positioned elements. In addition, a relatively positioned element limits the scope of absolutely positioned child elements. Any element that is a child of the relatively positioned element can be absolutely positioned within that block.

`absolute`: The element is removed from the normal document flow and no space is created for it in the page layout. It is positioned relative to its closest relatively positioned ancestor (if any), otherwise, it is placed relative to the initial containing block. Its final position is determined by the values of top, right, bottom, and left.

`fixed`: The element is displayed with respect to the viewport or the browser window itself. It always stays in the same place even if the page is scrolled. It is out of the flow of the rest of the document.

`sticky`: The element is positioned based on the user's scroll position. It basically acts like `position: relative` until an element is scrolled beyond a specific offset, in which case it turns into `position: fixed`. When it is scrolled back it gets back to its previous (relative) position.

</details>

---

Q. Have you ever played around with blend modes in CSS?

<details><summary>Answer</summary><p>

There are two properties that allow us to blend colors together in CSS: `mix-blend-mode` and `background-blend-mode`. With mix-blend-mode, we define the blending between the element and the elements that are behind it. With background-blend-mode, we define the blending between the element's background image and its background color. Some common blend modes are darken, multiply, overlay, screen and soft-light.

```css
.cover {
    background-image: url(blend-mode-example.jpg);
    background-color: #51B7D3;
    background-blend-mode: luminosity;
}
```

![background-blend-mode example](images/010.png)

```html
<style>
  .blend1 img:first-child {
    position: absolute;
    mix-blend-mode: soft-light;
  }
</style>

<div class="blend1">
  <img src="/images/css/blend-modes/monkey.jpg" width="400" height="600">
  <img src="/images/css/blend-modes/sky.jpg" width="400" height="600">
</div>
```

![mix-blend-mode original](images/011.png)

![mix-blend-mode blended](images/012.png)

</p></details>

---

Q. Are you familiar with the HSL color model and why one would want to use it in their CSS?

<details><summary>Answer</summary>

HSL (hue, saturation, lightness) is an alternative representation of the RGB color model.

Hue ranges from 0 to 360 degrees on the color wheel. 0 is red, 120 is green, 240 is blue. Saturation and Lightness are percentages. 0% saturation means a shade of gray and 100% is the full color. 100% lightness is white, 0% lightness is black, and 50% lightness is "normal."

![image](images/018.png)

Using HSL is a great way of making a color scheme for a website using complementary colors. e.g.

```css
hsl(0, 100%, 50%); /* base colour */
hsl(90, 100%, 50%);
hsl(180, 100%, 50%);
hsl(270, 100%, 50%);
```

![image](images/019.png)

</details>

---

Q. When would you use a mixin in Sass?

<details><summary>Answer</summary>

Mixins are blocks of code that can be re-used throughout the stylesheet.

A mixin is defined with the `@mixin` directive. To use a mixin, we simply use `@include` followed by the name of the mixin and a semi-colon.

```scss
@mixin reset-list {
  margin: 0;
  padding: 0;
  list-style: none;
}

@mixin horizontal-list {
  @include reset-list;

  li {
    display: inline-block;
    margin: {
      left: -2px;
      right: 2em;
    }
  }
}

nav ul {
  @include horizontal-list;
}
```

</details>

---

Q. When would you make use of CSS variables in your code?

<details><summary>Answer</summary>

CSS variables contain specific values to be reused throughout a CSS document. They are set using custom property notation that begins with a double hyphen e.g. `--main-color: black;` and are accessed using the `var()` function e.g. `color: var(--main-color);`.

CSS variables can have a global or local scope. Global variables can be accessed/used through the entire document, while local variables can be used only inside the selector where it is declared. To create a variable with global scope, declare it inside the `:root` selector. To create a variable with local scope, declare it inside the selector that is going to use it.

```css
:root {
  --blue: #6495ed;
  --white: #faf0e6;
}

body {
  background-color: var(--blue);
}

h2 {
  border-bottom: 2px solid var(--blue);
}
```

</details>

---

Q. What is the difference between pseudo-classes and pseudo-elements in CSS?

<details><summary>Answer</summary>

A pseudo-class is a selector that selects existing elements that are in a specific state, e.g. hovered over, checked, focused, etc. Pseudo-classes start with a colon `:`. Some common pseudo-classes are `:active`, `:checked`, `:enabled`, `:first-child`, `:first-of-type`, `:focus`, `:hover`, `:last-child`, `:last-of-type`, `:nth-of-type`, `:visited`, etc.

```css
article a:hover {
  font-size: 120%;
  font-weight: bold;
}
```

Pseudo-elements behave in a similar way, however they act as if you had added a whole new HTML element into the markup, rather than applying a class to existing elements. Pseudo-elements start with a double colon `::`. Most common pseudo-elements are `::after`, `::before`, `::first-letter`, and `::first-line`.

```css
article p::first-line {
  font-size: 120%;
  font-weight: bold;
}
```

</details>

---

Q. Are you aware of any accessibility concerns when using CSS pseudo-elements such as `::before` and `::after`?

<details><summary>Answer</summary>

Due to the inconsistencies in how assistive technologies (such as screen readers) interpret pseudo-elements, they may be either completely ignored or misunderstood, causing confusion for users.

W3C recommends using these elements for decorative purposes only, and not for inserting meaningful content into the DOM.

</details>

---

Q. How do the `rem` and `em` CSS units differ from each other?

<details><summary>Answer</summary>

rem (root em) is relative to the html (root) font-size. This means `1rem` is always equal to the font-size defined in `<html>`. For instance, if the font size defined in the root of the document is `16px`,

```css
h1 {
  font-size: 2rem;      /* 2rem = 32px */
  margin-bottom: 1rem;  /* 1rem = 16px */
}

p {
  font-size: 1rem;      /* 1rem = 16px */
  margin-bottom: 1rem;  /* 1rem = 16px */
}
```

em is relative to the font-size of its direct or nearest parent:

```css
h1 {
  font-size: 2em;       /* 1em = 16px */
  margin-bottom: 1em;   /* 1em = 32px */
}
```

The above phenomenon occurs because `1em` is equal to its current font-size. Since the font-size in `<h1>` is now set to `2em`, other properties computed with em in `<h1>` would see that `1em = 32px`.

```css
p {
  font-size: 1em;       /* 1em = 16px */
  margin-bottom: 1em;   /* 1em = 16px */
}
```

</details>

---

Q. What is the difference between RGB and RGBA?

<details><summary>Answer</summary>

They are both functions that define colors in the Red-Green-Blue (RGB) model. RGB is a 3-channel format containing data for Red, Green, and Blue. RGBA is a 4-channel format containing data for Red, Green, Blue, and Alpha. E.g. `background-color:rgba(255,0,0,0.3);`
The value for A (alpha) is from `0` completely transparent, to `1` completely opaque.

</details>

---

Q. Using CSS, what style can we add to the selector below to position the circles seen in the first image, in the center of the page like the second image?

![image1](images/020.png) 

![image2](images/021.png)

```css
.circles {
 /* Your code here */
}
```

<details><summary>Answer</summary>

```css
.circles {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

You may also achieve this using the translate function:

```css
.circles {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
```

</details>

---

Q. We commonly come across the following code at the beginning of the primary styles for a page. What does this piece of code do and why is it used?

```css
* {
  padding: 0;
  margin: 0;
}
```

<details><summary>Answer</summary>

This is known as the universal reset. Since we are using the universal selector (`*`), it resets the margins and padding of all HTML elements to 0.

CSS resets are used to override the default stylesheets that modern browsers use. Because each browser uses a different stylesheet, certain elements (submit buttons, links, etc) don't always have consistent styling across all browsers. A CSS reset will wipe out some of the browser's default styling and allows us developers set our own.

</details>

---

Q. How does resetting browser default styles differ from normalizing them in CSS?

<details><summary>Answer</summary>

All browsers come with a set of default styles. With resetting, we remove (reset) those default styles and start from scratch on a blank slate. With normalizing, we keep the default styles but modify some of them to make them look consistent across different browsers.

For example, with resetting, all headings (H1 to H6) can become the same font size, whereas with normalizing, the H1 tags will have the same font size across different browsers and will be larger than for example H2 tags.

</details>

---

Q. What is the difference between `display: none` and `visibility: hidden` in CSS?

<details><summary>Answer</summary>

`display: none` removes the element from the layout flow whereas `visibility:hidden` hides it but leaves the space.

![image](images/025.png)

</details>

---
