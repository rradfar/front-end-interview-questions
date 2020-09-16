<div align="center">
<h1>Javascript & DOM</h1>
</div>

🌼 `fromEntries()`  
🌼 `this` keyword  
🌼 Arrays: concat()  
🌼 Arrays: copying & the problem with using Array 1 = Array 2  
🌼 Arrays: Creation and initialization  
🌼 Arrays: creation with an initial length of 20.  
🌼 Arrays: every() vs. some()  
🌼 Arrays: fill()  
🌼 Arrays: filter()  
🌼 Arrays: flat()  

<details><summary><b>Answer</b></summary>
<p>

- It is used to flatten an array.
- It can receive an optional depth level parameter specifying how deep a nested array structure should be flattened. Defaults to 1.

```javascript
let arr1 = [1, 2, [3, 4]];
arr1.flat(); //=> [1, 2, 3, 4]

let arr2 = [1, 2, [3, 4, [5, 6]]];
arr2.flat(); //=> [1, 2, 3, 4, [5, 6]]

let arr3 = [1, 2, [3, 4, [5, 6]]];
arr3.flat(2); //=> [1, 2, 3, 4, 5, 6]

let arr4 = [1, 2, [3, 4, [5, 6, [7, 8, [9, 10]]]]];
arr4.flat(Infinity); //=> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

- It can also used to remove empty slots in an array.

```javascript
let arr5 = [1, 2, , , 4, 5];
arr5.flat(); //=> [1, 2, 4, 5]
```

</p></details>
🌼 Arrays: flatmap()  
🌼 Arrays: forEach()  
🌼 Arrays: forEach() vs. map()  
🌼 Arrays: from()  
🌼 Arrays: how to check for equality?  
🌼 Arrays: indexOf() vs. lastIndexOf() vs. includes()  
🌼 Arrays: join()  
🌼 Arrays: reduce()  
🌼 Arrays: reduce() vs. reduceRight()  
🌼 Arrays: slice()  
🌼 Arrays: slice() vs. splice()  
🌼 Arrays: splice()  
🌼 Arrays: the three methods introduced in ES6 that allow us to inspect all elements of an array.  
🌼 Arrays: What are the three methods used to perform a search in an array?

<details><summary><b>Answer</b></summary>
<p>

ECMAScript’s three strict equivalence lookup methods are `indexOf()` and `lastIndexOf()`, available in all ECMAScript versions, and `includes()`, which was introduced in the ECMAScript 7 specification.

</p></details>

🌼 Arrays: why is it Not recommended to use `for.. in` loops to iterate over an array.  
🌼 Arrow functions vs. classic function expressions  
🌼 Async & Await  
🌼 Atomics  
🌼 Bitwise operators  
🌱 BOM (Browser Object Model)  
🌼 Call vs. Apply  
🌼 Call vs. Apply vs. Bind  
🌱 Callback  
🌼 Classes: Static method being called from the class constructor or from other non-static methods within the same class  
🌼 Classes: Static method calling another static method within the same class  
🌼 Classes: Static methods  
🌼 Closure  
🌼 CommonJS  
🌱 Compiling vs. Transpiling  
🌼 `console.log()` vs. `console.dir()`  
🌼 Currying  
🌱 Date and Time formatting  
🌱 Debounce vs. throttle  
🌱 Debounce: When do we use a debounce function?  
🌱 Decimal points handling (since there is no Float data type)  
🌱 Decorators  
🌱 Design Pattern: Builder  
🌱 Design Pattern: Factory  
🌱 Design Pattern: Module  
🌱 Design Pattern: Nullobject  
🌱 Design Pattern: Singleton  
🌱 Destructuring an object or an array (Give an example)  
🌱 DOM (Document Object Model)  
🌱 DOM: firstElementChild  
🌼 DOM: Six JavaScript methods to access DOM elements

<details><summary><b>Answer</b></summary>
<p>

```javascript
document.getElementById()
document.getElementsByClassName()
document.getElementsByTagName()
document.getElementsByName()
document.querySelector();
document.querySelectorAll();
```

</p></details>

🌼 DOM: An important difference between `getElement(s)By*` methods and `querySelector(All)` methods

<details><summary><b>Answer</b></summary>
<p>

- All `getElement(s)By*` methods return a live HTML collection of elements. Such collections always reflect the current state of the document and auto-update when it changes.
- In contrast, `querySelector(All)` methods return a static NodeList object. It’s like a fixed array of elements. Because querySelectorAll() returns a list that is static from the moment it is called, its list of items cannot be updated thereafter even if changes are made to the DOM dynamically.

```javascript
<div>First div</div>

