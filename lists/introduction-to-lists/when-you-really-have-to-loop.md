# When you Really have to Loop

Consider the following problem:

Write a predicate `increasing?` that takes a list of numbers as input, and outputs `true` if the numbers are in increasing order \(equal neighbors are okay\), or `false` otherwise.![increasing of \(1 3 4 10\) returning true](https://beautyjoy.github.io/bjc-r/img/hof/increasing-list-true-report.png)  
![increasing of \(1 7 4 10\) returning false](https://beautyjoy.github.io/bjc-r/img/hof/increasing-list-false-report.png)

Because this is a predicate, it's tempting to try to make it use `keep`:![report &amp;lt;empty? \(keep items such that \(&amp;lt;\(\) &amp;lt; \(???\)&amp;gt;\) from \(list\)](https://beautyjoy.github.io/bjc-r/img/list/hof/wannabe-increasing.png)

But `map`, `keep`, and `combine` work when each item in a list can be considered independently of the others. In this problem we have to consider each item **in relation to** the ones that have come before it: "Is this number at least as big as the ones we've already seen?"

To do this, we need to write a loop. The loop needs to go through the lists items, from left to right, and keep track of the last item that it saw. But, as with `map`, we don't need to keep track of the specific number of where we are in the list \(e.g., the third position, the first position, etc.\) Those index numbers have nothing to do with the problem we're trying to solve. The solution is to use the `for each item` block, this way:![definition of INCREASING? block](https://beautyjoy.github.io/bjc-r/img/list/hof/increasing.png)

Like the functions used as input to `map` and friends, the script inside the C-shaped slot of `for each item` interprets empty input slots \(in the `<` and `set` blocks\) as placeholders into which an item of the list will be entered. `For each item` promises to go through the list starting with item `1` and continuing in sequence to the end of the list. We use a script variable `minimum` to remember the most recent item's value, which is the minimum allowable value for the next item. If any item is smaller than that remembered value, `increasing?` reports `false`. If we make it to the end of the list without violating that requirement, then `increasing?` reports `true`.

Note that the `for each item` block has the word "item" in a round orange block. It's a variable, and you can drag it into the script that goes inside the C-slot, instead of using an empty input to represent the list item:![for each using item variable](https://beautyjoy.github.io/bjc-r/img/list/hof/increasing-item.png)

You can work with the above script [here](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/loop/increasing.xml).

### Try these

**Try this:** Display a longish list using time instead of space on the screen by ![say](https://beautyjoy.github.io/bjc-r/img/blocks/say-fragment.png)ing each item for two seconds.

**Try this:** Write an `expand` reporter that takes a sentence as input, and reports a sentence that's the same except that each number in the input is replaced by that many copies of the following word:  
  
![she loves you 3 yeah -&amp;gt; she loves you yeah yeah yeah](https://beautyjoy.github.io/bjc-r/img/list/hof/she-loves-you-yeah.png) ![i really really really really really really like you](https://beautyjoy.github.io/bjc-r/img/list/hof/i-really-like-you.png)

