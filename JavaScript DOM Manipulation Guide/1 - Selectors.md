<style>
    .method {
        color: orange;
    }

    .property {
        color: cyan
    }

    .html {
        color: yellow
    }
</style>

# JavaScript DOM Manipulation Guide - Selectors

> ### Common, built-in JavaScript selection methods to query the DOM

JavaScript methods are properties that can be used to manipulate objects. Think of methods as fuctions or object properties followed by `()`. 

<span class="method">**getElementById()**</span> returns a single DOM element with an id selector. 

```javascript
document.getElementById('element');
```

Elements from the DOM are also able to be stored into variables.

```javascript
let element = document.getElementById('element');

console.log(element); 
// <div id="element"></div> 
```

Similar methods:

<span class="method">**getElementsByClassName()**</span> returns a collections of DOM elements that match the specified class selector as well as its decendants. Notice `elements` is plural because unlike an id selector, classes can be assigned to multiple DOM elements.



<span class="method">**getElementsByTagName()**</span> returns a collections of DOM elements that match the specified HTML tag as well as its decendants. Again notice the pural `elements` in the method name. There can be multiples of the same tag written in your HTML document.

<span class="method">**querySelector()**</span> returs a single DOM element that match the specified CSS selector: `.class`, `#id`, or `tag`. This method iterates through the DOM and finds the first element with the specified selector.

<span class="method">**querySelectorAll()**</span> returns a collection of DOM elements that match the specified CSS selector: `.class`, `#id`, or `tag`.