<script>
  let divs = document.getElementsByTagName('div');
</script>

<div>Second div</div>

<script>
  alert(divs.length); //=> 2
</script>
```

```javascript
<div>First div</div>

<script>
  let divs = document.querySelectorAll('div');
</script>

<div>Second div</div>

<script>
  alert(divs.length); //=> 1
</script>
```

</p></details>

🌱 Encapsulation: How do you implement Encapsulation in JavaScript? (interview)  
🌱 Error Handling  
🌱 ES2020 (ES11) new features  
🌱 `eval()`  
🌱 Event bubbling vs. Event capturing  
🌱 Event bubbling vs. Event propagation  
🌱 Event delegation  
🌱 Event listeners: target vs. currentTarget  
🌱 Event listeners. Name 5 events JS could be listening to.  
🌱 Event loop  
🌱 Event loop: Call stack vs. Task queue  
🌱 Event propagation. The three phases of event propagation.  
🌼 false vs. falsy  
🌼 Falsy values  
🌱 Feature detection, feature inference, and using the UA string  
🌱 Fetch API  
🌼 `for.. in` vs. `for.. of`  

<details><summary><b>Answer</b></summary>
<p>

- `for.. in` iterates over all enumerable property **keys** of an object
- `for.. of` iterates over the **values** of an iterable object.

```javascript
let arr = ['a', 'b', 'c'];

for (let key in arr) {
  console.log(key); //=> 0, 1, 2
}

for (let value of arr) {
  console.log(value) //=> a, b, c
}
```

</p></details>

🌼 Functions vs. methods  
🌱 Functions: `function Person(){}` vs. `var person = Person()` vs. `var person = new Person()`  
🌼 Functions: Higher order functions  
🌼 Functions: Idempotent functions  
🌼 Functions: Pure functions  
🌼 Functions: why do we say that in JavaScript, functions are first class citizens.  
🌼 Generator functions & yield keyword  
🌼 Generators  
🌼 Getters & Setters  
🌼 Hoisting  

<details><summary><b>Answer</b></summary>
<p>
- Hoisting is JavaScript's default behavior of moving all declarations to the top of the current scope (to the top of the current script or the current function). 
  
- It allows us to use a variable before it has been declared.

- Hoisted variables are initialized to `undefined` until they are assigned a value.

- Variables defined with let and const are hoisted to the top of the block, but not initialized.

- Function and Class **expressions** are not hoisted.

```javascript
console.log(a); //=> undefined
var a = 1;

console.log(b);
let b = 1;
// "ReferenceError: Cannot access 'b' before initialization
```

</p></details>

🌼 IIFE  
🌱 Image carousel tutorial  
🌱 Immutability  
🌼 Importing a JavaScript file into HTML  
🌼 Interpreter vs. Compiler  
🌱 Iterable vs. Enumerable  
🌱 Iterators  
🌱 Iterators used with Generators  
🌱 Jasmine vs. Mocha vs. Chai  
🌼 JavaScript vs. ECMAScript  
🌼 JavaScript vs. TypeScript  
🌱 JSON parse vs. stringify  
🌼 `let` vs. `const`  
🌼 `let` vs. `var`  
🌱 Maps  
🌱 Maps vs. WeakMaps  
🌱 Modules  
🌱 Modules: Tree shaking  
🌱 Multi-threaded: is JavaScript multi-threaded?  
🌱 NaN: where would be a situation in which you would see `NaN`. How to check for NaN?  
🌼 `null == undefined` ? How about `null === undefined`?  
🌼 `null` vs. `undefined`  
🌼 Null: how to check if something is null? How about undefined?  
🌼 Null: what does `typeof null` return?  
🌱 Nullish coalescing operator  
🌼 Objects: `assign()`  

<details><summary><b>Answer</b></summary>
<p>

- The Object.assign() method copies all enumerable own properties from one or more source objects to a target object. It returns the target object.

```javascript
const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };
const returnedTarget = Object.assign(target, source);

