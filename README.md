<div align="center">
  <img height="60" src="./images/logos/js.png"> 
  <h1>Javascript & DOM</h1>
</div>

### 1. What's the output?

```javascript
function sayHi() {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
}

sayHi();
```

- A: `Lydia` and `undefined`
- B: `Lydia` and `ReferenceError`
- C: `ReferenceError` and `21`
- D: `undefined` and `ReferenceError`

<details><summary><b>Answer</b></summary>
<p>

Within the function, we first declare the `name` variable with the `var` keyword. This means that the variable gets hoisted (memory space is set up during the creation phase) with the default value of `undefined`, until we actually get to the line where we define the variable. We haven't defined the variable yet on the line where we try to log the `name` variable, so it still holds the value of `undefined`.

Variables with the `let` keyword (and `const`) are hoisted, but unlike `var`, don't get <i>initialized</i>. They are not accessible before the line we declare (initialize) them. This is called the "temporal dead zone". When we try to access the variables before they are declared, JavaScript throws a `ReferenceError`.

</p>
</details>

 ✔️ `-0` vs. `+0`  
 ✅	`fromEntries()`  
- [x] 	`this` keyword
- [x] 	Arrays: concat()  
☑️ Arrays: copying & the problem with using Array 1 = Array 2
- [x] 	Arrays: Creation and initialization
- [x] 	Arrays: creation with an initial length of 20.
- [x] 	Arrays: every() vs. some()
- [x] 	Arrays: fill()
- [x] 	Arrays: filter()
- [x] 	Arrays: flat()
- [x] 	Arrays: flatmap()
- [x] 	Arrays: forEach()
- [x] 	Arrays: forEach() vs. map()
- [x] 	Arrays: from()
- [x] 	Arrays: how to check for equality?
- [x] 	Arrays: indexOf() vs. lastIndexOf() vs. includes()
- [x] 	Arrays: join()
- [x] 	Arrays: reduce()
- [x] 	Arrays: reduce() vs. reduceRight()
- [x] 	Arrays: slice()
- [x] 	Arrays: slice() vs. splice()
- [x] 	Arrays: splice()
- [x] 	Arrays: the three methods introduced in ES6 that allow us to inspect all elements of an array.
- [x] 	Arrays: why is it Not recommended to use `for...in` loops to iterate over an array.
- [x] 	Arrow functions vs. classic function expressions
- [x] 	Async & Await
- [x] 	Atomics
- [x] 	Bitwise operators
- [ ] 	BOM (Browser Object Model)
- [x] 	Call vs. Apply
- [x] 	Call vs. Apply vs. Bind
- [ ] 	Callback
- [x] 	Classes: Static method being called from the class constructor or from other non-static methods within the same class
- [x] 	Classes: Static method calling another static method within the same class
- [x] 	Classes: Static methods
- [x] 	Closure
- [x] 	CommonJS
- [ ] 	Compiling vs. Transpiling
- [x] 	console.log() vs. console.dir()
- [x] 	Currying
- [ ] 	Date and Time formatting
- [ ] 	Debounce vs. throttle
- [ ] 	Debounce: When do we use a debounce function?
- [ ] 	Decimal points handling (since there is no Float data type)
- [ ] 	Decorators
- [ ] 	Design Pattern: Builder
- [ ] 	Design Pattern: Factory
- [ ] 	Design Pattern: Module
- [ ] 	Design Pattern: Nullobject
- [ ] 	Design Pattern: Singleton
- [ ] 	Destructuring an object or an array (Give an example)
- [ ] 	DOM (Document Object Model)
- [ ] 	Encapsulation: How do you implement Encapsulation in JavaScript? (interview)
- [ ] 	Error Handling
- [ ] 	ES2020 (ES11) new features
- [ ] 	eval()
- [ ] 	Event bubbling vs. Event capturing
- [ ] 	Event bubbling vs. Event propagation
- [ ] 	Event delegation
- [ ] 	Event listeners: target vs. currentTarget
- [ ] 	Event listeners. Name 5 events JS could be listening to.
- [ ] 	Event loop
- [ ] 	Event loop: Call stack vs. Task queue
- [ ] 	Event propagation. The three phases of event propagation.
- [x] 	false vs. falsy
- [x] 	Falsy values
- [ ] 	Feature detection, feature inference, and using the UA string
- [ ] 	Fetch API
- [x] 	for in vs. for of
- [x] 	Functions vs. methods
- [ ] 	Functions: `function Person(){}` vs. `var person = Person()` vs. `var person = new Person()`
- [x] 	Functions: Higher order functions
- [x] 	Functions: Idempotent function
- [x] 	Functions: Pure functions
- [x] 	Functions: why do we say that in JavaScript, functions are first class citizens.
- [x] 	Generator functions & yield keyword
- [x] 	Generators
- [x] 	Getters & Setters
- [x] 	Hoisting
- [ ] 	Host objects vs. native objects
- [x] 	IIFE
- [ ] 	Image carousel tutorial
- [ ] 	Immutability
- [ ] 	Immutable objects
- [x] 	Importing a JavaScript file into HTML
- [x] 	Interpreter vs. Compiler
- [ ] 	Iterable vs. Enumerable
- [ ] 	Iterators
- [ ] 	Iterators used with Generators
- [ ] 	Jasmine vs. Mocha vs. Chai
- [x] 	JavaScript vs. ECMAScript
- [x] 	JavaScript vs. TypeScript
- [ ] 	JSON parse vs. stringify
- [x] 	Let vs. const
- [x] 	Let vs. var
- [ ] 	Maps
- [ ] 	Maps vs. WeakMaps
- [ ] 	Modules
- [ ] 	Modules: Tree shaking
- [ ] 	Multi-threaded. Is JavaScript multi-threaded?
- [ ] 	NaN: Where would be a situation in which you would see `NaN`. How to check for NaN?
- [x] 	null == undefined ? How about null === undefined?
- [x] 	Null vs. undefined
- [x] 	Null: How to check if something is null? How about undefined?
- [ ] 	Nullish coalescing operator
- [x] 	Objects: assign()
- [ ] 	Objects: assign() - Problem with not deep cloning
- [x] 	Objects: cloning an object
- [x] 	Objects: create()
- [x] 	Objects: Creation and initialization
- [x] 	Objects: freeze()
- [x] 	Objects: How to check if an object is an array?
- [ ] 	Objects: Is everything in JavaScript considered an object?
- [ ] 	Objects: is()
- [x] 	Objects: iterating over object properties
- [x] 	Objects: the two ways to access an object's properties.
- [ ] 	Pagination tutorial
- [x] 	Parameters vs. Arguments
- [ ] 	ParseInt vs. ParseFloat
- [ ] 	Passing by value vs. Passing by reference
- [x] 	Primitive data types
- [ ] 	Promises
- [x] 	Prototypal inheritance
- [ ] 	Prototype vs. __proto__
- [ ] 	Proxies
- [ ] 	Pub/Sub architecture
- [x] 	Rest vs. Spread operator
- [ ] 	Same-origin policy with regards to JavaScript.
- [ ] 	Scope: Global vs. Lexical
- [x] 	Scope: lexical scope
- [x] 	Sets & methods associated with them
- [x] 	Sets: iterating over a set
- [x] 	Shallow vs. Deep copying
- [ ] 	Shimming
- [x] 	Statically Typed vs. Dynamically Typed vs. Weakly Typed
- [ ] 	stopPropagation vs. preventDefault (interview)
- [x] 	Strict mode
- [x] 	Strict mode: Can strict mode be used within functions or block statements?
- [x] 	Strings: `trim()`
- [x] 	Strings: 3 common methods for working with characters
- [ ] 	Strings: An algorithm that returns the first duplicate character in a string (interview)
- [ ] 	Strings: Given a string (understood to be a sentence), reverse the order of the words. "Hello world" becomes "world Hello"
- [x] 	Strings: padStart() and padEnd()
- [x] 	Strings: Search() vs. indexOf()
- [x] 	Strings: Search() vs. Match()
- [x] 	Strings: substring vs. substr vs. slice
- [ ] 	Symbols
- [ ] 	Tagged template literal
- [ ] 	Temporal dead zone
- [ ] 	Ternary operator: what does the word "Ternary" indicate?
- [ ] 	toString() parameters
- [ ] 	Type Coercion (interview)
- [x] 	typeof operator
- [x] 	typeof vs. instanceof
- [x] 	Unary operators
- [x] 	V8 and SpiderMonkey.

