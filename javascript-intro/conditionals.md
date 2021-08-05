# Conditionals

### If

A condition looks like a fork in the road which allows you to choose a path to take based on some test. 

![](../.gitbook/assets/image%20%28104%29.png)

Here is the Snap! example translated to JavaScript. 

```javascript
if (x<y) {
    alert('x is less than y');
}
```

In the JavaScript code we're introducing a new piece of syntax, the curly braces, which are used to surround the code that will be executed within the `if` block if the condition is true. 

### If Else

We can also add an else block to the `if` statement if we want to follow an alternate code path when the condition is false.

![](../.gitbook/assets/image%20%2843%29.png)

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

The code above is syntactically correct, but it can be simplified. We do not need to have a final condition for the last case, since it is the only path possible if the other two conditions are false.

```javascript
if (x<y) {
    alert('x is less than y');
}
else if (x>y) {
    alert('x is greater than y');
}
else {
    alert('x is equal to y');
}
```

{% hint style="info" %}
Operators: Assignment vs. Equality

A long time ago, the early programming languages adopted the `=` symbol to mean assignment, and since that was already taken, they needed to adopt a different symbol to test for equality. So in most computer languages, `==` is the operator to test for equality.

Scratch uses the `=` symbol to test for equality instead of assignment, which is more intuitive for users new to programming. This is because in their visual programming language the assignment process is done with the set block and so there isn't an explicit assignment operator and the = symbol is available to use.  
{% endhint %}

### Logical Operators

If your condition involves more than one criteria, then you can use logical operators to string them together to build a larger boolean condition.

![](../.gitbook/assets/image%20%28131%29.png)

In JavaScript the **logical and operator** is two ampersands **&&.**

```javascript
const age = prompt('What is your age?');
if (age>12 && age<65) {
    alert('The cost is $100');
}
else {
    alert('The cost is $50');
}
```

The `if` condition could have been rewritten using the or logical operator.

In JavaScript the **logical or operator** is two pipe symbols **\|\|.**

![](../.gitbook/assets/image%20%2852%29.png)

```javascript
const age = prompt('What is your age?');
if (age<12 || age>65) {
    alert('The cost is $50');
}
else {
    alert('The cost is $100');
}
```

