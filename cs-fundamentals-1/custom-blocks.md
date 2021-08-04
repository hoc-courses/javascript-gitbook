# Custom Blocks

## What is a Custom Block? 

In most programming languages, we can take individual instructions and put them in a new code block that we can define. Different languages call them by different names. Some languages call procedures _**methods**_ ****or _**functions**_. Snap! calls them blocks. Snap! as a large repository of built-in code blocks and also lets you define your own.

A **code block** is a named sequence of instructions that may take inputs and may return a value. 

* Code blocks perform a function for us.
* We can create our code block once and use it as many times as we want without having to re-write the code. 
* We only need to “call” or “invoke” it. 
* This is called **Procedural Abstraction**.

There are three categories of code blocks in Snap!:

* **commands** -  tells the computer to do something without returning a value.
* **reporters** - returns a value.
* **predicates** - a type of reporter, returns either true or false

## Our First Custom Block 

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

