# Lab - Predicates

**In this lab,** you will develop tools to help solve word puzzles by searching for words that match specific characteristics.

**On this page**, you will review predicates and build a few that you can use in other projects.

As you know, predicates are reporter blocks \(functions\) that always report a _Boolean value_ \(they report only the values ![true](https://bjc.edc.org/bjc-r/img/blocks/true.png) or ![false](https://bjc.edc.org/bjc-r/img/blocks/false.png)\). In Snap_!_, predicates are represented by hexagonal blocks. They compute the _condition_ used by _conditionals_ \(such as `if`, `if else`, or `repeat until`\) to decide when to do something.

So, the _input type_ of a conditional is Booleans, and the _output type_ of a predicate is also Booleans.

* The **input type** of a function is the type of data that it accepts as input.
* The **output type** of a function is the type of data that it reports as output.

Along with "abstraction," these two ideas are among the most important in computer science. If you get in the habit of using them in your thinking, you'll have many fewer bugs in your programs, because you'll automatically double-check that the output type of a reporter matches the input type of the block in which you're trying to use it.

Predicates ask a true/false question such as "Is the random number 3?" or "Is this sprite touching the sprite called 'Leader'?"

Every `if else` block has two scripts inside of it, exactly one of which will be run depending on the value that the predicate reports. Then the computer continues with whatever comes after the `if else` block.  
[![if \(pick random \(1\) to \(4\)\) = \(3\) {
    report \(join \(who\) \(&apos;, who&apos;\) \(does what\) \( \) \(who\) \(,\)\)
} else {
    report \(who\)
}](https://bjc.edc.org/bjc-r/img/2-complexity/more-complicated-who-conditional.png)](https://bjc.edc.org/bjc-r/cur/programming/1-introduction/2-gossip-and-greet/5-if-else.html?topic=nyc_bjc%2F1-intro-loops.topic&course=bjc4nyc.html&novideo&noassignment) [![when green flag clicked:
repeat until \(touching \(Leader\)?\)
{
    point towards \(Leader\)
    move \(1\) steps
}](https://bjc.edc.org/bjc-r/img/1-introduction/move-tiny-no-comment.png)](https://bjc.edc.org/bjc-r/cur/programming/1-introduction/5-follow-the-leader/2-sprite-interaction.html?topic=nyc_bjc%2F1-intro-loops.topic&course=bjc4nyc.html&novideo&noassignment)

 Use one or more of the following _relational operators_ to create a script that lets you use your mouse to write on the stage in two colors depending on the mouse's position on the stage.  
![less than, equal to, and greater than predicate blocks](https://bjc.edc.org/bjc-r/img/2-complexity/relations.jpg)

 Make the sprite draw only if the mouse button is down, so that you can draw disconnected shapes. You'll need to uncheck the "draggable" box above the scripting area before you try this \(so that Snap_!_ doesn't think you are trying to drag the sprite when you click\).

![](../.gitbook/assets/image%20%2892%29.png)

  
You'll probably want to use the ![mouse down? predicate block](https://bjc.edc.org/bjc-r/img/blocks/mouse-down.png) block, which you can find in the Sensing palette.

![bicolor printed hello](https://bjc.edc.org/bjc-r/img/2-complexity/bicolor-hello.png)

#### Boolean Functions

At the very lowest level, computer circuitry is made of wires, and each wire is either on or off. So the only operations that can be performed at that lowest level are those that _operate on single-bit values_ \(just ones and zeros, that is, just ons and offs\). These are called _logical \(or Boolean\) functions_. \(They're predicates, because their range is Booleans, but these are special in that their _domain_ is also Booleans.\) There are three Boolean functions in the Operators palette:  
![and, or, not blocks](https://bjc.edc.org/bjc-r/img/prog/Booleans.png)  
Notice that both the blocks themselves and the input slots in the blocks are hexagonal. Boolean functions take Boolean values \(`True` or `False`\) as inputs and report a new Boolean value as output. When you use Boolean functions in a program, though, the inputs will usually be expressions such as ![variable = 3](https://bjc.edc.org/bjc-r/img/2-complexity/var=3.png).

Experiment with different input values in all three blocks, and take notes about the results you get.

Instead of dragging a `true` or `false` block into the input slot of an `and`, `or`, or `not` block, you can click the empty input slot to control a `true`/`false` toggle: ![\(true\) and \(false\)](https://bjc.edc.org/bjc-r/img/2-complexity/true-and-false.png)



The `and` and `not` blocks work exactly the way you'd expect from the meanings of those words in English:

* ![\(true\) and \(true\)](https://bjc.edc.org/bjc-r/img/2-complexity/true-and-true.png) reports `true`, and any other combination of inputs reports `false`.
* ![not \(\)](https://bjc.edc.org/bjc-r/img/blocks/not.png) reports the opposite of whichever input value you use.

But `or` is a little different in computer science. In English, the word "or" has two different meanings:

* **Either but not both:** such as "Let's check whether it will be rainy or sunny tomorrow." In computer science, this is called _exclusive or_ because one option excludes the other.
* **Either or both:** such as "Ask your teacher if you have any questions or if you need help." This is called _inclusive or_ because it's possible for both options to be included.

Experiment. Does the ![\(\) or \(\)](https://bjc.edc.org/bjc-r/img/blocks/or.png) block implement _exclusive_ or _inclusive_ `or`?

Make the blocks ![less than or equal](https://bjc.edc.org/bjc-r/img/blocks/less-than-or-equal.png), ![greater than or equal](https://bjc.edc.org/bjc-r/img/blocks/greater-than-or-equal.png), and ![\(\) not equal \(\)](https://bjc.edc.org/bjc-r/img/2-complexity/not-equal.png). \(You can copy the characters ≤, ≥, and ≠ from this page and paste them into the Snap! Make-a-block window.\)

Build a predicate that tells whether an input is between two other inputs, and test it with several different cases.  
You can decide whether `between?` will include the two boundary inputs or not.![is \(3.8\) between \(3.9\) and \(4.7\) ? reporting false](https://bjc.edc.org/bjc-r/img/2-complexity/number-between-two-others%28with-result-false%29.png) ![is \(apples\) between \(alphabet\) and \(azure\) ? reporting true](https://bjc.edc.org/bjc-r/img/2-complexity/word-between-two-others%28with-result-true%29.png)

**Making a Predicate**

* Choose the hexagonal _predicate_ shape. ![Make a block dialog highlighting the predicate button](https://bjc.edc.org/bjc-r/img/2-complexity/make-predicate.png)
* You must use the ![report\(\)](https://bjc.edc.org/bjc-r/img/blocks/report.png) block to report the result of reporters \(including predicates\).

1. Use `between?` to create a script that lets you write on the stage in three colors \(depending on the height on the stage\), using your mouse.

### Combining Conditionals

1. Here are four possible ways to define `≥`. Discuss what advantages each style has:  


   1. Do they all work correctly?
   2. Which seem elegant because they are short?
   3. Which seem elegant because they are clear?
   4. Which seem elegant because the steps are simple?
   5. Which is closest to how you think about ≥ in math class?
   6. Which seems _clearest to you_?



   ![a &#x2265; b {if \(a &amp;gt; b\) {report true} else {if \(a = b\) {report true} else {report false}}}](https://bjc.edc.org/bjc-r/img/2-complexity/ge-ifelseelse.png) ![a &#x2265; b {if \(a &amp;gt; b\) {report true} else {report \(a = b\)}}](https://bjc.edc.org/bjc-r/img/2-complexity/ge-ifelse.png) ![a &#x2265; b {report \(not \(a &amp;lt; b\)\)}](https://bjc.edc.org/bjc-r/img/2-complexity/ge-notless.png) ![a &#x2265; b {report \(\(a &amp;gt; b\) or \(a = b\)\)}](https://bjc.edc.org/bjc-r/img/2-complexity/ge-or.png)

Look back at the first two examples in the previous problem. Since the predicate expression a `=` b will report true when they are equal and false otherwise, it's unnecessary to use the nested conditional statement in the first example, and the second example using the predicate inside the `else` part is sufficient. Sometimes, however \(especially when you aren't building a predicate\), it can be helpful to use nested conditional statements.

A **nested conditional statement** is an `if` or `if else` statement inside the `else` part of another `if else` statement. If the predicate of the outer `if else` statement is false, then inner \(nested\) conditional statement will test its predicate and decide what to do.

Describe what this code segment will do.  
![ask \(Is today Tuesday?\) and wait
if \(answer = &apos;yes&apos;\)
{
    say \(Mary Chung&apos;s is closed today.\)
}
else
{
    if \(answer = &apos;no&apos;\)
    {
        say \(Mary Chung&apos;s is open today.\)
    }
    else
    {
        say \(You didn&apos;t answer yes or no.\)
    }
}](https://bjc.edc.org/bjc-r/img/2-complexity/is-today-tuesday.png)

Look back at your code for writing on the stage in three colors. If it doesn't already use a nested conditional statement, copy the code, and create a new version that does.



### Boolean Expressions Experiment



1. Read this script carefully, discuss it with your partner, and make sure you understand why it produces this picture on the stage: ![clear
   pen up
   forever {
       go to \(random position\)
       if \(x position &amp;lt; y position\) {
           set pen color to purple
       } else {
           set pen color to orange
       }
       make a point
   }](https://bjc.edc.org/bjc-r/img/2-complexity/dotscript.png) ![ Imagine a 45-degree line sloping upward toward the right, through the center of the stage. The area up and to the left of this line is purple; the area below and to the right is orange.](https://bjc.edc.org/bjc-r/img/2-complexity/y-gtr-x.png)
2. Changing the Boolean expression in the `if` block changes the picture. Discuss why the expression ![\(x position &amp;gt; 0\) and \(distance to apple &amp;gt; 100\)](https://bjc.edc.org/bjc-r/img/2-complexity/apple-script.png) generates this picture: ![There&apos;s an apple in the center. The entire left half of the stage is orange; so is a circle around the apple. What&apos;s left is purple.](https://bjc.edc.org/bjc-r/img/2-complexity/apple.png)
3. Match the Boolean expressions with the pictures. There are more expressions than pictures. 
   1. ![x position &amp;lt; -100](https://bjc.edc.org/bjc-r/img/2-complexity/x-lt--100-script.png)
   2. ![x position &amp;lt; 100](https://bjc.edc.org/bjc-r/img/2-complexity/x-lt-100-script.png)
   3. ![x position + y position &amp;lt; 100](https://bjc.edc.org/bjc-r/img/2-complexity/x+y-lt-100-script.png)
   4. ![y position &amp;gt; -100](https://bjc.edc.org/bjc-r/img/2-complexity/y-gt--100-script.png)
   5. ![y position &amp;lt; \(-100 - x position\)](https://bjc.edc.org/bjc-r/img/2-complexity/x+y-lt--100-script.png)
   6. ![y position &amp;lt; -100](https://bjc.edc.org/bjc-r/img/2-complexity/y-lt--100-script.png)
   7. ![distance to apple &amp;gt; 100](https://bjc.edc.org/bjc-r/img/2-complexity/dist-gt-100-script.png)
   8. ![x position &amp;gt; -100](https://bjc.edc.org/bjc-r/img/2-complexity/x-gt--100-script.png)
   9. ![y position &amp;gt; \(100 - x position\)](https://bjc.edc.org/bjc-r/img/2-complexity/x+y-gt-100-script.png)
   10. ![\(x position \* y position\) &amp;gt; 0](https://bjc.edc.org/bjc-r/img/2-complexity/xy-gt-0-script.png)
   11. ![\(x position + y position\) &amp;gt; -100](https://bjc.edc.org/bjc-r/img/2-complexity/x+y-gt--100-script.png)
   12. ![\(x position \* y position\) &amp;lt; 0](https://bjc.edc.org/bjc-r/img/2-complexity/xy-lt-0-script.png)
   13. ![y position &amp;gt; \(\(x position ^ 2\) / 100\)](https://bjc.edc.org/bjc-r/img/2-complexity/quadratic.png)
   14. ![direction to apple &amp;gt; 135](https://bjc.edc.org/bjc-r/img/2-complexity/dir-to-apple-gt-135-script.png)
   15. ![y position &amp;lt; 100](https://bjc.edc.org/bjc-r/img/2-complexity/y-lt-100-script.png)
   16. ![y position &amp;gt; 100](https://bjc.edc.org/bjc-r/img/2-complexity/y-gt-100-script.png)
   17. ![Stage divided in fourths by its x and y axes. Top left and bottom right are orange, top right and bottom left are purple.](https://bjc.edc.org/bjc-r/img/2-complexity/xy-gt-0.png)
   18. ![Narrow vertical purple bar at left side of stage, rest of stage orange.](https://bjc.edc.org/bjc-r/img/2-complexity/x-lt--100.png)
   19. ![Apple at center of stage, orange circle around it, and purple everywhere else on stage.](https://bjc.edc.org/bjc-r/img/2-complexity/dist-gt-100.png)
   20. ![Narrow vertical orange bar at left side of stage, rest of stage purple.](https://bjc.edc.org/bjc-r/img/2-complexity/x-gt-100.png)
   21. ![Stage divided in fourths by its x and y axes. Top left and bottom right are purple, top right and bottom left are orange.](https://bjc.edc.org/bjc-r/img/2-complexity/xy-lt-0.png)
   22. ![Narrow horizontal orange bar at top of stage, rest of stage purple.](https://bjc.edc.org/bjc-r/img/2-complexity/y-lt-100.png)
   23. ![Apple at center of stage. The area around the apple on the left side between south \(downward\) and northwest \(up and to the left\) is orange.  The area between south and northwest but on the right is purple.](https://bjc.edc.org/bjc-r/img/2-complexity/dir-to-apple-gt-135.png)
   24. ![Narrow horizontal orange bar at bottom of stage, rest of stage purple.](https://bjc.edc.org/bjc-r/img/2-complexity/y-gt--100.png)
   25. ![The inside of a parabola that is touching the center of the stage and opening upward is purple. The area below the parabola is orange.](https://bjc.edc.org/bjc-r/img/2-complexity/parabola.png)
   26. ![Imagine a 45-degree line sloping downward left to right.  The line hits the left edge of the stage, not quite at the top corner; it hits the bottom edge of the stage about 2/3 of the way from the left.  The area below and to the left of this line is purple; the area above and to the right is orange.](https://bjc.edc.org/bjc-r/img/2-complexity/x+y-lt--100.png)
   27. ![Narrow horizontal purple bar at top of stage, rest of stage orange.](https://bjc.edc.org/bjc-r/img/2-complexity/y-gt-100.png)
4. Compare answers with another pair and resolve any disagreements.
5. On paper, sketch the pictures for the expressions you didn't match with pictures in the previous problem \(without using Snap_!_\).
6. [![Click here to load this file. Then save it to your Snap! account.](https://bjc.edc.org/bjc-r/img/icons/load-save.png)](http://snap.berkeley.edu/snapsource/snap.html#open:https://bjc.edc.org/bjc-r/prog/2-complexity/U2L3-Dots.xml)
7. Invent Boolean expressions you can plug into the dot-picture script to generate these pictures: 
   1. ![The stage is mostly purple, except for a tall orange rectangle at the right edge, going not quite to the top \(so there&apos;s purple above it\).](https://bjc.edc.org/bjc-r/img/2-complexity/x-lt-100-or-y-gt-100.png)
   2. ![The stage is mostly orange, except for a wide purple rectangle in the top left corner, extending about 2/3 of the way to the right.](https://bjc.edc.org/bjc-r/img/2-complexity/x-lt-100-and-y-gt-100.png)
   3. ![Imagine a 45-degree line sloping upward left to right. The line hits the left edge of the stage almost at the bottom and hits the top edge about 2/3 of the way from left to right. The area above and to the left of this line is purple; the area below and to the right is orange.](https://bjc.edc.org/bjc-r/img/2-complexity/x-y-lt--100.png)

