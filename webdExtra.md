# Wd

## HTML

Use `<a>` for navigation (links, page-section)
`<button>` for actions

### HTML entities

&lt &gt
&nbsp
(r, l, u, d + arr) - arrow
&darr - down arrow

### HTML aria .. for screen-readers

```html
<div class="--" role="img" aria-label="img-desc"></div>
```

```css
.any{
    background-image: url(..)
}
```

'role'
'aria-label' is like 'alt' that help screen readers - mostly used in a empty div with bg-img(css)

## CSS

### For smooth scrolling on clicking nav-links of a single page

```css
html{
    scroll-behaviour: smooth;
}
```

[currently works with only chrome, firefox ; Not with safari]

### Focus

```css
*:focus{
    outline: --;
}
->  box-shadow: 0 0 0 0.8rem #---;
```

### Border inside

```css
box-shadow: inset 0 0 0 3px #---;
                  x y blur size color
```

(this doesnt effect other elements outside (mostly used in :hover))

### Modify images

```css
filter: blur(50%);  // blur, brightness, contrast, ..
opacity: 25%;
```

overflow: hidden;

## JS

### Topics

this.
Asynchronous JavaScript (promises, callbacks, async/await)
Closures.
The event loop.
Recursion.
Scope.
Hoisting.
Prototypical inheritance.
bind(), call(), apply()
reduce()
Generators
fetch()

React uses ES6, and you should be familiar with some of the new features like:

Classes
Arrow Functions
Variables (let, const, var)
Array Methods like .map()
Destructuring
Modules
Ternary Operator
Spread Operator

create-react-app includes built tools such as webpack, Babel, and ESLint.

### JS array methods

filter sort map reduce forEach

### JS libraries frameworks

jQuery lodash underscore ramda

### SSG static site generators

Gatsby - react
Gridsome - vue
Next - react
Astro - any

### Web API

Api types: SOAP REST GraphQL RPC

Webhooks Websockets HttpStreaming

### DOM

```js
//The window object
window.addEventListener("load", myheader.changeColor);

//A button object
document.getElementById("btn").addEventListener("click", myheader.changeColor);

// generate list from array in react
const myArray = ['apple', 'banana', 'orange'];
const myList = myArray.map((item) => <p>{item}</p>)
```

### JS window object

Window object - it is the global object of the browser

window.
console
.log -
.dir -
.warn - way of formatting
.error - way of formatting
.table - tabular data (useful for objects)
.

debugger; - to open debugger tool at the point

In Nodejs the window object is ..

### JSON

`JSON. parse()` is used for parsing data that was received as JSON; it deserializes a JSON string into a JavaScript object.

`JSON. stringify()` on the other hand is used to create a JSON string out of an object or array; it serializes a JavaScript object into a JSON string.

## Tools

Gulp
Grunt

Webpack
Vite

Jest
Cypress
Bcrypt

JWT