## Interview

- [ ] How do  you find a missing number in 1..n numbers. (interview)
- [ ] Describe Type Coercion in JavaScript. (interview)
- [ ] How do you implement Encapsulation in JavaScript? (interview)
- [ ] An algorithm that returns the first duplicate character in a string (interview)
- [ ] In a given sorted array of integers remove all the duplicates. (interview)
- [ ] Write a method to decide if the given binary tree is a binary search tree or not. (interview)
- [ ] Given a string (understood to be a sentence), reverse the order of the words. "Hello world" becomes "world Hello"
- [ ] how to sort a linked list using recursion only (interview)

## CSS

- [x] What does cascading in CSS mean?
- [x] What are some new features in CSS3?
- [ ] Compared with CSS2, CSS3 has adopted a modular approach for incorporating new features. What does this mean?
- [x] What is a CSS preprocessor?
- [x] What is Sass?
- [ ] What are some features of Sass?
- [ ] CSS IDs vs. Classes: IDs are unique per page but classes can be reused
- [x] CSS Child combinator vs. Descendant combinator
- [ ] BEM vs. SMACSS
- [x] How would you import a CSS file into another?
- [x] Grid vs. Flexbox. When would you use one over the other?
- [x] Using CSS grids, how do you make a div start at column 2 and end before column 4? (two ways)
- [x] Describe the CSS box model.
- [ ] What are the four CSS combinators?
- [x] CSS pseudo-classes vs pseudo-elements
- [ ] What are CSS pseudo-elements and how are they used?
- [ ] What are CSS pseudo-classes and how are they used?
- [ ] What are attribute selectors in CSS?
- [ ] Explain some of the pros and cons for CSS animations versus JavaScript animations.
- [ ] What is CSS selector specificity and how does it work?
- [x] What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?
- [ ] Describe z-index and how stacking context is formed.
- [ ] Describe BFC (Block Formatting Context) and how it works.
- [x] What does `{ box-sizing: border-box; }` do? What are its advantages?
- [ ] What's the difference between the `nth-of-type()` and `nth-child()` selectors?
- [ ] Describe the usage of border images in CSS.
- [x] Describe the usage of background images in CSS.
- [x] contain vs. cover when using background-size in CSS.
- [ ] What's the difference between a relative, fixed, absolute and statically positioned element?
- [x] What is Tweening?
- [ ] What is the use of CSS sprites?
- [x] What CSS property would you use to hide the bullets in an unordered list?
- [x] rem vs. em
- [ ] word-break vs. word-wrap
- [ ] overflow-wrap
- [x] How do we adjust the spacing between lines in CSS?
- [ ] Various overflow parameters
- [x] Describe the HSL color model.
- [x] Hex vs. RGB vs. HSL and pros & cons of each
- [x] RGB vs. RGBA
- [x] Describe the usage of box-shadow in CSS.
- [ ] Box shadow vs. Text shadow
- [ ] Linear vs. Radial gradient
- [ ] Transition vs. Transformation vs. Animation
- [x] How do you use the `transition` shorthand property in CSS?
- [ ] Pros and cons of using web fonts
- [ ] GSAP vs. CSS animations
- [x] CSS `display: none` vs. `visibility: hidden`
- [x] position:sticky vs. position:fixed
- [ ] what is transform-origin?

