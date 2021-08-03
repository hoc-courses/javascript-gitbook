# Lab - Predicates

**In this lab,** you will review predicates and build a few that you can use in other projects.

As you know, predicates are reporter blocks \(functions\) that always report a _Boolean value_ \(they report only the values ![true](https://bjc.edc.org/bjc-r/img/blocks/true.png) or ![false](https://bjc.edc.org/bjc-r/img/blocks/false.png)\).

In Snap!, predicates are represented by hexagonal blocks. **They compute the** _**condition**_ **used by** _**conditionals**_ \(such as `if`, `if else`, or `repeat until`\) to decide when to do something.

Predicates ask a true/false question such as "Is this sprite touching the sprite called 'Leader'?"

![](../.gitbook/assets/image%20%2889%29.png)

 Use one or more of the following _relational operators_ to create a script that lets you use your mouse to write on the stage in two colors depending on the mouse's position on the stage.  
![less than, equal to, and greater than predicate blocks](https://bjc.edc.org/bjc-r/img/2-complexity/relations.jpg)

 Make the sprite draw only if the mouse button is down, so that you can draw disconnected shapes. You'll need to uncheck the "draggable" box above the scripting area before you try this \(so that Snap! doesn't think you are trying to drag the sprite when you click\).

![](../.gitbook/assets/image%20%28117%29.png)

  
You'll probably want to use the ![mouse down? predicate block](https://bjc.edc.org/bjc-r/img/blocks/mouse-down.png) block, which you can find in the Sensing palette.

![bicolor printed hello](https://bjc.edc.org/bjc-r/img/2-complexity/bicolor-hello.png)

#### Boolean Functions

At the very lowest level, computer circuitry is made of wires, and each wire is either on or off. So the only operations that can be performed at that lowest level are those that _operate on single-bit values_ \(just ones and zeros, that is, just ons and offs\). These are called _logical \(or Boolean\) functions_. There are three Boolean functions in the Operators palette:

  
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

Make the blocks ![less than or equal](https://bjc.edc.org/bjc-r/img/blocks/less-than-or-equal.png), ![greater than or equal](https://bjc.edc.org/bjc-r/img/blocks/greater-than-or-equal.png), and ![\(\) not equal \(\)](https://bjc.edc.org/bjc-r/img/2-complexity/not-equal.png). 

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



### Boolean Expressions Experiment

Read this script carefully, and make sure you understand why it produces this picture on the stage:  
![clear
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

Changing the Boolean expression in the `if` block changes the picture. Discuss why the expression ![\(x position &amp;gt; 0\) and \(distance to apple &amp;gt; 100\)](https://bjc.edc.org/bjc-r/img/2-complexity/apple-script.png) generates this picture:  
![There&apos;s an apple in the center. The entire left half of the stage is orange; so is a circle around the apple. What&apos;s left is purple.](https://bjc.edc.org/bjc-r/img/2-complexity/apple.png)

Match the Boolean expressions with the pictures. There are more expressions than pictures.

![](../.gitbook/assets/image%20%2837%29.png)





### Building a Useful Collection of Predicates

Some tests—for example, a test to see if a number is even or if a letter is a vowel—are needed so often that you won't want to re-create them each time you need them. In this activity, you will create a set of tools that you may use often, especially for complicated programming tasks.

You've already built a predicate `vowel?` to test for vowels and a predicate to test for even numbers. Snap has a built-in test to see if something is a number, but not a test to see if the number is an integer, and often you will want that.

1. Snap has a "greater than" operator \(`>`\), an "equal" operator \(`=`\), and a "less than" operator \(`<`\) built in, but doesn't have a "greater than or equal to" \(`>=`\) operator.

   ![5 &amp;gt;= 3](https://bjc.edc.org/Sept2015/bjc-r/img/prog/5ge3.png)![5 &amp;gt;= 5](https://bjc.edc.org/Sept2015/bjc-r/img/prog/5ge5.png)![3 &amp;gt;= 5](https://bjc.edc.org/Sept2015/bjc-r/img/prog/3ge5.png)

   Build ![a greater than or equal to b](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/a-greater-than-or-equal-to-b.png) and test it well to make sure it does what you expect.

   ![creating an infix predicate](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/creating-an-infix-predicate.gif)

   * When you type the block's title in the **Make a block** dialog, choose the hexagonal _predicate_ block shape.
   * To set the block's name `>=` between the two input slots, use the left plus sign in the Block Editor. ![left plus sign](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/left-plus-sign.png)
   * You may find one or more of these Boolean operators helpful:

     ![and, or, not blocks](https://bjc.edc.org/Sept2015/bjc-r/img/prog/Booleans.png)

   There are several correct ways to do this! As long as your block gives the right `true` and `false` answers, it's correct.

 Operators like ![a times b](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/a-times-b.png) that stand in between their two inputs are called _infix_ operators. Operators like ![sqrt of](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/sqrt%20of%20120%C2%A0%C3%97%C2%A028%20pixels.png) that stand before their inputs are called _prefix_ operators. When we write _n_! to mean "_n_ factorial," the "!" is a _postfix_ operator—it comes after its input ![n factorial](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/postfix%20factorial%2047%C2%A0%C3%97%C2%A027%20pixels.png) In Snap, it is possible to mix the types, as you will do in the next problem.

1. Build a predicate that tests to see if its input is an integer. ![integer?-4=\(with-result-true\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/integer-4%28with-result-true%29.png) ![integer?-4-point-1\(with-result-false\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/integer-4-point-1%28with-result-false%29.png)

   You may find ![round a number](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/round-a-number.png) useful.

2. Build a block that tells whether a given number is between two other given numbers. ![number-between-two-others\(with-result-false\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/number-between-two-others%28with-result-false%29.png) ![number-between-two-others\(with-result-true\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/number-between-two-others%28with-result-true%29.png). You can decide whether "between," for your purposes, will _include_ the two boundary numbers or not.
3. Write a ![weekend?](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/weekend.png) block that reports whether a given day is a weekend. Let's assume that only Saturday and Sunday are part of the weekend.
4. Write a ![weekday?](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/weekday.png) block. You could write this without your ![weekend?](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/weekend.png) block, but it'll be much easier \(and cleaner code!\) if you use ![weekend?](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/weekend.png) as part of this new block.

