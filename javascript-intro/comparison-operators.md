# Comparison Operators

In Snap! a predicate is a function that returns a Boolean value. Snap! predicates are called Comparison Operators in JavaScript. 

A comparison operator compares the value of the left operand to the value of the right operand and returns a boolean value indicating whether they are equal or not.

There are two categories of Comparison Operators: relational and equality.

### Relational Operators

Snap does not have a built-in relational operator for `>=` or `<=`. When we were working in Snap!, we built a custom predicate block for `>=`.

![](../.gitbook/assets/image%20%2898%29.png)

```javascript
console.log(3>2);  // true
console.log(3<2);  // false
console.log(3>=3); // true
console.log(3<=2); // false
```

### 

### Equality Operators

The Equality Operators in JavaScript are one of the trickier parts to learn and cause a lot of confusion when you're first starting out.

#### Strict Equality

The “===” operator compares two values and if they are exactly equal \(**type and value**\) it returns true, otherwise false.

![](../.gitbook/assets/image%20%2810%29.png)

```javascript
console.log(3===3);    // true
console.log(true === true); // true
console.log(undefined === undefined); // true

console.log('1'===1);       // false
console.log(0 === false);   // false
```

#### Loose Equality

The “==” operator compares two values and if they are loosely equal \(**coercion and value**\) it returns true, otherwise false.

![](../.gitbook/assets/image%20%28103%29.png)

Any two values that pass the strict equality test will pass the loose equality test. If they are not the same type, then an attempt will be made to coerce the type of one value to the type of the other and then the two values will be compared. 

```javascript
console.log(1==1);     // true
console.log("hello" == "hello"); // true

// successful after coercion
console.log('1'==1);   // true
console.log(true==1);  // true

// unsuccessful after coercion
console.log('10'==true);
```

The term **falsy** is used in JavaScript to describe a value that evaluates to false when encountered in a boolean context.  Both "" and 0 are falsy values and will evaluate to false.

```javascript
console.log("" == false);  // true
console.log(0  == false);  // true
```

Two different objects, even if they have the same data within them, are not equal.

```javascript
let p1 = {firstName: 'Joe', lastName: 'Jones' };
let p2 = {firstName: 'Joe', lastName: 'Jones' };

console.log(p1 == p2); // false

let a1 = [1,2,3];
let a2 = [1,2,3];

console.log(a1 == a2);  // false
```

### Summary

The rules for determining whether two values will be loosely equal after coercion are complex.  To avoid unintentional errors, it is recommend to use the strict equality,  "===" operator. 

