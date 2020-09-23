# Study Notes for Front-end web development

<div align="center">
<h1>Javascript</h1>
</div>

🌼 Arrays: concat()  
🌼 Arrays: copying & the problem with using Array 1 = Array 2  
🌼 Arrays: creation & initialization  
🌼 Arrays: create an array with an initial length of 20  
🌼 Arrays: every() vs. some()  
🌼 Arrays: fill()  

<details><summary>Answer</summary>
<p>

- The fill() method changes all elements in an array to a static value.
- fill() is a mutator method: it will change the original array and return it, not a copy of it.

```markdown
arr.fill(value, start(optional), end(optional))
```

```javascript
const array1 = [1, 2, 3, 4];

console.log(array1.fill(0, 2, 4)); //=> [1, 2, 0, 0]
console.log(array1.fill(5, 1)); //=> [1, 5, 5, 5]
console.log(array1.fill(6)); //=> [6, 6, 6, 6]
```

</p></details>

🌼 Arrays: filter()  
🌼 Arrays: flat()  

<details><summary>Answer</summary>
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
🌼 Arrays: splice()  
🌼 Arrays: splice() vs. slice()  
🌼 Arrays: the three methods introduced in ES6 that allow us to inspect all elements of an array.  
🌼 Arrays: the three methods used to perform a search in an array?

<details><summary>Answer</summary>
<p>

- ECMAScript’s three strict equivalence lookup methods are `indexOf()` and `lastIndexOf()`, available in all ECMAScript versions, and `includes()`, which was introduced in the ECMAScript 7 specification.

</p></details>

🌼 Arrays: why is it Not recommended to use `for.. in` loops to iterate over an array.  
expressions  
🌼 Async & Await  
🌼 Atomics  
🌼 Bitwise operators  
🌼 BOM (Browser Object Model)  

<details><summary>Answer</summary>
<p>

- The Browser Object Model (BOM) is a browser-specific convention referring to all the objects exposed by the web browser.
- Unlike the DOM, there is no standard for implementation and no strict definition, so browser vendors are free to implement the BOM in any way they wish.
- The top level of the hierarchy is the window object which represents the browser window.

</p></details>

🌼 Call vs. Apply  
🌼 Call vs. Apply vs. Bind  
🌱 Callback  
🌼 Classes: static methods  
🌼 Classes: static method being called from the class constructor or from other non-static methods within the same class  
🌼 Classes: static method calling another static method within the same class  
🌼 Closure  
🌼 CommonJS  
🌱 Compiling vs. Transpiling  
🌼 console.log() vs. console.dir()  
🌼 Currying  

<details><summary>Answer</summary>
<p>

- Currying transforms a function with multiple arguments into a sequence of functions each taking a single argument.
- For instance it can make function `f(a,b,c)` callable as `f(a)(b)(c)`.

For example,

```javascript
function multiply(a, b, c) {
  return a * b * c;
}
multiply(1,2,3); // 6
```

can be modified to its curried version as such:

```javascript
function multiply(a) {
  return (b) => {
    return (c) => {
      return a * b * c;
    }
  }
}
multiply(1)(2)(3); // 6
```

</p></details>

🌱 Date and Time formatting  
🌱 Debounce vs. throttle  
🌱 Debounce: when do we use a debounce function?  
🌱 Decimal points handling (since there is no Float data type)  
🌱 Decorators  
🌱 Design Pattern: Builder  
🌱 Design Pattern: Factory  
🌱 Design Pattern: Module  
🌱 Design Pattern: Nullobject  
🌱 Design Pattern: Singleton  
🌱 Destructuring an object or an array (Give an example)  
🌱 Encapsulation: how do you implement Encapsulation in JavaScript? (interview)  
🌱 Error Handling  
🌱 ES2020 (ES11) new features  
🌱 Eval()  
🌱 Event bubbling vs. Event capturing  
🌱 Event bubbling vs. Event propagation  
🌱 Event delegation  
🌱 Event listeners: target vs. currentTarget  
🌱 Event listeners. Name 5 events JS could be listening to.  
🌱 Event loop  
🌱 Event loop: Call stack vs. Task queue  
🌱 Event propagation. The three phases of event propagation.  
🌼 Falsy values

