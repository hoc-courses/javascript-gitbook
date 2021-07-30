# Conditionals

### If

A condition looks like a fork in the road which allows you to choose a path to take based on some test.

Here is the Scratch example translated to JavaScript. 

![](https://lh3.googleusercontent.com/0yRj3rZbZTw97NEr3DGDC3-RzakdOIVvJRpYbglx9ZCSjWKGl7mvBJmMYBVnMKM-gwpEFDV4K0OSmVykzc3wfFX4EfHfco_VFiNppOWELwnDGyfqHzdGF_4ztkP2-TbBt6g_3YX0JQ)

In the JavaScript code we're introducing a new piece of syntax, the curly braces, which used to surround the code that will be executed within the if block if the test is true. 

```javascript
if (x<y) {
    alert('x is less than y');
}
```

### If Else

We can also add an else block to the if statement if we want to follow an alternate code path when the test is false.

![](https://lh5.googleusercontent.com/1YkZBjx68oSdlxN-mSndriiw-BRX6B6ZYrds-7fiXQ-dxQ1b5POz3JU6pFq0bbEhOYbXPomdbylSZQvKbsNOrRr4sPa6PpQltA0mff2tOG1yHvi09YHJgtMxmBTUbL_WuNUU6Nr11A)

```javascript
if (x<y) {
    alert('x is less than y');
}
else {
    alert('x is not less than y');
}
```

### If Else If

![](https://lh5.googleusercontent.com/gmcDz8_K5il9UBC-0rIUQtbZa9LLxhFOmv99Nfii9LhYYd0rtd9D2qqd_0kfShQ0eymc6wOFCo8amrdkHiXxUy_w3xvRTfTO46FisSukSVUmqxuZP3xyby39jrYNmAK5hWCKj28fDw)

In this case, the JavaScript equivalent is a little more succinct because we can put the else and if on the same line.

```javascript
if (x<y) {
    alert('x is less than y');
}
else if (x>y) {
    alert('x is greater than y');
}
else if (x==y) {
    alert('x is equal to y');
}
```

{% hint style="info" %}
Operators: Assignment vs. Equality

A long time ago, the early programming languages adopted the `=` symbol to mean assignment, and since that was already taken, they needed to adopt a different symbol to test for equality. So in most computer languages, `==` is the operator to test for equality.

Scratch uses the `=` symbol to test for equality instead of assignment, which is more intuitive for users new to programming. This is because in their visual programming language the assignment process is done with the set block and so there isn't an explicit assignment operator and the = symbol is available to use.  
{% endhint %}



