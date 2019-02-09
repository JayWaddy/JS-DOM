# JavaScript DOM Manipulation Guide - Properties

### **Common JavaScript properties for DOM manipulation.**

> JavaScript properties provide information about an object. Where methods change objects with (or without) parameters, properties hold specific values or data. For example, in `string.length`, the `length` property holds the value of the variable's length. Nothing has been changed at this point.

> We'll look at JavaScript properties that are commonly used to manipulate the DOM and change their values by assigning them to variables.

**textContent** is a property that can change the text within an HTML element by replacing DOM element text with its value.

```HTML
<!-- HTML -->
<div id="element"></div>
```

```javascript
// JavaScript
let element = document.querySelector('#element');

console.log(element.textContent);
// ''

element.textContent = 'Hello, World!';

console.log(element); 
// <div id="element">Hello, World!</div>
```

**innerText**, like *textContent*, can change the text in an HTML element by its text with the propery's value, but will also consider the style or the element and its decendants. 


For example:

```html
<div id="element">Hello, World!<span style="{display:none;}">123</span></div>
```

In the above HTML, a `span` tag has been added to the DOM element. The `span` element contains the style property `display: none;` which hides its content in the browser.

By console logging:

```javascript
console.log(element.textContent);
// Hello, World! 123
```

you will see that the span element is still not displayed in the browser, but shows in the console. *The styling is ignored.*

However, if you were to console log:

```javascript
console.log(element.innerText);
// Hello, World!
```

the `span` is ignored as it is in the browser. *The styling is payed attention to.*

