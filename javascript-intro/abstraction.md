# Abstraction

Let's start in Scratch to demonstrate this concept. We're going to write a sequence of steps to draw a square.

First, we'll assume that we're setup with a pen to draw. 

![](../.gitbook/assets/image%20%2828%29.png)

Now, what if we want to change the size of the square? We have to modify each of the move blocks to take a new value.

![](../.gitbook/assets/image%20%285%29.png)

We could improve this by creating a variable, named size, that would store the length of the square. That way we do not need to repeat the value 100 in each call to the function move.

![](../.gitbook/assets/image%20%2822%29.png)

There is still room for improvement. There is repetition in this series of steps. We can use a repeat loop to simplify the code further.

![](../.gitbook/assets/image%20%2815%29.png)

There's a further improvement that we can make. We can create a code block, or function, of our own named drawSquare, that will do these steps and then we can just call the function. 

Then we don't have to think about the implementation details of how the square is doing its job. We can just call it and count on it to fulfill the contract of what it says it will do. This is the essence of a function.

![](../.gitbook/assets/image%20%281%29.png)

As we saw earlier when we were calling the say function in Scratch, functions can have input arguments. For our square function, we can add an input argument to specify the size of the square.

![](../.gitbook/assets/image%20%2818%29.png)

It turns out that we can create an algorithm for drawing any polygon, because all of the interior angles must add up to 360 degrees. So we just need to calculate what the angle is that we need to turn by dividing 360 degrees by the number of sides for the polygon.

Now we have a re-usable function that has two input arguments: the number of sides, and the length of the side, and then one function can draw any polygon.

![](../.gitbook/assets/image%20%2826%29.png)

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

