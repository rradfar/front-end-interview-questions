<div align="center">
<h1>HTML</h1>
</div>

<ol>

<li>`<Button>` vs. `input type="button"`</li>
<li>Can a webpage contain multiple `<header>` or `<footer>` elements?</li>
<li>Can a webpage contain multiple `h1` tags?</li>
<li>Canvas tag</li>
<li>data-* attributes</li>

<details><summary>Answer</summary><p>

- The data-* attributes allow us to be able to make up our own HTML attributes and put our own information inside them.
- They are used to store custom data private to the page or application.
- The stored (custom) data can then be used in the page's JavaScript to create a more engaging user experience (without any Ajax calls or server-side database queries).

```html
<article
  id="electric-cars"
  data-columns="3"
  data-index-number="12314"
  data-parent="cars">
  <!-- additional content -->
</article>
```

- We can read the value of these attributes in JavaScript.

```javascript
const article = document.querySelector('#electric-cars');

article.dataset.columns // "3"
article.dataset.indexNumber // "12314"
article.dataset.parent // "cars"
```

- They can also be accessed in CSS.

```css
article[data-columns='3'] {
  width: 400px;
}
article[data-columns='4'] {
  width: 600px;
}
```

</p></details>

<li>Datalist tag</li>

<details><summary>Answer</summary><p>

- The `<datalist>` tag specifies a list of pre-defined options and allows user to add more to it. It provides an autocomplete feature that allows you to get the desired options with a type-ahead.

```html
<label for="ice-cream-choice">Choose a flavor:</label>
<input list="ice-cream-flavors" id="ice-cream-choice" name="ice-cream-choice" />
<datalist id="ice-cream-flavors">
    <option value="Chocolate">
    <option value="Coconut">
    <option value="Mint">
    <option value="Strawberry">
    <option value="Vanilla">
</datalist>
```

![datalist example](../../blob/master/images/datalist.png)

</p></details>

🌼 Defer vs. Async when loading JavaScript scripts  
🌱 Description Lists: `<dl>` vs. `<dt>` vs. `<dd>`  
🌼 Doctype  

<details><summary>Answer</summary><p>

- `DOCTYPE` or Document Type Declaration is not an HTML tag; it is an instruction to the web browser about what version of HTML the page is written in.
- Using it ensures that the user agent correctly parses the HTML as you intended it.
- HTML5: `<!DOCTYPE html>`
- HTML4: `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">`

</p></details>

🌼 Favicons: what are two ways to implement a favicon on a webpage?

<details><summary>Answer</summary><p>

1. By placing an image called `favicon.ico` in the root directory. All browsers will automatically check for this file.

2. By creating an image and linking it to the HTML using the link tag as such:

```html
<link rel="shortcut icon" type="image/png" href="img/favicon.png" />
```

or

```html
<link rel="icon" type="image/gif" href="img/favicon.gif" />
```

</p></details>

🌱 Favicons: `icon` vs. `shortcut icon` when used in the `<link rel=" " ...>` tag.  
🌱 Fieldset tag  
🌼 Figure tag  

<details><summary>Answer</summary><p>

- The HTML `<figure>` (Figure With Optional Caption) element represents self-contained content, potentially with an optional caption `<figcaption>` element. The figure, its caption, and its contents are referenced as a single unit.

```html
<figure>
  <img src="discovery.jpg" alt="Space Shuttle">
  <figcaption>NASA - Space Shuttle Discovery</figcaption>
</figure>
```

</p>
</details>

🌱 How to create a drop-down list?  
🌱 How to draw rectangle using Canvas and SVG using HTML5?  
🌱 How to serve a page with content in multiple languages?  
🌼 HTML5 new features  
🌱 Image tag: what is the `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.  
🌼 Integrate CSS into a Web page (three ways)  
🌼 Label tag: 2 advantages of using it in an HTML form.  
🌼 Label tag: how to associate a label with its corresponding input element in an HTML form?  
🌼 Map tag  

<details><summary>Answer</summary><p>
- The `map` tag is used to define a client-side image-map. An image-map is an image with clickable areas.
- The required name attribute of the `map` element is associated with the `usemap` attribute and creates a relationship between the image and the map.
- The `map` element contains a number of `area` elements that define the clickable areas in the image map.
- We use the `area` tag in conjunction with the shape of the clickable area [rect, circle, or poly] and coords [rect: left, top, right, bottom; circle: center-x, center-y, radius; poly: x1, y1, x2, y2, ...] attributes.

```html
<map name="primary">
  <area shape="circle" coords="75,75,75" href="left.html">
  <area shape="circle" coords="275,75,75" href="right.html">
</map>

<img usemap="#primary" src="https://placehold.it/350x150" alt="350 x 150 pic">
```

</p></details>

🌱 Meta tag  
🌱 MIME type  
🌱 Picture tag  
🌱 Svg tag and how it differs from `<canvas>`  
🌱 Tables: `<thead>` vs. `<th>`  
🌱 Wbr tag  

</ol>
