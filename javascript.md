<div align="center">
<h1>Javascript</h1>
</div>
<ol>
<li>Arrays: concat(): 2 special notes</li>

<details><summary>Answer</summary><p>

1. It returns a newly constructed array. The original array remains **unchanged**.
2. The `concat()` method **flattens** the result.

```javascript
let colors = ["red", "green", "blue"];
let colors2 = colors.concat("yellow", ["black", "brown"]);
console.log(colors); // ["red", "green","blue"]
console.log(colors2); // ["red", "green", "blue", "yellow", "black", "brown"]
```

</p></details>

<li>Arrays: 2 ways to create a new array</li>

<details><summary>Answer</summary><p>

- By using the Array constructor

```javascript
let colors = new Array();
let colors = new Array(20);
let colors = new Array("red", "blue", "green");
```

- By using array literal notation

```javascript
let names = [];
let values = [1,2,];
let colors = ["red", "blue", "green"];
```

</p></details>

<li>Arrays: 3 ways to clone an array & why we don't use array1 = array2</li>

<details><summary>Answer</summary><p>

```javascript
const newArray = originalArray.slice();
const newArray = [...originalArray];
const newArray = Array.from(originalArray);
```

- If we use the equal sign, the second array will point to the same memory location as the original array (shallow copying), so any changes to the second array will be reflected in the original array as well and vice versa.

```javascript
let a = [1, 2];
let b = a;

a.push(3);
console.log(b); // [1, 2, 3]

b.push(4);
console.log(a); // [1, 2, 3, 4]
```

</p></details>

<li>Arrays: create an array with an initial length of 20</li>

<details><summary>Answer</summary><p>

```javascript
let arr = new Array(20);
```

</p></details>

<li>Arrays: every() vs. some()</li>

<details><summary>Answer</summary><p>

- The `every()` method tests whether all elements in the array pass the test implemented by the provided function.
- The `some()` method tests whether at least one element in the array passes the test implemented by the provided function.

```javascript
[12, 5, 8, 130, 44].every(x => x >= 10); // false
[12, 54, 18, 130, 44].every(x => x >= 10); // true​
[2, 5, 8, 1, 4].some(x => x > 10); // false
[12, 5, 8, 1, 4].some(x => x > 10); // true
```

</p></details>

<li>Arrays: fill()</li>

<details><summary>Answer</summary><p>

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

<li>Arrays: flat()</li>

<details><summary>Answer</summary><p>

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

<li>Arrays: flat() vs. flatmap()</li>

<details><summary>Answer</summary><p>

- `flat()` is simply used to flatten an array.
- `flatmap()` is the combination of the `map()` method followed by the `flat()` method to a  depth of 1.

```javascript
let sentences = ["JavaScript Array flatMap()", " ", "is", " ", "Awesome"];
let words = sentences.flatMap(s => s.split(' '));
console.log(words);
// [ 'JavaScript', 'Array', 'flatMap()', '', '', 'is', '', '', 'Awesome' ]
```

</p></details>

<li>Arrays: forEach() vs. map()</li>

<details><summary>Answer</summary><p>

- The `forEach()` method doesn't return anything (`undefined`). It simply calls a provided function on each element in the array. This callback is allowed to mutate the calling array.
- The `map()` method also calls a provided function on every element in the array. The difference is that `map()` utilizes return values and actually returns a new Array of the same size.

</p></details>

<li>Arrays: from()</li>

<details><summary>Answer</summary><p>

- `Array.from()` creates a new array instance from an array-like or iterable object.
- It has an optional map parameter, which allows us to execute a `map()` function on each element of the array being created.

```javascript
function f() {
  return Array.from(arguments);
}
console.log(f(1, 2, 3));  // [ 1, 2, 3 ]
```

</p></details>

<li>Arrays: indexOf() vs. lastIndexOf() vs. includes()</li>

<details><summary>Answer</summary><p>

- `indexOf()` searches the array for the specified item, and returns its position or `-1` if the item is not found. The search will start at the specified position or at the beginning if no start position is specified and end at the end of the array.
- `lastIndexOf()` searches the array for the specified item, and returns its position or `-1` if the item is not found. The search will start at the specified position or at the end if no start position is specified and end at the beginning of the array.
- `includes()` checks to see whether an array contains a specified element. If it does, it returns true, and false otherwise.

