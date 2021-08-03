# Lab - Using Multiple If Statements



### Using Multiple `If` Statements

1. Make a ![state of water \(\)](https://bjc.edc.org/Sept2015/bjc-r/img/cond/state-of-water.png) block that takes in a temperature and says whether water will be liquid, solid, or gas at that temperature.
2. Make a ![traffic signal \(\)](https://bjc.edc.org/Sept2015/bjc-r/img/cond/traffic-signal.png) block that when given the words "red," "yellow," or "green," makes the sprite say the appropriate action. For example ![traffic signal \(&apos;green&apos;\)](https://bjc.edc.org/Sept2015/bjc-r/img/cond/traffic-signal-green.png) should make the sprite say "go." Decide what should happen if your `traffic signal` block gets something _other_ than "red," "yellow," or "green."
3. Click on this image [![red, yellow, and green stoplights](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/three-color-stoplights.png) ](http://snap.berkeley.edu/snapsource/snap.html#open:https://bjc.edc.org/Sept2015/bjc-r/prog/conditionals/stoplight-project.xml)to load stoplight costumes. Edit `traffic signal` so that it changes the sprite's costume to the correct color.

**Debugging code**

1. Load [these three scripts](http://snap.berkeley.edu/snapsource/snap.html#present:Username=Paul&ProjectName=U2L1p2).

   Only two of them work properly.

   Experiment with them and look at the code to see what they do. Explain what causes the buggy one to fail.

   When the sprite asks its question, you will see an "answer space" at the bottom of the stage. ![Answer space on stage](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/SpriteAskingQuestion,withAnswerBox.png)

   Type your answer there and click the check box \(or hit return\).![forever \[ask \(which direction do you want the sprite to move? Type up, down, right, or left and wait\); if answer = up \[go to x position, y position + 20\]; if answer = down \[go to x position y position - 20\]; if answer = right \[go to x position + 20 y position\]; if answer = left \[go to x position - 20 y position\]; if answer = stop \[stop all\]; if not \(answer = up\) or \(answer = down\) or \(answer = right\) or \(answer = left\) or \(answer = stop\) \[think \(huh?!\) for 2 seconds\] \]](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/ScriptForU2L1p2n1_ask-direction-up-down-left-right-and-move.png)

   ![Talk with Your Partner](https://bjc.edc.org/Sept2015/bjc-r/img/icons/talk-with-your-partner.png)![forever \[ask \(which direction do you want the sprite to move? Type up, down, right, or left and wait\); if answer = up \[go to x position, y position + 20\] else if answer = down \[go to x position y position - 20\] else if answer = right \[go to x position + 20 y position\] else if answer = left \[go to x position - 20 y position\] else if answer = stop \[stop all\] else \[think \(huh?!\) for 2 seconds\] \]](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/ScriptForU2L1p2n1_ask-direction-up-down-left-right-and-move_if-else_version.png)

   ![forever \[ask \(which direction do you want the sprite to move? Type up, down, right, or left and wait\); if answer = up \[go to x position, y position + 20\]; if answer = down \[go to x position y position - 20\]; if answer = right \[go to x position + 20 y position\]; if answer = left \[go to x position - 20 y position\]; if answer = stop \[stop all\] else \[think \(huh?!\) for 2 seconds\] \]](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/ScriptForU2L1p2n1_ask-direction-up-down-left-right-and-move_buggy.png)

**Analyzing code**

Load [these three blocks](http://snap.berkeley.edu/snapsource/snap.html#present:Username=Paul&ProjectName=U2L1p2b) that use `if` and `if-else` and try each one.

With your pair programmer _figure out **how** each one does what it does_.

Two of these scripts use the ![abs \(\)](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/abs.png) block. In the Operators palette, this block shows up as ![sqrt \(10\)](https://bjc.edc.org/Sept2015/bjc-r/img/blocks/sqrt-of-10.png).

To select `abs` \(or any of several mathematical functions, click the drop-down menu.

The **absolute value** of a number is that number's _distance from zero_.

![Number line from -5 to 5 showing that -4 and 4 are the same distance from 0.](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/Numberline.png)

As the number line shows, -3 and 3 are the same distance from 0, so `abs(-3)` and `abs(3)` are both 3. `abs(-2.5)` is 2.5.

In mathematical notation, we write `abs(-3)` as **\|**-3**\|**.

1. ![a mysterious block](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/mystery1-back-and-forth.png)
2. ![a mysterious block](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/mystery2-back-and-forth-no-abs.png)
3. ![a mysterious block](https://bjc.edc.org/Sept2015/bjc-r/img/2-conditionals-abstraction-testing/mystery3-dvd-player-screen-saver.png)