<details><summary>Answer</summary>
<p>

- A falsy value is a value that is considered false when encountered in a Boolean context.
- There are 8 falsy values: `false`, `0`, `-0`, `0n` (BigInt), `' '` (Empty string), `null`, `undefined`, `NaN`.

</p></details>

🌱 Feature detection, feature inference, and using the UA string  
🌼 for.. in vs. for.. of  

<details><summary>Answer</summary>
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
🌼 Functions: `arguments` object  
🌼 Functions: arrow functions vs. classic functions (4 differences)  

<details><summary>Answer</summary>
<p>
1. An arrow function does not have its own this. In regular functions the this keyword represented the object that called the function, which could be the window, the document, a button or whatever. With arrow functions the this keyword always represents the object that defined the arrow function (lexical).
2. Arrow functions cannot be used as constructors and will throw an error when used with new.
3. Unlike regular functions, the `arguments` object is not defined for arrow functions.
4. Arrow functions do not have a prototype property.

</p></details>

🌱 Functions: `function Person(){}` vs. `var person = Person()` vs. `var person = new Person()`  
🌼 Functions: higher order functions  

<details><summary>Answer</summary>
<p>

- Higher order functions take another function as an argument or return a function.
- Taking another function as an argument is often referred to as a callback function

</p></details>

🌼 Functions: idempotent functions  
🌼 Functions: pure functions  
🌼 Functions: why do we say that in JavaScript, functions are first class citizens.  
🌼 Generator functions & yield keyword  
🌼 Generators  
🌼 Getters & Setters  
🌼 Hoisting  

<details><summary>Answer</summary>
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
🌱 Immutability  
🌼 Importing a JavaScript file into HTML  
🌼 Interpreter vs. Compiler  
🌱 Iterable vs. Enumerable  
🌱 Iterators  
🌱 Iterators used with Generators  
🌱 Jasmine vs. Mocha vs. Chai  
🌼 JavaScript vs. ECMAScript  
🌼 JavaScript vs. TypeScript  
🌼 JSON parse() vs. stringify()  

<details><summary>Answer</summary>
<p>

- `JSON.parse()` takes a JSON string and transforms it into a JavaScript object.
- `JSON.stringify()` takes a JavaScript object and transforms it into a JSON string.

```javascript
const obj = {
  name: 'John',
  age: 23,
  favoriteFood: 'Pizza'
};

const objStr = JSON.stringify(obj);

console.log(objStr);
// "{"name":"John","age":23,"favoriteFood":"Pizza"}"

console.log(JSON.parse(objStr));
// Object {name:"John",age:23,favoriteFood:"Pizza"}
```

</p></details>

🌼 let vs. const  
🌼 let vs. var  
🌱 Maps  
🌱 Maps vs. WeakMaps  
🌱 Modules  
🌱 Modules: Tree shaking  
🌱 Multi-threaded: is JavaScript multi-threaded?  
🌱 NaN: where would be a situation in which you would see `NaN`. How to check for NaN?  
🌼 null vs. undefined  
🌼 null == undefined? How about null === undefined?  
🌼 Null: how to check if something is null? How about undefined?  
🌼 Null: what does `typeof null` return?  
🌱 Nullish coalescing operator  
🌼 Objects: assign()  

<details><summary>Answer</summary>
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

🌼 Objects: assign() - A problem with using it to copy objects  

<details><summary>Answer</summary>
<p>

- Object.assign() only does shallow copying. For deep cloning, we need to use alternatives. A common hack is to use `JSON.parse(JSON.stringify(obj))` as such:

```javascript
  obj1 = { a: 0 , b: { c: 0}};
  let obj2 = JSON.parse(JSON.stringify(obj1));
  console.log(JSON.stringify(obj2)); //=> { "a": 0, "b": { "c": 0}}

  obj1.a = 4;
  obj1.b.c = 4;
  console.log(JSON.stringify(obj2)); //=> { "a": 0, "b": { "c": 0}}
  ```

</p></details>

🌼 Objects: cloning an object (two ways)  

<details><summary>Answer</summary>
<p>

- Both of these methods perform shallow cloning:


