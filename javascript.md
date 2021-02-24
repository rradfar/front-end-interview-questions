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
