# Input Types

The `max` block has an unexpected behavior. We wanted it to work only for numbers. Yet, you can type text into it!  
![Max can also take text](https://beautyjoy.github.io/bjc-r/img/prog/max-of-cat-dog-output.png)  
  


To remedy this behavior we can specify the input type that should be used in our block. Now we are going to limit the `max` block to accept only numbers as arguments.

1. Open the `Block Editor` for the `max` block and click on the input `x`. ![Editing input &apos;x&apos;](https://beautyjoy.github.io/bjc-r/img/sys/edit-input-variable-x-BYOB.jpg)
2. 3. Then, click on the right arrow in the pop-up box shown above. This will open the dialog box shown below. This allows us to specify the shape of the slot. We want a numbers-only slot \(as shown selected below\). We can also specify that we want the variable to have a _default_ value; this is similar to blocks like `move` that always start out with the default value `10`. ![Input Type](https://beautyjoy.github.io/bjc-r/img/prog/x-long-dialog.png) 
4. 5. Modify both the `x` and `y` variables to take only numbers and to have the default values of `5` and `10`, respectively. Your `Block Editor` should then look like this, with the default values shown in the header. ![Default Values](https://beautyjoy.github.io/bjc-r/img/prog/max-defaults.png) 
6. 7. When you click `OK`, you should be able to see your block in the `Operators` tab, with the default values filled in. Also, note that you will no longer be able to enter text. ![&apos;max&apos; block with defaults](https://beautyjoy.github.io/bjc-r/img/prog/max-of-5-and-10.png) 

_Note_: Even if we specify an input type for a block it could still receive improper values when a variable is passed in as its argument \(Snap_!_ won't constantly check if the variable's type is the same as the block's input type\). As such, input types should only be used as an organizational tool to keep you thinking about what the domain \(input values\) of your blocks should be.

