[Previous](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")

# JavaScript DOM Manipulation Guide - Create New Elements

### **Creating a New Element**

***

### **New Element Methods**

#### createElement() -

> used on the document object, creates an HTML element with a specified tag name parameter as a string.

```javascript
let newDiv = document.createElement('div'); // <div></div>
```

#### setAttribute() -

> sets the value of the specified element's attribute. If an attribute already exists, this will update its value. This method takes two string parameters: a `name` and `value`.

```javascript
newDive.setSttribute('title', 'new-div'); // <div title="new-div"></div>
```

#### createTextNode() -

> creates a text node, not an element. This node will exist in memory until it is placed in a DOM element.

```javascript
let newDivText = document.createTextNode('Hello, World!');
```

#### appendChild() -

> adds a child node at the end of the node list of the specified element. The required parameter is the value of the node it will create. If the node already exists in the DOM, it will be removed. To clone a node use `cloneNode()`.

```javascript
newDiv.appendChild(newDivText); // <div title="new-div">Hello, World!</div>
```

The text node that was created earlier is used as a parameter of `appendChild` which adds text to `newDiv`.

#### insertBefore() -

> creates an HTML element with a specified tag name parameter as a string.

```javascript

```

***

### **New Element properties**

#### id -

> creates an HTML element with a specified tag name parameter as a string.

```javascript

```

#### className -

> creates an HTML element with a specified tag name parameter as a string.

```javascript

```

***

[Previous](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")


## Table of Contents

1. [Methods](/JavaScript%20DOM%20Manipulation%20Guide/1%20-%20Methods.md "1 - Methods")
2. [Properties](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")
3. [Traversing](/JavaScript%20DOM%20Manipulation%20Guide/3%20-%20Traversing.md "3 - Traversing")
4. [Create New Elements](/JavaScript%20DOM%20Manipulation%20Guide/4%20-%20Create%20New%20Elements.md "4 - Create New Elements")