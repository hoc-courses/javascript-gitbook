# Conditionals

## If and If-Else

Now that we have the idea of predicates under our belt, we can finally express full "if-then" statements, such as "if the weather is nice, you should go outside." This can be expressed in Snap using the ![if](https://beautyjoy.github.io/bjc-r/img/blocks/if.png) block. Notice how the first slot is shaped just like a predicate block. 

`if` blocks only know how to handle yes/no questions, so you should only ever put predicate blocks into this slot. The C-shaped part of the `if` block is where you put the commands that should be run if the condition is true. Let's take a look at an example:

![](https://beautyjoy.github.io/bjc-r/img/cond/mood.png)

In the above example, we had several possible cases to consider. However, in many situations, there are only two main cases. Take for example, the following sentence: "If a number is divisible by 2, it is even. Otherwise it is odd." For these situations we have the ![if-else](https://beautyjoy.github.io/bjc-r/img/blocks/if-else.png) block. It works like this:

![](https://beautyjoy.github.io/bjc-r/img/cond/even-or-odd.png)

Here, we didn't need to have an additional "if," because all whole numbers are either even or odd. If the boolean expression \(`x mod 2 = 0`\) evaluates to `false`, we know that the number is not even and thus must be odd.

#### mod Block

If you haven't seen the ![\(\) mod \(\)](https://beautyjoy.github.io/bjc-r/img/blocks/mod.png) block before, it reports the remainder \(or "modulus"\) when the first input is divided by the second. For example, `5 mod 2` reports `1` because `5 / 2 = 2 remainder 1`. This block is especially useful for checking whether a number is divisible by another, because the remainder will be 0. ![\(x mod 2\) = 0](https://beautyjoy.github.io/bjc-r/img/cond/x-mod-2-equals-0.png) is the same as asking if `x` is divisible by 2 \(i.e. that `x` is even\).

## Nested Conditions

A **nested conditional statement** is an `if` or `if else` statement inside the `else` part of another `if else` statement. If the predicate of the outer `if else` statement is false, then inner \(nested\) conditional statement will test its predicate and decide what to do.

Describe what this code segment will do.  
![ask \(Is today Tuesday?\) and wait
if \(answer = &apos;yes&apos;\)
{
    say \(Mary Chung&apos;s is closed today.\)
}
else
{
    if \(answer = &apos;no&apos;\)
    {
        say \(Mary Chung&apos;s is open today.\)
    }
    else
    {
        say \(You didn&apos;t answer yes or no.\)
    }
}](https://bjc.edc.org/bjc-r/img/2-complexity/is-today-tuesday.png)

## Predict the Output

Below are several blocks that use `if` and `if-else`. Predict what each one will do. Once you've done so, try running each of the blocks, which can be found [here](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/conditionals/predict-if-functions.xml).

#### abs block

You'll notice that a couple of the scripts below use the ![abs \(\)](https://beautyjoy.github.io/bjc-r/img/blocks/abs.png) block. This block actually allows you to use many different mathematical functions. It shows up in the palette as ![sqrt \(10\)](https://beautyjoy.github.io/bjc-r/img/blocks/sqrt-of-10.png). Just click the drop-down menu to select which function to use. "abs" is short for "absolute value." In case you're not already familiar, the absolute value of a number is just that number turned positive. For example, `abs(10)` is just `10`, while `abs(-2.5)` is `2.5`.

![a mysterious block](https://beautyjoy.github.io/bjc-r/img/cond/back-and-forth.png)

![a mysterious block](https://beautyjoy.github.io/bjc-r/img/cond/back-and-forth-no-abs.png)

![a mysterious block](https://beautyjoy.github.io/bjc-r/img/cond/crenellation.png)

![a mysterious block](https://beautyjoy.github.io/bjc-r/img/cond/dvd-player-screen-saver.png)



## Checking for Leap Years

Some years in our \(Gregorian\) calendar are **leap years**. February has a 29th day and the year overall has 366. Many people think that leap years come every fourth year, and some know that this is because it takes the earth takes 365.25 days to revolve around the sun.

But, things are a bit more complicated than that: leap years come slightly less often than once every four years. To figure out if a year \(say, 1999\) is a leap year, you need to test whether it is divisible evenly — that is, if there is no remainder after the division — by three different values.

A calendar year is a leap year if

* it can be divided evenly by **4**,
* unless it can also be divided evenly by **100**,
* except if it is also divisible evenly by **400**, in which case it is a leap year.

[We aren't making this up.](http://en.wikipedia.org/wiki/Leap_year#Gregorian_calendar)

Thus 2000 was a leap year \(divisible evenly by 400, 100, and 4\), 1900 was not \(divisible evenly by 100 and 4 but not by 400\), 1996 was \(divisible evenly by 4 but neither 100 nor 400\), and 1999 wasn't \(not divisible by anything!\) .

Consider the block sets below: they all say **"leap year"** if the `year` variable is a leap year and **"normal year"** otherwise. That is, they all work correctly, without any bugs. \(The scripts are available in [this Snap_!_ program](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/conditionals/dates/is-leap-year.xml)\).

| \(A\)   | ![](https://beautyjoy.github.io/bjc-r/img/cond/leap-year-script-boolean.png) |
| :--- | :--- |
| \(B\)   | ![](https://beautyjoy.github.io/bjc-r/img/cond/leap-year-script-conditional-1.png) |
| \(C\)   | ![](https://beautyjoy.github.io/bjc-r/img/cond/leap-year-script-conditional-2.png) |

Which version you prefer, and defend your answer.

* Which one is easiest to read?
* Which one would be easiest to rewrite from memory?
* In which one would it be the easiest to find a bug?
* Which one is the most beautiful?!

## Test for Understanding

{% embed url="https://beautyjoy.github.io/bjc-r/cur/programming/conditionals/complex-booleans-self-test.html?1&topic=berkeley\_bjc%2Fintro\_pair%2F3-conditionals.topic&course=cs10\_sp19.html&novideo&noreading&noassignment" %}



