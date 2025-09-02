- You can add style to an element by specifying it in the `style` element and setting a property for it like this:
```css
element {
 property: value;
}
```
- Ex: Centering an element (*type selector*)
```CSS
<style>
	h1 {text-align:center;}
</style>
```
- Since we may have many styles, it's good practice to put all styles in a separate file and link it to the main file
	- Use a `styles.css` file
```html
<link rel="stylesheet" href="styles.css">
``` 

- For the styling of the page to look similar on mobile as it does on a desktop or laptop, you need to add a `meta` element with a special `content` attribute.
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- Background color
```CSS
body {
	background-color:brown;
}
```