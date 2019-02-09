# JavaScript DOM Manipulation Guide - Selectors

### **Selection methods:**

> JavaScript *methods* are properties that can be used to manipulate objects. Think of methods as pre-built fuctions or object properties followed by `()`. For example, in `console.log();`, the `log()` method is a built-in JavaScript function used to display the value of its parameter into the console.

> The following methods select elements by their `id`, `class`, or `tag` and can be followed by another method or property.

**getElementById()** is a JavaScript method that returns a single DOM element with an id selector as a parameter in the form of a string, including its decendants. 

```javascript
document.getElementById('element');
```

This type of method is used to select elements from the DOM which are then manipulated. Methods used on objects are also able to be stored into variables.

```javascript
let element = document.getElementById('element');

console.log(element); 
// <div id="element"></div> 
```

Similar methods:

**getElementsByClassName()** returns a collection of DOM elements (including their decendants) that match the specified class selector as a parameter in the form of a string. Notice `elements` is plural here. Unlike an id selector, classes can be assigned to multiple DOM elements, thus allowing multiple elements to be selected.



**getElementsByTagName()** returns a collection of DOM elements (including their decendants) that match the specified HTML tag as a parameter in the form of a string. Again notice the pural `elements` in the method name. There can be multiples of the same tag written in your HTML document.

**querySelector()** returns a single DOM element (including its decendants) that matches the specified CSS selector: `.class`, `#id`, or `tag` as a parameter in the form of a string. This method iterates through the DOM and finds the first element with the specified selector.

**querySelectorAll()** returns a collection of DOM elements (including their decendants) that match the specified CSS selector: `.class`, `#id`, or `tag` as a parameter in the form of a string.