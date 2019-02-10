# JavaScript DOM Manipulation Guide - Methods

### **What is a Method?**

> JavaScript methods are *action* properties that can be used to manipulate objects. Think of methods as pre-built fuctions or object properties followed by `()`. For example, in `console.log();`, the `log()` method is a built-in JavaScript function calls an action to display the value of its parameter into the console.

### **DOM Selection Methods**

> These methods are used to select elements from the DOM which are then manipulated. The following methods select elements by their `id`, `class`, or `tag` and can be followed by another method or property.

***

**getElementById()** is a JavaScript method that returns a single DOM element (including its decendants) with an id selector as a parameter in the form of a string. Parameters include form inputs like `(input[type="submit"])`.

```HTML
<!-- HTML -->
<div id="element"></div> 
```

```javascript
document.getElementById('element');
```

When methods are used, they're also able to be stored into variables.

```javascript
let element = document.getElementById('element');

console.log(element); 
// <div id="element"></div> 
```

Other selector methods:

**getElementsByClassName() -**

>returns a collection of DOM elements (including their decendants) that match the specified class selector as a parameter in the form of a string. Notice `elements` is plural here. Unlike an id selector, classes can be assigned to multiple DOM elements, thus allowing multiple elements to be selected.



**getElementsByTagName() -**

>returns a collection of DOM elements (including their decendants) that match the specified HTML tag as a parameter in the form of a string. Again notice the pural `elements` in the method name. There can be multiples of the same tag written in your HTML document.

**querySelector() -**

>returns a single DOM element (including its decendants) that matches the specified CSS selector: `.class`, `#id`, or `tag` as a parameter in the form of a string. This method iterates through the DOM and finds the first element with the specified selector.

**querySelectorAll() -**

>returns a collection of DOM elements (including their decendants) that match the specified CSS selector: `.class`, `#id`, or `tag` as a parameter in the form of a string.

***

[Next page](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")

[Previous Page](/README.md "Home")

## Table of Contents

1. [Methods](/JavaScript%20DOM%20Manipulation%20Guide/1%20-%20Methods.md "1 - Methods")
2. [Properties](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")