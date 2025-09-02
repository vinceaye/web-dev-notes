- Strings are immutable, so using `let` variables will allow you to reassign them

## Concatenation
- You can concatenate strings in JS
- Using `+` is one of the simplest and most frequently used for concatenation
```js
let firstName = "John";
let lastName = "Doe";

let fullName = firstName + " " + lastName;
```

- You can also use `+=` to append/add to an existing string
```js
let string = "John";
string += " Doe";
```

- You can also use `concat()` function to concatenate
```js
let str1 = "Hello";
let str2 = "World";

let result = str1.concat(' ', str2);
```

## Bracket Notation
- You can access a character of a string using `[]` and an index

## Template Literals
- embedding variables directly into a string
	- Use backticks (\`) to do this
```js
let name = "Alice";
let greeting = `Hello, ${name}!`
```
- they also preserve linebreaks
```js
let poem = `line 1
line 2
line 3
line 4`;
```