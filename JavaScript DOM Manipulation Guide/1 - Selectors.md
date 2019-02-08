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

***

reference:

<span class="method"></span>

<span class="property"></span>

<span class="html"></span>

```html

```

```javascript

```

***

# JavaScript DOM Manipulation Guide - Selectors

> ### Selection methods to query the DOM

<span class="method">**getElementById**</span> selects a single DOM element with an id attribute.

```javascript
document.getElementById('element');
```

Elements from the DOM are also able to be stored into variables.

```javascript
let element = document.getElementById('element');

console.log(element); 
// <div id="element"></div> 
```

- By selecting elements on the DOM, you are able to change its contents.

- <span class="property">**.textContent**</span> is a property that can change the text within an HTML element.

    ```javascript
    element.textContent = 'Hello, World!';

    console.log(element); 
    // <div id="element">Hello, World!</div>
    ```

    In addition to <span class="property">.textContent</span>, there are other useful methods such as <span class="property">.innerText</span>. For the most part, both properties are similar. The main difference being: <span class="property">.innerText</span> pays attention to the style of the element.

    For example:

    ```html
    <div id="element">Hello, World!<span>123</span></div>
    ```

    In the above HTML, a <span class="html">span</span> tag has been added to the <span class="html">div</span>. Now suppose the <span class="html">span</span> element contains the style property "`display: none;`" which hides the <span class="html">span's</span> content in the browser.

    By console logging:

    ```javascript
    console.log(element.textContent);
    // Hello, World! 123
    ```

    in the browser, you will see that the <span class="html">span</span> element is still not displayed in the browser, but shows in the console. 
    
    However, if you were to console log:

    ```javascript
    console.log(element.innerText);
    // Hello, World!
    ```

    the <span class="html">span</span> is ignored as it is in the browser; the styling is payed attention to.