```javascript
const fruits = ['Banana', 'Orange', 'Apple', 'Mango', 'Banana', 'Orange', 'Apple'];
let a = fruits.indexOf('Apple', 4); // 6
let b = fruits.lastIndexOf('Apple', 4); // 2
let c = fruits.includes('Apple'); // true
```

</p></details>

<li>Arrays: join()</li>

<details><summary>Answer</summary><p>

- The `join()` method returns the array as a string.
- The elements will be separated by a specified separator. The default separator is comma `,`.
- This method will not change the original array.

```javascript
const elements = ['Fire', 'Air', 'Water'];
console.log(elements.join()); // "Fire,Air,Water"
console.log(elements.join('')); // "FireAirWater"
console.log(elements.join('-')); // "Fire-Air-Water"
```

</p></details>

<li>Arrays: reduce()</li>
<li>Arrays: reduce() vs. reduceRight()</li>
<li>Arrays: slice()</li>
<li>Arrays: splice()</li>
<li>Arrays: splice() vs. slice()</li>

<details><summary>Answer</summary><p>

- The `splice()` method changes the original array, `slice()` does not.
- The `splice()` method returns the removed items in an array. The `slice()` method returns the selected element(s) in an array, as a new array object.
- The `splice()` method can take `n` number of arguments: index, optional number of items to be removed, and optional item(s) to be added to the array. The `slice()` method can take `2` arguments: the starting index and an optional end index.

```javascript
[2,4,8].splice(1, 2) // returns [4, 8], original array is [2]
[2,4,8].slice(1, 2) // returns 4, original array is [2,4,8]
```

</p></details>

<li>Arrays: the three methods introduced in ES6 that allow us to inspect all elements of an array.</li>
<li>Arrays: the three methods used to perform a search in an array.</li>

<details><summary>Answer</summary><p>

- ECMAScript’s three strict equivalence lookup methods are `indexOf()` and `lastIndexOf()`, available in all ECMAScript versions, and `includes()`, which was introduced in the ECMAScript 7 specification.

</p></details>

<li>Arrays: why is it Not recommended to use `for.. in` loops to iterate over an array.</li>
<li>Async & Await</li>
<li>Atomics</li>
<li>Bitwise operators</li>
<li>BOM (Browser Object Model)</li>

<details><summary>Answer</summary>
<p>

- The Browser Object Model (BOM) is a browser-specific convention referring to all the objects exposed by the web browser.
- Unlike the DOM, there is no standard for implementation and no strict definition, so browser vendors are free to implement the BOM in any way they wish.
- The top level of the hierarchy is the window object which represents the browser window.

</p></details>

<li>Call vs. Apply</li>
<li>Call vs. Apply vs. Bind</li>
<li>Callback</li>
<li>Classes: static methods</li>
<li>Classes: static method being called from the class constructor or from other non-static methods within the same class</li>
<li>Classes: static method calling another static method within the same class</li>
<li>Closure</li>
<li>CommonJS</li>
<li>Compiling vs. Transpiling</li>
<li>console.log() vs. console.dir()</li>
<li>Currying</li>

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

<li>Date and Time formatting</li>
<li>Debounce vs. throttle</li>
<li>Debounce: when do we use a debounce function?</li>
<li>Decimal points handling (since there is no Float data type)</li>
<li>Decorators</li>
<li>Design Pattern: Builder</li>
<li>Design Pattern: Factory</li>
<li>Design Pattern: Module</li>
<li>Design Pattern: Nullobject</li>
<li>Design Pattern: Singleton</li>
<li>Destructuring an object or an array (Give an example)</li>
<li>Document Object Model (DOM)</li>
<li>DOM: classList and its common methods</li>
<li>DOM: cloneNode()</li>
<li>DOM: closest()</li>
<li>DOM: childNodes vs. children</li>
<li>DOM: firstChild vs. firstElementChild</li>
<li>DOM: getAttribute() & setAttribute()</li>
<li>DOM: getInnerText() vs. getHTML() vs. getTextContent()</li>

<details><summary>Answer</summary><p>

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

<li>DOM: parentNode vs. parentElement</li>
<li>DOM: Six JavaScript methods to access DOM elements</li>

<details><summary>Answer</summary><p>

