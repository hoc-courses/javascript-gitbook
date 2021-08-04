# Lab - Abstraction - Wall

### Build a Wall

We are going to draw this brick wall.

![](../.gitbook/assets/34%20%282%29.png)

This project is not just about drawing; it is also about practicing abstraction. You will draw the following brick wall by implementing the blocks listed below.

_Note: You must implement these blocks and adhere to the abstraction described below._

There are two kinds of rows in this brick wall:

![](../.gitbook/assets/35%20%281%29.png)

The big idea is that there are three levels of abstraction. Start creating your new blocks at Level 3, then create for Level 2 \(using your new blocks from Level 1\), and then create Level 1 using your Level 2 blocks.

_Note: a “brick” is just a thick line._

#### At the lowest level of abstraction \(Level 3\):

* You need to figure out how to draw individual bricks, small bricks and spaces. The bricks are simply thick lines.
* This level of abstraction contains the following blocks:
* The Draw Brick block, which draws a single brick.
* The Draw Small Brick block, which draws the small brick for the edges of row B. Note that this brick will not be exactly half as long as the full brick. Part of this assignment is figuring out how long the “small brick” should be.
* The Draw Space block, which draws a space between each brick or small brick.

#### At the middle level of abstraction \(Level 2\):

* You can use the functionality provided by the bottom level of abstraction to make entire rows of bricks.
* The rows referred to as “Row A” and “Row B” should look like the rows shown above.
* This level of abstraction contains the following blocks:
* The Initialize Pen block, which should initialize the pen color and size.
* The Initialize Character Position and Direction block, which should initialize the position and direction of the character.
* The Draw Row A block, which should draw a single copy of Row A.
* The Draw Row B block, which should draw a single copy of Row B.
* The Transition between Row A and B with \_\_ space block, which should transition between the end of Row A and the beginning of Row B, leaving a space as wide as the number of pixels specified by the input argument.
* The Transition between Row B and A with \_\_ space block, which should transition between the end of Row B and the beginning of Row A, leaving a space as wide as the number of pixels specified by the input argument.

HINT: You will need to determine if there is an even number of rows or an odd number of rows to be drawn as well as if the row being drawn is an even number or odd number one. You can use the **mod** block to help.

Example: if TotalNumberOfRows mod 2 = 0 then the total number of rows is even \(any even number divided by 2 leaves a remainder of 0\). You can use the same logic to determine if the row to be drawn is even or odd \(if RowNumber mod 2 = 0\).

See The [Mod Block]() topic for help.

#### At the highest level of abstraction \(level 1\)

* You will put together the full brick wall using only the functionality provided by the middle level of abstraction.
* This level of abstraction contains only the Draw a Brick Wall with \_\_ rows block, which draws a brick wall with the specified number of rows.

Note: Whenever you need to refer to a number in the program, use a variable. This is generally considered good style, because you can use the same variable in multiple places in your program, and you only need to change the value of the variable to change it in multiple places at once.

In summary, you should implement the following blocks:

![](../.gitbook/assets/36.png)

### Resources

![](../.gitbook/assets/image%20%2882%29.png)

{% embed url="https://youtu.be/bons028VLEU" %}



{% embed url="https://youtu.be/Y5lZQRawsFk" %}



### Abstraction: Brick Wall

{% embed url="https://bjc.edc.org/Sept2015/bjc-r/cur/programming/2-conditionals-abstraction-testing/3-building-more-complex-blocks/3-abstraction-brick-wall.html?topic=nyc\_bjc%2F2-conditionals-abstraction.topic&course=bjc4nyc\_2015-2016.html&novideo&noassignment" %}



Designing a program to draw this picture—a brick wall that you might later use as a stage background in some program you write—is good practice in analyzing structure.![Humpty Dunpty on brick wall](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Humpty_Dumpty_Tenniel.png)![Sample image of brick wall](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/wall.png)

#### Abstraction

While any good programming language might have many tools for drawing and moving, it wouldn't make sense to have special tools for drawing bricks because most programs don't involve bricks. That is the sort of tool you make yourself when you need it. When you need to draw bricks, having a special ![draw-brick](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/draw-brick.png) block lets your code use terms directly related to the problem you are trying to solve, rather than the more general-purpose terms that the computer uses for all kinds of tasks. The process of moving from what the programming language gives you to a natural language \(one that humans speak to communicate\) is a key part of good abstraction.

