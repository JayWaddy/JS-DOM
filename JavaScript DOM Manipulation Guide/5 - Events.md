[Previous - Create Elements](/JavaScript%20DOM%20Manipulation%20Guide/4%20-%20Create%20Elements.md "4 - Create Elements")

# JavaScript DOM Manipulation Guide - Events

### **What is an Event?**

Events fired to tell the code when something is happening. For instance, if a user clicks on a button, the event will notify the code and the code will respond with a function.

***

### **Event Methods**

#### addEventListener() -

> sets up a funtion to run after a specified event has ben executed. This method requires two parameters: a type, and a listener.

1. The *type* parameter holds a string value of the event that is being listened for before running a function: `click`, `scroll`, `focus`, `blur`, `mouseover`, `mouseout`, and [more](https://developer.mozilla.org/en-US/docs/Web/Events "Full list of web events").
2. The *listener* is the function name that will run after the type of even is executed. The function can be instantly executed or a named function.

```javascript
// Instantly Executed Function
let button = document.querySelector(button):

button.addEventListener('click', () => {
    console.log('The button was clicked!');
});
```

```javascript
// Named Function
let button = document.querySelector(button),
    buttonClick = function click() {
        console.log('The button was clicked!');
    };

button.addEventListener('click', buttonClick);
```

***

### **What is an Event Parameter?**

When making a fucntion, you can choose to add a parameter with any given name, commonly: `e` or `event`. This parameter is an object that holds a data list of all the properties of (in our case) the event that just fired.

Let's say we added a `click` event to a button. The moment this event fires, specific data is stored in its property values. The properties of this event object includes the X and Y values of your cursor's position, the current height of the document, etc.

```javascript
button.addEventListener('click', (event) => {
    console.log(event.target); // <button id="button"></button>
    console.log(event.target.id); // 'button'
    console.log(event.target.parentNode); // <body>...</body>
});
```

[Here is a complete list of event properties.](https://www.w3schools.com/jsref/dom_obj_event.asp "List of event properties and methods") (Scroll to the second list.)

***

[Previous - Create Elements](/JavaScript%20DOM%20Manipulation%20Guide/4%20-%20Create%20Elements.md "4 - Create New Elements")


## Table of Contents

1. [Methods](/JavaScript%20DOM%20Manipulation%20Guide/1%20-%20Methods.md "1 - Methods")
2. [Properties](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")
3. [Traversing](/JavaScript%20DOM%20Manipulation%20Guide/3%20-%20Traversing.md "3 - Traversing")
4. [Create Elements](/JavaScript%20DOM%20Manipulation%20Guide/4%20-%20Create%20Elements.md "4 - Create New Elements")
5. [Events](/JavaScript%20DOM%20Manipulation%20Guide/5%20-%20Events.md "5 - Events")