```javascript
document.getElementById()
document.getElementsByClassName()
document.getElementsByTagName()
document.getElementsByName()
document.querySelector();
document.querySelectorAll();
```

</p></details>

<li>DOM: getElement(s)By* vs. querySelector(All) methods</li>

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

<li>DOM: previousSibling vs. previousElementSibling</li>
<li>Encapsulation: how do you implement Encapsulation in JavaScript? (interview)</li>
<li>Error Handling</li>
<li>ES2020 (ES11) new features (8)</li>

<details><summary>Answer</summary><p>

**BigInt**  
A new numeric primitive that allows us to safely store and operate on large integers, even beyond the safe integer limit for Numbers.

**Dynamic importing**  
As the name implies, you can now import modules dynamically.

**Nullish Coalescing (`??`)**  
This operator will return a Right Hand Side operand when the Left Hand Side operand is either undefined or null.

```javascript
let student = {}
let name = student.name ?? ‘John’
```

**Promise.allSettled**  
This method returns a promise when all promises are settled regardless of the result (fulfilled or rejected).

```javascript
Promise.allSettled([
  fetch("https://api.github.com/users/abc").then(data => data.json()),
  fetch("https://api.github.com/users/def").then(data => data.json())
])
  .then(result => console.log(`All profile settled`));
```

**String#matchAll**  
The `matchAll()` method returns an iterator of all results matching a string against a regular expression, including capturing groups.

```javascript
const text = "From 2019.01.29 to 2019.01.30";
const regexp = /(?<year>\d{4}).(?<month>\d{2}).(?<day>\d{2})/gu;
const results = Array.from(text.matchAll(regexp));

// results:
// [
//   [
//     '2019.01.29',
//     '2019',
//     '01',
//     '29',
//     index: 5,
//     input: 'From 2019.01.29 to 2019.01.30',
//     groups: { year: '2019', month: '01', day: '29' }
//   ],
//   [ (...) ]
// ]
```

**globalThis**  
The `globalThis` property always refers to the global object, no matter where you are executing your code.

**Module Namespace Exports**  
Before we could do this: `import * as utils from './utils.mjs';`  

Now, we can also so the same with exports: `export * as utils from './utils.mjs';`

**Optional chaining**  
Optional Chaining syntax allows you to access deeply nested objects without worrying about whether the property exists or not.  
![Optional Chaining](../../blob/master/images/optional-chaining.png)  

</p></details>

<li>Eval()</li>
<li>Event handling: delegation</li>

<details><summary>Answer</summary><p>

- DOM event delegation is a mechanism of responding to UI events via a single common parent rather than each child.
- It is a technique for listening to events where we can delegate a parent element as the listener for all of the events that happen inside it.

</p></details>

<li>Event handling: bubbling vs. capturing</li>

<details><summary>Answer</summary><p>

- In bubbling mode, which is the default mode, the event will be triggered at the deepest element. Then it will be bubbled up to the its parents. In other words, if an event occurs on a given element, it will be triggered on its parent as well and on its parent’s parent and all the way up, until the html element.
- In capturing mode, the order is opposite. The handler will be invoked from the parent element first, then down to the its children. We can force the event to be fired in the capturing mode by passing the third parameter of addEventListener(event, handler, useCapture) to true.

</p></details>

<li>Event handling: propagation</li>
<li>Event handling: propagation: the three phases of event propagation.</li>

<details><summary>Answer</summary><p>

1. Capture phase — Starting from window, document and the root element, the event dives down through ancestors of the target element
2. Target phase — The event gets triggered on the element on which the user has clicked
3. Bubble phase — Finally, the event bubbles up through ancestors of the target element until the root element, document, and window.

</p></details>

<li>Event handling: stopPropagation() vs. preventDefault()</li>
<li>Event listeners: target vs. currentTarget</li>
<li>Event listeners. Name 5 events JS could be listening to.</li>
<li>Event loop</li>
<li>Event loop: Call stack vs. Task queue</li>
<li>Falsy values</li>

<details><summary>Answer</summary><p>

- A falsy value is a value that is considered false when encountered in a Boolean context.
- There are 8 falsy values: `false`, `0`, `-0`, `0n` (BigInt), `' '` (Empty string), `null`, `undefined`, `NaN`.

