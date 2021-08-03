# Checking for Leap Years

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

Form a small group and discuss which version you prefer, and defend your answer.

Which one is easiest to read?  
Which one would be easiest to rewrite from memory?  
In which one would it be the easiest to find a bug?  
Which one is the most beautiful?!

