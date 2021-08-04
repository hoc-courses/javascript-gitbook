# Variables

## Creating/Assigning Variables

In Snap! we saw that we could create a variable and assign it a value with the set block.

![](https://lh5.googleusercontent.com/HuXPos2yNMmc4bqQiKZN3ydBAL1xiPPDhUTaxeYN1E6dbH9AAyKrFBp3eaTf8l0hyOWITuGNE_lQeZ323gxw9OmjkTrYflOd0FpkDB0e-ZaJYcqgKsudTqisIPQtqwR9VvDTkHy3Sg)

In JavaScript, we need to do the following. 

```javascript
let counter = 0;
```

Unlike lower level languages, we do not need to specify the data type of the variable. JavaScript will figure it out when the program is running.

## Increment/Decrement a Numeric Variable

![](https://lh5.googleusercontent.com/dGRtH1EIwF96IQ0FyCv66s4DZHI7R5dXPJehYEFXEDh4fspph7vWpAwfdwyErOIzo8NsFS_J3LlPr2RfK-L-AiHHOJtu2QpOsgWdozHiZHzMjUIizteR-oIr2BEmpdfMEipyVAftGQ)

Here is the JavaScript equivalent. 

```javascript
counter = counter + 1;
```

This might look a little odd at first because in the JavaScript language the `=` symbol does not mean equal. It is the **assignment operator**. So, whatever is on the right side of the `=` symbol will be assigned to the variable on the left of the `=` symbol.

So, this is saying, take the result of counter + 1 and store it in the variable counter.

It is a very common operation in programming to keep track of a counter. So there are a couple of short-cuts, or more succinct ways of expressing the same thing.

```javascript
counter++;
```

```javascript
counter+=1;
```