console.log(target); //=> Object { a: 1, b: 4, c: 5 }
console.log(returnedTarget); //=> Object { a: 1, b: 4, c: 5 }
```

</p></details>

🌼 Objects: `assign()` - A problem when using `Object.assign()` to copy objects  

<details><summary><b>Answer</b></summary>
<p>

Object.assign() only does shallow copying. For deep cloning, we need to use alternatives. A common hack is to use `JSON.parse(JSON.stringify(obj))` as such:

```javascript
  obj1 = { a: 0 , b: { c: 0}};
  let obj2 = JSON.parse(JSON.stringify(obj1));
  console.log(JSON.stringify(obj2)); //=> { "a": 0, "b": { "c": 0}}

  obj1.a = 4;
  obj1.b.c = 4;
  console.log(JSON.stringify(obj2)); //=> { "a": 0, "b": { "c": 0}}
  ```

</p></details>

🌼 Objects: shallow cloning an object (two ways)  

<details><summary><b>Answer</b></summary>
<p>

```javascript
const obj = {a: 1};

const copy1 = Object.assign({}, obj) ;
console.log(copy1); //=> {a: 1}

const copy2 = {...obj} ;
console.log(copy2); //=> {a: 1}
```

</p></details>

🌼 Objects: `create()`  
🌼 Objects: Creation and initialization  
🌼 Objects: `freeze()`  

<details><summary><b>Answer</b></summary>
<p>

- `Object.freeze()` makes it impossible to add, remove, or modify properties of an object (unless the property's value is another object).

```javascript
const obj = {
  prop: 42
};

Object.freeze(obj);
obj.prop = 33;
console.log(obj.prop); //=> 42
```

</p></details>

🌼 Objects: `hasOwnProperty()`  

<details><summary><b>Answer</b></summary>
<p>

- The `Object.hasOwnProperty()` method returns a boolean indicating whether the object has the specified property as its own property (as opposed to inheriting it).

```javascript
obj = new Object();
console.log(obj.hasOwnProperty('prop')); // false
obj.prop = 'exists';
console.log(obj.hasOwnProperty('prop')); // true
console.log(obj.hasOwnProperty('toString')); // false
```

</p></details>

🌱 Objects: host objects vs. native objects  
🌼 Objects: how do we determine if an object is an array?  

<details><summary><b>Answer</b></summary>
<p>

By using the `Array.isArray()` method:

```javascript
if (Array.isArray(obj)) {
  // do something on the array
}
```

</p></details>

🌱 Objects: immutable objects  
🌱 Objects: is everything in JavaScript considered an object?  
🌱 Objects: `is()`  
🌼 Objects: iterating over object properties  
🌼 Objects: the optional chaining operator `?.`

<details><summary><b>Answer</b></summary>
<p>

The optional chaining operator `?.` allows us to optionally access deeper nested properties within objects without having to expressly validate that each reference in the chain is valid. The `?.` operator functions similarly to the `.` chaining operator, except that instead of causing an error if a reference is nullish (`null` or `undefined`), the expression short-circuits with a return value of `undefined`. When used with function calls, it returns `undefined` if the given function does not exist.

```javascript
const adventurer = {
name: 'Alice',
cat: {
  name: 'Dinah'
}
};

const dogName = adventurer.dog?.name;
console.log(dogName); //=> undefined
```

</p></details>

🌼 Objects: the two ways to access an object's properties and their differences  

<details><summary><b>Answer</b></summary>
<p>

- In JavaScript, we have two ways to access properties on an object: bracket notation, or dot notation.
- With dot notation, JavaScript tries to find the property on the object with that exact name.
- When we use bracket notation, it sees the first opening bracket [ and keeps going until it finds the closing bracket ]. Only then, it will evaluate the statement.

```javascript
const colorConfig = {
  red: true,
  blue: false,
  green: true,
  black: true,
  yellow: false,
};

