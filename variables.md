# Variables

### What is a Variable? <a id="different-kinds-of-variables"></a>

* A variable is a named space in memory. 
* Think of a mailroom with a large wall of slots for the mail as your memory. 
  * This is very simplified of course. 
* Each of these slots would be assigned to a variable \(by its name\) and would hold the values assigned.

![](.gitbook/assets/image%20%2839%29.png)

### Adding Variables

* You can add variables to your program to increase its flexibility. 
* The variable allows you to change a value as the script runs. 
* To add a variable, select the Variables palette, then click on the **Make a Variable** button.

![](.gitbook/assets/image%20%28108%29.png)

### Creating a Variable <a id="different-kinds-of-variables"></a>

When you click on the Make a Variable button, the Variable Name window will open.

Note you can create the variable for the active sprite only \(called a local variable\) or for all sprites \(called a global variable\).

![](.gitbook/assets/image%20%2823%29.png)

### Variable Blocks <a id="different-kinds-of-variables"></a>

You have multiple variable blocks.

Note: Checking the checkbox beside a variable name will display the value of the variable on the stage. \(only visible when there is a variable.\) 

* **set \[variableName\] to \(\)** - sets the value 
* **change \[variableName\] by \(\)** - changes the value
* **show variable \[variableName**\] - displays the value on the stage. 
* **hide variable \[variableName\]** - displays the value on the stage. 
* **script variables \(a\)** - creates local variables

#### Initializing Variables Example

The set command block is used to initialize a variable, not to update its value.

![](.gitbook/assets/image%20%2870%29.png)

#### Updating/Changing Variables Example

The change command block is used to change the value of a variable. The script below initializes the value of the beat variable to 2 and then changes it at the end of each loop.

![](.gitbook/assets/image%20%281%29.png)

### Different Kinds of Variables <a id="different-kinds-of-variables"></a>

We’ve seen a lot of different types of variables.

* **Normal/Global variables**: These variables are made in the regular menu and can be used ANYWHERE! The variable “score” below is an example. _These can be used by any sprite, in any block or in any script_.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-33.png)

* **Sprite Specific Variables**: When you create a “normal/global” variable you can select that the variable is “For this sprite only”. Then these variables will show up as variables listed below the line in the variables tab. _We recommend not using these variables in blocks._

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-34.png)

* **Arguments to a function**: A variable set by the person calling the function. We also refer to this as “input”. _This can ONLY be used within the block editor._

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-35.png)

* **Script Variables**: The “script variable” block gives us a variable that we can use inside of this script. _These can only be used in that particular script. The script could be a block script \(shown below\) or a regular script._

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-36.png)

