# Web Browser Objects

## Built-in Web Browser Objects

Beyond those generic built-in objects provide by the language, in the context of web applications, the web browser has its own domain-specific objects: the navigator, window and document. 

![https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side\_web\_APIs/Manipulating\_documents](.gitbook/assets/image%20%28149%29.png)

#### Window Object

The window is the browser tab that a web page is loaded into. Using methods available on this object you can do things like return the window's size, load a new document, or manipulate the document currently loaded.

#### Document Object

The document is the actual page loaded into the window. This object is referred to as the Document Object Model \(DOM\) and is an object that you will use heavily in your JavaScript programs. It is a complex object that models the entire HTML document loaded into the web browser.



You can use this object to return and manipulate information on the HTML and CSS that comprises the document, for example get a reference to an element in the DOM, change its text content, apply new styles to it, create new elements and add them to the current element as children, or even delete it altogether.



