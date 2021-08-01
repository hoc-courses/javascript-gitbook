# The DRY Principle

 **DRY** stand for **Don't Repeat Yourself,** a basic principle of software development aimed at **reducing repetition** of information.

> _Every piece of knowledge must have a single, unambiguous, authoritative representation within a system. - The Pragmatic Programmer_

#### Why is DRY important?

* Write code once, use it often.
* Change code in one place, see the change in all instances.
* Less code is good: It saves time and effort, is easy to maintain, and also reduces the chances of bugs.

#### Dry Violations

Writing/copying and pasting the same code or logic again and again.

Let's start out with a simple example. We want to draw a square. Here are the individual steps for drawing a square.

![](.gitbook/assets/image%20%2833%29.png)

Now let's draw a series of squares.

![](.gitbook/assets/image%20%2813%29.png)

Obviously, this is violating the DRY principle. There are a few common programming techniques to allow you to adhere to the DRY principle.

#### Refactoring

Refactoring is when you take some code that is functionally correct and modify it to do the same task more efficiently.

#### Loops

One way to reduce redundant code is to introduce a loop. In Snap! there is the repeat block, which will repeat a series of instructions a specified number of times. 

In the code below, we refactored the code into few lines of code by utilizing the repeat block to execute the same instructions three times.

![](.gitbook/assets/image%20%2811%29.png)



