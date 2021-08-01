# Including JavaScript

### Two Methods for Including JavaScript

JavaScript code you write is known as scripts. The scripts can be included in your web page in one of two ways:

**1. External File** - scripts are loaded from an external file referenced in a `<script>` element. This is the **preferred method**, as all of the scripts are maintained in one place and can be shared across web pages.

```markup
<body>
    <!-- after all html -->
    <script src="scripts.js"/>
</body>
```

```javascript
// scripts.js

document.write("Hello World");
```

**2. Embedded Scripts** - scripts are embedded directly in the html `<script>` element. This method is discouraged because it is harder to maintain and re-use scripts. It is used primarily for prototyping/testing out ideas.

```markup
<body>
    <script>
        document.write("Hello World");
    </script>
</body>
```

### Script Placement

While the `<script>` element can be placed anywhere within the HTML document, it is best to place it as the very last element in the `<body>` element. 

This is because the code in the script will be executed immediately when the web browser encounters it when reading the HTML document, and if the script refers to elements in the HTML document that occur later in the document, then those elements will not have been loaded yet by the web browser.

For example, if a script element is inside the head element, and it set the background color of the body element, an error would occur because the body element has not been generated yet.

```markup
<body>
  <script>
    document.getElementById('title').style.color="red";
  </script>
  
  <h1 id="title">Hello World</h1>
</body>
```

![](../.gitbook/assets/image%20%2825%29.png)

```markup
<body>
  <h1 id="title">Hello World</h1>
  
  <script>
    document.getElementById('title').style.color="red";
  </script>
</body>
```

![](../.gitbook/assets/image%20%2821%29.png)

{% embed url="https://www.htmldog.com/guides/javascript/beginner/makingstuffhappen/" %}



