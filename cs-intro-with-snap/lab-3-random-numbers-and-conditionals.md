# Lab - Guessing Game

In this lab you will create a guessing game. This game will draw on what we’ve learned in the past two labs and work with variables and conditionals.

**In this lab,** you will use local and global _variables_ to store information.

**On this page,** you will begin to develop a number guessing game that uses a _local variable_ to keep track of a secret number.

### Tracking the Secret Number

Start building a new command block called `number guessing game` that will contain the code for the game. Leave the Block Editor open.

In a number-guessing game, the player tries to guess the computer's secret number. The computer needs a way to store the secret number in a _variable_ so that it can compare it to the player's guesses.  
![script variables \(secret number\)](https://bjc.edc.org/bjc-r/img/2-complexity/script-variables-secret-number.png): **Variable**

A **variable** is like a box that can hold one value at a time, such as one word, one costume, or one list \(which can contain many things\). You can look at what's inside as many times as you want.

Here, we are starting to look at _data abstraction_, giving names to numbers, text, lists, etc. When you give something a name, you can refer to it without knowing exactly what the value is.

Create a script variable called secret number to store the number that the player will try to guess \(instructions below\).

**Making a Script Variable**

1. **Move a `script variables` block into the Scripting Area.** You can find it in the Variables palette. ![script variables](https://bjc.edc.org/bjc-r/img/prog/scriptvar.png)
2. **Name the variable** by clicking on the orange a at the end and typing the name you want. Here, it should be called secret number.

**Later, you will use the script variable** by dragging it out of the `script variables` block \(the way you drag an input\) and placing it where you need it in your code.

Use ![set \(\) to \(\)](https://bjc.edc.org/bjc-r/img/blocks/set-empty.png) to set the initial value of secret number to a random number from 1 to 10. The `set` menu lets you select which variable to set.  


The variable secret number is available in the `set` block only when you snap it somewhere after the `script variables` block.![set block menu selecting secret number](https://bjc.edc.org/bjc-r/img/2-complexity/set-secret-number-menu.jpg)

 Script variables are a kind of _local variable_; they work only within the script where they're created. If you drag one into a different script, it won't work. You've seen two kinds of local variables before: inputs to blocks and `for` counters.

A **local variable** can be set or used only in the environment in which it is defined. This term includes inputs to procedures and variables created by the `for` or `script variables` block.

### Checking the Player's Guess

 You'll want the computer to ask players to guess again and again until they guess correctly. To do that, you will use the ![repeat until](https://bjc.edc.org/bjc-r/img/blocks/repeat-until.png) block. `Repeat until` is a _loop_ \(just like `repeat`, `forever`, and `for`\) but also a _conditional_ \(like `if` and `if else`\). It repeats until a certain condition is met. For this program, the code should repeat until the player's answer equals the secret number.

Use `repeat until` to ask the player \(![ask \(\) and wait](https://bjc.edc.org/bjc-r/img/blocks/ask-empty-full-size.png)\) to guess the secret number until their ![answer](https://bjc.edc.org/bjc-r/img/blocks/answer-full-size.png) equals the secret number.

* Drag the secret number variable out of the `script variables` block to use it.
* The `ask` and `answer` blocks go together. If you use `ask` to ask a question, the user's answer will be reported by `answer`.

After the player guesses the secret number, make the computer congratulate the player.

`Repeat until` makes its decision based on the output of a hexagonal _predicate_ block.**:** 

\*\*\*\*

\*\*\*\*

**Vocabulary -** A **predicate** is a hexagon-shaped reporter that asks a true/false question such as these examples:  
![8 &amp;gt; 7 reporting true](https://bjc.edc.org/bjc-r/img/2-complexity/8-gt-7-reporting-true.png) ![6 &amp;gt; 7 reporting false](https://bjc.edc.org/bjc-r/img/2-complexity/6-gt-7-reporting-false.png)

Predicates report a **Boolean value** \(either ![true](https://bjc.edc.org/bjc-r/img/blocks/true.png) or ![false](https://bjc.edc.org/bjc-r/img/blocks/false.png)\).



Predicates fit into a hexagonal input slots of conditionals, such as in ![if block](https://bjc.edc.org/bjc-r/img/blocks/if-full-size.png) and ![repeat until](https://bjc.edc.org/bjc-r/img/blocks/repeat-until.png). Predicates help conditionals _decide when to do something_.

**Vocabulary** - The `if` and `if-else` blocks are called **conditionals** because they control the code based on a true-or-false **condition**.



Use more conditional blocks and predicates to make the computer tell the player whether a guess is too big or too small: "That's too big. Try again."

 Play your game enough to see if it works the way you want. It should:

* ask the player to guess its secret number;
* say whether a wrong guess is too big or too small, and then ask again;
* congratulate the player for a correct answer.

The script variable secret number exists only until the script finishes running. When the game is played again, the program will create a new secret number variable and give it a new random number.



### Extensions

1. Right now, the script always picks a number between 1 and 10. At the start of the game, ask the player what the maximum number should be, and make your program choose a number between 1 and maximum.
2. Use another script variable to keep track of how many guesses the player makes before getting the right number. When the player guesses the secret number, say how many guesses it took.
3. Find a way to vary the language a bit so that your program does not always repeat exactly the same words in the same situation. For example, if a player guesses too high twice in a row, the program could say "That's still too big. Try another number."



Look at the script below. The computer chooses a random number and then asks the player to guess the random number.

![](../.gitbook/assets/image%20%28126%29.png)

### Pseudocode

* Pseudocode is a mix of English language and code that represents what you want your program to do. 
* It helps you determine how you want the program to work as well as what variables and methods/functions you will want to include. 
* Developing pseudocode will help you work through your logic, reducing the number of errors and potential re-writes you will have to do.

### Pseudocode Example

![](../.gitbook/assets/image%20%2863%29.png)

Represents the same process for dealing with a guessing game in which the computer generates a random number and the player guesses the number.

```bash
When flag clicked
    Set the secret number between 1 and 10
    Repeat forever
        Ask player for guess and wait
        If guess = secret number Then 
            Display “Correct” 
            Stop Script
        
```

### Step 0

Before beginning to build your program, let’s look at what variables we will need to begin the game.

* The secret number
* The guess from the player

Next, we need to figure out the tasks that the sprite and player will be enacting.

* The Sprite will begin by setting up the game’s variables and choosing the secret number.
* The Sprite will ask for a guess from the player.
* The player will input their guess.
* If the player’s guess was correct, the sprite will give the player a message and the game will end.

Note that there is a new block above that will return a random number between the two input numbers \(inclusive\). This block is in the Operator palette. You can enter a number or use a variable. Because this is a reporter block you can use it inside other blocks as an input.

![](../.gitbook/assets/1.png)

The game is pretty basic, though. In the next few steps, we are going to make the game much more like playing the number-guessing game with a person. Here are tasks to try to make the code act more like a human. Try each of these in order. When you are done, your finished code should be able to deal with all of the tasks.

### Step 1

Add to your beginning script the blocks so that the sprite welcomes the player and asks for their name before beginning.

![](../.gitbook/assets/2%20%282%29.png)

### Step 2

We want to give the player more information if they don’t guess correctly. Have the sprite tell the player if the secret number is bigger or smaller than the number that they guessed.

![](../.gitbook/assets/image%20%2897%29.png)

### Step 3

Right now, the sprite always picks a number between 1 and 10. Change this so that the sprite always picks a number between 1 and a variable named max. \(Don’t forget to add the variable.\) Add to your script so that it asks the player what they would like the maximum number to be, before choosing a random number. Use this maximum number as the highest number that the sprite will choose.

![](../.gitbook/assets/image%20%28107%29.png)

![](../.gitbook/assets/image%20%2814%29.png)

### Step 4

Now let’s keep track of how many guesses it takes before the player guesses the right number. You will need a new variable for this task and will need to add to it every time a guess occurs.

![](../.gitbook/assets/image%20%28129%29.png)

![](../.gitbook/assets/image%20%2871%29.png)

### Step 5

When the player guesses the secret number, tell them how many guesses it took, and congratulate them using their name.

![](../.gitbook/assets/image%20%2869%29.png)

![](../.gitbook/assets/image%20%2866%29.png)



## **Lab- Guessing Game version 2.0**

The Number Guessing Game that you just created had you utilize IF statements and random number generators. This week, you will expand upon that game and make it smarter! The goal of this Expanded Guessing Game \(we’ll call it, version 2.0\) is to make sprites that play the game smarter! In addition, since this will make the game much faster, we’ll make the guessing sprite have to get three guesses right to win.

Open your Guessing Game project from the last unit to use as a reference. Create a new project called yourLastName\_GuessingGame2. This version will use two sprites: one to hold the secret number and give hints and the other to try to guess the secret.

### Step 0

Before beginning to build your program, let’s look at what variables we will need and what each sprite should do to play the game.

Variables:

* The guess from the guesser sprite
* List to hold the guesses
* The number of times the guesser sprite has guessed
* The secret number
* The number of times the guessing sprite wins

Tasks: \* The First Sprite \(the guide\) needs to initialize the variables by setting them to 0 and picking a secret number.

* The First Sprite asks the second Sprite to guess.
* The Second Sprite \(the guesser\) guesses a number.
* The Second Sprite adds its guess to a list.
* The First Sprite gives a hint based on the guess.
* Repeat the second through fifth step until the guess is correct.
* Repeat the program until the second sprite wins three times.

### Step 1

You will need to set up your ‘Game Guide’ sprite \(or sprite 1\) that will be asking for the guess just as it did in your last lab. Review the task list above if needed. The sprite will need to first set up all variables \(don’t forget to initialize\) then repeatedly ask for a guess checking to see it the secret number is guessed or if a hint should be displayed. When the secret number is guessed, you want to stop and tell the number of guesses it took to win that game \(and maybe say “Congrats” or another message\). Go ahead and set up this part of your script. Don’t forget you will need to ‘ask’ the guessing sprite for its guess. What is a good way to do this? How have you communicated with another sprite earlier?

### Step 2

Let’s create a Give Hint procedure and move the blocks that handle this task into the blocks editor. Now just add the Give Hint procedure into your sprite 1’s script where it should be.

### Step 3

Now let’s work with the guessing sprite to add a list of the guesses. Remember a list is a collection that can contain multiple values of information. Think of a list as a container for multiple values. You can add, search for, and remove information from a list. Lists are very powerful data structures, and have many uses in Computer Science! For our lab, we’ll make a simple list to store the guesses that our sprite has made so far.

To create a list, click “Make a Variable” in the Variables Tab.

![](../.gitbook/assets/3.png) ![](../.gitbook/assets/4%20%282%29.png)

Call your list variable whatever you like. The name should be something descriptive and informative though. In the example above, we named the list “GuessesList”.

Now we are going to tell BYOB/SNAP that the variable is a list. Notice that when you click on the set command, you will see the variable show a list as its contents \(it will not be a list until you click on the set command\).

![](../.gitbook/assets/5%20%281%29.png)

### Step 4

Let’s make a procedure called Guess Number for the guessing sprite to guess the number. To do that select the guessing sprite and click Make a Block in the Variables palette. Let’s look at the algorithm for this new block. We want the sprite to guess a number between 1 and 10 \(inclusive\) and say the number.

Will you need a variable to hold the guess?

#### Algorithm \(Pseudocode\)

To Guess Number:  
 Set the guess to a random number between 1 and 10, inclusive  
 Say the guess.

#### Code Script in Blocks Editor

![](../.gitbook/assets/6%20%282%29.png)

Add the code into the Block Editor. Click the block in the sprite’s window to make certain it works as expected.

### Step 5

Now let’s expand this procedure so that it will keep track of the guesses this sprite has already guessed so that the sprite does not guess the same number twice. In order to do this task, we will want to keep a list of all the guesses \(myGuess\).

First, drag the add \(thing\) to \(\) block into your block editor. The “add ‘thing’ to…” block will add the myGuess value to your list. This is a very useful block that you’ll likely use in the future as well \(hint hint\). The “thing” can be replaced by either something you specify, or a variable. In this case, we want to add the number that we’ve just guessed to the list. Drag the variable “myGuess” into the Block Editor and snap it into the ‘thing’ field. It should look like this now:

![](../.gitbook/assets/7.png)

So now our block will pick a random number, say it, and add it to a list. This doesn’t quite yet accomplish what we need. What we want is for the “Guess Number” function to only choose a number as long as it hasn’t already been guessed. What we need here is a loop with an IF statement! You will need to add this in Try It! \#1.

### Try It! Guessing Game v. 2

#### Try It \#1

Expand the “Guess Number” function in the guessing sprite so that it only says the guess and adds it to the list as long as the value of myGuess is not already in the list. This block with an IF block may come in handy.

![](../.gitbook/assets/8%20%283%29.png)

#### Try It \#2

Next, let’s expand the script we have in the original sprite \(not the guessing sprite\). Add an additional loop around the game so that the “repeat until” loop keeps running until the guessing sprite has guessed the secret number correctly \(or won\) 3 times. You may need a wins variable for this \(hint\).

Run your game. Make sure the check mark beside your guesses list is checked, and you can see the list of guesses populate itself on the stage as the guessing sprite adds guesses to its list! Notice that as guesses fills up, it takes the guessing sprite a bit longer to guess. This is because the guessing sprite is making sure that he does not guess a number he’s already guessed! Unless your guessing sprite is very lucky, once guesses fills up, the guessing sprite will freeze and stop guessing. Why is this?

Fix the game so that the guessing sprite doesn’t freeze! The way we have it now, once the guessing sprite wins, the guesses list is NOT cleared. The sprite should reset the guess list after winning! In addition, you’ll notice that guesses does not reset when you restart the game. The list should also be cleared when the game starts. On top of that, all of the variables should be reset when the game starts!

This block should help: ![](../.gitbook/assets/9%20%281%29.png)

#### Try It \#3

Let’s make the guessing sprite smarter! If you were playing a guessing game with someone and had guessed 3 and was told it was too low, would you guess 3 or lower? Of course not, you would guess 4 or above. Instead of guessing between 1 and 10, now you want the guessing sprite to guess between two values that will vary as guesses are made. If you want values to vary, maybe we should use variables to determine the low and the high for our guessing sprite to guess between.

So, give the same logic to the guessing sprite.

#### Try It \#4

**Test your game!**

![](../.gitbook/assets/10.png)

### Resources

{% embed url="https://youtu.be/ps8tc0cQsGg" %}



