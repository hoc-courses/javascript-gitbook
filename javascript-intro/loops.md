# Loops

## Looping Forever

![](../.gitbook/assets/image%20%28138%29.png)

There isn't a direct equivalent of the Snap! forever loop in JavaScript, but the while loop is pretty close. 

```javascript
while (true) {
    alert('hello, world');
}
```

A key difference is that the  JavaScript while loop is constantly testing a condition to see whether it should continue. Here are the key rules:

* you must have parenthesis after the while keyword
* you must have a boolean condition within the parenthesis
* you use the curly braces to surround the code to execute if the condition is true \(the curly braces are not required if there is only a single statement\).

## Looping a Finite Number of Times

Whenever you want to count to a pre-defined number of times in Scratch you can use the repeat loop.

![](../.gitbook/assets/image%20%2817%29.png)

In JavaScript we have two choices: the `while` loop and the `for` loop.

#### While Loop

With the `while` loop, you are responsible for declaring and incrementing the variable that will count the number of iterations through the loop.

```javascript
let i = 0;
while (i<50) {
    alert('hello, world');
    i++;
}
```

#### For Loop

![](../.gitbook/assets/image%20%2842%29.png)

With the `for` loop, the loop includes the syntax for declaring and incrementing the variable that will count the number of iterations through the loop. It allows you to express the steps more concisely.

The syntax is as follows:

```javascript
for (initialization; condition; post-expression) {
    // statements
}
```

* **initialization**: declare and initialize the value stored in variable `i=0`
* **condition**: test whether `i<50` and if so execute the code with the for block, otherwise stop looping
* **post-expression**: after the code has been executed, increment the value store in variable `i` by one

```javascript
for (let i=0;i<50;++i) {
    alert('hello, world');
}
```

