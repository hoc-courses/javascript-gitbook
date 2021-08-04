# Valid Date?

The procedure shown below checks whether its arguments represent a valid date in the Gregorian calendar \(the one we use in the United States\). The calendar was instituted in 1582, so only dates in that year or in the future are legal. **Simplify the valid-date block and make it more readable by defining and using well-named helper procedures** \(hint: Is leap year?\). When you are done, there should be more code than when you started, but it should be easier to understand.[![messy code for valid-date](https://beautyjoy.github.io/bjc-r/img/building-blocks/valid-date-messy-code.png)](http://snap.berkeley.edu/snapsource/snap.html#open:https://beautyjoy.github.io/bjc-r/prog/building-blocks/valid-date.xml)

_Important:_ as this example shows there can be huge benefits to using our own custom blocks. The process in this exercise is aptly referred to as functional decomposition, whereby we break a larger function into smaller pieces and then reassemble the original function. This is one important way that we can build abstractions as the larger function \(valid-date?\) doesn't need to know what the functions that compose it do, it can just assume that they work.

