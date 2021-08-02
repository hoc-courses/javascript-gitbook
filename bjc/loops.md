# Loops

Repeating a part of your program is a very common practice in programming. We'll call this _looping_, and there many different blocks you can use to do it in many different ways.

The ![](https://beautyjoy.github.io/bjc-r/img/blocks/forever.png) block is appropriate if you want to repeat the same behavior for... ever.  
  
The ![](https://beautyjoy.github.io/bjc-r/img/blocks/repeat.png) block is great if you want to loop the same behavior a certain number of times.Sometimes, though, you want to do _almost_ the same thing for a certain number of times, but with a slight variation. For instance:

* You want to draw 20 squares on the screen, but each a different size.
* You want to draw 100 polygons with different numbers of sides.

Many such situations can be handled by the `for` block near the bottom of the Control palette:

![for](https://beautyjoy.github.io/bjc-r/img/prog/for.png)

![for](https://beautyjoy.github.io/bjc-r/img/blocks/for.png)

The numbers in the `for` block work as you probably think they do: the inner script is run enough times to count from the left number \(`1`\) to the right number \(`10`\). As with the `repeat` block, you can change the numbers it comes with by default to change the way the block repeats.

What's new to you here, though, is the orange oval with "`i`" in it. By using this `i`, your inner blocks can know which time through the loop they are currently on. Here's how:

The ![](https://beautyjoy.github.io/bjc-r/img/blocks/variable-i.png) block is a _variable_ that acts like a counter. You use it any place you would use a number, and it will report the value that it currently holds.

Think of the _variable_ like a box with a name—this one has the name `i`. This box is made for you by the ![for](https://beautyjoy.github.io/bjc-r/img/prog/for.png) block, and holds a different number each time through the loop. The first time it will hold `1`, or whatever is the left number in the `for` block.

You use it by dragging ![](https://beautyjoy.github.io/bjc-r/img/blocks/variable-i.png) from the source within the `for` block down to the slot in which you will use it.

For instance:![](https://beautyjoy.github.io/bjc-r/img/looping/for-loop-drag-i.gif)

is the equivalent of![](https://beautyjoy.github.io/bjc-r/img/looping/for-loop-equivalent.png)

Click on the script below to load it in a new Snap_!_ window:[![squiral script](https://beautyjoy.github.io/bjc-r/img/looping/squirral-script.png)](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/draw-squirral.xml)

Note that we changed the name of the variable, by clicking on the orange oval _without_ dragging it.

This shape is called a "squiral" — a square spiral. Do you see why it spirals outward? The length value in the ![](https://beautyjoy.github.io/bjc-r/img/blocks/move.png) varies between repetitions.

Try changing the turning angle to other numbers: 92, 126, etc. People might pay cash money for some of these pictures!  
  
Also, try changing the turning angle and the move length to see how close you can get to a smooth spiral:  
  
![spiral](https://beautyjoy.github.io/bjc-r/img/prog/spiral.png)

![](../.gitbook/assets/image%20%2897%29.png)

## Looping Blocks

There are times when you will want blocks to repeat. Instead of duplicating blocks and ending up with a long script that might be confusing, there are looping control blocks that you can wrap around the script you want to repeat.

* **forever** Loops until the program ends. This is basically an _**infinite loop**_ as it goes on forever.
* **repeat \(\)** Loops the specified number of times.
* **repeat until &lt; &gt;** Repeat until the condition is _True_.

For the repeat until &lt; &gt; you will use a predicate block that returns true or false. These blocks have pointed ends and can be found in the Operators palette.

![](../.gitbook/assets/29%20%282%29.png)

Other helpful blocks include the operator blocks.

![](../.gitbook/assets/30%20%282%29.png)

## Looping Examples

![](../.gitbook/assets/31%20%282%29.png)

## The For Block

The repeat block is great if you want to repeat exactly the same behavior each time. Sometimes, though, you want to do almost the same thing every time, but with a slight variation. Many such situations can be handled by the for block near the bottom of the Control palette:

![](../.gitbook/assets/32%20%282%29.png)

What’s new here is the orange oval with “i” in it. This is called a variable. It represents a different value in each repetition. Try this:

![](../.gitbook/assets/33%20%282%29.png)

Note that we changed the numbers in the two white-oval input slots. We also dragged the variable i from the for block itself into the say block within its action slot. This “for loop” is equivalent to the following script:

![](../.gitbook/assets/34%20%281%29.png)

Just saying the variable isn’t all that interesting.

But now try this:

![](../.gitbook/assets/35.png)

Note that we changed the name of the variable, by clicking on the orange oval without dragging it. This shape is called a “squiral” — a square spiral. Do you see why it spirals outward? The length of the move varies between repetitions. If we wanted to create this shape without using **for**, the script would look like this:

![](../.gitbook/assets/36%20%281%29.png)

By the way, try changing the turning angle from 90 to 92. It makes a beautiful picture! Then play around with the numbers and see how close you can come to a smooth spiral:

![](../.gitbook/assets/37.png)



![](../.gitbook/assets/image%20%2879%29.png)

![](../.gitbook/assets/image%20%2880%29.png)

![](../.gitbook/assets/image%20%285%29.png)

![](../.gitbook/assets/image%20%2821%29.png)

![](../.gitbook/assets/image%20%28119%29.png)