const colors = ['pink', 'red', 'blue'];
console.log(colorConfig.colors[1]); //=> TypeError (colorConfig does not have a colors property.)
```

</p></details>

🌼 Parameters vs. Arguments  
🌱 ParseInt vs. ParseFloat  
🌱 Passing by value vs. Passing by reference  
🌼 Primitive data types  
🌱 Promises  
🌼 Prototypal inheritance  
🌱 Prototype vs. __proto__  
🌱 Proxies  
🌱 Pub/Sub architecture  
🌼 Rest vs. Spread operator  
🌱 Same-origin policy with regards to JavaScript.  
🌱 Scope: Global vs. Lexical  
🌼 Scope: lexical scope  
🌼 Sets & methods associated with them  
🌼 Sets: iterating over a set  
🌼 Shallow vs. Deep copying  

<details><summary><b>Answer</b></summary>
<p>

- In shallow copying, both items point to the same memory location.
- In deep copying, the second item is assigned a separate memory location than the original item.
- In other words, in a shallow copy, object B points to object A's location in memory. In deep copy, all things in object A's memory location get copied to object B's memory location.

![Shallow versus deep cloning diagram](https://i.stack.imgur.com/AWKJa.jpg))

</p></details>

🌱 Shimming  
🌼 Statically Typed vs. Dynamically Typed vs. Weakly Typed  
🌱 stopPropagation vs. preventDefault (interview)  
🌼 Strict mode  
🌼 Strict mode: Can strict mode be used within functions or block statements?  
🌼 Strings: `trim()`  
🌼 Strings: 3 common methods for working with characters  
🌱 Strings: An algorithm that returns the first duplicate character in a string (interview)  
🌱 Strings: Given a string (understood to be a sentence), reverse the order of the words. "Hello world" becomes "world Hello"  
🌼 Strings: padStart() and padEnd()  
🌼 Strings: Search() vs. indexOf()  
🌼 Strings: Search() vs. Match()  
🌼 Strings: substring vs. substr vs. slice  
🌱 Symbols  
🌱 Tagged template literal  
🌱 Temporal dead zone  
🌱 Ternary operator: what does the word "Ternary" indicate?  
🌱 toString() parameters  
🌱 Type Coercion (interview)  
🌼 typeof operator  
🌼 typeof vs. instanceof  
🌼 Unary operators  
🌼 V8 and SpiderMonkey.  
🌼 `-0` vs. `+0`  

<div align="center">
<h1>CSS</h1>
</div>

🌼 Animations: `animation-fill-mode`

<details><summary><b>Answer</b></summary>
<p>

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
🌼 box-sizing: border-box  
🌼 Cascading in CSS  
🌱 Combinators (4)  
🌼 Combinators: child vs. descendant  
🌼 contain vs. cover when using background-size  
🌱 CSS animations vs. JavaScript animations: pros & cons of each  
🌼 CSS3 new features  
🌼 display: none vs. visibility: hidden  
🌼 Grid vs. Flexbox  
🌼 Grids: how do you make a div start at column 2 and end before column 4? (two ways)  
🌱 GSAP vs. CSS animations  
🌼 Hex vs. RGB vs. HSL  
🌼 HSL color model  
🌼 Importing a CSS file into another  

<details><summary><b>Answer</b></summary>
<p>

`@import url('navigation.css');` or `@import 'navigation.css';`

</p></details>

🌼 Line spacing  
🌱 Linear vs. Radial gradient  
🌼 list-style: none  
🌱 nth-of-type() vs. nth-child()  
🌱 Overflow parameters  
🌱 overflow-wrap  
🌱 Position: relative vs. fixed vs. absolute vs. static  
🌼 position:sticky vs. position:fixed  
🌼 Prefixes  

<details><summary><b>Answer</b></summary>
<p>

- CSS vendor prefixes, also sometimes known as or CSS browser prefixes, are a way for browser makers to add support for new CSS features before those features are fully supported in all browsers. This may be done during a sort of testing and experimentation period where the browser manufacturer is determining exactly how these new CSS features will be implemented. These prefixes became very popular with the rise of CSS3 a few years ago.
- The CSS browser prefixes that you can use (each of which is specific to a different browser) are:

```css
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
🌱 Pseudo-classes  
🌼 Pseudo-classes vs pseudo-elements  
🌱 Pseudo-elements  
🌼 rem vs. em  
🌼 Reset vs. Normalize  
🌼 RGB vs. RGBA  

