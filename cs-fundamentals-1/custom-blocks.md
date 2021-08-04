# Custom Command Blocks

{% hint style="info" %}
#### Command blocks perform an action but do not return a value.
{% endhint %}

We are going to teach the computer how to draw a square using a block named `draw square`. Please follow the steps below:

Click on `make a block` at the bottom of the `Variables` palette \(or right-click or control-click on the scripting area background and choose "`make a block`"\).![&apos;make a block&apos;](https://beautyjoy.github.io/bjc-r/img/sys/MakeABlock-BYOB.jpg)

This will open up the `Make a block` dialog box. There are several steps that you'll do here, corresponding to each area of the dialog. Now, you get to choose which tab the block should go into. Our block is going to draw a square, so let us choose `Motion`. \(Note: A very common mistake is to omit this step. If you do forget, your block will become a gray Other block, in the Variables palette.\)

![&apos;make a block&apos; dialog box](https://beautyjoy.github.io/bjc-r/img/sys/make-a-block-BYOB.png)

First, at the top of the dialog, you should select in which palette the block will be place. This block is going to draw a square, so choose `Motion`. The `Motion` tab should highlight in blue, as in the picture below.

Second, you'll want to enter a title for the block in the edit field. Type `draw square`, which should show up as in the picture below.

Third, you have the option of making blocks of different shapes, corresponding to the `Command`, `Reporter`, and `Predicate` icons. By default the `Command` icon is selected, and this is the one you want. \(You will learn about the other shapes of custom blocks in the next topic\).

Fourth, there are two radio buttons that you can safely ignore. You will almost always want to keep `for all sprites` selected in this course.

![Make a command block](https://beautyjoy.github.io/bjc-r/img/sys/make-draw-square-block.png)

Click `OK`.

After you click `OK`, a dialog titled `Block Editor` will appear.

![Block Editor for &apos;draw square&apos;](https://beautyjoy.github.io/bjc-r/img/prog/empty-draw-square-BYOB.png)

Inside the you will see a specially shaped block with the title of the custom block that you are creating. This kind of block is called a "hat" block, and it indicates a starting place for the `draw square` script.

You can treat this dialog like you do the scripting area of the main Snap_!_ window. Drag blocks here from the palette to define the script that will run when your custom block is used.

1. Use the blocks from the Control and Motion palettes to create a script that draws a square, as shown below.![Script to draw a square](https://beautyjoy.github.io/bjc-r/img/building-blocks/draw-square-no-arguments.png)
2. When you click `OK`, you should be able to use this block as if it were a regular block. Since you created the block as a `Motion` block, it will end up at the bottom of the `Motion` tab.![Using the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/prog/draw-square-block-BYOB.gif)

Congratulations! You have just created your first custom block.

## Adding an Input 

You have created a block that draws a square, but only a square in which each side is of length `100` steps. It would be better if you could specify how long you wanted each side to be.

Edit the block to accept an _input_ \(or _argument_\), which tells it the length of the square it has to draw:

Right-click or control-click on the new block \(either in the palette or in a script\) and select `edit` to go back to the block editor.![Editing the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/sys/edit-current-block.png)

In the `Block Editor`, hover your cursor over the words and plus signs \(**`+`**\) in the top block. \(This top block is called a "hat" block because of the curved top. Hat blocks can never be in the middle of a script, only at the top\).

Clicking on a word will let you change that word; clicking on a **`+`** will let you add something in that position. We want to add an input at the end of the block, so clickon the **`+`** at the end.

![draw square editor](https://beautyjoy.github.io/bjc-r/img/sys/draw-square-block-editor.png)

You should get the following dialog box.![Adding an argument to the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/sys/add-argument-in-block-signature.png)

You have two choices about what you want to add or modify to the block definition:

1. `Title text` \(unselected in the picture above\) will let you add a word or words to the block's title. For example, if you wanted to change the name of the block from `draw square` to `draw square picture` you'd click on 'Title text' and type the word "picture" into the text box.
2. `Input name` \(selected in the picture above\) will let you add an input. This is the choice we want here, and will by default be selected when you open this dialog.

We want to add an input named `size` to our block definition. Type "size" in the input field and click `OK` \(since `Input name` is selected already\).

1. Your block title has changed: there is now a variable named `size` at the end of the title.![New variable in the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/building-blocks/draw-square-size-unused-argument.png)
2. In order to use the `size` variable within the `draw square` block, drag the variable `size` down into the move block. Whenever you need a new copy of a variable, just drag another down. \(If you have extra copies you want to get rid of, you can drag the copy all the way to the palette at the left of the Snap_!_ window.\)  Snap_!_ will determine the value of the `size` variable automatically for you whenever you use the `draw square` block in a program.![Adding a variable to the body](https://beautyjoy.github.io/bjc-r/img/building-blocks/draw-square-size-pull-argument.gif)
3. When you click `OK`, you'll see that the `draw square` block in the scripting area now takes an argument. You can put different numbers in the blank and draw squares of different sizes.![Running the &apos;draw square&apos; block with an argument](https://beautyjoy.github.io/bjc-r/img/prog/draw-square-block-with-arg-BYOB.gif)

## Adding a Second Input

Now, you are going to make a block that takes two inputs.

We want to create a `draw polygon` block that takes as inputs:

1. a number of sides and
2. the length of each side.

![draw polygon \(\) sides of length \(\)](https://beautyjoy.github.io/bjc-r/img/prog/polyblock.png)

In the block, call these inputs `sides` and `length`. 

You should remember from the previous lesson how to draw a regular polygon. How many degrees altogether? How many turns?

Be sure to test out your solution with several polygons, with different lengths and number of sides.

## Composition of Blocks

You can treat your custom-made blocks like any other block in snap, including using them within other block you define. In fact, bigger programming tasks are usually best solved by writing simple blocks that are used within slightly more complicated blocks, which are in turn used in even more complicated blocks, and so on.

We'll look more closely at this sort of composition of blocks in a later topic, because it is important.

For now, remember the ![](https://beautyjoy.github.io/bjc-r/img/blocks/draw-square-empty-parameter.png) block? Use it to create a block that draws the petals of a flower, like:![flower with 6 square petals](https://beautyjoy.github.io/bjc-r/img/drawing/flower-with-6-square-petals.png)

If you look this flower, you'll see it has 6 squares drawn at equal angles around a full 360-degree rotation.

Create the block  
![block: draw square-leaved flower with \[\] leaves of size \[\]](https://beautyjoy.github.io/bjc-r/img/drawing/draw-square-leaved-flower-empty-paramters.png)  
that will draw a square-leaved flower with any number of square-shaped petals with the specified size. In this block, you will turn the sprite between calls to `draw square` in a way similar to that in the `draw polygon` blocks: using an angle of ![360 divided by the number of leaves](https://beautyjoy.github.io/bjc-r/img/drawing/calculating-turn-angle-for-draw-flower.png). 

An invocation of ![block: draw square-leaved flower with 6 leaves of size 50](https://beautyjoy.github.io/bjc-r/img/drawing/draw-square-leaved-flower-6-50-parameters.png) should draw the example picture above.

## Compose a draw flower Block

Write a block that draws a full flower in the middle of the stage.![draw a flower block](https://beautyjoy.github.io/bjc-r/img/drawing/draw-a-flower.png)

Write simple custom blocks, or borrow from blocks you have already written, and then use those blocks inside your `draw a flower` block. If you can, write blocks of intermediate complexity that use and are used by other blocks you write.  
  
You might write:  
  
     `draw flower head with ...`  
  
     `draw stem with length []`  
  
but don't feel constrained by this list.

Use several inputs that control aspects of what the flower should look like. You might change the number of petals, the size of the petals, the shape of the petals, or something else!

After you've worked on this for a bit, take a moment to look at what other students have done and chat. If you see something nice, spend some time trying to incorporate that design into your program.

## Test for Understanding

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/functions/intro/buggy-house-and-square.html?1&2&3&4&topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## Creating Command Blocks That Use If and If-Else

Let's try making a few more blocks that use if and if-else.

* Make a ![traffic signal \(\)](https://beautyjoy.github.io/bjc-r/img/cond/traffic-signal.png) block that when given a light color, makes the sprite say the appropriate action. For example ![traffic signal \(&apos;green&apos;\)](https://beautyjoy.github.io/bjc-r/img/cond/traffic-signal-green.png) should say "go!"
* Make a ![letter grade \(\)](https://beautyjoy.github.io/bjc-r/img/cond/letter-grade.png) block that takes in a percentage and makes the sprite say the associated letter grade. For example, ![letter grade \(74\)](https://beautyjoy.github.io/bjc-r/img/cond/letter-grade-74.png) should say "C."
* Make a ![state of water \(\)](https://beautyjoy.github.io/bjc-r/img/cond/state-of-water.png) block that takes in a temperature and says whether water will be liquid, solid, or gas.

