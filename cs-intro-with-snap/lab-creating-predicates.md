# Lab - Creating Predicates

 **Analyzing and debugging:** These two blocks are quite similar. Build them both. Which one works properly?

![Block title Even Or Odd, input n; if \(n mod 2 equals 0\) \[say \(join n with text is even\) for 1 second\]; say \(join n with text is odd\) for 1 second](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Block_even-or-odd_if%28incorrect%29.png) ![Block title even or odd, input n; if \(n mod 2 equals 0\) \[say \(join n with text is even\) for 1 second\]  else \[say  \(join n with text is odd\) for 1 second\]](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Block_even-or-odd_if-else%28correct%29.png)



_You_ know that the code ![if-n-mod-2-equals-0](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/if-n-mod-2-equals-0.png) means "if _n_ is even," but programs are much easier to read and debug when the code _says_ what it means, something like ![if even? n](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/if-even-n.png) or ![if n is even](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/if-n-is-even.png).

1. Create the `even? (n)` block. The video also shows a different \(optional\) way to create an input name. You can, if you like, type the title text and input name at the same time, and _then_ change the part that you want to use as an input name by clicking on it and choosing "input name." Use whatever way you like best.The video below shows _almost_ all you need to do to define ![the even predicate](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/even-predicate.png), but an important step is missing.
   * You must define your block to be a _predicate_ rather than a command.
   * You must use the ![report](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/report.png) block to report the result.
2. **What else must be done before clicking OK?**
3. **Test** your new block to make sure it works properly.

   ![defining a predicate block](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/defining-even-predicate.gif)

4. Edit `even or odd` \(from problem 1\) to make it use the ![the even predicate](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/even-predicate.png) block. As always, _test_ the result to be sure it works. ![if the number is even, run these steps, else run some other steps](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/run-these-steps.png)

 _**n**_ `mod` _**m**_ reports the remainder when _n_ is divided by _m_. That remainder is 0 only when _n_ is a multiple of _m_. So, ![127 mod 60](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Direction-mod-60_203x28.png) reports 0 only when the sprite's `direction` is a multiple of 60°. So, the predicate ![direction-mod-60-equals-0](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/direction-mod-60-equals-0.png) is true only when `direction` is 0, 60, 120, 180, 240, or 300.

When the sprite's direction is not a multiple of 60, ![127 mod 60](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Direction-mod-60_203x28.png) reports a number other than 0. For example, if the sprite's direction is 127°, ![127 mod 60](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Direction-mod-60_203x28.png) reports 7.

![127 divided by 60 leaving a remainder of 7](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/227DividedBy60.png)

When the sprite is pointing in direction 90, ![direction mod 30](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/direction-mod-30.png) reports 0.![90 divided by 30 with zero remainder](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/90-divided-by-30.png).

In how many other directions will the predicate ![direction-mod-30-equals-0](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/direction-mod-30-equals-0.png) report `true`

\`\`

\`\`

1. To solve the puzzles in problems 7 and 8, you will need to understand how the conditionals \(`if-else` and `repeat until`\) control each of these scripts. Construct and analyze them with your pair programmer, experimenting with the conditions until you are sure you can explain exactly how this code does what it does.

   ![If Direction Mod 60 equals 0 set Pen Size to 5 Else Set Pen Size to 1](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/IfDirectionMod60=0PenSize5ElsePenSize1_325x256.png) ![Script](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Script-with-two-repeat-untils-and-mod.png)

   1. What if, instead of `direction mod` _`whatever`_ `= 0`, you used `direction mod` _`whatever`_ `= 20`?
   2. What if you tried `direction mod` _`23`_ `= 0`?
   3. What if you use `turn 2 degrees` or `turn 7 degrees` instead of `turn 1`?

2. Two puzzles: For each picture, create a script \(or modify one you already have\) that keeps the sprite moving in a circle drawing that picture.

   ![Puzzle 5: thin green circumference with four thick red dots at north, west, south, and east, sprite facing counterclockwise](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Challenge5.png) ![Puzzle 6: thin blue circumference with two very thick red dots in southeast at roughly four-o&apos;clock and five-o&apos;clock positions, sprite circling clockwise](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Challenge6.png)

3. And try to create a script that has this behavior.

   ![Clock animation: draws circle with dots for each number and says &quot;another hour has passed&quot;](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/ClockAnimation.gif)

### Extra Challenge

Problems 7 and 8 can be solved with conditionals or without. Whichever way you solved it, figure out how to solve it the other way.

**Challenge:** In problem 8, the sprite always says "Another hour has passed." You can do better than that: Make it say _what_ time it has just reached, like this.

![animated clock that says the hour](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/clock.gif)