```javascript
const obj = {a: 1};

const copy1 = Object.assign({}, obj) ;
console.log(copy1); //=> {a: 1}

const copy2 = {...obj} ;
console.log(copy2); //=> {a: 1}
```

</p></details>

🌼 Objects: create()  
🌼 Objects: creation & initialization (two ways)  

<details><summary>Answer</summary>
<p>

- There are two ways to explicitly create an instance of Object.
- The first is to use the new operator with the Object constructor like this:

```javascript
let person = new Object();
person.name = "Nicholas";
person.age = 29;
```

- The other way is to use object literal notation:

```javascript
let person = {
  name: "Nicholas",
  age: 29
};
```

</p></details>

🌼 Objects: entries()  

<details><summary>Answer</summary>
<p>
- The Object.entries() method returns an array of a given object's own enumerable string-keyed property [key, value] pairs.

```javascript
const obj = {
  a: 'something',
  b: 42,
};

console.log(Object.entries(obj));
//=> [['a', 'something'], ['b', 42]]

for (const [key, value] of Object.entries(obj)) {
console.log(`${key}: ${value}`);
//=> a: something, b: 42
}
```

</p></details>

🌼 Objects: freeze()  

<details><summary>Answer</summary>
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

🌼 Objects: freeze() vs. seal()  

<details><summary>Answer</summary>
<p>

- `Object.freeze()` makes it impossible to add, remove, or modify properties of an object.
- `Object.seal()` is similar, however it does allow exiting properties to be modified.

</p></details>

🌱 Objects: freeze() vs. preventExtensions()  
🌼 Objects: fromEntries()  

<details><summary>Answer</summary>
<p>

- The `Object.fromEntries()` method transforms a list of key-value pairs into an object. It accepts an iterable such as Array or Map and returns a new iterable object.

```javascript
const map = new Map([ ['foo', 'bar'], ['baz', 42] ]);
const obj = Object.fromEntries(map);
console.log(obj); //=> { foo: "bar", baz: 42 }

const arr = [ ['0', 'a'], ['1', 'b'], ['2', 'c'] ];
const obj = Object.fromEntries(arr);
console.log(obj); // { 0: "a", 1: "b", 2: "c" }
```

</p></details>

🌼 Objects: hasOwnProperty()  

<details><summary>Answer</summary>
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

<details><summary>Answer</summary>
<p>

- By using the `Array.isArray()` method.

```javascript
if (Array.isArray(obj)) {
  // do something on the array
}
```

</p></details>

🌱 Objects: immutable objects  
🌱 Objects: is everything in JavaScript considered an object?  
🌱 Objects: is()  
🌼 Objects: iterating over object properties  
🌼 Objects: the optional chaining operator `?.`

<details><summary>Answer</summary>
<p>

- The optional chaining operator `?.` allows us to optionally access deeper nested properties within objects without having to expressly validate that each reference in the chain is valid.  
- The `?.` operator functions similarly to the `.` chaining operator, except that instead of causing an error if a reference is nullish (`null` or `undefined`), the expression short-circuits with a return value of `undefined`. When used with function calls, it returns `undefined` if the given function does not exist.

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

<details><summary>Answer</summary>
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

<details><summary>Answer</summary>
<p>

- In shallow copying, both items point to the same memory location.
- In deep copying, the second item is assigned a separate memory location than the original item.
- In other words, in a shallow copy, object B points to object A's location in memory. In deep copy, all things in object A's memory location get copied to object B's memory location.

