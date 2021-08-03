# Lab - Abstraction - game board

{% embed url="https://bjc.edc.org/Sept2015/bjc-r/cur/programming/2-conditionals-abstraction-testing/3-building-more-complex-blocks/1-abstraction-developing-a-board-game.html?topic=nyc\_bjc%2F2-conditionals-abstraction.topic&course=bjc4nyc\_2015-2016.html&novideo&noassignment" %}



### Abstraction: Developing a Board Game

1. Many board games are played on a square array of tiles. The goal now is to build a block that lets you draw boards with various numbers of tiles, fitting neatly on the stage. For example, ![draw-n-by-n-board\(3\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/draw-n-by-n-board%283%29.png) and ![draw-n-by-n-board\(5\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/draw-n-by-n-board%285%29.png) should draw these boards:

   ![3x3array-of-squares-on-stage](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/3x3array-of-squares-on-stage.png)![5x5array-of-squares-on-stage](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/5x5array-of-squares-on-stage.png)

   The task is complex, so build specialists that accomplish part of the task and then put them together. For example, you might start by building:

   1. ![tile of size \(size\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/tile%28size%29.png), which takes a size and draws one square.
   2. ![row of](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/row%28tiles,size%29.png), which uses ![tile of size \(size\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/tile%28size%29.png) to draw one row of tiles, like this: ![row of 5 tiles](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Row-of-5-tiles.png)
   3. ![nxn-array-of-tiles\(tiles-3,size-100\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/nxn-array-of-tiles%28tiles-3,size-100%29.png), which uses ![row of](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/row%28tiles,size%29.png) to draw as many rows as needed—the same number of rows as there are tiles in each row.
   4. And, ![calculate tile size](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/calculate-tile-size.png) which can be used in ![nxn-array-of-tiles\(tiles-3,size-calculated-to-fit-3-by-3\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/nxn-array-of-tiles%28tiles-3,size-calculated-to-fit-3-by-3%29.png) to make sure the entire board fits. \(In the example, `3 tiles` means three tiles on each row \(and three rows\), not three tiles altogether.\)

   Test each block by itself before building a block that uses it.

   Your top-level board-drawing block, `draw n-by-n board`, might look something like this.

   ![draw an n-by-n board that fits within a 300 by 300 space centered on the stage](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/draw-n-by-n-board%28n%29.png).

   **Abstraction:** Why building the block `clear and go to starting place`, when all it contains is a few commands to assure that the sprite starts in the right place, pointed the right way, with its pen down, and that the stages is cleared?

   One purpose of hiding the details is to make your code clear, understandable, and easy to debug and update. Instead of seeing the details and wondering what they are for, you know exactly what this piece of code does just by reading the block's name.

   The same is true of ![tile of size \(size\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/tile%28size%29.png). Instead of building that block, you could have used  
   ![repeat 4, move, turn](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/rep4-move-turn.png)

2. Hiding those details does
3. 4. _two_
5. 6. useful things. It makes your code easier to read. And if, some day, you decide to create the tiles differently—maybe with thicker borders or fills of random colors or by using
7. 8. ![stamp, from the Pen palette](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/stamp.png)
9. —you can make those changes in a logical place rather than looking all over your program to find where the change might be needed.
10. Now build some tools you might need for a game.
    1. Build a predicate ![on the board?](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/on-the-boardP.png) that uses your `between?` block to report `true` if the sprite is on the board, and reports `false` if the sprite is dragged completely off the board.
    2. Build `which cell?` that tells which cell the sprite has been dragged into. Here is one way to do it that uses two other blocks that specialize in reporting `which column?` and `which row?` the sprite is in.

       ![partial script for &quot;which-cell?&quot; reporter](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/which-cell%28n%29%20without%20computation.png)

       These blocks will, of course, need to know how many rows and columns there were, so they'll need the input `n`.There are many ways to write `which row?` and `which column?` You can, of course, use lots of `if` statements, but since the number of rows can change, it's hard to know how many to use. One convenient way is to divide the total size of the game board by the size of each cell. To use that result, you need to round down. ![round a number](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/round-a-number.png) can do it, but it rounds to the _nearest_ integer, up _or_ down. The function ![floor of number](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/floor%20of%20number.png) always rounds _down_, making it easier to use. The `floor` function is in the same block as `sqrt`.

    3. Here's a block that you can use to test how well your other blocks work together. ![play on n-by-n board](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/play-on-n-by-n-board.png) ![animation of play](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/play-on-n-by-n-board.gif) Try it out for boards of different sizes.
11. Create a block `move to tile (n)` that takes a tile number as input and moves your sprite to the center of that tile. Because the location of tile 9 depends on how many tiles there are, your `move to tile` block will need to know the size of the board.
12. Create `mark tile (n)` to move to the specified tile and ![stamp, from the Pen palette](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/stamp.png) the sprite's shape on that tile to mark it as "taken."
13. Create a second sprite with a different shape so that people can take turns, with their own sprite, stamping its mark on a tile.
14. In Unit 3, you will learn ways to keep track of which tiles have been taken by which player. Then you can improve your game more. It could become like tic-tac-toe, or connect-four, or...

