# Lab - Repeat Loop

### [https://bjc.edc.org/Sept2015/bjc-r/cur/programming/1-introduction/3-control-commands/1-the-repeat-block.html?topic=nyc\_bjc%2F1-intro-loops.topic&course=bjc4nyc\_2015-2016.html&novideo&noassignment](https://bjc.edc.org/Sept2015/bjc-r/cur/programming/1-introduction/3-control-commands/1-the-repeat-block.html?topic=nyc_bjc%2F1-intro-loops.topic&course=bjc4nyc_2015-2016.html&novideo&noassignment)

### 

### The Real Value of the `Repeat` Block

It is, of course, much easier to create this script...  
![repeat 4 \(move 50 steps, turn right 90 degrees\)](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/repeat-4%28move-50-turn-right-90%29.png)  
...than to create this one:

![move 50 steps, turn right 90 degrees, move 50 steps, turn right 90 degrees, move 50 steps, turn right 90 degrees, move 50 steps, turn right 90 degrees](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/move-50-turn-right-90-%284-times%29.png)

Even more importantly, using `repeat` makes the _structure_ of the program clearer. This is essential to good coding. Clearly structured code is easier to understand and easier to debug \(to catch and fix errors\). In the longer script above \(without `repeat`\), we'd have to count the parts to see if it's right. And it would be very easy to make a mistake if we were drawing a 20-sided figure instead of a 4-sided one!



1. **Analyze structure:** Here are four pictures. ![Square with sides alternating red and blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/Square-alternating-red-and-blue.png) ![6-sided figure, sides alternating red-blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/6-sided-figure-alternating-red-and-blue.png) ![8-sided figure, sides alternating red-blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/8-sided-figure-alternating-red-and-blue.png) ![12-sided figure, sides alternating 3 red 3 blue](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/12-sided-figure-alternating-3-red-and-3-blue.png) 
2. Which one\(s\) of these pictures could be drawn by running the following script? ![repeat 4, red move turn, blue move turn](https://bjc.edc.org/Sept2015/bjc-r/img/1-introduction/non-pseudo.png)



 Use ![empty repeat-n block](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/repeat-empty.png) to draw the following regular polygons _using the smallest number of lines_:A _regular_ polygon is a polygon in which all the sides are the same length and all the turning angles are the same. A square is a regular four-sided polygon.

* Equilateral Triangle
* Pentagon
* Hexagon
* Octagon

![](../.gitbook/assets/image%20%2813%29.png)

![](../.gitbook/assets/image%20%28131%29.png)

### Taking it Further

1. Determine the turning angles to draw a 12-sided or 36-sided regular polygon.
2. Make small enough sides so that the shapes can fit on the stage. With more and more sides, the polygons get closer and closer to a circle. Is there a point at which the result
3. 4. _is_
5. 6. a circle?
7. ![drawn star](https://bjc.edc.org/Sept2015/bjc-r/img/drawing/draw-star-picture.png)
8. The code in self check question 2 above created a regular 9-pointed star. Through how many degrees did the sprite turn altogether to draw that star?
9. Adjust the numbers in that script to get a regular 5-pointed star.
10. Through how many degrees did your sprite turn altogether when you drew the five-pointed star?
11. Find a starting direction so that the star sits "straight."