<details><summary><b>Answer</b></summary>
<p>

- RGB is a 3-channel format containing data for Red, Green, and Blue.
- RGBA is a 4-channel format containing data for Red, Green, Blue, and Alpha. `background-color:rgba(255,0,0,0.3);`
- The value for A (alpha) is from `0` completely transparent, to `1` completely opaque.

</p></details>

🌼 Sass definition  
🌱 Sass features & benefits  
🌱 Selector specificity and how it works  
🌱 Sprites  
🌱 TailwindCSS  
🌱 transform-origin  
🌼 Transition shorthand property  
🌱 Transition vs. Transformation vs. Animation  
🌼 Tweening  
🌱 Webfonts: Pros and cons of using them  
🌱 word-break vs. word-wrap  
🌱 z-index and how stacking context is formed  

<div align="center">
<h1>HTML</h1>
</div>

🌱 `<dl>` vs. `<dt>` vs. `<dd>`  
🌼 `<figure>`  

<details><summary><b>Answer</b></summary>
<p>

- The HTML `<figure>` (Figure With Optional Caption) element represents self-contained content, potentially with an optional caption `<figcaption>` element. The figure, its caption, and its contents are referenced as a single unit.

```html
<figure>
  <img src="discovery.jpg" alt="Space Shuttle">
  <figcaption>NASA - Space Shuttle Discovery</figcaption>
</figure>
```

</p>
</details>

🌼 `<input type="button" />` vs. `<button>...</button>` in a form  
🌼 `<label>`: 2 advantages of using the `<label>` element in an HTML form.  
🌼 `<label>`: How would you associate a label with its corresponding input element in an HTML form.  
🌼 `<map>`  
🌱 `<svg>` vs. `<canvas>`  
🌱 Can a web page contain multiple `<header>` elements? What about `<footer>` elements?  
🌱 data- attribute  
🌱 datalist  
🌼 defer vs. async when loading JavaScript scripts  
🌼 Doctype  
🌼 Favicons: what are two ways to implement a favicon on a webpage?

<details><summary><b>Answer</b></summary>
<p>

1. By placing an image called `favicon.ico` in the root directory. All browsers will automatically check for this file.

2. By creating an image and linking it to the HTML using the link tag as such:

```html
<link rel="shortcut icon" type="image/png" href="img/favicon.png" />
```
or
```html
<link rel="icon" type="image/gif" href="http://domain.com/image.gif" />
```

</p></details>

🌱 Favicons: `icon` vs. `shortcut icon` when used in the `<link rel=" " ...>` tag.  
🌱 How do you serve a page with content in multiple languages  
🌱 How to draw rectangle using Canvas and SVG using HTML5.  
🌼 HTML5 new features  
🌼 Integrate CSS into a Web page (three ways)  
🌱 MIME type  
🌱 Should a website always have a `H1` tag? Is it possible to have multiple `H1` tags on a page?  
🌱 srcset attribute in an image tag. Explain the process the browser uses when evaluating the content of this attribute.  

<div align="center">
<h1>General CS</h1>
</div>

