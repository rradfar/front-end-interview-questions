<div align="center">
<h1>Javascript</h1>
</div>

🌼 Arrays: concat(): 2 special notes  

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

🌼 Arrays: 2 ways to create a new array  

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

🌼 Arrays: 3 ways to clone an array & why we don't use array1 = array2  

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

🌼 Arrays: create an array with an initial length of 20  

<details><summary>Answer</summary><p>

```javascript
let arr = new Array(20);
```

</p></details>

🌼 Arrays: every() vs. some()  

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

🌼 Arrays: fill()  

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

🌼 Arrays: flat()  

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

🌼 Arrays: flat() vs. flatmap()  

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

🌼 Arrays: forEach() vs. map()  

<details><summary>Answer</summary><p>

- The `forEach()` method doesn't return anything (`undefined`). It simply calls a provided function on each element in the array. This callback is allowed to mutate the calling array.
- The `map()` method also calls a provided function on every element in the array. The difference is that `map()` utilizes return values and actually returns a new Array of the same size.

</p></details>

🌼 Arrays: from()  

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

🌼 Arrays: how to check for equality?  
🌼 Arrays: indexOf() vs. lastIndexOf() vs. includes()  
🌼 Arrays: join()  
🌼 Arrays: reduce()  
🌼 Arrays: reduce() vs. reduceRight()  
🌼 Arrays: slice()  
🌼 Arrays: splice()  
🌼 Arrays: splice() vs. slice()  

<details><summary>Answer</summary><p>

- The `splice()` method changes the original array, `slice()` does not.
- The `splice()` method returns the removed items in an array. The `slice()` method returns the selected element(s) in an array, as a new array object.
- The `splice()` method can take `n` number of arguments: index, optional number of items to be removed, and optional item(s) to be added to the array. The `slice()` method can take `2` arguments: the starting index and an optional end index.

```javascript
[2,4,8].splice(1, 2) // returns [4, 8], original array is [2]
[2,4,8].slice(1, 2) // returns 4, original array is [2,4,8]
```

</p></details>

🌼 Arrays: the three methods introduced in ES6 that allow us to inspect all elements of an array.  
🌼 Arrays: the three methods used to perform a search in an array?

<details><summary>Answer</summary><p>

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
🌱 Document Object Model (DOM)  
🌱 DOM: classList and its common methods  
🌱 DOM: cloneNode()  
🌱 DOM: closest()  
🌱 DOM: childNodes vs. children  
🌱 DOM: firstChild vs. firstElementChild  
🌱 DOM: getAttribute() & setAttribute()  
🌼 DOM: getInnerText() vs. getHTML() vs. getTextContent()  

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
🌱 Encapsulation: how do you implement Encapsulation in JavaScript? (interview)  
🌱 Error Handling  
🌱 ES2020 (ES11) new features  
🌱 Eval()  
🌼 Event handling: delegation  

<details><summary>Answer</summary><p>

- DOM event delegation is a mechanism of responding to UI events via a single common parent rather than each child.
- It is a technique for listening to events where we can delegate a parent element as the listener for all of the events that happen inside it.

</p></details>

🌼 Event handling: bubbling vs. capturing  

<details><summary>Answer</summary><p>

- In bubbling mode, which is the default mode, the event will be triggered at the deepest element. Then it will be bubbled up to the its parents. In other words, if an event occurs on a given element, it will be triggered on its parent as well and on its parent’s parent and all the way up, until the html element.
- In capturing mode, the order is opposite. The handler will be invoked from the parent element first, then down to the its children. We can force the event to be fired in the capturing mode by passing the third parameter of addEventListener(event, handler, useCapture) to true.

</p></details>

🌱 Event handling: propagation  
🌼 Event handling: propagation: the three phases of event propagation.  

<details><summary>Answer</summary><p>

1. Capture phase — Starting from window, document and the root element, the event dives down through ancestors of the target element
2. Target phase — The event gets triggered on the element on which the user has clicked
3. Bubble phase — Finally, the event bubbles up through ancestors of the target element until the root element, document, and window.

