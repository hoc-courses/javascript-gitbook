# Combining All Items In a List

Let's say you have a list of numbers, such as all the students' grades on a quiz. You want to find the average grade. There are two steps: First, add up all the numbers; then divide that sum by the number of numbers - that is, by the length of the list.  
![average uses COMBINE WITH +](https://beautyjoy.github.io/bjc-r/img/list/hof/average.png)  
Notice that the red `length` `of` block that finds the number of items in a list is different from the green `length of` block that finds the number of letters in a text string.  
  
The first input to the `combine with` block is a two-input function. In this case, it's the **`+`** block, because we want to add all the numbers. In fact, unlike the situation with the `map` and `keep` blocks, there are really only a handful of functions you'll ever use with **combine**:  
![+, \*, and, or, join, join words](https://beautyjoy.github.io/bjc-r/img/list/hof/bad-operators.png)Why did we include the addition and multiplication operators, but not subtraction or division? Using an operator with `combine` makes sense only if it doesn't matter whether the values are combined left to right or right to left. That is,  
3+\(4+5\) = \(3+4\)+5  
but  
3-\(4-5\) ≠ \(3-4\)-5

  
Very occasionally you'll define a two-input custom reporter for use with `combine`. The two-input `max` block is an example; try using that to find the largest of a list of numbers.  
****  
We should try out the `average` block:  
![average of the list 7,8,1 iw 5.333333](https://beautyjoy.github.io/bjc-r/img/list/hof/avg781.png)  
Is that the answer you'd expect?

