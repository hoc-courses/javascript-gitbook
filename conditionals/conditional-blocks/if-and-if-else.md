# If and If Else

Now that we have the idea of predicates under our belt, we can finally express full "if-then" statements, such as "if the weather is nice, you should go outside." This can be expressed in Snap using the ![if](https://beautyjoy.github.io/bjc-r/img/blocks/if.png) block. Notice how the first slot is shaped just like a predicate block. `if` blocks only know how to handle yes/no questions, so you should only ever put predicate blocks into this slot. The C-shaped part of the `if` block is where you put the commands that should be run if the condition is true. Let's take a look at an example:

![](https://beautyjoy.github.io/bjc-r/img/cond/mood.png)

In the above example, we had several possible cases to consider. However, in many situations, there are only two main cases. Take for example, the following sentence: "If a number is divisible by 2, it is even. Otherwise it is odd." For these situations we have the ![if-else](https://beautyjoy.github.io/bjc-r/img/blocks/if-else.png) block. It works like this:

![](https://beautyjoy.github.io/bjc-r/img/cond/even-or-odd.png)

Here, we didn't need to have an additional "if," because all whole numbers are either even or odd. If the boolean expression \(`x mod 2 = 0`\) evaluates to `false`, we know that the number is not even and thus must be odd.

If you haven't seen the ![\(\) mod \(\)](https://beautyjoy.github.io/bjc-r/img/blocks/mod.png) block before, it reports the remainder \(or "modulus"\) when the first input is divided by the second. For example, `5 mod 2` reports `1` because `5 / 2 = 2 remainder 1`. This block is especially useful for checking whether a number is divisible by another, because the remainder will be 0. ![\(x mod 2\) = 0](https://beautyjoy.github.io/bjc-r/img/cond/x-mod-2-equals-0.png) is the same as asking if `x` is divisible by 2 \(i.e. that `x` is even\).

