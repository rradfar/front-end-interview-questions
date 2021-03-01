![JavaScript logo](images/logos/logo-js.png)

# JavaScript Interview Questions

Q. Can you name some of the new features introduced in ES2020 (ES11)?

<details><summary>Answer</summary>

**BigInt**  
A new numeric primitive that allows us to safely store and operate on large integers, even beyond the safe integer limit for Numbers.

**Dynamic importing**  
As the name implies, you can now import modules dynamically.

**Nullish Coalescing (`??`)**  
This operator will return a Right Hand Side operand when the Left Hand Side operand is either undefined or null.

```javascript
let student = {}
let name = student.name ?? 'John'
```

**Promise.allSettled**  
This method returns a promise when all promises are settled regardless of the result (fulfilled or rejected).

```javascript
Promise.allSettled([
  fetch("https://api.github.com/users/abc").then(data => data.json()),
  fetch("https://api.github.com/users/def").then(data => data.json())
])
  .then(result => console.log('All profile settled'));
```

**String.matchAll()**  
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

Now, we can also do the same with exports: `export * as utils from './utils.mjs';`

**Optional chaining**  
Optional Chaining syntax allows you to access deeply nested objects without worrying about whether the property exists or not.

```js
const student = {
  name: 'Max',
  age: 20,
  address: {
    street: {
      number: 45,
      name: 'Oxford'
    }
  }
}

const streetNumber = student?.address?.street?.number;
```

</details>

---

Q. Can you name some of the new features introduced in ES2021 (ES12)?

<details><summary>Answer</summary>

**String.replaceAll()**  
```js
const str = "Backbencher sits at the Back";
const newStr = str.replaceAll("Back", "Front");
console.log(newStr); // "Frontbencher sits at the Front"
```

**Promise.any()**  
Promise.any() is settled as soon as any promises are fulfilled, or they are all rejected.

**Numeric separators**  
`const money = 1_000_000_000_000;`

**Logical Assignment Operator**  
```js
let x = 1;
let y = 2;
x &&= y;
console.log(x); // 2

// which is the same as:
if(x) {
  x = y;
}
```

**Private Methods**  
```js
class Person {

  // Private method
  #setType() {
    console.log("I am Private");
  }

  // Public method
  show() {
    this.#setType();
  }
}

const personObj = new Person();
personObj.show(); // "I am Private";
personObj.setType(); // TypeError: personObj.setType is not a function
```

**WeakRef**  
A WeakRef object contains a weak reference to an object. A weak reference to an object is a reference that does not prevent the object from being recovered by the garbage collector.

</details>

---

Q. What are some ways to create a new array in JavaScript?

<details><summary>Answer</summary>

We can use the Array constructor:

```javascript
const names = new Array();
const values = new Array(2);
const colors = new Array('red', 'blue', 'green');
```

We can also use an array literal notation

```javascript
const names = [];
const values = [1, 2];
const colors = ['red', 'blue', 'green'];
```

</details>

---

Q. What are some ways to clone an array? Why don't we typically use `array1 = array2`?

<details><summary>Answer</summary>

To copy a one-dimensional array, any of these methods would work:

```javascript
const newArray = originalArray.slice();
const newArray = [...originalArray];
const newArray = Array.from(originalArray);
```

If we use the equal sign, the second array will point to the same memory location as the original array, so any changes to the second array will be reflected in the original array and vice versa.

```javascript
const originalArray = [1, 2];
const newArray = originalArray;

originalArray.push(3);
console.log(newArray); // [1, 2, 3]

newArray.push(4);
console.log(originalArray); // [1, 2, 3, 4]
```

</details>

---

Q. Can you think of two possible disadvantages of using Closures in JavaScript?

<details><summary>Answer</summary>

As long as the closures are active, the memory can't be garbage collected. For instance, if we are using closure in ten places then unless all the ten processes complete, the memory will be held which can cause memory leaks. As a countermeasure, if there comes a point in our program where we are done using closures then we can set them to null.

Creating a function inside a function leads to duplicity in memory and can slow down the application. We need to be selective about using closures in our application and use them mainly when we need data privacy, otherwise we can use the module pattern to create new objects with shared methods.

</details>

---

Q. What is a promise in JavaScript?

<details><summary>Answer</summary>

The Promise object represents the eventual completion (or failure) of an asynchronous operation and its resulting value. A promise may be in one of three possible states: pending, fulfilled, or rejected.

</details>

---

Q. How does event bubbling differ from event capturing when using the DOM API?

<details><summary>Answer</summary>

Event bubbling and capturing are two ways of event propagation in the HTML DOM API, when an event occurs in an element inside another element, and both elements have registered a handle for that event.