</p></details>

🌱 Event handling: stopPropagation() vs. preventDefault()  
🌱 Event listeners: target vs. currentTarget  
🌱 Event listeners. Name 5 events JS could be listening to.  
🌱 Event loop  
🌱 Event loop: Call stack vs. Task queue  
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

🌼 let vs. const (2 differences)  

<details><summary>Answer</summary>
<p>

1. Unlike `let`, variables declared with `const`  cannot be reassigned a new value since `const` defines a constant reference to a value.
2. Unlike `let`, variables declared with `const` must be assigned a value as soon as they are declared.  

</p></details>

🌼 let vs. var (3 differences)  

<details><summary>Answer</summary>
<p>
1. `let` is block-scoped whereas `var` is function-scoped.
2. Variables declared with `let` are not hoisted whereas variables declared with `var` are hoisted.
3. Variables declared with `let` cannot be re-declared whereas variables declared with `var` can.

</p></details>

🌱 Maps  
🌱 Maps vs. WeakMaps  
🌱 Modules  
🌱 Modules: Tree shaking  
🌱 Multi-threaded: is JavaScript multi-threaded?  
🌱 NaN: where would be a situation in which you would see `NaN`. How to check for NaN?  
🌼 null vs. undefined (3 differences)  

<details><summary>Answer</summary>
<p>

1. `undefined` means a variable has been declared but has not yet been assigned a value. `null` on the other hand can be assigned to a variable as an intentional representation of no value or empty value.
2. In arithmetic, `undefined` is treated as `NaN` whereas `null` is treated as zero.
3. `undefined` is not valid in JSON whereas `null` is.

</p></details>

🌼 null == undefined? How about null === undefined?  

<details><summary>Answer</summary>
<p>

```javascript
null == undefined // true
null === undefined // false
```

- `undefined` and `null` are two distinct types: `undefined` is a type itself while `null` is an object.

</p></details>

🌼 Null: how to check if something is null? How about undefined?  

<details><summary>Answer</summary>
<p>

- Since `null == undefined` we could simply check if `variable == null` or `variable == null`.
- We can also use `typeof variable === 'undefined'` to check if a variable is `undefined`. The same cannot be done for `null` since `typeof null` is object.

</p></details>

🌼 Null: what does `typeof null` return?  

<details><summary>Answer</summary>
<p>

```javascript
typeof null === 'object'; // true
```

</p></details>

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

<details><summary>Answer</summary><p>

- Each object in JavaScript has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype.
- Prototypical inheritance allows us to reuse the properties or methods from one JavaScript object to another through a reference pointer function.

</P></details>

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

<details><summary>Answer</summary><p>

- In shallow copying, both items point to the same memory location.
- In deep copying, the second item is assigned a separate memory location than the original item.
- In other words, in a shallow copy, object B points to object A's location in memory. In deep copy, all things in object A's memory location get copied to object B's memory location.

![Shallow versus deep cloning diagram](https://i.stack.imgur.com/AWKJa.jpg)

</p></details>

🌱 Shimming  
🌼 Statically Typed vs. Dynamically Typed vs. Weakly Typed  
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
🌱 Web APIs: Canvas API  
🌱 Web APIs: Console API  
🌱 Web APIs: Drag & Drop API  
🌱 Web APIs: Fetch API  
🌱 Web APIs: History API  
🌱 Web APIs: HTMLCollection vs. NodeList  
🌱 Web APIs: Geolocation API  
🌱 Web APIs: Service Workers API  
🌱 Web APIs: Touch events  
🌱 Web APIs: URL API  
🌱 Web APIs: Web Storage API  
🌱 Web APIs: Web Workers API  
🌱 Web APIs: WebGL  
🌱 Web APIs: WebSocket API  
🌱 Web APIs: Window  

<div align="center">
<h1>Know-how</h1>
</div>

🌱 Form design & validation  
🌱 Image carousel  
🌱 Infinite scrolling  
🌱 Pagination  
🌱 Pinterest board  
🌱 Progress bar  
