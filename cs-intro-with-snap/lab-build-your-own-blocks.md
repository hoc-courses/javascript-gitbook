# Lab - Make Your Own Blocks

We are going to teach the computer how to draw a square using a block named `draw square`. Please follow the steps below:

* Click on M**ake a block** at the bottom of the variables tab.

![Button](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-1.png)

* This will open up the `Make a block` dialog box. Now, you get to choose which tab the block should go into. Our block is going to draw a square, so let us choose `Motion`.  \(Note: A very common mistake is to omit this step. If you do forget, your block will become a gray Other block in the Variables palette.\)

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-2.png)

* When we selected `Motion`, the block became blue. 
* We now have the option of making blocks of different shapes. Right now, however, we are just going to make a \(regular\) command block, because our block is not going to return a value.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-3.png)

* When we click `OK`, we should see the block editor below.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-4.png)

* Use the blocks from the regular menus to create a script that draws a square, as shown below.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-5.png)

* When you click `OK`, you should be able to use this block as if it were a regular block. Since you created the block as a `Motion` block, it will end up at the bottom of the `Motion` tab.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-6.png)

Congratulations! You have just created your own block!

### Improving the draw square block <a id="improving-the-draw-square-block"></a>

You have created a block that draws a square, but it only draws a square where each side is of length `100` steps. It would be great if we could specify how long we wanted each side to be. We will edit the block to accept an _argument_ \(or _input_\), which tells it the length of the square it has to draw.

* We are going to go back and edit the block. Right-click on the new block and select edit to go back to the block editor.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-8.png)

* In the `Block Editor`, notice that when you move the mouse over the top row of the new block, some plus signs \(+\) show up. When you click on these plus signs, you can add more text or arguments. When you click on the text between the plus signs, you can delete or modify that text. Click on the plus sign at the far right as shown below:

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-9.png)

* When you click on the plus sign on the far right, you should get the following dialog box. With this dialog box, we can select if we want to add input \(orange\) or more text \(blue\). We want to add the input `size`, so we type `size`, select `Input Name` and click `OK`.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-10.png)

* Now, we have a variable inside our block definition.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-11.png)

* Drag the variable `size` down into the move block. Whenever we need a new copy of a variable, we just grab the copy from that variable in the top row.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-12.png)

* When we click OK, we will see that our draw square block now takes an argument. We can put different numbers in the blank and draw squares of different sizes!

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-14.png)

### The Max block <a id="the-max-block"></a>

We will now make a different kind of block ??? a _**reporter**_ ****block. To demonstrate this, we will make a block called `max` that takes two numbers as input and reports the bigger value \(the maximum\).

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-16.png)

* Click `Make a block` and select the `Operators` tab. We want a reporter block. This will give the block its round shape as shown above. As the name implies, reporter blocks can report a value. In the image below, you can see that we used the % shortcut for making input variables.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-17.png)

* This should give you a blank Block editor. We need to figure out what should be reported. To keep track of the value to be reported, we are going to make another variable. 
* There are two ways to do this: Use a `Script Variable` block. You can click on the name of the variable and change it to bigger value. Alternatively, you can just report which of the two is larger.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-18.png)

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-19.png)

### Input Types <a id="input-types"></a>

Unfortunately, we have a bug with our `max` block! We wanted the `max` block to work only for numbers. Yet, you can type text in!

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-20.png)

We are going to limit the `max` block to accept only numbers as arguments.

* Open the Block Editor for the `max` block and click on the input `x`

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-21.png)

* Then, click on the right arrow in the pop-up box shown above. This will open the dialog box shown below. This allows us to specify the shape of the slot. We want a numbers-only slot \(as shown selected below\). We can also specify that we want the variable to have a _default_ value; this is similar to blocks like move that always start out with the default value 10.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-22.png)

* Modify both the `x` and `y` variables to take only numbers and to have the default values of `5` and `10`, respectively. Your `Block Editor` should then look like this, with the default values shown in the header.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-23.png)

* When you click OK, you should be able to see your block in the Operators tab, with the default values filled in. Also, note that you will no longer be able to enter text.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-24.png)

### Composition of Functions <a id="composition-of-functions"></a>

Our custom-made blocks are blocks like any other, and we can use them in other block definitions. To demonstrate this, we are going to make a block that computes the maximum of three values

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-25.png)

Repeat the steps from the last tutorial to make this version of the `max` block also only take numbers. Then, in the script for the block, we can use two copies of our `max` block.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-26.png)

### Lab Exercise <a id="try-it-addnumbers-and-jointext"></a>

Your challenge is to create the following two blocks. You can use the same project file.

* **Add Numbers** - A three-argument addition operator that only accepts numbers.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-27.png)

* **Join** - A three-argument `join` operator that has the default values shown below and only accepts text.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-28.png)

### Predicates <a id="predicates"></a>

We want to make our own predicate, a kind of block that reports either `true` or `false`. We have a ???greater than??? operator `>`, an ???equal??? operator `=`, and a ???less than??? operator`<`, but we want a new ???greater than or equal to??? `>=` operator.

* We will create the new block and select the `predicate` shape.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-29.png)

* This gives a `Block Editor` that has a predicate-shaped blank at the bottom. There, we need to place the predicate that we want to report.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-30.png)

* We can fill that in with a composition of a ???greater than???, ???or???, and ???equal??? operators. Make this and then try it out. Notice that this predicate block reports either `true` or `false`.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-31.png)

### Make a between block <a id="try-it-predicates-make-a-between-block"></a>

Create a new predicate block that determines if a number is between two other numbers. The block should return `true` if the first number is between the two numbers or if it is equal to either of the numbers.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-32.png)

\*\*\*\*

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-36.png)

### Simplifying a tic-tac-toe board drawer using functions <a id="try-it-simplifying-a-tic-tac-toe-board-drawer-using-functions"></a>

When drawing a square, we used a `repeat` block to avoid duplicating code. Similarly, we can use a function to avoid duplicating code. Below is some code to draw a tic-tac-toe board. Your goal is to create functions \(code blocks\) that make this code simpler. One important thing to keep in mind is to give your new functions really intuitive names, so that it is easy to read the code and understand what it does.

Using the blocks below, create two new function blocks, draw line and next line, to draw the tic-tac-toe board. You will still have some of the code from the original script. You can create additional blocks for those functions.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-37.png)

