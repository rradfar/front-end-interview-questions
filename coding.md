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
