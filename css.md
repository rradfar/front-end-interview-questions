<div align="center">
<h1>CSS</h1>
</div>

🌼 Animations: animation-fill-mode  

<details><summary>Answer</summary><p>

- This CSS property sets which values are applied before/after the animation. For example, you can set the last state of the animation to remain on screen (forwards), or you can set it to switch back to before when the animation began (backwards).

- `animation-fill-mode: none|forwards|backwards|both;`

</p></details>

🌱 Attribute selectors  
🌼 Background images  
🌱 BEM vs. SMACSS  
🌱 BFC (Block Formatting Context) and how it works  
🌱 Border images  
🌼 Box model  
🌱 Box shadow vs. Text shadow  
🌼 Box-shadow  

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

🌼 Box-sizing  
🌼 Cascading in CSS  

<details><summary>Answer</summary><p>

- Cascading is the process of combining several style sheets and resolving conflicts between them.
- The rule used is chosen by cascading down from the more general rules to the specific rule required.
- Concepts such as **inheritance** and **specificity** are used to decide which styles get applied.  

For instance,  

- a more specific rule will override a less specific rule.
- a rule defined in an external stylesheet is overruled by a style defined in the `<head>` of the document, which, in turn, is overruled by an inline style within the element itself.

</p></details>

🌱 Combinators (4)  
🌼 Combinators: child vs. descendant  
🌼 contain vs. cover when using background-size  
🌱 CSS animations vs. JavaScript animations: pros & cons of each  
🌼 CSS3 new features  
🌱 Custom fonts: how to use them  
🌱 display: block vs. inline vs. inline-block  
🌱 display: float vs. inline-block  
🌱 display: flex vs. inline-flex  
🌼 display: none vs. visibility: hidden  
🌱 Flex: align-items vs. align-self
🌼 Flex: `flex: auto` vs. `flex: none`  
🌼 Grid vs. Flexbox  
🌼 Grids: create a grid with three equal columns (2 ways)  

<details><summary>Answer</summary><p>

```css
grid-template-columns: 1fr 1fr 1fr;

grid-template-columns: repeat(3, 1fr);
```

</p></details>

🌼 Grids: how do you make a div start at column 2 and end before column 4? (two ways)  
🌱 GSAP vs. CSS animations  
🌼 Hex vs. RGB vs. HSL  
🌱 How to hide content visually but make it available to screen readers  
🌱 How to make a triangle with pure CSS  
🌼 HSL color model  
🌼 Importing a CSS file into another  

<details><summary>Answer</summary><p>

`@import url('navigation.css');` or `@import 'navigation.css';`

</p></details>

🌼 Line spacing: e.g. how to adjust the space between lines in a paragraph.  

<details><summary>Answer</summary><p>

- The `line-height` CSS property is commonly used to set the distance between lines of text.

```css
p { line-height: 1.2;   font-size: 10pt; }
p { line-height: 1.2em; font-size: 10pt; }
p { line-height: 120%;  font-size: 10pt; }
p { font: 10pt/1.2  Georgia,serif; }
```

</p></details>

🌱 Linear vs. Radial gradient  
🌼 list-style: none  
🌼 mix-blend-mode  

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

🌱 not() pseudo-class  
🌱 nth-of-type() vs. nth-child()  
🌱 Overflow parameters  
🌱 overflow-wrap  
🌱 Position: relative vs. absolute vs. fixed vs. sticky  
🌼 Prefixes  

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

🌼 Preprocessor  
🌱 Pros and cons of translate() vs. position: absolute  
🌼 Pseudo-classes vs pseudo-elements  

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

🌼 rem vs. em  
🌱 Pros & cons of using rem vs. em
🌼 Reset vs. Normalize  
🌼 Responsive vs. Adaptive design  
🌼 RGB vs. RGBA  

<details><summary>Answer</summary><p>

- RGB is a 3-channel format containing data for Red, Green, and Blue.
- RGBA is a 4-channel format containing data for Red, Green, Blue, and Alpha. `background-color:rgba(255,0,0,0.3);`
- The value for A (alpha) is from `0` completely transparent, to `1` completely opaque.

</p></details>

🌼 Sass: definition  
🌱 Sass: features & benefits  
🌱 Selector specificity and how it works  
🌱 Sprites  
🌱 TailwindCSS  
🌱 transform-origin  
🌼 Transition shorthand property  
🌱 Transition vs. Transformation vs. Animation  
🌼 Tweening  

<details><summary>Answer</summary><p>

- It is short for in-betweening.
- It is the process of generating intermediate frames between two images.
- It gives the impression that the first image has smoothly evolved into the second one.
- It is an important method used in all types of animations.
- In CSS3, Transforms (matrix,translate,rotate,scale etc) module can be used to achieve tweening.

</p></details>

🌱 Webfonts: Pros and cons of using them  
🌱 word-break vs. word-wrap  
🌱 Universal selector  
🌱 z-index and how stacking context is formed  