In this problem, you will build an abstraction for drawing a brick wall, first by creating ![draw-brick](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/draw-brick.png), then blocks for drawing rows, and ultimately the goal: ![draw-brick-wall-n](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/draw-brick-wall-num.png).

#### Drawing One Brick

A picture of a brick is rectangle, filled in "brick red" \(darker than the primary-color red\). There's no `draw rectangle` block in Snap. One way to fake it is by thinking of a rectangle as a very thick line.![Code for draw brick](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/draw-brick-code.png)

1. Try out this block.If your "brick" has rounded ends, remember that you can [change how lines are drawn ](https://bjc.edc.org/Sept2015/bjc-r/cur/programming/2-conditionals-abstraction-testing/3-building-more-complex-blocks/bjc-r/cur/programming/2-conditionals-abstraction-testing/2-script-variables/2-script-variable-projects.html)by clicking the settings button \(![settings button](https://bjc.edc.org/Sept2015/bjc-r/img/sys/settings.png)\) in the toolbar, and turning on "Flat line ends." Rounded ends stick out beyond the length of the line you asked to draw. Here's a picture of the rounded brick with a same-length regular line \(pen size 1\) inside it:

   ![Round brick](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/round-brick.png)

   These rounded ends are better for most line drawings, but not for this purpose.

#### Using Problem Decomposition to Write an Abstraction

You'd like the "top level" block to be something like this:![draw-brick-wall-7](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/draw-brick-wall-7.png)

A human brick-layer would understand exactly how to build such a wall. A compute, doesn't know, so you must fill in the details. This means going from the abstract \(draw a brick wall\) to the concrete \(pardon the pun\). This involves **problem decomposition**.

There are two kinds of rows, so we make blocks that specialize in each:

* **Row A**: ![Row A](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/row-a.png)
* **Row B**: ![Row B](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/row-b.png)

1. Make blocks ![Row A](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/rowa-block.png) and ![Row B](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/rowb-block.png).
2. Think about what helper blocks besides ![Draw Brick](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/draw-brick.png) you might want.

   **Too much abstraction?** It's possible to go overboard on abstraction and build so many blocks that your program is just as cluttered as it would be without the special blocks.

   But it can also be useful to make a special block even when its definition is just one built-in block. For example, to draw the mortar \(the cement between bricks, shown as white space\), you can just use ![Move 4 Steps](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/move4.png), but it might make sense to define a `draw mortar` block.

   Why? You might later decide that 4 steps is the wrong thickness for mortar, and you'd rather have 5. Or you might want the mortar to be cement-colored, slightly gray. And your complete project might have ![Move 4 Steps](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/move4.png) blocks that _aren't_ about mortar. With many `move` blocks scattered through your program, you would have to find and change each one, and keep putting in `set pen color` blocks. With a `draw mortar` block, you can just change its definition, and all the mortar in your picture will be changed.

3. The two kinds of rows should be exactly the same length. Your first try at drawing Row B may be a little too long. If so, think through what causes that bug.

   How are you going to fix it? Should Row B have different-size bricks, different-size mortar gaps, or different-size half-bricks? If you're not sure, try all the possibilities and see which looks right in the finished wall. Or think "What would _make most sense_ in a _real_ brick wall?"

4. Once you have rows A and B the same length, you can write the ![Draw a Brick Wall with \( \) Rows](https://bjc.edc.org/Sept2015/bjc-r/img/abstraction/new-brickwall/draw-brick-wall-num.png) block. Make sure that it works sensibly for both even and odd numbers of rows.

 

1. ![Now Would be a Good Time to Save](https://bjc.edc.org/Sept2015/bjc-r/img/icons/save-now.png)
2. After you've drawn the picture at the top of this page, add more inputs to the `Draw a Brick Wall` block:

   1. Length of the wall \(how many bricks\)
   2. Length of a brick
   3. Mortar thickness

   Add these one at a time, not all at once! When you modify the length of a brick, that should also change the length of a half-brick. When you modify the mortar thickness, that should also change the distance between rows \(since that's mortar too\).

