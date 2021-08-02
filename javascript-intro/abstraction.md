# Abstraction

The main goal of abstraction is to handle complexity by hiding unnecessary details from the user. That enables the user to implement more complex logic on top of the provided abstraction without understanding or even thinking about all the hidden complexity.

Abstraction doesn't only relate to computer programs. Your coffee machine is an abstraction. You know how to make a cup of coffee by using the machine, but you do not need to know how it works internally. 

But, we're here to talk about abstraction in the context of computer programming. Let's start in Scratch to demonstrate this concept. We're going to write a sequence of steps to draw a square.

First, we'll assume that we're setup with a pen to draw. 

![](../.gitbook/assets/image%20%2865%29.png)

Now, what if we want to change the size of the square? We have to modify each of the move blocks to take a new value.

![](../.gitbook/assets/image%20%289%29.png)

We could improve this by creating a variable, named size, that would store the length of the square. That way we do not need to repeat the value 100 in each call to the function move.

![](../.gitbook/assets/image%20%2855%29.png)

There is still room for improvement. There is repetition in this series of steps. We can use a repeat loop to simplify the code further.

![](../.gitbook/assets/image%20%2837%29.png)

There's a further improvement that we can make. We can create a code block, or function, of our own named `drawSquare`, that will do these steps and then we can just call the function. 

Now we don't have to think about the implementation details of how the square is doing its job. We can just call it and count on it to fulfill the contract of what it says it will do. The function hides the complexity of drawing a square.

![](../.gitbook/assets/image%20%281%29.png)

As we saw earlier when we were calling the say function in Scratch, functions can have input arguments. For our square function, we can add an input argument to specify the size of the square.

![](../.gitbook/assets/image%20%2844%29.png)

It turns out that we can create an algorithm for drawing any polygon, because all of the interior angles must add up to 360 degrees. So we just need to calculate what the angle is that we need to turn by dividing 360 degrees by the number of sides for the polygon.

Now we have a re-usable function that has two input arguments: the number of sides, and the length of the side, and then one function can draw any polygon.

![](../.gitbook/assets/image%20%2863%29.png)

```javascript
function drawPolygon(numSides, sideLength) {
  for (let i = 0; i < numSides; i++) {
    move(sideLength);
    direction += 360 / numSides;
  }
}

drawPolygon(4, 100);
drawpPolygon(3, 100);
```

The goal for your code will be to abstract as much of functionality as possible into re-usable functions.

