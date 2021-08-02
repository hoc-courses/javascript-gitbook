# Loops

## Looping Blocks

There are times when you will want blocks to repeat. Instead of duplicating blocks and ending up with a long script that might be confusing, there are looping control blocks that you can wrap around the script you want to repeat.

* **forever** Loops until the program ends. This is basically an _**infinite loop**_ as it goes on forever.
* **repeat \(\)** Loops the specified number of times.
* **repeat until &lt; &gt;** Repeat until the condition is _True_.

For the repeat until &lt; &gt; you will use a predicate block that returns true or false. These blocks have pointed ends and can be found in the Operators palette.

![](../.gitbook/assets/29%20%281%29.png)

Other helpful blocks include the operator blocks.

![](../.gitbook/assets/30%20%281%29.png)

## Looping Examples

![](../.gitbook/assets/31%20%281%29.png)

## The For Block

The repeat block is great if you want to repeat exactly the same behavior each time. Sometimes, though, you want to do almost the same thing every time, but with a slight variation. Many such situations can be handled by the for block near the bottom of the Control palette:

![](../.gitbook/assets/32%20%281%29.png)

What’s new here is the orange oval with “i” in it. This is called a variable. It represents a different value in each repetition. Try this:

![](../.gitbook/assets/33%20%281%29.png)

Note that we changed the numbers in the two white-oval input slots. We also dragged the variable i from the for block itself into the say block within its action slot. This “for loop” is equivalent to the following script:

![](../.gitbook/assets/34.png)

Just saying the variable isn’t all that interesting.

But now try this:

![](../.gitbook/assets/35.png)

Note that we changed the name of the variable, by clicking on the orange oval without dragging it. This shape is called a “squiral” — a square spiral. Do you see why it spirals outward? The length of the move varies between repetitions. If we wanted to create this shape without using **for**, the script would look like this:

![](../.gitbook/assets/36%20%281%29.png)

By the way, try changing the turning angle from 90 to 92. It makes a beautiful picture! Then play around with the numbers and see how close you can come to a smooth spiral:

![](../.gitbook/assets/37.png)

