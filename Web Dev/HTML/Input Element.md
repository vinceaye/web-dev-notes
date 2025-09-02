- The `input` element allows you several ways to collect data from a web form. Like `img` elements, 
- `input` elements are a void element and do not need closing tags.
- There are many types of inputs you can create using the `type` attribute
```html
<input type="text">
```
- In order for a form's data to be accessed by the location specified in the `action` attribute, you must give the text field a `name` attribute and assign it a value to represent the data being submitted.
```html
<input type="text" name="name">
```
- Placeholder text is used to give people a hint about what kind of information to enter into an input.
	- Shows a preview in a textbox
```html
<input type="text" placeholder="Ex. Jane Doe">
```
![[Pasted image 20241217212716.png]]
- `required` prevents a user from submitting the form when information is missing