</p></details>

<li>Feature detection, feature inference, and using the UA string</li>
<li>for.. in vs. for.. of</li>

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

<li>Functions vs. methods</li>
<li>Functions: `arguments` object</li>
<li>Functions: arrow functions vs. classic functions (4 differences)</li>

<details><summary>Answer</summary>
<p>
1. An arrow function does not have its own this. In regular functions the this keyword represented the object that called the function, which could be the window, the document, a button or whatever. With arrow functions the this keyword always represents the object that defined the arrow function (lexical).
2. Arrow functions cannot be used as constructors and will throw an error when used with new.
3. Unlike regular functions, the `arguments` object is not defined for arrow functions.
4. Arrow functions do not have a prototype property.

</p></details>

<li>Functions: `function Person(){}` vs. `var person = Person()` vs. `var person = new Person()`</li>
<li>Functions: higher order functions</li>

<details><summary>Answer</summary>
<p>

- Higher order functions take another function as an argument or return a function.
- Taking another function as an argument is often referred to as a callback function

</p></details>

<li>Functions: idempotent functions</li>
<li>Functions: pure functions</li>
<li>Functions: why do we say that in JavaScript, functions are first class citizens.</li>
<li>Generator functions & yield keyword</li>
<li>Generators</li>
<li>Getters & Setters</li>
<li>Hoisting</li>

<details><summary>Answer</summary><p>

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

<li>IIFE</li>
<li>Immutability</li>
<li>Importing a JavaScript file into HTML</li>
<li>Interpreter vs. Compiler</li>
<li>Iterable vs. Enumerable</li>
<li>Iterators</li>
<li>Iterators used with Generators</li>
<li>Jasmine vs. Mocha vs. Chai</li>
<li>JavaScript vs. ECMAScript</li>
<li>JavaScript vs. TypeScript</li>
<li>JSON parse() vs. stringify()</li>

<details><summary>Answer</summary><p>

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

<li>let vs. const (2 differences)</li>

<details><summary>Answer</summary><p>

1. Unlike `let`, variables declared with `const`  cannot be reassigned a new value since `const` defines a constant reference to a value.
2. Unlike `let`, variables declared with `const` must be assigned a value as soon as they are declared.  

</p></details>

<li>let vs. var (3 differences)</li>

<details><summary>Answer</summary><p>

1. `let` is block-scoped whereas `var` is function-scoped.
2. Variables declared with `let` are not hoisted whereas variables declared with `var` are hoisted.
3. Variables declared with `let` cannot be re-declared whereas variables declared with `var` can.

</p></details>

<li>Maps</li>
<li>Maps vs. WeakMaps</li>
<li>Modules</li>
<li>Modules: Tree shaking</li>
<li>Multi-threaded: is JavaScript multi-threaded?</li>
<li>NaN: where would be a situation in which you would see `NaN`. How to check for NaN?</li>
<li>null vs. undefined (3 differences)</li>

<details><summary>Answer</summary><p>

1. `undefined` means a variable has been declared but has not yet been assigned a value. `null` on the other hand can be assigned to a variable as an intentional representation of no value or empty value.
2. In arithmetic, `undefined` is treated as `NaN` whereas `null` is treated as zero.
3. `undefined` is not valid in JSON whereas `null` is.

</p></details>

<li>null == undefined? How about null === undefined?</li>

<details><summary>Answer</summary><p>

```javascript
null == undefined // true
null === undefined // false
```

- `undefined` and `null` are two distinct types: `undefined` is a type itself while `null` is an object.

</p></details>

<li>Null: how to check if something is null? How about undefined?</li>

<details><summary>Answer</summary><p>

- Since `null == undefined` we could simply check if `variable == null` or `variable == null`.
- We can also use `typeof variable === 'undefined'` to check if a variable is `undefined`. The same cannot be done for `null` since `typeof null` is object.

</p></details>

<li>Null: what does `typeof null` return?</li>

<details><summary>Answer</summary><p>

```javascript
typeof null === 'object'; // true
```

</p></details>

<li>Nullish coalescing operator</li>
<li>Objects: assign()</li>

<details><summary>Answer</summary><p>

- The Object.assign() method copies all enumerable own properties from one or more source objects to a target object. It returns the target object.

