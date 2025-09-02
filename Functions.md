```js
function greetings(name) {
	console.log("Hello, " + name);
}
```

- Arrow Function Syntax
```js
// no need for parentheses around single param
const greetings = name => { 
	console.log("Hello, " + name + "!");
}
```
- If arrow function has no parameters 
```js
const greetings = () => {
	console.log("Hello");
}
```
- If your function body only has a single line of code, you can remove the curly braces
```js
const greetings = name => console.log("Hello, " + name + "!");
```
- Arrow function with multiple parameters
```js
const calculateArea = (width, height) => {
	const area = width * height;
	return area
};
console.log(calculateArea(5, 3));
```
- You don't need to use a `return` statement in single line arrow function
```js
const calculateArea = (width, height) => width * height;
```