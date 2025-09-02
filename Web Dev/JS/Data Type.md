## Number Type
- numbers represent integer and floating-point values

## String
- sequence of chars, or text, enclosed in quotes

## Boolean
- true or false values

## Undefined and Null Types
- undefined means a variable has been declared but hasn't been given a value
- null means the variable is intentionally set to nothing

## Object 
- can hold collections of key-value pairs
```js
let book = {
  title: "The Great Gatsby",
  author: "F. Scott Fitzgerald",
  year: 1925
};
```

## Symbol
- value that's always unique and can't be changed
- meant to create unique labels or identifiers for properties
```js
// creating 2 symbols
const symbol1 = Symbol('mySymbol');
const symbol2 = Symbol('mySymbol');
```

## BigInt
- used for very large numbers that exceed limit of Number type
```js
const bigNum = 12345555555555555555555555555555555;
```
