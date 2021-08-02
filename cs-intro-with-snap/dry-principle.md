# The DRY Principal

 **DRY** stand for **Don't Repeat Yourself,** a basic principle of software development aimed at **reducing repetition** of information.

> _Every piece of knowledge must have a single, unambiguous, authoritative representation within a system. - The Pragmatic Programmer_

#### Why is DRY important?

* Write code once, use it often.
* Change code in one place, see the change in all instances.
* Less code is good: It saves time and effort, is easy to maintain, and also reduces the chances of bugs.

#### Dry Violations

Writing/copying and pasting the same code or logic again and again.

Let's start out with a simple example. We want to draw a square. Here is an algorithm for drawing a square.

![](../.gitbook/assets/image%20%28107%29.png)

Now let's draw a series of squares.

![](../.gitbook/assets/image%20%2841%29.png)

Obviously, this is violating the DRY principle. There are a few common programming techniques to allow you to adhere to the DRY principle.

### Refactoring

Refactoring is when you take some code that is functionally correct and modify it to do the same task more efficiently.

### Loops

One way to reduce redundant code is to introduce a loop. In Snap, we can use the **repeat** block to make drawing shapes a lot easier! The **repeat** block will repeat a series of instructions a specified number of times. 

In the code below, we refactored the code into fewer instructions by utilizing the repeat block to execute the same instructions three times.

![](../.gitbook/assets/image%20%2836%29.png)

### Nested Loops

We can further refactor our code by adding another loop nested within the outer repeat block to repeat the drawing of each side of the square.

![](../.gitbook/assets/image%20%2848%29.png)

### Procedures

A **procedure** is a named sequence of instructions that may take inputs and may return a value. Different languages call them by different names. Some languages call procedures _methods_ or _functions_. 

In Snap!,  you can create a new procedure by **creating a new block**. There are three categories of blocks:

* **commands** -  tells the computer to do something without returning a value.
* **reporters** - returns a value.
* **predicates** - a type of reporter, returns either true or false

Procedures have a few benefits.

### Procedures allow Abstraction

The main goal of abstraction is to handle complexity by hiding unnecessary details from the user. That enables the user to implement more complex logic on top of the provided abstraction without understanding or even thinking about all the hidden complexity.

We are going to apply that principle here to create a **command** block \(no return value\) that will be responsible for performing the instructions necessary to draw a square.

![](../.gitbook/assets/image%20%2856%29.png)

![](../.gitbook/assets/image%20%2843%29.png)

And now the code has been greatly simplified. We no longer need to think about the individual instructions necessary to draw a square. We can simply use the `drawSquare` command to perform the instructions whenever we need to draw a square.

### Procedures allow Re-use

Another important feature of writing procedures is that they can receive input that allows them to work in a wider range of circumstances.

In our `drawSquare` command, it currently hard-codes the size of the square. While this works for this particular use-case, it would be more re-usable if it allowed the user to specify the size of the square. This is done by adding input variables to a procedure.

Snap! allows the addition of input parameters by clicking on the plus sign in the command's name block.

![](../.gitbook/assets/image%20%2829%29.png)

Once the parameters are added, they can be used within the procedure by dragging them from the parameter list to where they are used.

![](../.gitbook/assets/image%20%2827%29.png)

### A DRY Solution

And now we have our finished algorithm to draw a series of three squares.

![](../.gitbook/assets/image%20%2860%29.png)

