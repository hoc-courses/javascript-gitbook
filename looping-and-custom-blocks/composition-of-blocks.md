# Composition of Blocks

You can treat your custom-made blocks like any other block in snap, including using them within other block you define. In fact, bigger programming tasks are usually best solved by writing simple blocks that are used within slightly more complicated blocks, which are in turn used in even more complicated blocks, and so on.

We'll look more closely at this sort of composition of blocks in a later topic, because it is important.

For now, remember the ![](https://beautyjoy.github.io/bjc-r/img/blocks/draw-square-empty-parameter.png) block? Use it to create a block that draws the petals of a flower, like:![flower with 6 square petals](https://beautyjoy.github.io/bjc-r/img/drawing/flower-with-6-square-petals.png)

If you look this flower, you'll see it has 6 squares drawn at equal angles around a full 360-degree rotation.

Create the block  
![block: draw square-leaved flower with \[\] leaves of size \[\]](https://beautyjoy.github.io/bjc-r/img/drawing/draw-square-leaved-flower-empty-paramters.png)  
that will draw a square-leaved flower with any number of square-shaped petals with the specified size. In this block, you will turn the sprite between calls to `draw square` in a way similar to that in the `draw polygon` blocks: using an angle of ![360 divided by the number of leaves](https://beautyjoy.github.io/bjc-r/img/drawing/calculating-turn-angle-for-draw-flower.png).An invocation of ![block: draw square-leaved flower with 6 leaves of size 50](https://beautyjoy.github.io/bjc-r/img/drawing/draw-square-leaved-flower-6-50-parameters.png) should draw the example picture above.

