<div align="center">
<h1>CSS</h1>
</div>
<ol>
<li>Animations: animation-fill-mode</li>

<details><summary>Answer</summary><p>

- This CSS property sets which values are applied before/after the animation. For example, you can set the last state of the animation to remain on screen (forwards), or you can set it to switch back to before when the animation began (backwards).

- `animation-fill-mode: none|forwards|backwards|both;`

</p></details>

<li>Attribute selectors</li>
<li>Background images</li>
<li>BEM vs. SMACSS</li>
<li>BFC (Block Formatting Context) and how it works</li>
<li>Border images</li>
<li>Box model</li>
<li>Box shadow vs. Text shadow</li>
<li>Box-shadow</li>

<details><summary>Answer</summary><p>

```css
box-shadow: (offset-x | offset-y | blur-radius(optional) | spread-radius(optional) | color(optional));
```

- `blur radius`: if set to 0 the shadow will be sharp, the higher the number, the more blurred it will be, and the further out the shadow will extend.
- `spread radius`: positive values increase the size of the shadow, negative values decrease the size. Default is 0 (the shadow is same size as blur).

```css
/* offset-x | offset-y | color */
box-shadow: 60px -16px teal;

/* offset-x | offset-y | blur-radius | color */
box-shadow: 10px 5px 5px black;

/* offset-x | offset-y | blur-radius | spread-radius | color */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

/* inset | offset-x | offset-y | color */
box-shadow: inset 5em 1em gold;

/* Any number of shadows, separated by commas */
box-shadow: 3px 3px red, -1em 0 0.4em olive;
```

</p></details>

<li>Box-sizing property</li>

<details><summary>Answer</summary><p>

The CSS box-sizing property defines whether the width and height of an element should include padding and borders.

**content-box**  
This is the initial and default value as specified by the CSS standard. The width and height properties include the content, but does not include the padding, border, or margin. For example, `.box {width: 350px; border: 10px solid black;}` renders a box that is `370px` wide.

**border-box**  
The width and height properties include the content, padding, and border, but do not include the margin. Note that padding and border will be inside of the box. For example, `.box {width: 350px; border: 10px solid black;}` renders a box that is `350px` wide.

</p></details>

<li>Cascading in CSS</li>

<details><summary>Answer</summary><p>

- Cascading is the process of combining several style sheets and resolving conflicts between them.
- The rule used is chosen by cascading down from the more general rules to the specific rule required.
- Concepts such as **inheritance** and **specificity** are used to decide which styles get applied.  

For instance,  

- a more specific rule will override a less specific rule.
- a rule defined in an external stylesheet is overruled by a style defined in the `<head>` of the document, which, in turn, is overruled by an inline style within the element itself.

</p></details>

<li>Combinators (4)</li>
<li>Combinators: child vs. descendant</li>
<li>contain vs. cover when using background-size</li>
<li>CSS animations vs. JavaScript animations: pros & cons of each</li>
<li>CSS3 new features</li>
<li>Custom fonts: how to use them</li>
<li>display: block vs. inline vs. inline-block</li>
<li>display: float vs. inline-block</li>
<li>display: flex vs. inline-flex</li>
<li>display: none vs. visibility: hidden</li>
<li>Flex: align-items vs. align-se</li>
<li>Flex: `flex: auto` vs. `flex: none`</li>
<li>Grid vs. Flexbox</li>
<li>Grids: create a grid with three equal columns (2 ways)</li>

<details><summary>Answer</summary><p>

```css
grid-template-columns: 1fr 1fr 1fr;

grid-template-columns: repeat(3, 1fr);
```

</p></details>

<li>Grids: how do you make a div start at column 2 and end before column 4? (two ways)</li>
<li>GSAP vs. CSS animations</li>
<li>Hex vs. RGB vs. HSL</li>
<li>How to hide content visually but make it available to screen readers</li>
<li>How to make a triangle with pure CSS</li>
<li>HSL color model</li>
<li>Importing a CSS file into another</li>

<details><summary>Answer</summary><p>

`@import url('navigation.css');` or `@import 'navigation.css';`

</p></details>

<li>Line spacing: e.g. how to adjust the space between lines in a paragraph.</li>

<details><summary>Answer</summary><p>

- The `line-height` CSS property is commonly used to set the distance between lines of text.

```css
p { line-height: 1.2;   font-size: 10pt; }
p { line-height: 1.2em; font-size: 10pt; }
p { line-height: 120%;  font-size: 10pt; }
p { font: 10pt/1.2  Georgia,serif; }
```

