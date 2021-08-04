# Custom Reporter Blocks

{% hint style="info" %}
#### Reporter blocks return a value
{% endhint %}

So far, all of the blocks you've defined have been "command" blocks. These actual carry out an action that affects the state of the program, but do not return a value. 

For example, the `move` block makes the sprite move, and the `say` block makes the sprite say something. We call these effects "side effects."

Sometimes, we aren't interested in any side effects, and just want a block that performs a calculation for us. These are called "reporters," because rather than causing the program to do something, they simply give us back a value. 

Many blocks on the "operators" palette are reporters. Here are just a few:

![a portion of the &apos;operators&apos;
	palette](https://beautyjoy.github.io/bjc-r/img/building-blocks/some-reporters.png)

Notice how all of these are rounded, and can't be attached directly to other blocks. Because of this, we need to use them in combination with other blocks, like `say` or `set`. For example:![say \(4 + 7\)](https://beautyjoy.github.io/bjc-r/img/cond/say-4-plus-7.png)

## Custom Reporters

Let's take a look at an example:![square\(x\) block definition](https://beautyjoy.github.io/bjc-r/img/building-blocks/square-of-x.png)

This block will take in a parameter `x`, and report `x2`.

Here's a more complex example, using `if`:![homemade absolute value block](https://beautyjoy.github.io/bjc-r/img/building-blocks/homemade-abs.png)

This block is a home-made version of the `abs` \(absolute value\) block that we saw earlier. Notice that it contains two `report` blocks. Reporter blocks can have as many `report`s as you want/need.

## Create a Custom Reporter - max

Let's try writing our own reporter block!  We will make a block called `max` that takes two numbers as input and reports the bigger value \(the maximum\).

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

## Extra Challenge

Create the following two blocks. 

* **Add Numbers** - A three-argument addition operator that only accepts numbers.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-27.png)

* **Join** - A three-argument `join` operator that has the default values shown below and only accepts text.

![Dialog](http://bjc-nc.github.io/bjc-course/curriculum/03-build-your-own-blocks/labs/lab-block-28.png)

Here's a more complex block. Predict what it will report when run with inputs "hello" and 5.

![mysterious block definition](https://beautyjoy.github.io/bjc-r/img/building-blocks/join-word-n-times.png)

