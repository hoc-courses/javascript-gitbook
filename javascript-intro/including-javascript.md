# Including JavaScript

### Including JavaScript in a Web Page

The JavaScript code you write is known as scripts. Scripts can be included in your web page using the `<script>` element.

The `<script>` element can either contain scripts directly \(internal\) or link to an external resource by using the `src` attribute \(external\). 

**Internal** - you can just put the script inside the `<script>` element.

```markup
<script>
    alert("Hello World");
</script>
```

\*\*\*\*

**External** - an external JavaScript resource is a text file with a `.js` extension, just like an external CSS resource with a `.css` extension. 

```markup
<script src="scripts.js"/>
```

When the web browser is loading a web page, and encounters a `<script>` element, it will pass the script off to a special component called the JavaScript Engine, which will then read and execute the code line by line.

\*\*\*\*

**Embedded** - there is one other way you will see JavaScript code: directly within an HTML element as part of an event handler.

```markup
<button onclick="alert('Hello World')">Click me</button>
```

### 

### Script Placement

While the `<script>` element can be placed anywhere within the HTML document, it is best to place it as the very last element in the `<body>` element. 

This is because the when the web browser is loading a web page, it reads the document  line by line and when it encounters a `<script>` element, the script code will be executed immediately. If the executing script refers to an element later in the document, that hasn't been loaded yet, an error will occur.

For example, if a script element is inside the head element, and when the script is run, it sets the background color of the body element, an error would occur because the body element has not been loaded yet.

```markup
<body>
  <script>
    document.getElementById('title').style.color="red";
  </script>
  
  <h1 id="title">Hello World</h1>
</body>
```

![](../.gitbook/assets/image%20%2857%29.png)

```markup
<body>
  <h1 id="title">Hello World</h1>
  
  <script>
    document.getElementById('title').style.color="red";
  </script>
</body>
```

![](../.gitbook/assets/image%20%2852%29.png)

