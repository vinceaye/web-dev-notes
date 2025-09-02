- The `div` element is used mainly for design layout purposes
- The div below is named menu
```html
<div id="menu">
      <main>
        <h1>CAMPER CAFE</h1>
        <p>Est. 2020</p>
        <section>
          <h2>Coffee</h2>
        </section>
      </main>
    </div>
```
- The div can now be modified as its own entity in CSS
```CSS
#menu {
  background-color: burlywood;
  width: 300px;
}
```
- Horizontally centering a div:
```CSS
#menu {
	margin-left: auto;
	margin-right: auto;
}
```
- Background Image:
```CSS
body {
  background-image: url(https://cdn.freecodecamp.org/curriculum/css-cafe/beans.jpg)
}
```