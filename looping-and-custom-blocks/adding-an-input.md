# Adding an Input



You have created a block that draws a square, but only a square in which each side is of length `100` steps. It would be better if you could specify how long you wanted each side to be.

Edit the block to accept an _input_ \(or _argument_\), which tells it the length of the square it has to draw:

1. Right-click or control-click on the new block \(either in the palette or in a script\) and select `edit` to go back to the block editor.![Editing the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/sys/edit-current-block.png)
2. In the `Block Editor`, hover your cursor over the words and plus signs \(**`+`**\) in the top block. \(This top block is called a "hat" block because of the curved top. Hat blocks can never be in the middle of a script, only at the top\).

   Clicking on a word will let you change that word; clicking on a **`+`** will let you add something in that position. We want to add an input at the end of the block, so click on the **`+`** at the end.![draw square editor](https://beautyjoy.github.io/bjc-r/img/sys/draw-square-block-editor.png)

3. You should get the following dialog box.![Adding an argument to the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/sys/add-argument-in-block-signature.png)

   You have two choices about what you want to add or modify to the block definition:

   1. `Title text` \(unselected in the picture above\) will let you add a word or words to the block's title. For example, if you wanted to change the name of the block from `draw square` to `draw square picture` you'd click on 'Title text' and type the word "picture" into the text box.
   2. `Input name` \(selected in the picture above\) will let you add an input. This is the choice we want here, and will by default be selected when you open this dialog.

   We want to add an input named `size` to our block definition. Type "size" in the input field and click `OK` \(since `Input name` is selected already\).

4. Your block title has changed: there is now a variable named `size` at the end of the title.![New variable in the &apos;draw square&apos; block](https://beautyjoy.github.io/bjc-r/img/building-blocks/draw-square-size-unused-argument.png)
5. In order to use the `size` variable within the `draw square` block, drag the variable `size` down into the move block. Whenever you need a new copy of a variable, just drag another down. \(If you have extra copies you want to get rid of, you can drag the copy all the way to the palette at the left of the Snap_!_ window.\)  Snap_!_ will determine the value of the `size` variable automatically for you whenever you use the `draw square` block in a program.![Adding a variable to the body](https://beautyjoy.github.io/bjc-r/img/building-blocks/draw-square-size-pull-argument.gif)
6. When you click `OK`, you'll see that the `draw square` block in the scripting area now takes an argument. You can put different numbers in the blank and draw squares of different sizes.![Running the &apos;draw square&apos; block with an argument](https://beautyjoy.github.io/bjc-r/img/prog/draw-square-block-with-arg-BYOB.gif)