```javascript
const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };
const returnedTarget = Object.assign(target, source);

console.log(target); //=> Object { a: 1, b: 4, c: 5 }
console.log(returnedTarget); //=> Object { a: 1, b: 4, c: 5 }
```

</p></details>

<li>Objects: assign() - A problem with using it to copy objects</li>

<details><summary>Answer</summary><p>

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

<li>Objects: cloning an object (two ways)</li>

<details><summary>Answer</summary><p>

- Both of these methods perform shallow cloning:


```javascript
const obj = {a: 1};

const copy1 = Object.assign({}, obj) ;
console.log(copy1); //=> {a: 1}

const copy2 = {...obj} ;
console.log(copy2); //=> {a: 1}
```

</p></details>

<li>Objects: create()</li>
<li>Objects: creation & initialization (two ways)</li>

<details><summary>Answer</summary><p>

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

<li>Objects: entries()</li>

<details><summary>Answer</summary><p>

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

<li>Objects: freeze()</li>

<details><summary>Answer</summary><p>

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

<li>Objects: freeze() vs. seal()</li>

<details><summary>Answer</summary><p>

- `Object.freeze()` makes it impossible to add, remove, or modify properties of an object.
- `Object.seal()` is similar, however it does allow exiting properties to be modified.

</p></details>

<li>Objects: freeze() vs. preventExtensions()</li>
<li>Objects: fromEntries()</li>

<details><summary>Answer</summary><p>

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

<li>Objects: hasOwnProperty()</li>

<details><summary>Answer</summary><p>

- The `Object.hasOwnProperty()` method returns a boolean indicating whether the object has the specified property as its own property (as opposed to inheriting it).

```javascript
obj = new Object();
console.log(obj.hasOwnProperty('prop')); // false
obj.prop = 'exists';
console.log(obj.hasOwnProperty('prop')); // true
console.log(obj.hasOwnProperty('toString')); // false
```

</p></details>

<li>Objects: host objects vs. native objects</li>
<li>Objects: how do we determine if an object is an array?</li>

<details><summary>Answer</summary><p>

- By using the `Array.isArray()` method.

```javascript
if (Array.isArray(obj)) {
  // do something on the array
}
```

</p></details>

<li>Objects: immutable objects</li>
<li>Objects: is everything in JavaScript considered an object?</li>
<li>Objects: is()</li>
<li>Objects: iterating over object properties</li>
<li>Objects: the optional chaining operator `?</li>

<details><summary>Answer</summary><p>

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

<li>Objects: the two ways to access an object's properties and their differences</li>

<details><summary>Answer</summary><p>

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

<li>Parameters vs. Arguments</li>
<li>ParseInt vs. ParseFloat</li>
<li>Passing by value vs. Passing by reference</li>
<li>Primitive data types</li>
<li>Promises</li>
<li>Promises: Promise.all() vs. Promise.allSettled()</li>

<details><summary>Answer</summary><p>

- With `Promise.all()`, a rejection of the first promise would reject the whole promise, and the second promise might not be able to be fulfilled.
- `Promise.allSettled` handles the case when all promises are settled regardless of the result (fulfilled or rejected). It helps cover such cases where partial results are valuable (one promise rejecting, the other fulfilling).

</p></details>

<li>Prototypal inheritance</li>

<details><summary>Answer</summary><p>

- Each object in JavaScript has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype.
- Prototypical inheritance allows us to reuse the properties or methods from one JavaScript object to another through a reference pointer function.

</P></details>

<li>Prototype vs. __proto__</li>
<li>Proxies</li>
<li>Pub/Sub architecture</li>
<li>Rest vs. Spread operator</li>
<li>Same-origin policy with regards to JavaScript.</li>
<li>Scope: Global vs. Lexical</li>
<li>Scope: lexical scope</li>
<li>Sets & methods associated with them</li>
<li>Sets: iterating over a set</li>
<li>Shallow vs. Deep copying</li>

<details><summary>Answer</summary><p>

- In shallow copying, both items point to the same memory location.
- In deep copying, the second item is assigned a separate memory location than the original item.
- In other words, in a shallow copy, object B points to object A's location in memory. In deep copy, all things in object A's memory location get copied to object B's memory location.

![Shallow versus deep cloning diagram](https://i.stack.imgur.com/AWKJa.jpg)

</p></details>

<li>Shimming</li>
<li>Statically Typed vs. Dynamically Typed vs. Weakly Typed</li>
<li>Strict mode</li>
<li>Strict mode: Can strict mode be used within functions or block statements?</li>
<li>Strings: trim()</li>
<li>Strings: 3 common methods for working with characters</li>
<li>Strings: An algorithm that returns the first duplicate character in a string (interview)</li>
<li>Strings: Given a string (understood to be a sentence), reverse the order of the words. "Hello world" becomes "world Hello"  
<li>Strings: padStart() and padEnd()</li>
<li>Strings: indexOf() vs. search()</li>

<details><summary>Answer</summary><p>

- `indexOf()` is for searching for plain substrings. It also allows us to specify a starting index. It does not allow for regular expressions.
- `search()` allows for substrings as well as regular expressions. It does not allow for a starting index.

```javascript
console.log('Blue Whale'.indexOf('Whale', 3)); //=> 5
console.log('hey JudE'.search(/[A-Z]/g)); //=> 4
```

</p></details>

<li>Strings: search() vs. match()</li>

<details><summary>Answer</summary><p>

- `Search()` returns the index of the first match between the regular expression and the given string, or `-1` if no match was found.
- `Match()` returns an array or `null` if no matches are found.

```javascript
const str1 = 'hey JudE';
console.log(str1.search(/[A-Z]/g)); // 4

