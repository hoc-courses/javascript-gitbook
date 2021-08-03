# The Random Block

We can generate a random number between any two whole numbers using the `random` block:![Random](https://beautyjoy.github.io/bjc-r/img/blocks/pick-random-1-to-10.png)

This block generates numbers with about equal likelihood, and can generate both the lower and upper bounds that you give it. So, ![pick random](https://beautyjoy.github.io/bjc-r/img/blocks/pick-random-1-to-10.png) can generate 1, 2, 3, 4, 5, 6, 7, 8, 9, and 10.

This block \(and others with round edges\) is a **reporter** block—it _reports_ a value. Use this block inside other blocks that take an input.

![Random Everywhere](https://beautyjoy.github.io/bjc-r/img/prog/pick-random-block-inside-various-blocks.png)



### Using the Random Block

Next, you'll add blocks so that every time he is clicked, Alonzo moves to a random position on the stage.

1. Find the ![pick random \(1\) to \(10\)](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/pick-random-1-to-10.png) block in the green Operators palette, and click it several times to try it out.
2. What values did the `random` block report? How can you code "Alonzo moves to a random position on the stage"?
3. Add a line of code so that every time Alonzo is clicked, he not only turns, but also moves to a random position \(between -190 and 190 in the _x_ direction and between -130 and 130 in the _y_ direction\). Use two ![pick random \(\) to \(\)](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/pick-random-empty-args.png) blocks and one ![go to x=0 y=0](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/go-to-x-y-0-0.png) block together at the end of your code to make this happen. The video shows how to snap these together, but you will need to do more than it shows. ![Placing random block in goto block](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/alonzo-go-to-random.gif) 

The Snap_!_ stage \(the white space in the upper right where sprites act out their scripts\) is just like the coordinate plane. The _x_ axis goes from -240 to 240, and the _y_ axis goes from -180 to 180.  
![Coordinate Grid](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/snap-coord-grid.png)  


Make Alonzo move to a random position between -190 and 190 in the _x_ direction and between -130 and 130 in the _y_ direction so he doesn't go off the edges of the screen.

Click on Alonzo. If your script works, Alonzo should face the other way _and_ move to a random spot on the stage.

