# Lab - Refactoring

### Drawing Regular Polygons <a id="drawing-polygons"></a>

![regular polygons](https://github.com/hoc-labs/images/blob/main/polygon-row.png?raw=true)

A **regular polygon** is a shape in which all the sides are the same length and all the turning angles are the same. A square is a regular 4-sided polygon.[![drawing a square and squiggle](https://beautyjoy.github.io/bjc-r/img/looping/drawing-regular-polygons.gif)](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/draw-square-and-squiggle.xml)

#### Drawing a Square

Before beginning this exercise, you should have already completed the [Drawing a Square]() Lab to become familiar with building Snap blocks and using the repeat block.

**Draw a Triangle**

Based on your knowledge from drawing a square, create a series of commands to draw a triangle.

If you are having trouble with determining the angle to turn, think about the direction the sprite it pointing and how far it needs to rotate when it turns. The [video ](https://www.youtube.com/watch?v=qLU3PtaG3ww)may also be helpful to understand how the external angles of any polygon add up to 360 degrees.

![regular polygons](https://github.com/hoc-labs/images/blob/main/racecar.gif?raw=true)

**Draw a Pentagon and an Octagon**

Based on your knowledge from drawing a square and a triangle, create a series of commands to draw a pentagon \(five sides\) and an octagon \(eight sides\).

### \*\*\*\*

### **Refactoring - Create a Draw Polygon Command Block**

Now we have several commands that perform very similar instructions. Due to the nature of how the exterior angles of a regular polygon add up to 360 degrees, we can calculate the amount of rotation for any regular polygon by dividing 360 by the number of sides.

![](../.gitbook/assets/image%20%2887%29.png)

**Refactoring** is when you take some code that is functionally correct and modify/replace it to do the same task more efficiently. For this exercise, we're going to create a new command block that will draw any regular polygon and replace the ones we have built so far.

Create a command block in the **motion** palette, named **draw polygon**, that will draw all of the shapes above. It should accept to inputs:

* the number of sides
* the length of each side

Create titles for the input parameters so that it is easier to use them.

![regular polygons](https://github.com/hoc-labs/images/blob/main/draw-polygon.png?raw=true)

### **Create Art**

To use our new drawing blocks we're going to create some interesting art work. One more command block will be useful before we start.

**Create a Draw Rectangle Command Block**

Create a command block in the **motion** palette, named **draw rectangle**, that will draw a rectangle with the specified width and length.

![regular polygons](https://github.com/hoc-labs/images/blob/main/draw-rect.png?raw=true)

#### Prepare for Drawing

In the scripting area, set out a collection of the tools and blocks that may be handy in creating your art work. You can adjust the input values for these blocks as needed as you create your art. This [video](https://www.youtube.com/embed/pthWazhu474?rel=0) shows how to create some overlapping regions and then fill some of them with color.

![](https://github.com/hoc-labs/images/blob/main/poly-video.png?raw=true)

Make your own art. Explore a few different combinations of shape and color. Take screen shots of your art work and save them to your repository and then create a web page in your  repo that displays your work so you can share them with the class.

### Going Further

To add some randomness to your drawings try using the [random reporter](the-random-block.md) in your calls to your shape commands:

![random polygons](https://github.com/hoc-labs/images/blob/main/random-polys.png?raw=true)

Here are some ideas:

_\*\*\*\*_![](https://github.com/hoc-labs/images/blob/main/random-polys-2.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/random-polys-3.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/random-polys-4.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/just-reds.png?raw=true) ![](https://github.com/hoc-labs/images/blob/main/AbstractArtReflect.png?raw=true) 

### Resources

{% embed url="https://www.youtube.com/watch?v=XbZqfRGPom0" %}

{% embed url="https://www.youtube.com/watch?v=qLU3PtaG3ww" %}


