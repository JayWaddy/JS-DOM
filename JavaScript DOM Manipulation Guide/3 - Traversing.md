# JavaScript DOM Manipulation Guide - Traversing

### **What is Traversing?**

> In HTML, elements refered to as *nodes* are infinitely nested inside one another. Each node may posesss a parent node, or element in which the specified node is nested in; a sibling node, or an element adjecnt to the specified node that shares the same parent; or a child node known as decendants which are elements that are nested within the specified node. By *traversing* the DOM, we are jumping between the parent, sibling, and child nodes of an element.

```
            <html>
           /     \
        <head>  <body>
        /       /    \
    <meta>   <div>  <div>
             /      /   \
          <...>   <h1>  <p>

DOM Tree
```

In the example above, you will see the layout of the DOM. The `body` tag has a *parent node* known as the `HTML` document object, a *sibling node* known as the `head` tag, and two `div` elements as *children nodes*.


### **Which Properties are Used for Traversing?**

> We'll look at JavaScript properties that are commonly used to traverse the DOM and change node values.

***

#### parentNode -

> returns the parent node of the specified element in the DOM tree. If there is no parent node, this will return the `HTML` document node.

```HTML
<body>
    <div class="container">
        <h1>Hello, Wrold!</h1>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
        </ul>
    </div>
</body>
```

```javascript
let element = document.querySelectorAll('li');

element.parentNode; // <ul>...</ul>
element.parentNode.parentNode; // <div class="container">...</div>
element.parentNode.parentNode.parentNode; // <body>..</body>

```

Remember, properties are able to stack or chain.

***

#### parentElement -

> works similarly to *parentNode*. Only if there is no parent node, this will return `null`.

```javascript
document.body.parentNode; // the <html> element
document.body.parentElement; // the <html> element

document.documentElement.parentNode; // the document node
document.documentElement.parentElement; // null

(document.documentElement.parentNode === document);  // true
(document.documentElement.parentElement === document);  // false
```

#### childNodes -

> returns the children elements of a node. Remember `nodes` is plural here. Like `querySelectorAll()`,  this will return a node list which can be accessed as an array if there are multiple children.

```HTML
<body>
    <div>
        <h1>Hello, World!</h1>
    </div>
</body>
```

```javascript
let element = document.querySelector('div');

element.childnodes // <h1>Hello, World!</h1>
```

[Previous](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")


## Table of Contents

1. [Methods](/JavaScript%20DOM%20Manipulation%20Guide/1%20-%20Methods.md "1 - Methods")
2. [Properties](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")
3. [Traversing DOM Elements](/JavaScript%20DOM%20Manipulation%20Guide/3%20-%20Traversing%20DOM%20Elements.md "3 - Traversing DOM Elements")