# Variables

### What are Variables?

Variables are named spaces in memory that your program can access. You can set and modify the values that are contained in these named spaces. To visualize a variable’s name space think of mail slots in a large mail room. Your computer has memory that the program is going to use to create and store information. When you create a variable, you are assigning one of the “slots” of memory to a name and then can put a value in that slot and modify it as needed.

![](../.gitbook/assets/19%20%281%29.png)

### Why create variables? 

Variables allow the programmer to make the value modifiable in the script. For example, you want to be able to update a score variable as the player wins/loses in a game. You will see many different uses of variables during this course.

You have multiple blocks to create and manipulate variables in the Variables tab palette.

![](../.gitbook/assets/20.png)

* **Make a variable button** allows you to create a new variable
* **Delete a variable button** will allow you to delete a button – this button only shows after you have created a variable.
* **Set \[variable name\] to \(0\)** will allow you to initialize, or set a beginning value, the variable to a value.
* **Change \[variable name\] by \(1\)** allows you to modify the value of a variable
* **Show variable \[variable name\]** will show the variable and value on the stage.
* **hide variable \[variable name\]** will hide the variable and value on the stage.
* **Script variables \(a\)** will allow you to create local variables, more on this use later

### To create a variable

* In the box that pops up - type the name of the variable. The default selection “for all sprites” means that all sprites have access to this variable. Select “for this sprite only” if you want only the sprite currently selected to be able to access/modify the value of the variable.

![](../.gitbook/assets/21.png)

* Now you’ll have blocks to use for your variable.
* Note that you now have a rounded button with the name of the variable in the window with a checkbox to the left. If checked, the variable and value will be show on the stage. Uncheck to hide.
* When you use one of the variable blocks you will be able to click on the combo box arrow for a list of your variables.

![](../.gitbook/assets/22.png)

#### Initializing Variables Example

The **set** command block is used to initialize a variable, not to update its value.

![](../.gitbook/assets/image%20%2877%29.png)

#### Updating/Changing Variables Example

The **change** command block is used to change the value of a variable. The script below initializes the value of the beat variable to 2 and then changes it at the end of each loop.

![](../.gitbook/assets/image%20%281%29.png)

## Script Variables

Sometimes you need a variable in your script, but you don’t want it to step through consecutive integer values as in the for block. A more general way to handle variables uses the block

![](../.gitbook/assets/23%20%282%29.png)

to create a variable, and the block

![](../.gitbook/assets/24%20%281%29.png)

to give that variable a value. Both of these blocks are in the Variables palette. Here’s an example:

![](../.gitbook/assets/25%20%281%29.png)

The script variables block creates a variable called sides \(click on the orange “a” to change the name\) that can be used throughout this script. \(Each time you click the green flag, a new variable is created, and it exists only during that time through the script.\) 

The set block says what value the variable should have. In this case, Snap! will pick a random integer value between 3 and 10 \(inclusive\). \(The pick random block is in the Operators palette; note that we changed the first input from 1 to 3.\) 

The script will draw a regular polygon with that number of sides. The value of sides is used twice, first in the repeat block to say how many times the move-and-turn combination should be done, and again in computing the angle through which to turn for each side.

We needed the script variable in this script because the randomly chosen number is used twice. If it had been used only once, we could have put the pick random block directly in the script, like this:

![](../.gitbook/assets/26.png)

## Global Variables

Sometimes it’s not good enough to remember a value inside one script. Instead, you need the value available everywhere in your project. The classic example is the score in a video game; even when no script is running, the score should be remembered.

There was a time, in the early history of programming languages, when all variables were global. This led to a lot of bugs, because different parts of the program would use the same name for different purposes and erase each others’ saved values. So don’t use global variables as your first choice; think whether a script variable or a for block \(which makes a variable local to just that block\) would work instead.

To make a global variable, you must go to the Variables palette and click on the Make a variable button \(not a block – you can’t put it into a script!\):

![](../.gitbook/assets/27.png)

You will be prompted to give your variable a name. After you do that, you’ll see an orange variable oval in the Variables palette:

![](../.gitbook/assets/28.png)

This can be dragged into scripts just like the orange variable ovals in the for block and the script variables block.

The checkbox to the left of the variable block determines whether or not the value of the variable is displayed on the stage. The variable watcher \(which is what that display is called\) can be useful for debugging, or can be displayed permanently so that the user of your project can see the score, or whatever you have in the variable. By right-clicking on the watcher, you can change the format in which it appears on the screen.

When you make a global variable, you also get a “Delete a variable” button that can be used for the obvious purpose.





### Script Variables

You have used variables that the `for` block _gave_ you. ![squiral script](https://bjc.edc.org/Sept2015/bjc-r/img/looping/squirral-script.png)

You also _created_ variables ![plural-hat-block-and-first-line-only](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/plural-hat-block-and-first-line-only.png) as inputs to blocks that you made.

A script variable exists only while the script is running.Sometimes you will need _extra_ variables to store information temporarily while your script is running. The ![script variables](https://bjc.edc.org/Sept2015/bjc-r/img/prog/scriptvar.png) block lets you do that.

1. Watch the video \(or read the instructions that follow it\) to see how to create, name, and set the value of a script variable.

   ![movie showing how to choose the name of a script variable and set its initial value](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/ScriptVariables.gif)

   1. To create the variable, use ![script variables](https://bjc.edc.org/Sept2015/bjc-r/img/prog/scriptvar.png) \(in the variables tab, of course\).
   2. To name the variable, click on the orange _`a`_ and type the name you want.
   3. To set your variable's value, use ![set](https://bjc.edc.org/Sept2015/bjc-r/img/prog/set.png). The down-arrow lets you select the variable you want \(in this example, there's only one variable to choose\).
   4. Then set its value.

2. This script draws polygons with a random number of sides.

   ![random polygon script](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Random-Polygon-script_372x300.png)This script uses the value of `sides` twice, once in the `repeat` block to say how many times the `move`-and-`turn` combination should be done, and once in computing the angle to `turn`.

   1. Make the script and run it several times to see what it draws.
   2. **Check your understanding:** Why does it make sense to start the range of possible random numbers at 3?
   3. **Check your understanding:** Where did the formula ![360/sides](https://bjc.edc.org/Sept2015/bjc-r/img/prog/360-over-sides.png) come from?

3. **Challenge:** Modify the script so that it also picks a _size_ randomly, from 30 through 60 using _only multiples of 10_.There are two ways to create a second script variable. You could use another `script variables` block ![script-variables-sides-script-variables-size](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/script-variables-sides-script-variables-size.png) or you could extend the one block, using the right-arrow ![adding a second script variable](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/second-script-variables-movie.gif)"U2Lab2Polygons"![save your work as U2Lab2Polygons](https://bjc.edc.org/Sept2015/bjc-r/img/icons/save-this-as.png)
4. **Analyzing and debugging:** Instead of setting a script variable, this script just uses the `pick random` block in the two places that need the random number. Before you build and run this script, try to figure out what is likely to go wrong. ![buggy random polygon](https://bjc.edc.org/Sept2015/bjc-r/img/prog/bad-random-poly.png)



