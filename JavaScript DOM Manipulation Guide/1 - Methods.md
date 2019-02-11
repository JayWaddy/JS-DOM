# JavaScript DOM Manipulation Guide - Methods

### **What is a Method?**

JavaScript methods are *action* properties that can be used to manipulate objects. Think of methods as pre-built fuctions or object properties followed by `()`. For example, in `console.log();`, the `log()` method is a built-in JavaScript function calls an action to display the value of its parameter into the console.

***

### **DOM Selection Methods**

These methods are used to select elements from the DOM which are then manipulated. The following methods select elements by their `id`, `class`, or `tag` and can be followed by another method or property.


#### getElementById() -
> a JavaScript method that returns a single DOM element (including its decendants) with an id selector as a parameter in the form of a string. Parameters include form input types `('input[type="submit"]')`.

```HTML
<div id="element"></div> 
```

```javascript
document.getElementById('element');
```

When methods are used, they're also able to be stored into variables.

```javascript
let element = document.getElementById('element');

element; // <div id="element"></div> 
```

Other selector methods:

#### getElementsByClassName() -

>returns a collection of DOM elements (including their decendants) that match the specified class selector as a parameter in the form of a string. Notice `elements` is plural here. Unlike an id selector, classes can be assigned to multiple DOM elements, thus allowing multiple elements to be selected.



#### getElementsByTagName() -

>returns a collection of DOM elements (including their decendants) that match the specified HTML tag as a parameter in the form of a string. Again notice the pural `elements` in the method name. There can be multiples of the same tag written in your HTML document.

#### querySelector() -

>returns a single DOM element (including its decendants) that matches the specified CSS selector: `.class`, `#id`, or `tag` as a parameter in the form of a string. This method iterates through the DOM and finds the first element with the specified selector.

#### querySelectorAll() -

>returns a collection of DOM elements (including their decendants) that match the specified CSS selector: `.class`, `#id`, or `tag` as a parameter in the form of a string.

***
### **Which methods are Useful?**

We'll look at JavaScript methods that are commonly used to manipulate the DOM and change their values by assigning them to variables.

#### toUpperCase() -

> returns a string value, and converts it to uppercase.

```javascript
let sentence = 'I love JavaScript.';

sentence.toUpperCase(); // 'I LOVE JAVASCRIPT.'
```

#### toLowerCase() -

> returns a string value, and converts it to lowercase.

```javascript
let sentence = 'I love JavaScript.';

sentence.tolowerCase(); // 'i love javascript.'
```

#### indexOf() -

> returns the first index of an object where an element can be found, or returns -1 if the element doesn't exist.

```javascript
let sentence = 'I love JavaScript.';

sentence.indexOf('love'); // 2
sentence.indexOf('hate'); // -1
```

```javascript
let array = [ 'item 1', 'item 2', 'item 3', 'item 4' ];

array.indexOf('item 2'); // 1
array.indexOf('item 10'); // -1
```

```javascript
let array = [ true, false, false ,true, false ];

array.indexOf(true); // 0
array.indexOf(false); // 1
```

#### addEventListener() -

> sets up a funtion to run after a specified event has ben executed. This method requires two parameters: a type, and a listener.

1. The *type* parameter holds a string value of the event that is being listened for before running a function: `click`, `scroll`, `focus`, `blur`, `mouseover`, `mouseout`, [more types here](https://developer.mozilla.org/en-US/docs/Web/Events "Full list of web events").
2. The *listener* is the function name that will run after the type of even is executed.

```javascript
let button = document.querySelector(button),
    buttonClick = button.addEventListener('click', () => {
        console.log('Button clicked!');
    });
```

```javascript
let button = document.querySelector(button),
    buttonClick = button.addEventListener('click', click);

    function click() {
        console.log('Button clicked!');
    }
```



<!-- #### removeEventListener() -

> definition and example. -->
***

[Previous](/README.md "Home")

[Next](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")

## Table of Contents

1. [Methods](/JavaScript%20DOM%20Manipulation%20Guide/1%20-%20Methods.md "1 - Methods")
2. [Properties](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")
3. [Traversing DOM Elements](/JavaScript%20DOM%20Manipulation%20Guide/3%20-%20Traversing%20DOM%20Elements.md "3 - Traversing DOM Elements")