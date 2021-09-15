# How do I Write a Script?

### HOW DO I WRITE A SCRIPT FOR A WEB PAGE?

#### HOW HTML, CSS, & JAVASCRIPT FIT TOGETHER

Before diving into the JavaScript language, you need to know how it will fit together with the HTML and CSS in your web pages.

Web developers usually talk about three languages that are used to create web pages: HTML, CSS, and JavaScript.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p044-001.jpg)

**CONTENT LAYER - HTML \(`.html extension`\)**

This is where the content of the page lives. The HTML gives the page structure and adds semantics.

Where possible, aim to keep the three languages in separate files, with the HTML page linking to CSS and JavaScript files.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p044-002.jpg)

**PRESENTATION LAYER - CSS file \(`.css extension`\)**

The CSS enhances the HTML page with rules that state how the HTML content is presented \(backgrounds, borders, box dimensions, colors, fonts, etc.\).

Each language forms a separate **layer** with a different purpose. Each layer, from left to right, builds on the previous one.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p044-003.jpg)

**BEHAVIOR LAYER - JavaScript files \(`.js extension`\)**

This is where we can change how the page behaves, adding interactivity. We will aim to keep as much of our JavaScript as possible in separate files.

Programmers often refer to this as a **separation of concerns**.

#### PROGRESSIVE ENHANCEMENT

These three layers form the basis of a popular approach to building web pages called progressive enhancement.

As more and more web-enabled devices come onto the market, this concept is becoming more widely adopted.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p045-001.jpg)

**HTML ONLY**

Starting with the HTML layer allows you to focus on the most important thing about your site: its content.

Being plain HTML, this layer should work on all kinds of devices, be accessible to all users, and load quite quickly on slow connections.

It's not just screen sizes that are varied - connection speeds and capabilities of each device can also differ.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p045-002.jpg)

**HTML + CSS**

Adding the CSS rules in a separate file keeps rules regarding how the page looks away from the content itself.

You can use the same style sheet with all of your site, making your sites faster to load and easier to maintain. Or you can use different style sheets with the same content to create different views of the same data.

Also, some people browse with JavaScript turned off, so you need to make sure that the page still works for them.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p045-003.jpg)

**HTML + CSS + JAVASCRIPT**

The JavaScript is added last and enhances the usability of the page or the experience of interacting with the site.

Keeping it separate means that the page still works if the user cannot load or run the JavaScript. You can also reuse the code on several pages \(making the site faster to load and easier to maintain\).

#### CREATING A BASIC JAVASCRIPT

JavaScript is written in plain text, just like HTML and CSS, so you do not need any new tools to write a script. This example adds a greeting into an HTML page. The greeting changes depending on the time of day.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/green-fill001.png) Create a folder to put the example in called c01, then start up your favorite code editor, and enter the text to the right.

A JavaScript file is just a text file \(like HTML and CSS files are\) but it has a .js file extension, so save this file with the name add-content.js

Don't worry about what the code means yet, for now we will focus on how the script is created and how it fits with an HTML page.

```text
var today = new Date();
var hourNow = today.getHours();
var greeting;

if (hourNow > 18) {
    greeting = ‘Good evening!’;
} else if (hourNow > 12) {
    greeting = ‘Good afternoon!’;
} else if (hourNow > 0) {
    greeting = ‘Good morning!’;
} else {
    greeting = ‘Welcome!’;
}

document.write(‘<h3>’ + greeting + ‘</h3>’);
```

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/green-fill002.png) Get the CSS and images for this example from the website that accompanies the book: [www.javascriptbook.com](http://www.javascriptbook.com/)

To keep the files organized, in the same way that CSS files often live in a folder called styles or css, your JavaScript files can live in a folder called scripts, javascript, or js. In this case, save your file in a folder called js

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p046-001.jpg)

Here you can see the file structure that you will end up with when you finish the example. Always treat file names as being case-sensitive.

#### LINKING TO A JAVASCRIPT FILE FROM AN HTML PAGE

When you want to use JavaScript with a web page, you use the HTML &lt;script&gt; element to tell the browser it is coming across a script. Its src attribute tells people where the JavaScript file is stored.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/green-fill003.png) In your code editor, enter the HTML shown on the left. Save this file with the name add-content.html

The HTML &lt;script&gt; element is used to load the JavaScript file into the page. It has an attribute called src, whose value is the path to the script you created.