With bubbling, the event is first captured and handled by the innermost element and then propagated to outer elements. With capturing, the event is first captured by the outermost element and propagated to the inner elements.

By default javascript is set the event propagation to bubble. If we want to use capture we have to set the third argument in `addEventListener(type, listener, useCapture)` function to true.

</details>

---

Q. Is JavaScript asynchronous?

<details><summary>Answer</summary>

JavaScript is synchronous and single-threaded with various callback mechanisms. It can seem as though it is asynchronous with the help from the browser engine and the event loop.

</details>

---

Q. Are you familiar with the `eval()` function?

<details><summary>Answer</summary>

It is a global function that evaluates JavaScript code represented as a string.

```js
console.log(eval('2 + 2')); // 4
```

Using the `eval()` function is generally considered a security risk. For example, invoking it can crash a system if we use `eval()` server-side and a mischievous user decides to use an infinite loop as their username. `window.Function()` is the safer recommended alternative.

</details>

---

Q. When is the `defineProperty()` method used and how does it differ from `defineProperties()`?

<details><summary>Answer</summary>

`Object.defineProperty(obj, prop, descriptor)`

With the `defineProperty` method, we can add new properties to an object, or modify existing ones. By default, properties added using the defineProperty method are not writable, enumerable, or configurable. But we can override this behavior using the writable, configurable and enumerable properties.

```js
const obj = {};
Object.defineProperty(obj, 'name', {
  value: 'John',
  configurable: true,
});
console.log(obj.name); // John
```

The JavaScript `Object.defineProperties()` method adds or modifies multiple properties on an object.

```js
let obj = {};
Object.defineProperties(obj, {
  property1: {
    value: true,
    writable: true,
  },
  property2: {
    value: 'Hello',
    writable: false,
  },
});

console.log(obj); // {property1: true, property2: "Hello"}
```

</details>

---

Q. When is the delete operator used in JavaScript?

<details><summary>Answer</summary>

The delete operator removes a given property from an object and will return true if successful. The delete operator is designed to be used on object properties. It has no effect on variables or functions.

```js
const Employee = {
  firstName: 'John',
  lastName: 'Doe'
};

console.log(Employee.firstName); // "John"

delete Employee.firstName;
console.log(Employee.firstName); // undefined
```

</details>

---

Q. Explain the `this` keyword in JavaScript?

<details><summary>Answer</summary>

The JavaScript `this` keyword refers to the object it belongs to. It has different values depending on where it is used:

- In a method, `this` refers to the owner object.
- In a function, `this` refers to the global object.
- In a function, in strict mode, `this` is undefined.
- In an event, `this` refers to the element that received the event.
- Methods like `call()`, and `apply()` can refer `this` to any object.

</details>

---

Q. What is a prototypal inheritance in JavaScript?

<details><summary>Answer</summary>

In JavaScript, objects can have other objects associated with them known as their "prototype" object. So if we attempt to access a property (or method) from an object, and that object doesn't have that property, the version of that property in the object's prototype object can be returned instead.

For example, let's say we have two objects:

```js
const mother = { firstName: 'Anne', lastName: 'Adams' }
const daughter = { firstName: 'Bella' }
```

Both objects have a firstName property but only mother has a lastName property.

```js
console.log(daughter.firstName) // 'Bella'
console.log(daughter.lastName)  // undefined
```

One way to set up a prototype association in JavaScript is using `Object.setPrototypeOf()`:

```js
Object.setPrototypeOf(daughter, mother) // daughter's prototype is now mother
```

Now, if we try to get the lastName from the daughter object we will no longer get undefined. Instead we'll get the value of lastName from the mother object since mother is daughter's prototype.

```js
console.log(daughter.lastName) // 'Adams'
```

The process of looking to a prototype for values happens automatically by JavaScript every time we access a property. If the property doesn't exist, the prototype of that object is checked. If that prototype doesn't have the property either, JavaScript will look to that prototype's prototype object, and so on until there are no more prototype objects to check. This sequence represents what is known as the prototype chain or prototypal inheritance.

</details>

---

Q. Can you think of a few ways to check if a JavaScript variable is a number?

<details><summary>Solution</summary>

By using `isNaN()`. If `isNaN()` returns false, the value is a number:

```js
console.log(!isNaN('test'));  // false
console.log(!isNaN(1.2));     // true
console.log(!isNaN('1.2'));   // true (if input can be coerced into a number, it is a number)
```

By using `typeof`:

```js
console.log(typeof 123 === 'number');      // true
console.log(typeof 'hello' === 'number');  // false
```

