# JavaScript DOM Manipulation Guide - Properties

### **What are Properties?**

> JavaScript properties provide information about an object. Where methods change objects with (or without) parameters, properties hold specific values or data. For example, in `string.length`, the `length` property holds the value of the variable's length. Nothing has been changed at this point.

### **Which Properties are Useful?**

> We'll look at JavaScript properties that are commonly used to manipulate the DOM and change their values by assigning them to variables.

***

**textContent -**

> a property that contains the raw text value of an HTML element that is visible to the document object. Re-assigning its value will replace DOM element text with its current value.

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

**innerText -**

> like *textContent*, *innerText* contains the text value of an HTML element, but will also consider the style or the element and its decendants. 


```html
<div id="element">Hello, World!<span style="{display:none;}">123</span></div>
```

In the above HTML, a `span` tag has been added to the DOM element. The `span` contains the style property `display: none;` which hides its content in the browser.

By console logging:

```javascript
console.log(element.textContent);
// Hello, World! 123
```

you will see the span element is visible in the console, but is not displayed in the browser. *The styling is ignored in JavaScript.*

However, if you were to console log:

```javascript
console.log(element.innerText);
// Hello, World!
```

the `span` does not show in the console, and is also is not displayed in the bowser. *The styling is payed attention to in JavaScript.*

**innerHTML -**

> contains the HTML value within a DOM element. This won't *change* the parent element, but will hold the value of its children.

```javascript
element.innerHTML = '<h3>This is an h3</h3>';

console.log(element);
// <div id="element">
//    <h3>This is an h3</h3>
// </div>
```
The variable `element` will remain as the same `div`, but its HTML content changed to an `h3` element.

**Style -**

> holds the value of the inline style of an object. To change the style, add a scond property that is a cammel cased version of a CSS style property.  

```javascript
element.style.fontSize = '10px';
element.style.borderBottom = 'solid 2px red';
```

Adding styles to multiple objects with a single variable will throw an error in the console. To change the style of multiple ojects, create a loop that iterates through each object and return the style value.

```HTML
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    <li>Item 4</li>
</ul>
```

```javascript
let listItemm = document.querySelectorAll('li');

for (let i = 0; i < listItem.length; i++) {
    listItem.style.background = 'red';
}
```

**Value -**

> hold the value (in our case) of form keywords like `input`, `submit`, etc. This is the text entered in forms

```javascript
let input = document.querySelector('input');

input.value = 'Hello, World!';

if (input.value.toLowerCase() == 'hello, world!') {
    return true;
}

// true
```

*** 

[Previous Page](/JavaScript%20DOM%20Manipulation%20Guide/1%20-%20Methods.md "1 - Methods")

## Table of Contents

1. [Methods](/JavaScript%20DOM%20Manipulation%20Guide/1%20-%20Methods.md "1 - Methods")
2. [Properties](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")