## HTML

- [x] What is Doctype?
- [ ] How do you serve a page with content in multiple languages?
- [x] What are some new features of HTML5? (e.g. new tags introduced in HTML5)
- [ ] What are `data-` attributes good for?
- [ ] What is a MIME type?
- [x] What is the difference between defer and async when loading JavaScript scripts?
- [ ] Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
- [ ] Can a web page contain multiple `<header>` elements? What about `<footer>` elements?
- [ ] What’s the difference between the `<svg>` and `<canvas>` elements?
- [ ] How to draw rectangle using Canvas and SVG using HTML5 ?
- [ ] What are `<dl>`, `<dt>` and `<dd>` tags used for?
- [x] What is `<map>` used for in HTML?
- [x] What is the use of `<figure>` in HTML5?
- [ ] What is `<datalist>` used for in HTML?
- [x] What are different ways to integrate a CSS into a Web page?
- [ ] Should a website always have a `H1` tag? Is it possible to have multiple `H1` tags on a page?
- [ ] In HTML, what is the difference between `icon` and `shortcut icon` when used in the `<link rel=" " ...>` tag?
- [x] What are 2 advantages of using the `<label>` element in an HTML form?
- [x] How would you associate a label with its corresponding input element in an HTML form?
- [x] What is the difference between using `<input type="button" />` and `<button>...</button>` in a form?

