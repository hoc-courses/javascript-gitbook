# Lab - Variables

{% embed url="https://bjc.edc.org/Sept2015/bjc-r/cur/programming/2-conditionals-abstraction-testing/2-script-variables/2-script-variable-projects.html?topic=nyc\_bjc%2F2-conditionals-abstraction.topic&course=bjc4nyc\_2015-2016.html&novideo&noassignment" %}

### Script Variable Projects

Open a new file. ![Create a new project](https://bjc.edc.org/Sept2015/bjc-r/img/icons/new-project-mini.png)

**You have a choice.** Some of the problems below are about language or linguistics, some are about mathematics, and some are about art. **Choose any three** that interest you and do them.

1. **Mondrian—an art project:** The Dutch artist Piet Mondrian is possibly best known for his artwork using brightly colored rectangles.

   ![Tableau\_I,\_by\_Piet\_Mondriaan, from Wikimedia Commons](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Tableau-I-Piet-Mondrian.png) "Tableau 1" by Piet Mondrian

   Mondrian wasn't at all random in his choice of colors and locations, but even some random choices can be interesting. A Snap script can produce designs like these.

   ![Mondrian-like art drawn with Snap](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Snap-Piet-Mondrian.png) ![another Mondrian-like design drawn with Snap](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Snap-Piet-Mondrian2.png)This isn't the actual Snap_!_ program. You could write custom blocks with these names, but they're a little verbose to use as real block names, especially that two-line one in the middle. This algorithm is for you to read, not for a computer to read.This algorithm produced those designs:  
   ![Draw outer frame \(400 x 300\); Fill with some color; Repeat many times; Pick random location, Pick random height and width for a rectangle that, at that location, won&apos;t extend beyond frame; Draw rectangle boundary in thick black line; Fill rectangle with random color](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/mondrian-script.png)

   To keep your code clear, you may want to create separate blocks that specialize in boundary and fill and choosing locations and calculating size.

   Snap has no `fill with color` block. One way to make such a block is  
   ![Repeat until height or width is less than 2; Draw rectangle of specified height and width; Set height slightly smaller; Set width slightly smaller](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/fill-script.png)

   To get bright colors, use `set pen shade to 100`, and you get a good collection of colors with ![set-pen-color-to\(2-times-pick-random-0-to-50\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/set-pen-color-to%282-times-pick-random-0-to-50%29.png)

   1. Build a program that draws different pictures each time, always using colored rectangles. Use the algorithm suggested above or some idea of your own. _Take screen shots of the artworks your program generates and **save the ones that you like** best._
   2. Mondrian limited his colors and used a lot of white and some black. Experiment with that to see if you get designs you like.
   3. Find ways to improve your program.

2. **Another art idea:** The code ![Set-pen-size-50-move-100-steps](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Set-pen-size-50-move-100-steps.png) does not do what you might expect, because the "ends of the lines" are rounded. Try it. Now `clear` the stage and try ![Set-pen-size-50-move-0.1-steps](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Set-pen-size-50-move-0.1-steps.png). Why does _that_ happen?![Talk with Your Partner](https://bjc.edc.org/Sept2015/bjc-r/img/icons/talk-with-your-partner.png) ![colored circles randomly placed](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/colored-circles.png) ![colored ovals](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Colored-ovals.png) Experiment with the possibilities. You can choose between flat and round ends in the settings menu. ![settings menu, flat line ends](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Flat%20Line%20Ends.png) If you switch to "Flat line ends" for this project, you will probably want to switch back to "round ends" for other drawing projects.
3. **Writing secret code:** Create a block that takes a word as input, changes each letter into the _next_ letter in the alphabet—for example, A becomes B, Y becomes Z...—and reports the result, like this: ![encode-decode\(HANDY\)-with-result\(IBOEZ\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/encode-decode%28HANDY%29-with-result%28IBOEZ%29.png).

   In order to do this, you will need to be able to change a letter into a number, add 1 to that number, and then change the new number back to a letter. The blocks ![unicode-of\(Y\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/unicode-of%28Y%29.png) and ![unicode\(89\)as-letter](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/unicode%2889%29as-letter.png) will help you do that. Experiment with them to see how they work.

   1. This block encodes by adding 1 to the unicode for each letter. You could, instead, always add 2 or 5 or whatever. Give your block a second variable that allows you to specify what to add to the unicode.
   2. When you give your `encode` block the input `z`, what does it report? If that's not what you would _like_ it to report, change it.
   3. Make a `decode` block.

4. **Linguistic research:** Build a block that can take a piece of text as input and which letter, **t** or **s**, is used more often in that bit of text. Later, you will be able to generalize this and take a large block of text and figure out the frequency of each letter. _Letter frequency differs from language to language. That information has been used as one clue in decoding encrypted messages._
5. **A mathematical function:** Create a `factorial` block ![n factorial](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/n-factorial.png) \(or ![n!](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/n-factorial-symbol.png)\) that takes a positive integer _n_ and reports the product of all whole numbers from 1 through _n_, in other words 1 × 2 × 3 × ... × \(_n_ - 1\) × _n_. When the input is 4, the output should be 24 \(because 1 × 2 × 3 × 4 = 24\).
   1. Dividing 5! by 4!, the result should be 5 ![5-factorial-divided-by-4-factorial-with-result\(5\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/5-factorial-divided-by-4-factorial-with-result%285%29.png) because 5 factorial is really just 5 times 4 factorial. Using your block, check each of these computations—![4-factorial-divided-by-3-factorial](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/4-factorial-divided-by-3-factorial.png), ![3-factorial-divided-by-2-factorial](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/3-factorial-divided-by-2-factorial.png), ![2-factorial-divided-by-1-factorial](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/2-factorial-divided-by-1-factorial.png) and ![1-factorial-divided-by-0-factorial](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/1-factorial-divided-by-0-factorial.png)—to see what it reports. One of these is inconsistent with the others. To fix the problem, we need to _define_ 0! = 1. Edit your `n!` block to report 1 if _n_ = 0. Then fully test `n!` again to make sure it works as it should.
   2. **Debugging:** Obviously ![cookie-factorial-bug](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/cookie-factorial-bug.png) should not work. Check to see what does happen. Then edit your block and find a way to use ![is n a number](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/is-n-a-number.png) to check that the input is a number and report some sensible result or message.
   3. **Analyzing code:** In mathematics, factorial is defined only for positive integers and zero, so 3.7! would make no mathematical sense. But ![three-point-seven-factorial](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/three-point-seven-factorial.png) reports a result. Find out what it reports and analyze what the block does so that you can figure out why _that_ is the result.
6. **Another mathematical function:** Create a block `triangular number n` that _adds_ all of the whole numbers from 1 through _n_:1+2+3+⋯+\(n−1\)+n1+2+3+⋯+\(n−1\)+nWhen its input is 4, your block should report 10 \(that is, 1 + 2 + 3 + 4\). Define your block so that `triangular number 0` reports 0.
   1. Create ![sum from a to b](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/sum%20from%20a%20to%20b%20170%C2%A0%C3%97%C2%A027%20pixels.png) so that ![sum from 3 to 7](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/sum%20from%203%20to%207%20170%C2%A0%C3%97%C2%A027%20pixels.png) reports the sum 3 + 4 + 5 + 6 + 7, and ![sum from -3 to 3](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/sum%20from%20-3%20to%203.png) reports the sum of -3 + -2 + -1 + 0 + 1 + 2 + 3.
7. Recall that `n mod i` will tell you if _i_ is a divisor of _n_.**Counting divisors:** Create a block that takes a whole number as input and checks numbers from 1 through that input and counts the ones that evenly divide the input. So, for example, ![number of divisors of 8, with result = 4](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/number-of-divisors-of-8-with-result%284%29.png) because, from 1 through 8, only the numbers 1, 2, 4, and 8 evenly divide 8. `number-of-divisors 10` should also report 4 because, of the numbers from 1 through 10, only 1, 2, 5, and 10 are divisors of 10. **Experiment** to find several numbers that have an odd number of divisors.

 

1. "Flat line ends" should be unchecked for this one.Here is a block and the picture it makes.

   ![Block that makes nested colored circles, looking a bit like a tunnel](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Albers-circles.png) ![The picture of nested circles made by that block](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/tunnelpic-%28steps-6%29%28color-0%29.png)

   Edit it and give it inputs that let you produce pictures like these. You don't have to use script variables.

   ![command ](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/tunnel-%28steps-3%29%28color-0%29.png) ![three embedded red circles](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/tunnelpic-%28steps-3%29%28color-0%29.png)

   ![command tunnel-\(steps-4\)\(color-50\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/tunnel-%28steps-4%29%28color-50%29.png) ![four embedded aqua-blue circles](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/tunnelpic-%28steps-4%29%28color-50%29.png)

   Experiment with various inputs.

2. The artist Joseph Albers became famous for paintings a bit like this: ![AlbersPic-\(steps-4\)\(color-60\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/AlbersPic-%28steps-4%29%28color-60%29.png) ![Albers-\(steps-4\)\(color-60\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Albers-%28steps-4%29%28color-60%29.png)

   Set "flat line ends" and create a block that draws pictures like this. It will be convenient to use script variables

3. Edit your `raise (n) to the power (b)` block to make it work for negative integer exponents.
4. **Old-fashioned divisibility test—divisibility by 3 or 9:**
   * Create a helper reporter `digit sum` that adds up the digits in a number. So, for example `digit sum 7` should report 7, and `digit sum 12` should report 3, and `digit sum 126` should report 9 \(the sum of 1, 2 and 6\). You may find these blocks useful. ![fletter-i-of-number](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/letter-i-of-number.png) ![for-i=1-to-length-of-number](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/for-i=1-to-length-of-number.png)
   * Then write `repeated digit sum`, which keeps taking the `digit sum` until the result is a single digit. For example, the digit sum of 238 is 2+3+8=13, which is more than a single digit. The digit sum of 13 is 1+3=4, which _is_ a single digit. So the repeated digit sum of 238 is 4.
   * Write predicates `divisible by 3?` and `divisible by 9?`. A number is divisible by 3 if its repeated digit sum is 0, 3, 6, or 9; it's divisible by 9 if its digit sum is 0 or 9.
     * ![Tough Stuff](https://bjc.edc.org/Sept2015/bjc-r/img/icons/tough-stuff-mini.png)![Tough Stuff](https://bjc.edc.org/Sept2015/bjc-r/img/icons/tough-stuff-mini.png) Why?
5. **Old-fashioned divisibility test—divisibility by 7:** Create a `multiples of 7 algorithm` block that takes any whole number as input and then puts it through this process:For this project, ![all but last letter of](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/all-but-last-letter-of.png) and ![last letter of](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/last-letter-of.png) are useful. They are in [the **Words, sentences** library](http://snap.berkeley.edu/snapsource/snap.html#open:http://snap.berkeley.edu/snapsource/libraries/word-sentence.xml).

   ![multiples of 7 algorithm](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/divisibility-by-7-algorithm.png)

   Test it first on several multiples of 7 \(small and large\) and make sure that, for multiples of 7, it reports only the results 14, 7, 0, -7, and -14. Also test it on several numbers that are _not_ multiples of 7; for those numbers, it should never report 14, 7, 0, -7, or -14. ![multiples-of-7-algorithm-block-with-501298-as-input\(and-result-neg14\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/multiples-of-7-algorithm-block-with-501298-as-input%28and-result-neg14%29.png)

6. Look up a test for divisibility by 11 or 13 and see if you can build a block that performs that algorithm.
7. In
8. 9. Snap
10. , as in most programming languages, you can test for divisibility just by using
11. 12. `mod`
13. , but before computers were widespread, algorithms like these greatly simplified some computations.

![Import Tools](https://bjc.edc.org/Sept2015/bjc-r/img/icons/import-tools-mini.png)Although this ![set variable to function of variable](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/clobber.png) style of programming is very common, pretty soon you'll learn a better way: _functional programming,_ in which you never change the value of a variable. You're not quite ready to write functional programs yet \(that'll come in Unit 3\), but here are some examples from above, rewritten functionally, that you can probably understand:  
![factorial: combine with times items of numbers from 1 to n](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/better-factorial.png)![number-of-divisors: length of keep items such that \(\(n mod \_\_\) = 0\) from \(values from 1 to n\)](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/better-divisors.png) ![digit sum: combine with + items of word to list of number](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/better-digit-sum.png)"U2L2-MathTools"![save your work as U2L2-MathTools](https://bjc.edc.org/Sept2015/bjc-r/img/icons/save-this-as.png)