</p></details>

<li>Linear vs. Radial gradient</li>
<li>list-style: none</li>
<li>mix-blend-mode</li>

<details><summary>Answer</summary><p>

- The `mix-blend-mode` CSS property sets how an element's content should blend with the content of the element's parent and the element's background.

```css
mix-blend-mode: normal|multiply|screen|overlay|darken|lighten|color-dodge|color-burn|difference|exclusion|hue|saturation|color|luminosity;
```

An example:

```html
<style>
  .container {
    background-color: gold;
    padding: 15px;
  }

  .container img {
    mix-blend-mode: overlay;
  }
</style>

<div class="container">
  <img src="pineapple.jpg" alt="Pineapple" width="300" height="300">
</div>
```

![mix-blend-mode example](../../blob/master/images/mix-blend-mode.png)

</p></details>

<li>not() pseudo-class</li>
<li>nth-of-type() vs. nth-child()</li>
<li>Overflow parameters</li>
<li>overflow-wrap</li>
<li>Position: relative vs. absolute vs. fixed vs. sticky</li>
<li>Prefixes</li>

<details><summary>Answer</summary><p>

- CSS vendor prefixes, also sometimes known as or CSS browser prefixes, are a way for browser makers to add support for new CSS features before those features are fully supported in all browsers. This may be done during a sort of testing and experimentation period where the browser manufacturer is determining exactly how these new CSS features will be implemented. These prefixes became very popular with the rise of CSS3 a few years ago.
- The CSS browser prefixes that you can use (each of which is specific to a different browser) are:

```markdown
Android: -webkit-
Chrome: -webkit-
iOS: -webkit-
Safari: -webkit-
Firefox: -moz-
Internet Explorer: -ms-
Opera: -o-
```

```css
.container {
  -webkit-transition: all 4s ease;
  -moz-transition: all 4s ease;
  -ms-transition: all 4s ease;
  -o-transition: all 4s ease;
  transition: all 4s ease;
}
```

</p></details>

<li>Preprocessor</li>
<li>Pros and cons of translate() vs. position: absolute</li>
<li>Pseudo-classes vs pseudo-elements</li>

<details><summary>Answer</summary><p>
- A pseudo-class is a selector that selects existing elements that are in a specific state, e.g. hovered over, checked, focused, etc.
- Pseudo-classes start with a colon `:`
- Some common pseudo-classes are `:active`, `:checked`, `:enabled`, `:first-child`, `:first-of-type`, `:focus`, `:hover`, `:last-child`, `:last-of-type`, `:nth-of-type`, `:visited`, etc.

```css
article a:hover {
  font-size: 120%;
  font-weight: bold;
}
```

- Pseudo-elements behave in a similar way, however they act as if you had added a whole new HTML element into the markup, rather than applying a class to existing elements.
- Pseudo-elements start with a double colon `::`
- Most common pseudo-elements are `::after`, `::before`, `::first-letter`, and `::first-line`.

```css
article p::first-line {
  font-size: 120%;
  font-weight: bold;
}
```

</p></details>

<li>rem vs. em</li>
<li>Pros & cons of using rem vs. </li>
<li>Reset vs. Normalize</li>
<li>Responsive vs. Adaptive design</li>
<li>RGB vs. RGBA</li>

<details><summary>Answer</summary><p>

- RGB is a 3-channel format containing data for Red, Green, and Blue.
- RGBA is a 4-channel format containing data for Red, Green, Blue, and Alpha. `background-color:rgba(255,0,0,0.3);`
- The value for A (alpha) is from `0` completely transparent, to `1` completely opaque.

</p></details>

<li>Sass: definition</li>
<li>Sass: features & benefits</li>
<li>Selector specificity and how it works</li>
<li>Sprites</li>
<li>TailwindCSS</li>
<li>transform-origin</li>
<li>Transition shorthand property</li>
<li>Transition vs. Transformation vs. Animation</li>
<li>Tweening</li>

<details><summary>Answer</summary><p>

- It is short for in-betweening.
- It is the process of generating intermediate frames between two images.
- It gives the impression that the first image has smoothly evolved into the second one.
- It is an important method used in all types of animations.
- In CSS3, Transforms (matrix,translate,rotate,scale etc) module can be used to achieve tweening.

</p></details>

<li>Webfonts: Pros and cons of using them</li>
<li>word-break vs. word-wrap</li>
<li>Universal selector</li>
<li>z-index and how stacking context is formed</li>
</ol>
