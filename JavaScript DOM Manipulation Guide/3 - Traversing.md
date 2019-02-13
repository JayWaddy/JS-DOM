[Previous - Properties](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")

[Next - Create Elements](/JavaScript%20DOM%20Manipulation%20Guide/4%20-%20Create%20Elements.md "4 - Create New Elements")

# JavaScript DOM Manipulation Guide - Traversing

### **What is Traversing?**

In HTML, elements refered to as *nodes* are infinitely nested inside one another. Each node may posesss a parent node, or element in which the specified node is nested in; a sibling node, or an element adjecnt to the specified node that shares the same parent; or a child node known as decendants which are elements that are nested within the specified node. By *traversing* the DOM, we are jumping between the parent, sibling, and child nodes of an element.

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

We'll look at JavaScript properties that are commonly used to traverse the DOM and change node values.

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
document.body.parentNode; // <html>...</html>
document.body.parentElement; // <html>...</html>

document.documentElement.parentNode; // #document
document.documentElement.parentElement; // null

(document.documentElement.parentNode === document);  // true
(document.documentElement.parentElement === document);  // false
```

#### children -

> returns only children DOM elements of a node. `Children` is plural and will return an HTML collection. **The difference between a node list and HTML collection is that *node lists* contain all types of nodes including text nodes at each line break, and an *HTML collection* only provides HTML elements.**

```HTML
<body>
    <div>
        <h1>Hello, World!</h1>
        <p>Paragraph text</p>
    </div>
</body>
```

```javascript
let element = document.querySelector('div');

element.childnodes.length; // 2 
// line breaks before and after nodes are ignored.
```

#### firstElementChild -

> returns the first child that is an HTML element. If there is no child, this will return null.

```HTML
<body>
    <div>
        <h1>Hello, World!</h1>
        <p>Paragraph text</p>
    </div>
</body>
```

```javascript
let element = document.querySelector('div');

element.firstElementChild; // <h1>Hello, World!</h1>
```

#### lastElementChild -

> like *firstElementChild*, it returns the last child that is an HTML element. If there is no child, this will return null.

```HTML
<body>
    <div>
        <h1>Hello, World!</h1>
        <p>Paragraph text</p>
    </div>
</body>
```

```javascript
let element = document.querySelector('div');

element.lastElementChild; // <p>Paragraph text</p>
```

#### nextElementSibling -

> returns the next DOM element in the HTML. If there is no sibling, this will return null.

```HTML
<body>
    <div>
        <h1>Hello, World!</h1>
        <p>Paragraph text</p>
    </div>
</body>
```

```javascript
let element = document.querySelector('div'),
    h1 = document.querySelector('h1');

element.nextElementSibling; // null
h1.nextElementSibling; // <p>Paragraph text</p>
```

#### previousElementSibling -

> returns the previous DOM element in the HTML. If there is no sibling, this will return null.

```HTML
<body>
    <div>
        <h1>Hello, World!</h1>
        <p>Paragraph text</p>
    </div>
</body>
```

```javascript
let h1 = document.querySelector('h1'),
    p = document.querySelector('p');

h1.nextElementSibling; // null
p.nextElementSibling; // <h1>Hello, World!</h1>
```

***

[Previous](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")

[Next](/JavaScript%20DOM%20Manipulation%20Guide/4%20-%20Create%20Elements.md "4 - Create Elements")

## Table of Contents

1. [Methods](/JavaScript%20DOM%20Manipulation%20Guide/1%20-%20Methods.md "1 - Methods")
2. [Properties](/JavaScript%20DOM%20Manipulation%20Guide/2%20-%20Properties.md "2 - Properties")
3. [Traversing](/JavaScript%20DOM%20Manipulation%20Guide/3%20-%20Traversing.md "3 - Traversing")
4. [Create Elements](/JavaScript%20DOM%20Manipulation%20Guide/4%20-%20Create%20Elements.md "4 - Create New Elements")
5. [Events](/JavaScript%20DOM%20Manipulation%20Guide/5%20-%20Events.md "5 - Events")