## General (front-end tools & technologies, performance, testing, accessibility, SEO, basic DevOps, agile, etc.)

- [x] What is the difference between a library and a framework?
- [x] What is Node.js?
- [ ] Describe the event loop in Node.
- [ ] What is React?
- [ ] Is Node a framework?
- [ ] Is React a framework? Why or why not?
- [ ] What are some advantages of using React over Vanilla JavaScript?
- [ ] Is it always a better idea to use React than Vanilla JavaScript in a project?
- [ ] What is an SPA?
- [ ] When would you not want to use a Single Page Application?
- [ ] What do we mean by a static site?
- [ ] What are tools like Gatsby or Jekyll used for?
- [ ] What is CRUD?
- [ ] What is an MVC? What are some pros and cons of using an MVC?
- [ ] Are MVCs and frameworks the same?
- [ ] What is an MVVC?
- [ ] What is GraphQL?
- [ ] What is Apollo?
- [ ] What is WebPack?
- [ ] What are NPM and Yarn used for?
- [ ] What is jQuery?
- [ ] Why has jQuery become less popular in recent years?
- [ ] What is ReactNative?
- [ ] What is Redux?
- [ ] What is Svelte?
- [ ] What is Flutter?
- [ ] What is a linter?
- [ ] What is a PWA?
- [ ] What is a CMS?
- [ ] What is WordPress?
- [ ] WordPress vs. Drupal vs. Joomla
- [ ] What is Docker?
- [ ] What is AWS?
- [ ] Describe the Serverless architecture?
- [ ] What is AWS Lambda?
- [ ] What is Ansible?
- [ ] What is Kubernetes?
- [ ] What is Elasticsearch?
- [ ] VMs vs. Containers
- [ ] SQL vs. NoSQL databases?
- [ ] What is Redis?
- [ ] What is Nginx?
- [ ] What is a templating language?
- [ ] What is a REPL?
- [ ] What is a CLI?
- [x] What does a Load Balancer do and what are some of its advantages?
- [ ] Caching
- [ ] What is database sharding?
- [ ] CI/CD
- [ ] What are web components?
- [ ] What is lazyloading?
- [ ] What are some ways to improve performance of a page?
- [ ] What are some ways that Chrome DevTools can help us with finding ways to improve our site performance?
- [ ] Name 3 ways to decrease page load (perceived or actual load time).
- [ ] What are some ways to increase code maintainability?
- [ ] What are some a11y guidelines?
- [ ] Describe ARIA.
- [ ] What are some of the tools available to test the accessibility of a website or web application?
- [ ] What are skip links? What benefit(s) do they provide? What are some of their limitations?
- [ ] What is WCAG? What are the differences between A, AA, and AAA compliance?
- [ ] What are some SEO best practices?
- [ ] Describe the difference between progressive enhancement and graceful degradation.
- [ ] What is progressive rendering?
- [ ] What is a polyfill?
- [ ] What are some things you can do to make a website compatible with some earlier versions of IE?
- [ ] How would you go about accepting payments via Credit cards or PayPal for a shopping cart feature you are developing for a client?
- [ ] How many resources will a browser download from a given domain at a time? What are the exceptions?
- [ ] What is a CDN and what is the benefit of using one?
- [ ] What is domain pre-fetching and how does it help with performance?
- [x] What is an API?
- [x] What is REST? What does it mean for an API to ne RESTful?
- [x] What are the four parts of a RESTful web service request?
- [x] REST APIs are stateless. What does this mean?
- [x] PUT vs. PATCH methods in RESTful APIs
- [ ] REST vs. SOAP APIs
- [ ] What is HTTP? List some of the HTTP methods that you are familiar with.
- [ ] Is HTTP the same as REST?
- [ ] What is the purpose of a HTTP header?
- [ ] HTTP vs HTTPS
- [ ] What are the HTTP status codes?
- [ ] Web 2.0
- [ ] URL vs. URI
- [ ] What is a Clean URL?
- [ ] What is TCP/IP?
- [ ] TCP vs. UDP (Interview)
- [ ] SaaS vs. PaaS
- [ ] What is AJAX?
- [ ] JSON vs. XML
- [ ] JSONP
- [ ] Native vs. Hybrid apps
- [ ] What are microservices and how do they differ from monoliths?
- [ ] What is middleware?
- [ ] What is functional programming? How does it differ from object oriented programming?
- [x] What are the four pillars of object oriented programming
- [ ] What are the SOLID principles?
- [ ] Software Development Life Cycle (SDLC)
- [ ] What does it mean for an image to be optimized for web?
- [ ] What are some ways to optimize an image for web?
- [ ] JPEG vs. PNG vs. GIF
- [ ] What is data binding?
- [ ] What is server side rendering and why would you want to do it?
- [ ] How does Server side rendering differ from Client side rendering?
- [ ] What is the DOM? What is the virtual DOM?
- [ ] What is Flash of Unstyled Content? How do you avoid FOUC?
- [ ] What is Dependency injection?
- [ ] As front-end developers, do we need to worry about SQL injections?
- [ ] What is Cross Site Scripting (XSS)?
- [ ] What does CORS stand for and what issue does it address?
- [ ] Unit testing vs. functional/integration testing
- [ ] BDD vs. TDD
- [ ] What is Selenium?
- [ ] What are some best practices for a 404 page?
- [ ] How does a 403 differ from 404 error?
- [ ] What are some causes of a 500 error?
- [ ] What are some best practices when designing a form?
- [ ] How can we make a form more accessible?
- [ ] What is a Websocket?
- [ ] Web workers
- [ ] Concurrency vs. Parallelism
- [ ] Service worker
- [ ] What is SVG?
- [ ] Vector vs. raster images
- [ ] Is it better to perform animations on a webpage using CSS or JavaScript?
- [ ] What is Minifying? Is it always a good idea to minify?
- [ ] Bulma vs. Bootstrap
- [ ] Materialize vs. Bootstrap
- [ ] ORM
- [ ] What is SSH?
- [ ] What is SSL?
- [ ] DNS
- [ ] What happens behind the scenes when you enter a URL into the browser and press enter.
- [ ] Sessions vs. Cookies
- [ ] Cookie vs. SessionStorage vs. LocalStorage.
- [ ] What is the lifetime of local storage?
- [ ] What is agile?
- [ ] Agile vs. Waterfall
- [ ] What is scrum?
- [ ] Scrum artifacts
- [ ] Scrum ceremonies
- [ ] Scrum vs. Kanban
- [ ] What is acceptance testing?
- [ ] What is Extreme Programming (XP)?
- [ ] What is a wireframe? Are you familiar with any wireframing tools?
- [ ] Low-fidelity vs. High-fidelity prototyping
- [ ] What is UX?
- [ ] What are personas in the context of UX?
- [ ] What is a user journey map?
- [ ] What is content strategy?
- [ ] What is usability testing?
- [ ] What is A/B testing?
- [ ] What is visual hierarchy?
- [ ] In the context of databases, what is a transaction? What are the ACID properties?

