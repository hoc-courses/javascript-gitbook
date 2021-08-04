# For Loop

## Tracking Progress with the For Loop

Repeating a part of your program is a very common practice in programming. We'll call this _looping_, and there many different blocks you can use to do it in many different ways.

The ![](https://beautyjoy.github.io/bjc-r/img/blocks/forever.png) block is appropriate if you want to repeat the same behavior for... ever.  
  
The ![](https://beautyjoy.github.io/bjc-r/img/blocks/repeat.png) block is great if you want to loop the same behavior a certain number of times. 

Sometimes, though, you want to do _almost_ the same thing for a certain number of times, but with a slight variation. For instance:

* You want to draw 20 squares on the screen, but each a different size.
* You want to draw 100 polygons with different numbers of sides.

Many such situations can be handled by the `for` block near the bottom of the Control palette:

## For Loop Details

![for](https://beautyjoy.github.io/bjc-r/img/prog/for.png)

The numbers in the `for` block work as you probably think they do: the inner script is run enough times to count from the left number \(`1`\) to the right number \(`10`\). As with the `repeat` block, you can change the numbers it comes with by default to change the way the block repeats.

What's new to you here, though, is the orange oval with "`i`" in it. By using this `i`, your inner blocks can know which time through the loop they are currently on. Here's how:

The ![](https://beautyjoy.github.io/bjc-r/img/blocks/variable-i.png) block is a _variable_ that acts like a counter. You use it any place you would use a number, and it will report the value that it currently holds.

Think of the _variable_ like a box with a name—this one has the name `i`. This box is made for you by the ![for](https://beautyjoy.github.io/bjc-r/img/prog/for.png) block, and holds a different number each time through the loop. The first time it will hold `1`, or whatever is the left number in the `for` block.

You use it by dragging ![](https://beautyjoy.github.io/bjc-r/img/blocks/variable-i.png) from the source within the `for` block down to the slot in which you will use it.

For instance:![](https://beautyjoy.github.io/bjc-r/img/looping/for-loop-drag-i.gif)

is the equivalent of![](https://beautyjoy.github.io/bjc-r/img/looping/for-loop-equivalent.png)

## Using the For Loop Block

Click on the script below to load it in a new Snap_!_ window:[![squiral script](https://beautyjoy.github.io/bjc-r/img/looping/squirral-script.png)](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/draw-squirral.xml)

Note that we changed the name of the variable, by clicking on the orange oval _without_ dragging it.

This shape is called a "squiral" — a square spiral. Do you see why it spirals outward? The length value in the ![](https://beautyjoy.github.io/bjc-r/img/blocks/move.png) varies between repetitions.

Try changing the turning angle to other numbers: 92, 126, etc.   
  
Also, try changing the turning angle and the move length to see how close you can get to a smooth spiral:  
  
![spiral](https://beautyjoy.github.io/bjc-r/img/prog/spiral.png)

## Extra Challenge

**Predict what the following script will produce** and then build the script to test your hypothesis.

![](../.gitbook/assets/image%20%2872%29.png)

**Build the following**

* Build a **nest squares** block that uses a **for loop** block and your **draw polygon** block to draw nested squares. Give it an input so that it will draw whatever number of squares you specify, with each square larger than the previous.
* Build a **nest polygons** block that accepts the number of polygons and the number of sides for the polygons.
* Build a script that draws 12 regular polygons, each with one more side than the previous one, as shown below.

![](https://github.com/hoc-labs/images/blob/main/polygons.png?raw=true)

3. Use a **for loop** to nest squares this way. 

![](https://github.com/hoc-labs/images/blob/main/concentric-squares.png?raw=true)

Build your block with two inputs that let you specify how many squares the design will contain and how much bigger each square will be than the previous one.



#### Find the Bugs

Now let's consider a slightly more complicated block that makes use of a loop. It accepts two numbers as inputs \(`start` and `end`\) and finds the sum of all of the numbers in the range from `start` to `end`, inclusive.![sum of nums in a range](https://beautyjoy.github.io/bjc-r/img/blocks/sum-of-numbers-between-8-and-10.gif)

When `start = 8` and `end = 10`, the value reported by this function should be `27` \(8+9+10\). However, the attempts at a solution shown below have some bugs. See if you can fix the bugs in the code below so that each version reports the correct sum:

_Note:_ click on any of the pictures to go to a Snap_!_ file containing the code.

[![buggy sum of nums set block](https://beautyjoy.github.io/bjc-r/img/debugging/set-bug-sum-of-range.png)![buggy sum of nums no report](https://beautyjoy.github.io/bjc-r/img/debugging/buggy-sum-of-nums-no-report.png)![buggy sum of nums repeat until](https://beautyjoy.github.io/bjc-r/img/debugging/buggy-sum-of-nums-repeat-until.png)](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/debugging/sum-of-nums-buggy.xml)