By using the `Number.isInteger()` method (only works for integers):

```js
console.log(Number.isInteger(123));     // true
console.log(Number.isInteger(-123));    // true
console.log(Number.isInteger('123'));   // false
console.log(Number.isInteger('123.5')); // false (doesn't work for floats)
```

</details>

---

Q. What is the output?

```js
let a = 5;
let b = 1;

console.log(a ^ b);   // ?
console.log(a << b);  // ?
console.log(a >> b);  // ?
console.log(a >>> b); // ?
```

<details><summary>Solution</summary>

```js
let a = 5; // 101
let b = 1; // 001

console.log(a ^ b); // 4 
// XOR operation: 101 ^ 001 = 100 (bin) or 4 (dec)

console.log(a << b); // 10
// Left Shift: 101 << 1 = 1010 (bin) or 10 (dec)

console.log(a >> b); // 2
// Sign Propagating Right Shift: 101 >> 1 = 010 (bin) or 2 (dec)

console.log(a >>> b); // 2
// Zero Fill Right Shift: 101 >>> 1 = 010 (bin) or 2 (dec)
```

</details>

---

Q. What is the output?

```js
const config = {
  languages: [],
  set language(lang) {
    return this.languages.push(lang);
  },
};

console.log(config.language); // ?
```

<details><summary>Solution</summary>

```js
const config = {
  languages: [],
  set language(lang) {
    return this.languages.push(lang);
  },
};

console.log(config.language); // undefined

// The language method is a setter. Setters don't hold an actual value, their purpose is to modify properties. 
// When calling a setter method, undefined gets returned.
```

</details>

---

Q. What is the output?

```js
const colors = ["red", "green", "blue"];
const colors2 = colors.concat("yellow", ["black", "brown"]);

console.log(colors);  // ?
console.log(colors2); // ?
```

<details><summary>Solution</summary>

```js
const colors = ["red", "green", "blue"];
const colors2 = colors.concat("yellow", ["black", "brown"]);

console.log(colors);  // ["red", "green","blue"]
console.log(colors2); // ["red", "green", "blue", "yellow", "black", "brown"]

// Reminder:
// concat() does not change the original array.
// concat() flattens the resulting array.
```

</details>

---

Q. What is the output?

```js
const arr = [1, 2, 3, 4];

console.log(arr.fill(0, 2, 4)); // ?
console.log(arr.fill(5, 1));    // ?
console.log(arr.fill(6));       // ?
```

<details><summary>Solution</summary>

```js
const arr = [1, 2, 3, 4];

console.log(arr.fill(0, 2, 4)); // [1, 2, 0, 0]
console.log(arr.fill(5, 1));    // [1, 5, 5, 5]
console.log(arr.fill(6));       // [6, 6, 6, 6]
```

