# The Mod Block

The `mod` block **reports the remainder** when the first input is divided by the second. For example, ![\(17\) mod \(5\)](https://bjc.edc.org/bjc-r/img/1-introduction/17-mod-5.png) reports 2 because when 17 is divided by 5, the remainder is. 

When one number divides another evenly, the remainder is 0. So for example, ![\(15\) mod \(5\)](https://bjc.edc.org/bjc-r/img/1-introduction/15-mod-5.png) reports 0.



 **Order of operations:** In a block language, the nesting of blocks determines the order of operations. For example, in ![3 &#xD7; \(5 + 4\)](https://bjc.edc.org/bjc-r/img/6-computers/3-times%285+4%29.png) you can _see_ that the `+` block is an input to the `×` block, so the expression means 3×\(5+4\). 

Similarly, ![\(3 &#xD7; 5\) + 4](https://bjc.edc.org/bjc-r/img/6-computers/%283-times-5%29+4.png) means \(3×5\)+4. 

In Snap!, it's as if there are parentheses around _every_ operation. But in text languages, you can write `3 * 4 + 5`without parentheses, so they need the rules you learn in math class \(multiplication before addition, and so on\). The `mod` operator is like multiplication and division; it happens _before_ addition and subtraction. So for example, `7 + 5 MOD 2 - 6` means `7 + 1 - 6`

Use `mod` to build a ![is \(\) divisible by \(\) ?](https://bjc.edc.org/bjc-r/img/2-complexity/divisible-by.png) predicate that tests for divisibility.  
![is \(15\) divisible by \(3\) ? reporting true](https://bjc.edc.org/bjc-r/img/2-complexity/15-divisible-by-3-reporting-true.png) ![is \(15\) divisible by \(6\) ? reporting false](https://bjc.edc.org/bjc-r/img/2-complexity/15-divisible-by-6-reporting-false.png)

Use this `divisible by?` predicate to build a predicate that tests whether its input is even \(divisible by 2\).  
![even? \(-22\) reporting true](https://bjc.edc.org/bjc-r/img/2-complexity/even--22-reporting-true.png) ![even? \(7\) reporting false](https://bjc.edc.org/bjc-r/img/2-complexity/even-7-reporting-false.png)

 In a later lab, you can use your `even?` block to draw a [brick wall](lab-build-a-wall.md) because the even and odd numbered rows are different.

![](../.gitbook/assets/image%20%2875%29.png)



