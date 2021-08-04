# Repeat Loop

## Don't Repeat Yourself - let Snap! do it for you!

We can use the ![empty repeat-n block](https://beautyjoy.github.io/bjc-r/img/blocks/repeat.png) block to make drawing shapes a lot easier! You can see below a script to draw a square. It is, of course, much easier to create this script..

  
![repeat 4 \(move 50 steps, turn right 90 degrees\)](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/repeat-4%28move-50-turn-right-90%29.png)  


than to create this one:

![](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/move-50-turn-right-90-%284-times%29.png)

Even more importantly, using `repeat` makes the _structure_ of the program clearer. This is essential to good coding. Clearly structured code is easier to understand and easier to debug \(to catch and fix errors\). In the longer script above \(without `repeat`\), we'd have to count the parts to see if it's right. And it would be very easy to make a mistake if we were drawing a 20-sided figure instead of a 4-sided one!

Here are four pictures.  
![Square with sides alternating red and blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/Square-alternating-red-and-blue.png) ![6-sided figure, sides alternating red-blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/6-sided-figure-alternating-red-and-blue.png) ![8-sided figure, sides alternating red-blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/8-sided-figure-alternating-red-and-blue.png) ![12-sided figure, sides alternating 3 red 3 blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/12-sided-figure-alternating-3-red-and-3-blue.png)  


Which one\(s\) of these pictures could be drawn by running the following script? 

![repeat 4, red move turn, blue move turn](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/non-pseudo.png)

## Drawing Regular Polygons with Repeat

![](../.gitbook/assets/image%20%28106%29.png)

A regular polygon is a shape in which all the sides are the same length and all the turning angles are the same. A square is a regular 4-sided polygon.[![drawing a square and squiggle](https://beautyjoy.github.io/bjc-r/img/looping/drawing-regular-polygons.gif)](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/draw-square-and-squiggle.xml)

Using a ![empty repeat-n block](https://beautyjoy.github.io/bjc-r/img/blocks/repeat.png) to draw the following regular shapes:

* Equilateral Triangle
* Pentagon
* Hexagon
* Octagon

If you are having trouble with determining the angle to turn, think about the direction the sprite it pointing and how far it needs to rotate when it turns. It may also be helpful to understand how the external angles of any polygon add up to 360 degrees.

![regular polygons](https://github.com/hoc-labs/images/blob/main/racecar.gif?raw=true)

As you draw regular polygons with more and more sides, you are getting closer and closer to a circle. Is there a point at which is actually \(mathematically?\) a circle?

## Check for Understanding - External Angles

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/intro/drawing/angles-self-test-2.html?1&topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## Check For Understanding - Nested Loops

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/intro/drawing/repeat-self-test.html?topic=berkeley\_bjc%2Fintro\_pair%2F2-loops-variables.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}

## **Refactoring - Create a Draw Polygon Command Block**

Now we have several commands that perform very similar instructions. Due to the nature of how the exterior angles of a regular polygon add up to 360 degrees, we can calculate the amount of rotation for any regular polygon by dividing 360 by the number of sides.

![](../.gitbook/assets/image%20%2893%29.png)

**Refactoring** is when you take some code that is functionally correct and modify/replace it to do the same task more efficiently. For this exercise, we're going to create a new command block that will draw any regular polygon and replace the ones we have built so far.

Create a command block in the **motion** palette, named **draw polygon**, that will draw all of the shapes above. It should accept to inputs:

* the number of sides
* the length of each side

Create titles for the input parameters so that it is easier to use them.

![regular polygons](https://github.com/hoc-labs/images/blob/main/draw-polygon.png?raw=true)

## **Create Art**

To use our new drawing blocks we're going to create some interesting art work. One more command block will be useful before we start.

**Create a Draw Rectangle Command Block**

Create a command block in the **motion** palette, named **draw rectangle**, that will draw a rectangle with the specified width and length.

![regular polygons](https://github.com/hoc-labs/images/blob/main/draw-rect.png?raw=true)

#### Prepare for Drawing

In the scripting area, set out a collection of the tools and blocks that may be handy in creating your art work. You can adjust the input values for these blocks as needed as you create your art. This [video](https://www.youtube.com/embed/pthWazhu474?rel=0) shows how to create some overlapping regions and then fill some of them with color.

![](https://github.com/hoc-labs/images/blob/main/poly-video.png?raw=true)

Make your own art. Explore a few different combinations of shape and color. Take screen shots of your art work and save them to your repository and then create a web page in your  repo that displays your work so you can share them with the class.

## Going Further

To add some randomness to your drawings try using the [random reporter]() in your calls to your shape commands:

![random polygons](https://github.com/hoc-labs/images/blob/main/random-polys.png?raw=true)

Here are some ideas:

_\*\*\*\*_![](https://github.com/hoc-labs/images/blob/main/random-polys-2.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/random-polys-3.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/random-polys-4.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/just-reds.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/AbstractArtReflect.png?raw=true) 

## Resources

{% embed url="https://www.youtube.com/watch?v=XbZqfRGPom0" %}

{% embed url="https://www.youtube.com/watch?v=qLU3PtaG3ww" %}