This tells the browser to find and load the script file \(just like the src attribute on an &lt;img&gt; tag\).

```text
<!DOCTYPE html>
<html>
  <head>
    <title>Constructive &amp; Co.</title>
    <link rel=“stylesheet” href=“css/c01.css” />
  </head>
  <body>
    <h1>Constructive &amp; Co.</h1>
    <script src=“js/add-content.js”></script>
    <p>For all orders and inquiries please call
      <em>555-3344</em></p>
  </body>
</html>
```

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/green-fill004.png) Open the HTML file in your browser. You should see that the JavaScript has added a greeting \(in this case, Good Afternoon!\) to the page. \(These greetings are coming from the JavaScript file; they are not in the HTML file.\)

**Please note:** Internet Explorer sometimes prevents JavaScript running when you open a page stored on your hard drive. If this affects you, please try Chrome, Firefox, Opera, or Safari instead.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p047-001.jpg)

#### THE SOURCE CODE IS NOT AMENDED

If you look at the source code for the example you just created, you will see that the HTML is still exactly the same.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/green-fill005.png) Once you have tried the example in your browser, view the source code for the page. \(This option is usually under the View, Tools or Develop menu of the browser.\)

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p048-001.jpg)

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/green-fill006.png) The source of the web page does not actually show the new element that has been added into the page; it just shows the link to the JavaScript file.

As you move through the book, you will see most of the scripts are added just before the closing &lt;/body&gt; tag \(this is often considered a better place to put your scripts\).

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p048-002.jpg)

#### PLACING THE SCRIPT IN THE PAGE

You may see JavaScript in the HTML between opening &lt;script&gt; and closing &lt;/script&gt; tags \(but it is better to put scripts in their own files\).

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/green-fill007.png) Finally, try opening the HTML file, removing the src attribute from the opening &lt;script&gt; tag, and adding the new code shown on the left between the opening &lt;script&gt; tag and the closing &lt;/script&gt; tag. The src attribute is no longer needed because the JavaScript is in the HTML page.

As noted on p44, it is better not to mix JavaScript in your HTML pages like this, but it is mentioned here as you may come across this technique.

```text
<!DOCTYPE html>
<html>
  <head>
    <title>Constructive &amp; Co.</title>
    <link rel=“stylesheet” href=“css/c01.css” />
  </head>
  <body>
    <h1>Constructive &amp; Co.</h1>
    <script>document.write(‘<h3>Welcome!</h3>’);
    </script>
    <p>For all orders and inquiries please call
      <em>555-3344</em></p>
  </body>
</html>
```

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/green-fill008.png) Open the HTML file in your web browser and the welcome greeting is written into the page.

As you may have guessed, document.write\(\) writes content into the document \(the web page\). It is a simple way to add content to a page, but not always the best. [Chapter 5](https://learning-oreilly-com.ezproxy.spl.org/library/view/javascript-and-jquery/9781118531648/10_chapter05.html#chap5) discusses various ways to update the content of a page.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p049-001.jpg)

#### HOW TO USE OBJECTS & METHODS

This one line of JavaScript shows how to use objects and methods. Programmers refer to this as **calling** a method of an object.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p050-001.jpg)

Behind the scenes, the browser uses a lot more code to make the words appear on the screen, but you don't need to know how the browser does this.

You only need to know how to call the object and method, and how to tell it the information it needs to do the job you want it to. It will do the rest.

There are lots of objects like the **document** object, and lots of methods like the **write\(\)** method that will help you write your own scripts.

#### JAVASCRIPT RUNS WHERE IT IS FOUND IN THE HTML

When the browser comes across a &lt;script&gt; element, it stops to load the script and then checks to see if it needs to do anything.

![image](https://learning-oreilly-com.ezproxy.spl.org/api/v2/epubs/urn:orm:book:9781118531648/files/images/p051-001.jpg)

### SUMMARY

* It is best to keep JavaScript code in its own JavaScript file. JavaScript files are text files \(like HTML pages and CSS style sheets\), but they have the .js extension.
* The HTML &lt;script&gt; element is used in HTML pages to tell the browser to load the JavaScript file \(rather like the &lt;link&gt; element can be used to load a CSS file\).
* If you view the source code of the page in the browser, the JavaScript will not have changed the HTML, because the script works with the model of the web page that the browser has created.