## Git

- [ ] What is Git?
- [ ] How does Git differ from GitHub? Can you use Git without GitHub?
- [ ] What is a Git repository? How does it differ from a branch?
- [ ] Git command to create a new branch and switch to it: `git checkout -b <branchname>`
- [ ] Git command to switch from one branch to another: `git checkout <branchname>`
- [ ] Git command to list all branches in a repo: `git branch`
- [ ] Git command to delete a feature branch: `git branch -d <branchname>`
- [ ] What is the `origin`?
- [ ] SSH vs. Https when cloning a repo
- [ ] Cloning vs. Forking
- [ ] What is gitignore?
- [ ] How do you undo and edit the last commit message?
- [ ] How do you undo your most recent commit before it is pushed? How about after it's been pushed?
- [ ] How do you delete a feature branch?
- [ ] How do you rename a feature branch?
- [ ] How do you merge a feature branch into the master branch?
- [ ] What is a pull request and why is it beneficial?
- [ ] How do you do a pull request?
- [ ] How do you see a list of most recent commits to a branch?
- [ ] What is cherry-pick used for?
- [ ] What is stash used for?
- [ ] How do you add a new remote Git repository to your project?
- [ ] How do rename an existing remote Git repository in your project?
- [ ] How do you view the remote Git repository in your project?
- [ ] How do you view your credentials (e.g. email and name) for a git repository?
- [ ] Remote vs. Origin
- [ ] Rebase vs. Fetch
- [ ] Pull vs. Fetch
- [ ] What does the `-u` flag in `git push -u origin master` do?
  
## Data Structures & Algorithms

- [ ] What are hash tables?

## Tutorials

- [ ] Pagination
- [ ] Carousel