The array `fill()` method can take three parameters. A value to fill the array with. An optional start index (default is 0), and an optional end index (default is array's length).

```js
arr.fill(value, start(optional), end(optional))
```

`fill()` is a mutator method: it will change the original array and return it, not a copy of it.

</details>

---

Q. What method is used on the array below?

```js
const arr = [1, 2, , , 4, 5];
console.log(arr.?); // [1, 2, 4, 5]
```

<details><summary>Solution</summary>

```js
const arr = [1, 2, , , 4, 5];
console.log(arr.flat()); // [1, 2, 4, 5]
```

The `flat()` method can be used to remove empty slots in an array.

</details>

---

Q. What parameter is passed to the `flat()` method below?

```js
const arr = [1, 2, [3, 4, [5, 6, [7, 8, [9, 10]]]]];
console.log(arr.flat(?)); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

<details><summary>Solution</summary>

```js
const arr = [1, 2, [3, 4, [5, 6, [7, 8, [9, 10]]]]];
console.log(arr.flat(Infinity)); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

The `flat()` method can receive an optional depth level parameter specifying how deep a nested array structure should be flattened. `Infinity` will flatten all nested arrays.

In this particular example, `arr.flat(4)` would also be a correct answer.

</details>

---

Q. What are the outputs?

```js
console.log(typeof 3.14);           // ?
console.log(typeof Number(42));     // ?
console.log(typeof NaN);            // ?
console.log(typeof 42n);            // ?
console.log(typeof typeof 42);      // ?
console.log(typeof false);          // ?
console.log(typeof Symbol('foo'));  // ?
console.log(typeof undefined);      // ?
console.log(typeof null);           // ?
console.log(typeof [1, 2, 3]);      // ?
console.log(typeof new Number(42)); // ?
console.log(typeof function() {});  // ?
console.log(typeof Math.sin);       // ?
```

<details><summary>Solution</summary>

```js
console.log(typeof 3.14);           // 'number'
console.log(typeof Number(42));     // 'number'
console.log(typeof NaN);            // 'number'
console.log(typeof 42n);            // 'bigint'
console.log(typeof '3.14');         // 'string'
console.log(typeof typeof 42);      // 'string'
console.log(typeof false);          // 'boolean'
console.log(typeof Symbol('foo'));  // 'symbol'
console.log(typeof undefined);      // 'undefined'
console.log(typeof null);           // 'object'
console.log(typeof [1, 2, 3]);      // 'object'
console.log(typeof new Number(42)); // 'object'
console.log(typeof function() {});  // 'function'
console.log(typeof Math.sin);       // 'function'
```

Some observations:

- Currently there are 8 possible return values of the `typeof` operator: number, bigint, string, boolean, symbol, undefined, object, and function.
- While both functions and arrays are considered objects in JavaScripts, `typeof` an array returns object, whereas `typeof` a function returns function.
- `typeof undefined` is undefined, whereas `typeof null` is object. This is a popular interview questions and is often followed up by asking how we can check if something is specifically null since using `typeof` does not seem to help.
- `typeof NaN` is number. So how can we check if a user input is NaN or not? Thankfully JavaScript has a built-in `isNan()` method.

</details>

---

Q. What is the output?

```js
let x = [1, 2, 3] + [4, 5, 6];
console.log(x); // ?
```

<details><summary>Solution</summary>

```js
let x = [1, 2, 3] + [4, 5, 6];
console.log(x); // '1,2,34,5,6'
```

Note that `x` is a string not an array.

</details>

---

Q. What value can we assign to `i` to obtain the following outputs?

```js
let i = ?;

console.log(i * i); // 0
console.log(i + 1); // 1
console.log(i - 1); // -1
console.log(i / i); // 1
```

<details><summary>Solution</summary>

```js
let i = Number.MIN_VALUE;

console.log(i * i); // 0
console.log(i + 1); // 1
console.log(i - 1); // -1
console.log(i / i); // 1
```

The `Number.MIN_VALUE` property represents the smallest positive numeric value representable in JavaScript. You can think of it as the closest possible value to 0 (but not 0).

</details>

---

Q. what are the outputs?

```js
const originalColors = ['red', 'green', 'blue', 'yellow', 'purple'];

const colors2 = originalColors.slice(1);
console.log(originalColors);  // ?
console.log(colors2);         // ?

const colors3 = originalColors.slice(1, 4);
console.log(originalColors);  // ?
console.log(colors3);         // ?
```

```js
const originalColors = ['red', 'green', 'blue'];

const colors2 = originalColors.splice(0, 1);
console.log(originalColors);  // ?
console.log(colors2);         // ?

const colors3 = originalColors.splice(1, 0, 'yellow', 'orange');
console.log(originalColors);  // ?
console.log(colors3);         // ?

const colors4 = originalColors.splice(1, 1, 'red', 'purple');
console.log(originalColors);  // ?
console.log(colors4);         // ?
```

<details><summary>Solution</summary>

```js
const originalColors = ['red', 'green', 'blue', 'yellow', 'purple'];

const colors2 = originalColors.slice(1);
console.log(originalColors); // ['red', 'green', 'blue', 'yellow', 'purple']
console.log(colors2); // ['green', 'blue', 'yellow', 'purple']

const colors3 = originalColors.slice(1, 4);
console.log(originalColors); // ['red', 'green', 'blue', 'yellow', 'purple']
console.log(colors3); // ['green', 'blue', 'yellow']
```

```js
const originalColors = ['red', 'green', 'blue'];

const colors2 = originalColors.splice(0, 1);
console.log(originalColors); // ['green', 'blue']
console.log(colors2); // ['red']

const colors3 = originalColors.splice(1, 0, 'yellow', 'orange');
console.log(originalColors); // ['green', 'yellow', 'orange', 'blue']
console.log(colors3); // []

const colors4 = originalColors.splice(1, 1, 'red', 'purple');
console.log(originalColors); // ['green', 'red', 'purple', 'orange', 'blue']
console.log(colors4); // ['yellow']
```
Some observations:

- The `splice()` method changes (mutates) the original array, `slice()` does not.
- The `splice()` method returns the removed items in an array. The `slice()` method returns the selected element(s) in an array, as a new array object.
- The `splice()` method can take `n` number of arguments: index, optional number of items to be removed, and optional item(s) to be added to the array. The `slice()` method can take up to `2` arguments: the starting index and an optional end index.
