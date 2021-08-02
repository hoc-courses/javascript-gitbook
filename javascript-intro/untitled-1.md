# Functions

Functions are blocks of code that we can use in our program to do something. They can be thought of as small actions or verbs for the task that they perform in a program.

![](../.gitbook/assets/image%20%2841%29.png)

### Input - Arguments

The inputs to functions are called **arguments**. A function isn't required to have inputs. They are used when the function needs additional information to complete its task.

For example, the “say” block in Scratch has a single input, the text to display on the screen.

![](https://lh5.googleusercontent.com/0umy7NpnGxo03tlKa73tzeEaFKHMKWsydJ2cjo8RysDrhtVIwo0SZp9xswLsVEzk10gD5cxV2cMK4uudHl1Tom5IDXrWpkoya-PZo621NQ9PrKMGnw4Ak3emccN6chKIxY3OSueraA)

In JavaScript, the function to display something to the screen is called `alert`, and it also takes a single argument of what text to display.

```javascript
alert("hello, world");
```

Since it's a text-based language, the syntax in JavaScript is more verbose.

* we pass in arguments within parentheses
* the double quotes indicate that we want to print out the letters `hello, world` literally
* the semicolon at the end indicates the end of our line of code.

###  Outputs

Functions can have two kinds of outputs:

**Side effects -** such as something displayed on the screen

**Return values**, a value that is passed back to our program that we can use or store for later.

The `ask` block in Scratch, for example, created an `answer` block.

![](https://lh6.googleusercontent.com/qcZr24T0NgkTUBnp0Y31z2z9cpO5p35VIBSxLtJv9Xds8de0zVCC0tAkpj0D9d4hmGhnL83kULDdBQavkTn0vBaP8NQB-jrQRuYGCsqWyRU5Uwhe-b2n9dACJfdHwJrEmXZcxD46tw)

In JavaScript, the function to ask the user a question is called `prompt`. And just like the Scratch version, the prompt function returns a value that you can use in your program. While Scratch automatically creates the variable to hold the return value, in JavaScript, we have to explicitly declare and name the variable that will hold the value.

```javascript
const answer = prompt("What's your name?");
```

![](../.gitbook/assets/image%20%2812%29.png)

### Using the Return Value

Once we have received the return value from a function we can then proceed to do something with that value.

![](../.gitbook/assets/image%20%2830%29.png)

In JavaScript, the equivalent of the join function is a special string formatting syntax that can plug in the values of variables to a string template.

```javascript
const answer = prompt("What's your name?");
alert(`hello, ${answer}`);
```

