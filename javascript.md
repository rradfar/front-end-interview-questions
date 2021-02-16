## JavaScript Interview Questions

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