const str2 = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz';
console.log(str2.match(/[A-E]/gi)); // ['A', 'B', 'C', 'D', 'E', 'a', 'b', 'c', 'd', 'e']
```

</p></details>

<li>Strings: substring vs. substr vs. slice</li>
<li>Symbols</li>
<li>Tagged template literal</li>
<li>Temporal dead zone</li>
<li>Ternary operator: what does the word "Ternary" indicate?</li>
<li>`this` keyword</li>
<li>toString() parameters</li>
<li>Type Coercion</li>
<li>typeof operator (8 possible types)</li>

<details><summary>Answer</summary><p>

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

<li>typeof vs. instanceof</li>
<li>Unary operators</li>
<li>Unary operators: what is `~3` equal to?</li>

<details><summary>Answer</summary><p>

- The bitwise Not operator `~` converts the integer `N` to `-(N+1)` value. Therefore `~3 = -4`.

</p></details>

<li>Unary operators: what is `~~3.9` equal to?</li>

<details><summary>Answer</summary><p>

- Double bitwise NOT performs the same operation as the `Math.floor()` method but a lot quicker.

```javascript
~~3.9 === Math.floor(3.9); //true, 3
~~2.4 === Math.floor(2.4); //true, 2
~~2 === Math.floor(2); //true, 2
```

</p></details>

<li>V8 and SpiderMonkey.</li>
<li>`-0` vs. `+0`</li>
<li>Web APIs: Canvas API</li>
<li>Web APIs: Console API</li>
<li>Web APIs: Drag & Drop API</li>
<li>Web APIs: Fetch API</li>
<li>Web APIs: History API</li>
<li>Web APIs: HTMLCollection vs. NodeList</li>

<details><summary>Answer</summary><p>

An **HTMLCollection** is an array-like list (collection) of of HTML elements. HTMLCollection items can be accessed by their name, id, or index number. The element methods `getElementsByClassName()` and `getElementsByTagName()` return a live HTMLCollection.

A **NodeList** is a collection of document nodes. NodeList items can only be accessed by their index number. Only the NodeList object can contain attribute nodes and text nodes. The element method `querySelectorAll()` returns a static NodeList.

</p></details>

<li>Web APIs: Geolocation API</li>
<li>Web APIs: Service Workers API</li>
<li>Web APIs: Touch events</li>
<li>Web APIs: URL API</li>
<li>Web APIs: Web Storage API</li>
<li>Web APIs: Web Workers API</li>
<li>Web APIs: WebGL</li>
<li>Web APIs: WebSocket API</li>
<li>Web APIs: Window</li>

<div align="center">
<h1>Know-how</h1>
</div>

<li>Form design & validation</li>
<li>Image carousel</li>
<li>Infinite scrolling</li>
<li>Pagination</li>
<li>Pinterest board</li>
<li>Progress bar</li>
</ol>
