# Objects

## Basic Data Types

In most programming languages there are three basic data types: strings \(text\), numbers \(integers and decimal\) and boolean.  But when your program needs to store data, it must create a variable to store data based on one of these basic types.

For example, in our draw polygon block we created earlier, we store two pieces of data about a shape: the number of sides and the length of each side.

![](../.gitbook/assets/image%20%28147%29.png)

This was a simple script, and those two variables were all that was needed to accomplish the task of drawing a polygon. But what happens as the complexity of what we are building increases?  Computer applications are complex and need to model processes that involve real world objects, such as movies, products, shopping carts, users, hotels, cars, family trees, etc... The list is endless. How do we represent the data we need to store for these more complex objects?

## Composite Data Types

We build objects \(composite data types\) to model the real world things that we want to represent in our programs.

In addition to storing data associated with these objects we're modelling, we typically also want to associate functionality with the object.  So an object has two components:

* properties: data
* methods: functionality

#### A real world example: the Snap! Pen object

Let's take the example of the Snap! program itself and the software developers that built that program. What are the objects that they are modelling? There's the window, palette, blocks, pen, stage, etc. Let's look at the pen more closely. To represent the pen in the Snap! program, what are some examples of the type of data it needs to store and the functionality that operate on that data?

#### Data/Properties

| Variable | Data Type |
| :--- | :--- |
| Color | numeric |
| Size \(line thickness\) | numeric |
| Draw State \(up/down\) | boolean |

#### Methods

| Method | Description |
| :--- | :--- |
| Clear | Erase any drawings on the stage |
| Pen Up | Change the state of the pen so that it will not draw when the sprite is moved |
| Pen Down | Change the state of the pen so that it will draw when the sprite is moved |
| Fill | Fills a containing polygon at the current position of the sprite |

So a Pen has a number of basic properties that store the data about the pen being used by the user and a set of methods that allow the user to perform actions with the pen.

## Built-in JavaScript Objects

In our web applications there are also real world objects that are being modelled. In some cases, these objects are so common that the JavaScript language authors built the objects and provided them so that you can use them in your programs without having to write them yourself.

For example, almost all applications need to store a collection of objects, or lists. In JavaScript, the Array object is built-in and can be used in your program to store a collection of any type of data.  

Just like the Pen object in the Snap! program, the Array can be described as a set of properties and methods.

#### Data/Properties

| Variable | Data Type |
| :--- | :--- |
| Length | numeric |
| Elements, accessed with \[index\] | any |

#### Methods

| Name | Action |
| :--- | :--- |
| push | add an item to the end of the array |
| pop | remove an item from the end of the array |
| shift | removes the item at the front of the array |
| find | find an item in the array |

Other useful built-in objects include Date, String, Math and Map.

## Built-in Web Browser Objects

Beyond those generic built-in objects provide by the JavaScript runtime environment, the web browser has its own domain-specific objects: the window and the document.





But, in JavaScript we have just three basic data types: strings, numbers and booleans to store data. We need to be able to build more complex data types from these basic building blocks, and that's what objects are.

For example, let's say I want to represent a newspaper article inside of my JavaScript application. There isn't an "article" data type. But the data associated with an article can be represented by the basic data types. It just needs to be described within a larger structure enumerates the properties 

But we can represent all of the information within an article with these basic data types:

* title \(text\)
* abstract \(text\)
* body \(text\)
* date written \(numeric\)
* published \(boolean\)
* author 
  * first name \(text\)
  * last name \(text\)
  * email \(text\)
  * profile image path \(text\)



Objects can contain related data and code, which represent information about the thing you are trying to model, and functionality or behavior that you want it to have. 

As you've been going through these examples, you have probably been thinking that the dot notation you've been using is very familiar. That's because you've been using it throughout the course! Every time we've been working through an example that uses a built-in browser API or JavaScript object, we've been using objects, because such features are built using exactly the same kind of object structures that we've been looking at here, albeit more complex ones than in our own basic custom examples.



{% embed url="https://www.mikedane.com/web-development/javascript/real-world-objects/" %}



