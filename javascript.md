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
