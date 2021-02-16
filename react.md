# React Interview Questions

Q. When do we use `useEffect()`?

<details><summary>Answer</summary>

Data fetching, DOM manipulation, subscriptions, timers, logging, and other side effects are not allowed inside the main body of a function component. Instead, we can use `useEffect()`.

By default, effects run after every completed render, but you can choose to fire them only when certain values have changed.

</details>

---
