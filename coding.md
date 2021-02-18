![Coding logo](images/logos/logo-coding.png)

# Front-End Coding Challenges

Q. Write a function that accepts an array of integers and counts the number of its unique values. Can you solve this in one line of code?

```js
const countUniqueValues = arr => {
  // Your solution
};

console.log(countUniqueValues([1, 1, 1, 1, 1, 2])); // 2
console.log(countUniqueValues([1, 2, 3, 4, 4, 7, 7, 7, 13])); // 6
console.log(countUniqueValues([-2, -1, -1, 0, 1])); // 4
console.log(countUniqueValues([5])); // 1
console.log(countUniqueValues([])); // 0
```

<details><summary>Solution</summary>

```js
const countUniqueValues = arr => {
  return new Set(arr).size;
};
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

Q. Our football team finished the championship. The result of each match look like `x:y`. Results of all matches are recorded in the collection. For example: `['3:1', '2:2', '0:1', ...]`. Write a function that takes such collection and counts the points of our team in the championship. Rules for counting points for each match: if `x > y` add 3 points and if `x = y` add 1 point. Can you solve this in one line of code?

```js
const countPoints = games => {
  // Your solution
};

const points = ['2:1', '2:2', '3:3', '4:4', '2:2', '3:3', '4:4', '3:3', '4:4', '2:4'];
console.log(countPoints(points)); // 11
```
<details><summary>Solution</summary>

```js
const countPoints = games => {
  return games.reduce((score, cur) => score + (cur[0] > cur[2] ? 3 : cur[0] === cur[2] ? 1 : 0), 0);
};

const points = ['2:1', '2:2', '3:3', '4:4', '2:2', '3:3', '4:4', '3:3', '4:4', '2:4'];
console.log(countPoints(points)); // 11
```

</details>

---

Q. Write a function that takes two strings and checks to see if they are anagrams. Inputs consist of lower case alphanumeric letters or spaces.
Further considerations:
- You may **NOT** use the built-in `sort()` method.
- If you need to create a new object, do **NOT** create more than one.
- Expected performance: `O(n)` or better.

```js
const validAnagram = (s1, s2) => {
  // Your solution
};

console.log(validAnagram(' ', ' ')); // true
console.log(validAnagram('s 7n', 'sn7 ')); // true
console.log(validAnagram('cinema', 'iceman')); // true
console.log(validAnagram('anagram', 'nagaram')); // true
console.log(validAnagram('aza', 'zaz')); // false
console.log(validAnagram('rat', 'cart')); // false
```

<details><summary>Solution</summary>

```js
const validAnagram = (s1, s2) => {
  if (s1.length !== s2.length) return false;

  const freq = {};

  for (let letter of s1) {
    freq[letter] = (freq[letter] || 0) + 1;
  }

  for (let letter of s2) {
    if (!freq[letter]) {
      return false;
    } else {
      freq[letter]--;
    }
  }

  return true;
};

console.log(validAnagram(' ', ' ')); // true
console.log(validAnagram('s 7n', 'sn7 ')); // true
console.log(validAnagram('cinema', 'iceman')); // true
console.log(validAnagram('anagram', 'nagaram')); // true
console.log(validAnagram('aza', 'zaz')); // false
console.log(validAnagram('rat', 'cart')); // false
```

</details>

---

Q. Write a function that counts the number of duplicates (case-insensitive) in the input string. The input string can contain alphabets (both uppercase and lowercase) or numbers. Expected performance: `O(n)` or better.

```js
const duplicateCount = text => {
  // Your solution
};

console.log(duplicateCount('')); // 0
console.log(duplicateCount('abcde')); // 0
console.log(duplicateCount('aabbcde')); // 2
console.log(duplicateCount('aabBcde')); // 2
console.log(duplicateCount('aA11')); // 2
console.log(duplicateCount('Indivisibility')); // 1
console.log(duplicateCount('Indivisibilities')); // 2
```

<details><summary>Solution</summary>

```js
const duplicateCount = text => {
  const obj = {};
  let count = 0;

  for (let letter of text.toLowerCase()) {
    obj[letter] = (obj[letter] || 0) + 1;
    if (obj[letter] === 2) count++;
  }

  return count;
};

console.log(duplicateCount('')); //  0
console.log(duplicateCount('abcde')); //  0
console.log(duplicateCount('aabbcde')); //  2
console.log(duplicateCount('aabBcde')); //  2
console.log(duplicateCount('aA11')); //  2
console.log(duplicateCount('Indivisibility')); //  1
console.log(duplicateCount('Indivisibilities')); //  2
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

Q. Write a function that takes a string as input and returns true if the parentheses in the input string are 'balanced' and false otherwise. For the parentheses to be balanced, each open parenthesis must have a corresponding closing parenthesis, in the correct order. For example:
- `((()))` is balanced
- `(()(()()))` is balanced
- `)(` is not balanced
- `((()` is not balanced
- `()))` is not balanced

```js
const isBalanced = str => {
  // Your solution
};

console.log(isBalanced('(){}')); // true
console.log(isBalanced('({(()))}}')); // false
console.log(
  isBalanced(
    '[{()()}({[]})]({}[({})])((((((()[])){}))[]{{{({({({{{{{{}}}}}})})})}}}))[][][]'
  )
); // true
```

<details><summary>Solution</summary>

```js
const isBalanced = str => {
  const stack = [];

  for (let char of str) {
    if (char === '(' || char === '[' || char === '{') {
      stack.push(char);
    } else if (char === ')') {
      if (stack.pop() !== '(') return false;
    } else if (char === ']') {
      if (stack.pop() !== '[') return false;
    } else if (char === '}') {
      if (stack.pop() !== '{') return false;
    }
  }

  return !stack.length;
};

console.log(isBalanced('(){}')); // true
console.log(isBalanced('({(()))}}')); // false
console.log(
  isBalanced(
    '[{()()}({[]})]({}[({})])((((((()[])){}))[]{{{({({({{{{{{}}}}}})})})}}}))[][][]'
  )
); // true
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
