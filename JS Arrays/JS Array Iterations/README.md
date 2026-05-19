# JavaScript Array Iterations

This section documents important JavaScript array iteration methods:
- `map()`
- `flatMap()`
- `filter()`
- `reduce()`

These examples compare traditional callback functions with modern ES6 arrow functions where useful.
All examples here return new values and do not modify the original array.
---

## 1. `map()` — Transform Each Element

File: [`JSMap.html`](./JSMap.html)

### Core Concept

`map()` creates a new array by transforming every element of the original array.

```js
const numbers = [45, 4, 9, 16, 25];
const doubledNumbers = numbers.map(x => x * 2);
console.log(doubledNumbers); // [90, 8, 18, 32, 50]
```

### Key Learning

`map()` does not modify the original array. It returns a new array. Each input element produces one output element.

```text
map() = transform values
```

## 2. `flatMap()` — Map and Flatten

File: [`JSFlatMap.html`](./JSFlatMap.html)

### Core Concept

`flatMap()` first applies `map()`, then flattens the result one level deep.

```js
const numbers = [1, 2, 3];
const mapResult = numbers.map(x => [x, x * 2]);
console.log(mapResult); // [[1, 2], [2, 4], [3, 6]]

const flatMapResult = numbers.flatMap(x => [x, x * 2]);
console.log(flatMapResult); // [1, 2, 2, 4, 3, 6]
```

### Key Learning

`map()` keeps nested arrays. `flatMap()` removes one level of nesting. `flatMap()` is useful when one input element may produce multiple output elements.

```text
flatMap() = map() + flatten one level
```

## 3. `filter()` — Keep Matching Elements

File: [`JSArrayFilter.html`](./JSArrayFilter.html)

### Core Concept

`filter()` creates a new array containing only the elements that satisfy a condition.

```js
const numbers = [45, 4, 9, 16, 25];

const filteredNumbers =
    numbers.filter(x => x > 18);

console.log(filteredNumbers);
// [45, 25]
```

### Key Learning

The callback should return `true` or `false`. If the condition is true, the value is kept. If the condition is false, the value is removed.

```text
filter() = keep/remove values
```

## 4. `reduce()` — Reduce Many Values Into One

File: [`JSArrayReduce.html`](./JSArrayReduce.html)

### Core Concept

`reduce()` processes array elements one by one and reduces them into a single final value.

```js
const numbers = [45, 4, 9, 16, 25];
const sum = numbers.reduce((total, value) => total + value, 0);
console.log(sum); // 99
```
```text
Unlike `map()` and `filter()`, `reduce()` usually returns a non-array value.
```

#### Under the Hood

With initial value 0:

```text
0 + 45 = 45
45 + 4 = 49
49 + 9 = 58
58 + 16 = 74
74 + 25 = 99
```

### Key Learning

`reduce()` returns one final value. The accumulator can be a number, string, object, array, or other structure. Providing an initial value is safer and more predictable.

```text
reduce() = many values → one value
```

#### Quick Comparison


| Method | Purpose | Returns |
| :--- | :--- | :--- |
| `map()` | Transform each value | New array |
| `flatMap()` | Transform and flatten | New flattened array |
| `filter()` | Keep matching values | New filtered array |
| `reduce()` | Combine values | One final value |

#### Mental Model

```text
map() → transform values
flatMap() → transform + flatten
filter() → keep/remove values
reduce() → combine into one final result
```

### Notes

These examples are written for learning purposes and intentionally show both older callback-style syntax and modern ES6 arrow function syntax.