🌱 A/B testing  
🌱 A11y: ARIA  
🌱 A11y: best practices  
🌱 A11y: How can we make a form more accessible? (interview)  
🌱 A11y: skip links What benefit(s) do they provide some of their limitations  
🌱 A11y: some of the tools available to test the accessibility of a website or web application  
🌱 A11y: WCAG the differences between A, AA, and AAA compliance  
🌱 Acceptance testing  
🌱 Agile  
🌱 Agile vs. Waterfall  
🌱 AJAX  
🌱 Ansible  
🌼 API  
🌱 Apollo  
🌱 AWS  
🌱 AWS Lambda  
🌱 Babel  
🌱 BDD vs. TDD  
🌱 Bootstrap vs. Bulma  
🌱 Bootstrap vs. Materialize  
🌱 Caching  
🌱 CI/CD  
🌱 CLI  
🌱 CMS  
🌱 Concurrency vs. Parallelism  
🌱 Content strategy  
🌱 CORS. What issue does it address?  
🌱 Cross Site Scripting (XSS)  
🌱 CRUD  
🌱 Data binding  
🌱 Database sharding  
🌱 Databases: ACID properties of a transaction  
🌱 Deadlocks & Mutex  
🌱 Dependency injection  
🌱 DevTools: some ways that Chrome DevTools can help us with finding ways to improve our site performance  
🌱 DNS  
🌱 Docker  
🌱 Elasticsearch  
🌱 Extreme Programming (XP)  
🌱 Flash of Unstyled Content (FOUC). How do you avoid FOUC?  
🌱 Flutter  
🌱 Forms: some best practices when designing a form  
🌼 Four pillars of OOP  
🌱 Functional programming. How does it differ from object oriented programming?  
🌱 GraphQL  
🌱 How would you go about accepting payments via Credit cards or PayPal for a shopping cart feature you are developing for a client  
🌱 HTTP: How does a 403 differ from 404 error  
🌱 HTTP: HTTP vs HTTPS  
🌱 HTTP: Is HTTP the same as REST  
🌱 HTTP: List some of the HTTP methods that you are familiar with.  
🌱 HTTP: Purpose of a HTTP header  
🌱 HTTP: some best practices for a 404 page  
🌱 HTTP: some causes of a 500 error  
🌱 HTTP: Status codes  
🌱 HTTP: What happens behind the scenes when you enter a URL into the browser and press enter? (interview)  
🌱 JIRA  
🌱 JPEG vs. PNG vs. GIF  
🌱 jQuery  
🌱 jQuery: Why has jQuery become less popular in recent years?  
🌱 JSON vs. XML  
🌱 JSONP  
🌱 Kubernetes  
🌱 Lazyloading  
🌼 Library vs. framework  
🌱 Linters  
🌼 Load Balancer and its advantages  
🌱 Low-fidelity vs. High-fidelity prototyping  
🌱 Microservices and how do they differ from monoliths  
🌱 Middleware  
🌱 MVC  
🌱 MVC: Are MVCs and frameworks the same  
🌱 MVC: some pros and cons of using an MVC  
🌱 MVVC  
🌱 Native vs. Hybrid apps  
🌱 Nginx  
🌼 Node.js  
🌱 NPM & Yarn  
🌱 ORM  
🌱 Performance: CDN and the benefit of using one  
🌱 Performance: domain pre-fetching and how does it help with performance  
🌱 Performance: How many resources will a browser download from a given domain at a time the exceptions  
🌱 Performance: Is it better to perform animations on a webpage using CSS or JavaScript  
🌱 Performance: Minifying Is it always a good idea to minify  
🌱 Performance: Name 3 ways to decrease page load (perceived or actual load time).  
🌱 Performance: some things you can do to make a website compatible with some earlier versions of IE  
🌱 Performance: some ways to improve performance of a page  
🌱 Performance: some ways to increase code maintainability  
🌱 Performance: some ways to optimize an image for web  
🌱 Performance: What does it mean for an image to be optimized for web  
🌱 Polyfill  
🌱 Progressive enhancement vs. graceful degradation  
🌱 Progressive rendering  
🌼 PUT vs. PATCH methods in RESTful APIs  
🌱 PWA  
🌱 React  
🌱 React: Is it always a better idea to use React than Vanilla JavaScript in a project  
🌱 React: Is React a framework Why or why not  
🌱 React: some advantages of using React over Vanilla JavaScript  
🌱 ReactNative  
🌱 Redis  
🌱 Redux  
🌱 REPL  
🌼 REST  
🌱 REST vs. SOAP APIs  
🌼 RESTful API  
🌼 RESTful APIs are stateless. What does this mean?  
🌼 RESTful web service request (its four components)  
🌱 SaaS vs. PaaS  
🌱 Scrum  
🌱 Scrum artifacts  
🌱 Scrum ceremonies  
🌱 Scrum vs. Kanban  
🌱 Selenium  
🌱 SEO: best practices  
🌱 Server side rendering and why would you want to do it  
🌱 Server side rendering vs. Client side rendering  
🌱 Serverless architecture  
🌱 Software Development Life Cycle (SDLC)  
🌱 SOLID principles  
🌱 SPA  
🌱 SPA: When would you not want to use a Single Page Application  
🌱 SQL injection: As front-end developers, do we need to worry about SQL injections? (interview)  
🌱 SQL vs. NoSQL databases  
🌱 SSH  
🌱 SSL  
🌱 Static site  
🌱 Static cite: Gatsby vs. Jekyll  
🌱 Storage: Cookie vs. SessionStorage vs. LocalStorage.  
🌱 Storage: Cookies vs. Sessions  
🌱 Storage: the lifetime of local storage  
🌱 Svelte  
🌱 SVG  
🌼 TC39  
🌱 TCP vs. UDP (Interview)  
🌱 TCP/IP  
🌱 Templating languages  
🌱 Unit testing vs. functional/integration testing  
🌱 URL vs. URI  
🌱 URL: Clean URL  
🌱 Usability testing  
🌱 UX  
🌱 UX personas  
🌱 UX user journey maps  
🌱 Vector vs. raster images  
🌱 Virtual DOM  
🌱 Visual hierarchy  
🌱 VMs vs. Containers  
🌱 Web 2.0  
🌱 Web components  
🌱 Web workers  
🌱 Web workers vs. Service worker  
🌼 WebAssembly (WASM)  
🌱 WebPack  
🌱 Websockets  
🌱 Wireframes. Are you familiar with any wireframing tools?  
🌱 WordPress  
🌱 WordPress vs. Drupal vs. Joomla  

