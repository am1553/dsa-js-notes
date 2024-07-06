# Data Structures and Algorithms Notes in JavaScript

## Big O Notation

> Big O notation is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity.

The 'O' in this stands for Ordnung, which means order of approximation. The only way to classify an algorithm as an efficient solution is to approximate its time and space complexity.

Consider the following problem, where an algorithm is required to sum up all the numbers upto the given parameter:

```js
function addUpTo(num) {
  let total = 0;
  for (let i = 0; i <= num; i++) {
    total += i;
  }
  return total;
}
```

Though this would give the correct answer, the time it would take would significantly grow as the parameter is increased. The function calculates the total by looping over till the condition is met. If 'num' is 5, it will loop 5 times, and if 'num' is 5000 it will loop 5000 times.

However, consider the following algorithm:

```js
function addUpTo(num) {
  return (n * (n + 1)) / 2;
}
```

Though a mathematical approach, this is much more efficient because the time it will take to execute is not dependant on the size of the parameter.
