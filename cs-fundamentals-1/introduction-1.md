# Introduction

Let’s first look at the IDE \(Integrated Development Environment\). You should see the following arrangement of regions in the window:

![](../.gitbook/assets/1%20%282%29.png)

## Blocks

The area at the left edge of the window is the _palette_. As you see in the picture, it contains tabs for eight different-color block categories. 

These tabs are an important organizational structure in Snap_!_ because they are home to the various blocks that you will use to tell the computer what to do. The blocks are categorized under each tab based on what kind of thing each block does.

Look at the **Motion** tab. Under this tab you will find a bunch of blocks that correspond to motion-like actions. For example, click on the ![Move 10 Steps Block](https://beautyjoy.github.io/bjc-r/img/blocks/move-10-steps.png) block, drag it to the scripting area, and drop it anywhere in the scripting area.

![animation of move block dragging from palette to scripting area](https://beautyjoy.github.io/bjc-r/img/intro/drag-a-block.gif)

The block that you just dragged and dropped into the scripting area controls something that we call a _**sprite**_, which is the arrowhead-looking thing in the middle of the stage \(the white part of the window\).

![](../.gitbook/assets/image%20%2815%29.png)

Back to the scripting area, if you click on the ![Move 10 Steps Block](https://beautyjoy.github.io/bjc-r/img/blocks/move-10-steps.png) you just put there, the sprite will move 10 steps. You can see this visually depicted by the sprite moving in the stage. You can vary the input of the block, i.e., the number 10, to change the number of steps you want to the sprite to move. See if you can figure out how to change the block input so that the sprite moves backwards!

## Scripts

Now that you have figured out how to make a sprite move, you might be wondering how to make the sprite do other things as well.

To make a sprite do more than just move, we need to use different types of blocks and link them together. You can link blocks by snapping \(hence the name Snap_!_\) them together -- drag a block right underneath the one to which you want to attach it. Blocks will snap together when one block’s indentation is near the tab of the one above it. You should see a white bar appear like the one in the image below, which just shows you where the block will go after you drop it.

![Blocks Snapping Together](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_blocks_snapping.png)

If you keep attaching blocks together in this way, you will create a _script_. A Snap_!_ program consists of one or more of these scripts.

Try recreating the following script in the scripting area in Snap_!_. The purple `say...` blocks are available from the **Looks** tab.  
  
![You just made a script!](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_justmadeascript.png)

What will happen if you run this script? Remember, a script will tell the sprite what to do. Click on the script and see what happens! You will know that your script is running if it has a highlighted border around it:

![Script Running](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_highlightedscript.png)

Be sure to note: **blocks in a script run in a specific order, from the top of the script to the bottom**. Generally, Snap_!_ waits until one block has finished its job before continuing on to the block below it. \(One common exception is blocks that play sounds: a block's job can be to start the sound, which means the block below it will execute while the sound is still playing.

At the bottom of Motion palette are three blocks shaped differently from the others. The oval-shaped ![X Position
   Reporter](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_xposition.png) and ![Y Position
   Reporter](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_yposition.png) are called _reporters_. \(We don't need the third one right now.\) 

## Reporters

Unlike the jigsaw-puzzle-piece-shaped _command_ blocks we've used until now, reporters don't carry out an action \(such as moving the sprite or displaying a speech balloon\) by themselves. Instead they _report_ a value, usually for use in another block's input slot.

These particular reporters tell you where the sprite is on the stage. As in algebra class, **x** means left-to-right position, and **y** means bottom-to-top position.

If your sprite is in the middle of the stage, drag it somewhere off-center. Then, drag an **x position** block into the scripting area and click on it. You should see a little speech balloon next to the block:![X Position
   speech balloon](https://beautyjoy.github.io/bjc-r/img/topic1/xpos-bubble.png)

Click on the gray box to the left of the **x position** block in the palette, and then look over to the stage. You will see that the value that the block would report is displayed on the stage:![X Position block&apos;s checkbox](https://beautyjoy.github.io/bjc-r/img/topic1/palette-checkbox.png)     ![X Position stage
   watcher](https://beautyjoy.github.io/bjc-r/img/topic1/watcher.png)

This on-stage display is called a _watcher_.

The ![X Position
   Sensor Block](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_xposition.png) and the ![Y Position
   Sensor Block](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_yposition.png) will tell you the position of your sprite on the screen. Move the sprite around and the values reported by these blocks change.

## The Stage

A sprite occupies a position \(x, y\) on the stage where x represents the horizontal position, from -240 \(left\) to 240 \(right\), and y represents the vertical position, from -180 \(bottom\) to 180 \(top\). 

Here's a picture:

![Coordinate Grid](https://beautyjoy.github.io/bjc-r/img/topic1/topic1_coordgrid.png)



The black sprite is at the center of the stage, called the origin, with coordinates \(0, 0\). The green sprite is to the right of the origin, so its x position is positive. The green sprite is also below the origin, so its y position is negative. Each grid line above represents 20 steps, so the green sprite's coordinates are \(140, -100\). 

**Try this:** What are the coordinates of the red sprite?

In your _Snap!_ window, take a look at the blocks under the Motion tab. The majority of the blocks there will help you position your sprite on the stage. Try them and see what they do! Change the input values to see what happens.

## Experiment with Drawing Commands

Try to get comfortable with the blocks under the **Motion** tab and the **Pen** tab. Figure out what each one does, and try to use these blocks to draw a square or a simple picture. Get started by testing these blocks:

![Move 10 Steps Block](https://beautyjoy.github.io/bjc-r/img/blocks/move-10-steps.png)

![Turn Right 15 Degrees Block](https://beautyjoy.github.io/bjc-r/img/blocks/turn-right-15.png)

![Clear Block](https://beautyjoy.github.io/bjc-r/img/blocks/clear.png)

![Pen Down Block](https://beautyjoy.github.io/bjc-r/img/blocks/pen-up.png)

![Pen Up Block](https://beautyjoy.github.io/bjc-r/img/blocks/pen-down.png)

### Tips and Tricks:

1. Once the pen is down, it stays down even in a different script. Use the `pen up` block to lift the pen so that no lines will be drawn.
2. You also will want to show the direction and x and y position of the sprite. In the Motion tab, you can select for these to be shown on the stage as described above in the Reporters section. 
3. **Try this**: Does the **turn** block change the x or the y position?

## Follow the Mouse

What do you think the following script will do?![Follow That Mouse Script](https://beautyjoy.github.io/bjc-r/img/blocks/follow-that-mouse.png)

Hint: ![Mouse X Reporter](https://beautyjoy.github.io/bjc-r/img/blocks/mouse-x.png) and ![Mouse Y Reporter](https://beautyjoy.github.io/bjc-r/img/blocks/mouse-y.png) are reporters in the **Sensing** palette; they tell you where the mouse is pointing.

Open [the program](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/follow-that-mouse.xml) \(click on the forever block to run it\). Did it follow your expectations?

Drag the mouse to a different part of the screen while the program is running and see what happens!

**Try this:** change the go to block to look like this:

![Go
                To X+60 Script](https://beautyjoy.github.io/bjc-r/img/topic1/xplus60.png)

How does this change the program's behavior?

## Forever Block

From the previous exercise, you may have figured out what the ![Forever block](https://beautyjoy.github.io/bjc-r/img/blocks/forever.png) block does. The **forever** block is the first block you have see that holds, or wraps around, other blocks. We call this a _C block_ because of its shape. As the name **forever** implies, it will run the blocks inside it again and again and again and ... well, forever. 

![Forever And a Day Script](https://beautyjoy.github.io/bjc-r/img/intro/the-person-kept-talking-and-talking.png)

You will find this block under the **Control** tab.

Will a ![Forever block](https://beautyjoy.github.io/bjc-r/img/blocks/forever.png) block ever stop?  
  
Not unless you tell it to: Click on the stop sign icon on the upper right hand corner of the Snap_!_ window.  
![Stop button](https://beautyjoy.github.io/bjc-r/img/topic1/stopbutton.png)

This stop sign will stop all scripts that are running in any sprite. This is equivalent to executing the ![stop all block](https://beautyjoy.github.io/bjc-r/img/blocks/stop-all.png) in the `Control` palette.

