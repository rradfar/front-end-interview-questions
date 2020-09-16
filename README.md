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

 🌼 `-0` vs. `+0`  
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
 🌼 Arrays: why is it Not recommended to use `for...in` loops to iterate over an array.  
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
 🌼 console.log() vs. console.dir()  
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
 🌱 Encapsulation: How do you implement Encapsulation in JavaScript? (interview)  
 🌱 Error Handling  
 🌱 ES2020 (ES11) new features  
 🌱 eval()  
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
 🌼 for in vs. for of  
 🌼 Functions vs. methods  
 🌱 Functions: `function Person(){}` vs. `var person = Person()` vs. `var person = new Person()`  
 🌼 Functions: Higher order functions  
 🌼 Functions: Idempotent function  
 🌼 Functions: Pure functions  
 🌼 Functions: why do we say that in JavaScript, functions are first class citizens.  
 🌼 Generator functions & yield keyword  
 🌼 Generators  
 🌼 Getters & Setters  
 🌼 Hoisting  
 🌱 Host objects vs. native objects  
 🌼 IIFE  
 🌱 Image carousel tutorial  
 🌱 Immutability  
 🌱 Immutable objects  
 🌼 Importing a JavaScript file into HTML  
 🌼 Interpreter vs. Compiler  
 🌱 Iterable vs. Enumerable  
 🌱 Iterators  
 🌱 Iterators used with Generators  
 🌱 Jasmine vs. Mocha vs. Chai  
 🌼 JavaScript vs. ECMAScript  
 🌼 JavaScript vs. TypeScript  
 🌱 JSON parse vs. stringify  
 🌼 Let vs. const  
 🌼 Let vs. var  
 🌱 Maps  
 🌱 Maps vs. WeakMaps  
 🌱 Modules  
 🌱 Modules: Tree shaking  
 🌱 Multi-threaded. Is JavaScript multi-threaded?  
 🌱 NaN: Where would be a situation in which you would see `NaN`. How to check for NaN?  
 🌼 null == undefined ? How about null === undefined?  
 🌼 Null vs. undefined  
 🌼 Null: How to check if something is null? How about undefined?  
 🌱 Nullish coalescing operator  
 🌼 Objects: assign()  
 🌱 Objects: assign() - Problem with not deep cloning  
 🌼 Objects: cloning an object  
 🌼 Objects: create()  
 🌼 Objects: Creation and initialization  
 🌼 Objects: freeze()  
 🌼 Objects: How to check if an object is an array?  
 🌱 Objects: Is everything in JavaScript considered an object?  
 🌱 Objects: is()  
 🌼 Objects: iterating over object properties  
 🌼 Objects: the two ways to access an object's properties.  
 🌱 Pagination tutorial  
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

<div align="center">
  <img height="60" src="./images/logos/css.png"> 
  <h1>CSS</h1>
</div>

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
 🌼 Line spacing  
 🌱 Linear vs. Radial gradient  
 🌼 list-style: none  
 🌱 nth-of-type() vs. nth-child()  
 🌱 Overflow parameters  
 🌱 overflow-wrap  
 🌱 Position: relative vs. fixed vs. absolute vs. static  
 🌼 position:sticky vs. position:fixed  
 🌼 Preprocessor  
 🌱 Pseudo-classes  
 🌼 Pseudo-classes vs pseudo-elements  
 🌱 Pseudo-elements  
 🌼 rem vs. em  
 🌼 Reset vs. Normalize  
 🌼 RGB vs. RGBA  
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
  <img height="60" src="./images/logos/html.png"> 
  <h1>HTML</h1>
</div>

🌱 `icon` and `shortcut icon` when used in the `<link rel=" " ...>` tag.  
🌱 `<dl>` vs. `<dt>` vs. `<dd>`  
🌼 `<figure>`  
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
🌱 How do you serve a page with content in multiple languages  
🌱 How to draw rectangle using Canvas and SVG using HTML5 .  
🌼 HTML5 new features  
🌼 Integrate CSS into a Web page (three ways)  
🌱 MIME type  
🌱 Should a website always have a `H1` tag? Is it possible to have multiple `H1` tags on a page?  
🌱 srcset attribute in an image tag. Explain the process the browser uses when evaluating the content of this attribute.  

<div align="center">
  <img height="60" src="./images/logos/cs.png"> 
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
  <img height="60" src="./images/logos/git.jpg"> 
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
  <img height="60" src="./images/logos/tutorials.png"> 
  <h1>Tutorials</h1>
</div>

 🌱 Form design  
 🌱 Image carousel  
 🌱 Infinite scrolling  
 🌱 Pagination  
 🌱 Pinterest board  
 🌱 Progress bar  