![Shallow versus deep cloning diagram](https://i.stack.imgur.com/AWKJa.jpg)

</p></details>

🌱 Shimming  
🌼 Statically Typed vs. Dynamically Typed vs. Weakly Typed  
🌱 stopPropagation() vs. preventDefault()  
🌼 Strict mode  
🌼 Strict mode: Can strict mode be used within functions or block statements?  
🌼 Strings: trim()  
🌼 Strings: 3 common methods for working with characters  
🌱 Strings: An algorithm that returns the first duplicate character in a string (interview)  
🌱 Strings: Given a string (understood to be a sentence), reverse the order of the words. "Hello world" becomes "world Hello"  
🌼 Strings: padStart() and padEnd()  
🌼 Strings: indexOf() vs. search()  

<details><summary>Answer</summary>
<p>

- `indexOf()` is for searching for plain substrings. It also allows us to specify a starting index. It does not allow for regular expressions.
- `search()` allows for substrings as well as regular expressions. It does not allow for a starting index.

```javascript
console.log('Blue Whale'.indexOf('Whale', 3)); //=> 5
console.log('hey JudE'.search(/[A-Z]/g)); //=> 4
```

</p></details>

🌼 Strings: search() vs. match()  

<details><summary>Answer</summary>
<p>

- `Search()` returns the index of the first match between the regular expression and the given string, or `-1` if no match was found.
- `Match()` returns an array or `null` if no matches are found.

```javascript
const str1 = 'hey JudE';
console.log(str1.search(/[A-Z]/g)); // 4

const str2 = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz';
console.log(str2.match(/[A-E]/gi)); // ['A', 'B', 'C', 'D', 'E', 'a', 'b', 'c', 'd', 'e']
```

</p></details>

🌼 Strings: substring vs. substr vs. slice  
🌱 Symbols  
🌱 Tagged template literal  
🌱 Temporal dead zone  
🌱 Ternary operator: what does the word "Ternary" indicate?  
🌼 `this` keyword  
🌱 toString() parameters  
🌱 Type Coercion  
🌼 typeof operator (8 possible types)  

<details><summary>Answer</summary>
<p>

- The typeof operator returns a string indicating the type of the unevaluated operand.
- The possible return values are: `object`, `boolean`, `number`, `bigint`, `string`, `symbol`, `function`, `undefined`.

```javascript
console.log(typeof 3.14); //=> number
console.log(typeof NaN); //=> number
console.log(typeof 42n); //=> bigint
console.log(typeof 'hello'); //=> string
console.log(typeof true); //=> boolean
console.log(typeof Symbol('foo')); //=> symbol
console.log(typeof someVariable); //=> undefined
console.log(typeof [1, 2]); //=> object
console.log(typeof { a: 1 }); //=> object
console.log(typeof null); //=> object
console.log(typeof Math.min); //=> function
console.log(typeof function() {}); //=> function
console.log(typeof class C {}); //=> function
```

</p></details>

🌼 typeof vs. instanceof  
🌼 Unary operators  
🌼 Unary operators: what is `~3` equal to?  

<details><summary>Answer</summary>
<p>

- The bitwise Not operator `~` converts the integer `N` to `-(N+1)` value. Therefore `~3 = -4`.

</p></details>

🌼 Unary operators: what is `~~3.9` equal to?  

<details><summary>Answer</summary>
<p>

- Double bitwise NOT performs the same operation as the `Math.floor()` method but a lot quicker.

```javascript
~~3.9 === Math.floor(3.9); //true, 3
~~2.4 === Math.floor(2.4); //true, 2
~~2 === Math.floor(2); //true, 2
```

</p></details>

🌼 V8 and SpiderMonkey.  
🌼 `-0` vs. `+0`  






<div align="center">
<h1>Web APIs</h1>
</div>





🌱 Canvas API  
🌱 Console API  
🌱 Document Object Model (DOM)  
🌱 DOM: classList and its common methods  
🌱 DOM: cloneNode()  
🌱 DOM: closest()  
🌱 DOM: childNodes vs. children  
🌱 DOM: firstChild vs. firstElementChild  
🌱 DOM: getAttribute() & setAttribute()  
🌼 DOM: getInnerText() vs. getHTML() vs. getTextContent()  

<details><summary>Answer</summary>
<p>

- The `innerText` property returns just the text, without spacing and inner element tags.
- The `innerHTML` property returns the text, including all spacing and inner element tags.
- The `textContent` property returns the text with spacing, but without inner element tags.


```html
<p id="demo">   This element has extra spacing     and contains <span>a span element</span>.</p>

<script>
  function getInnerText() {
    console.log(document.getElementById("demo").innerText);
    //=> "This element has extra spacing and contains a span element."
  }

  function getHTML() {
    console.log(document.getElementById("demo").innerHTML);
    //=> "   This element has extra spacing     and contains <span>a span element</span>."
  }

  function getTextContent() {
    console.log(document.getElementById("demo").textContent);
    //=> "   This element has extra spacing    and contains a span element."
  }
</script>
```

</p></details>

🌱 DOM: parentNode vs. parentElement  
🌼 DOM: Six JavaScript methods to access DOM elements

<details><summary>Answer</summary>
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

🌼 DOM: getElement(s)By* vs. querySelector(All) methods

<details><summary>Answer</summary>
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

🌱 DOM: previousSibling vs. previousElementSibling  
🌱 Drag & Drop API  
🌱 Fetch API  
🌱 History API  
🌱 HTMLCollection vs. NodeList  
🌱 Geolocation API  
🌱 Service Workers API  
🌱 Touch events  
🌱 URL API  
🌱 Web Storage API  
🌱 Web Workers API  
🌱 WebGL  
🌱 WebSocket API  
🌱 Window  






<div align="center">
<h1>CSS</h1>
</div>






🌼 Animations: animation-fill-mode  

<details><summary>Answer</summary>
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

<details><summary>Answer</summary>
<p>

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

<details><summary>Answer</summary>
<p>

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
🌼 display: none vs. visibility: hidden  
🌼 Flex: `flex: auto` vs. `flex: none`  
🌼 Grid vs. Flexbox  
🌼 Grids: create a grid with three equal columns (2 ways)  

<details><summary>Answer</summary>
<p>

```css
grid-template-columns: 1fr 1fr 1fr;

grid-template-columns: repeat(3, 1fr);
```

</p></details>

🌼 Grids: how do you make a div start at column 2 and end before column 4? (two ways)  
🌱 GSAP vs. CSS animations  
🌼 Hex vs. RGB vs. HSL  
🌼 HSL color model  
🌼 Importing a CSS file into another  

<details><summary>Answer</summary>
<p>

`@import url('navigation.css');` or `@import 'navigation.css';`

</p></details>

🌼 Line spacing: e.g. how to adjust the space between lines in a paragraph.  

<details><summary>Answer</summary>
<p>

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

<details><summary>Answer</summary>
<p>

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

<details><summary>Answer</summary>
<p>

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
🌼 Pseudo-classes vs pseudo-elements  

<details><summary>Answer</summary>
<p>
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
🌼 Reset vs. Normalize  
🌼 RGB vs. RGBA  

<details><summary>Answer</summary>
<p>

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

<details><summary>Answer</summary>
<p>

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







<div align="center">
<h1>HTML</h1>
</div>






🌼 Button tag vs. input type="button"  
🌱 Can a web page contain multiple `<header>` elements? What about `<footer>` elements?  
🌱 Canvas tag  
🌼 data-* attributes  

<details><summary>Answer</summary>
<p>

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

🌼 Datalist tag  

<details><summary>Answer</summary>
<p>

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

<details><summary>Answer</summary>
<p>

- `DOCTYPE` or Document Type Declaration is not an HTML tag; it is an instruction to the web browser about what version of HTML the page is written in.
- Using it ensures that the user agent correctly parses the HTML as you intended it.
- HTML5: `<!DOCTYPE html>`
- HTML4: `<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">`

</p></details>

🌼 Favicons: what are two ways to implement a favicon on a webpage?

<details><summary>Answer</summary>
<p>

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

<details><summary>Answer</summary>
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

🌱 How to create a drop-down list?  
🌱 How to draw rectangle using Canvas and SVG using HTML5?  
🌱 How to serve a page with content in multiple languages?  
🌼 HTML5 new features  
🌱 Image tag: what is the `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.  
🌼 Integrate CSS into a Web page (three ways)  
🌼 Label tag: 2 advantages of using it in an HTML form.  
🌼 Label tag: how to associate a label with its corresponding input element in an HTML form?  
🌼 Map tag  

<details><summary>Answer</summary>
<p>
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
🌱 Should a website always have a `H1` tag? Is it possible to have multiple `H1` tags on a page?  
🌱 Svg tag and how it differs from `<canvas>`  
🌱 Tables: `<thead>` vs. `<th>`  
🌱 Wbr tag  







<div align="center">
<h1>React</h1>
</div>

🌱 Components: How to prevent from re-rendering
🌱 Lifecycle methods and their purpose  






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

<details><summary>Answer</summary>
<p>

- An application programming interface (API) is a set of clearly defined methods of communication among various components.
- An API simplifies programming by abstracting the underlying implementation and only exposing objects or actions the developer needs.

![API visual](../../blob/master/images/api.png)  
Image credit: [https://learn.g2.com/api](https://learn.g2.com/api)

</p></details>

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
🌱 Imperative vs. Declarative Programming  
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

<details><summary>Answer</summary>
<p>

- REST is acronym for REpresentational State Transfer.
- It is an architectural style that developers follow when they create their RESTful APIs.

</p></details>

🌱 REST vs. SOAP APIs  
🌼 RESTful API (6 constraints)  

<details><summary>Answer</summary>
<p>

- In order to be a true RESTful API, a web service must adhere to the following six REST architectural constraints:
  
1. **Client-Server based**:  
The client and the server should be separate from each other and allowed to evolve individually and independently.
2. **Use of a uniform interface (UI)**:  
The key to the decoupling client from server is having a uniform interface that allows independent evolution of the application without having the application’s services, models, or actions tightly coupled to the API layer itself. The uniform interface lets the client talk to the server in a single language, independent of the architectural backend of either.
3. **Stateless operations**:  
Meaning that requests can be made independently of one another, and each request contains all of the data necessary to complete itself successfully. A REST API should not rely on data being stored on the server or sessions to determine what to do with a request, but rather solely rely on the data that is provided in that request itself. Identifying information is not being stored on the server when making requests. Instead, each request has the necessary data in itself, such as the API key, access token, user ID, etc.
4. **Caching**:  
A REST API should be designed to encourage the storage of cacheable data on the client side in order to reduce the number of interactions with the API. This means that when data is cacheable, the response should indicate that the data can be stored up to a certain time (expires-at), or in cases where data needs to be real-time, that the response should not be cached by the client.
5. **Layered system**:  
REST allows for an architecture composed of multiple layers of servers. The requesting client need not know whether it’s communicating with the actual server, a proxy, or any other intermediary.
6. **Code on demand (optional)**:  
Most of the time, a server will send back static representations of resources in the form of XML or JSON. However, when necessary, servers can send executable code to the client.

</p></details>

🌼 RESTful APIs are stateless. What does this mean?  

<details><summary>Answer</summary>
<p>

- It means that API requests can be made independently of one another, and each request contains all of the data necessary to complete itself successfully.

</p></details>

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
🌱 WebSockets  
🌱 Wireframe: are you familiar with any wireframing tools?  
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

🌱 Form design & validation  
🌱 Image carousel  
🌱 Infinite scrolling  
🌱 Pagination  
🌱 Pinterest board  
🌱 Progress bar  




<div align="center">
<h1>Coding Challenges</h1>
</div>




🌼 Given an input string and an integer array indices of the same length. The input string will be shuffled such that the character at the `i`th position moves to `indices[i]` in the shuffled string. Return the shuffled string.  

```javascript
const shuffleString = (input, indices) => {
  // ...
};

input = "abc";
indices = [0,1,2];
console.log(shuffleString(input, indices)); // "abc"

input = "aiohn";
indices = [3,1,4,2,0];
console.log(shuffleString(input, indices)); // "nihao"

input = "aaiougrt";
indices = [4,0,2,6,7,3,1,5];
console.log(shuffleString(input, indices)); // "arigatou"

input = "art";
indices = [1,0,2];
console.log(shuffleString(input, indices)); // "rat"
```

<details><summary>Answer</summary>
<p>

```javascript
const shuffleString = (input, indices) => {
  const shuffledString = Array(input.length);
  indices.forEach((i, ele) => (shuffledString[i] = input.charAt(ele)));
  return shuffledString.join('');
};
```

</p></details>

🌼 A function that determines if a string has all unique characters.  

```javascript
const isUnique = str => {
  // ...
}

console.log(isUnique('abcd')); // true
console.log(isUnique('aabcd')); // false
```

<details><summary>Answer</summary>
<p>

```javascript
const isUnique = str => {
  let obj = {};
  for (char of str) {
    if (obj[char]) return false;
    obj[char] = true;
  }
  return true;
}
```

</p></details>