<div align="center">
<h1>Git</h1>
</div>

🌱 What is Git?  
🌱 How does Git differ from GitHub? Can you use Git without GitHub?  
🌱 What is a Git repository? How does it differ from a branch?  
🌱 Git command to create a new branch and switch to it: `git checkout -b <branchname>`  
🌱 Git command to switch from one branch to another: `git checkout <branchname>`  
🌱 Git command to list all branches in a repo: `git branch`  
🌱 Git command to delete a feature branch: `git branch -d <branchname>`  
🌱 What is the `origin`?  
🌱 SSH vs. Https when cloning a repo  
🌱 Cloning vs. Forking  
🌱 What is gitignore?  
🌱 How do you undo and edit the last commit message?  
🌱 How do you undo your most recent commit before it is pushed? How about after it's been pushed?  
🌱 How do you delete a feature branch?  
🌱 How do you rename a feature branch?  
🌱 How do you merge a feature branch into the master branch?  
🌱 What is a pull request and why is it beneficial?  
🌱 How do you do a pull request?  
🌱 How do you see a list of most recent commits to a branch?  
🌱 What is cherry-pick used for?  
🌱 What is stash used for?  
🌱 How do you add a new remote Git repository to your project?  
🌱 How do rename an existing remote Git repository in your project?  
🌱 How do you view the remote Git repository in your project?  
🌱 How do you view your credentials (e.g. email and name) for a git repository?  
🌱 Remote vs. Origin  
🌱 Rebase vs. Fetch  
🌱 Pull vs. Fetch  
🌱 What does the `-u` flag in `git push -u origin master` do?  

<div align="center">
<h1>Tutorials</h1>
</div>

🌱 Form design  
🌱 Image carousel  
🌱 Infinite scrolling  
🌱 Pagination  
🌱 Pinterest board  
🌱 Progress bar  
