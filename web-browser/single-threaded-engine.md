# Asynchronous Web Events

JavaScript code execution is synchronous, meaning it cannot be interrupted. The JavaScript Engine will execute the instructions within a script from top to bottom, line by line, all the way until the end.

But there are certain instructions within a web application that cannot be synchronous.  For example, if you were to make a _synchronous_ HTTP request, then no other JavaScript code could run until the request completes and the site would become unresponsive. 

### Some code needs to be _asynchronous_.

In computer science, asynchronous means suspending executing code, allowing other code to run in the same thread, and eventually resuming the suspended code. This technique is utilized to avoid blocking an entire thread while waiting for some slow resource \(like an HTTP request\).

### HTTP requests are asynchronous

The web browser provides the **XMLHttpRequest** object for executing HTTP requests asynchronously.  In your code you create the XMLHttpRequest object and supply a function \(callback\) that will be called when the HTTP request completes. 

To make the call asynchronous, the XMLHttpRequest object suspends the code that is making the request, allowing the JavaScript Engine to continue executing the script, and then initiates the HTTP request in another thread. When the HTTP request is complete, the suspended code is resumed by placing the callback function in a task queue, which contains code that should be executed by the JavaScript Engine.

The web browser has an event loop that continually checks for callback functions in the queue and delegates them in order to the JavaScript Engine when it is not busy executing other code.

![](../.gitbook/assets/image%20%28156%29.png)

### User events are asynchronous

User events, such as a button click, are processed using this same technique. Your code calls a method on the document object, `document.addEventHandler()`, and supplies a function \(callback\) that will be executed when the button click occurs. 

The web browser will suspend the callback function until the user event occurs, and then resumes the function by placing it in the task queue for the JavaScript Engine to process when it becomes available.

### Long running tasks should be asynchronous

Some tasks just take a long time to run and we don't want them to block. To simulate such a scenario, look at the following code. There is a while loop inside the `task()` function that emulates a time-consuming tasks. The `task()` function is a blocking function.

```javascript
function task(message) {
    // emulate time consuming task
    let n = 10000000000;
    while (n > 0){
        n--;
    }
    console.log(message);
}

console.log('Start script...');
task('Download a file.');
console.log('Done!');
```

The script just hangs for a few seconds \(depending on how fast the computer is\) and issues the following output:

```text
Start script...
Download a file.
Done!
```

To prevent blocking functions from blocking other activities, you can utilize the window object's setTimeout method, which will use the same technique as the previous examples to suspend the current code and resume it at a later time.  

Unlike the previous cases, where the browser is invoking the callback function when an HTTP request completes, or a user clicks a button, in the case of the setTimeout method, the browser sets a timer to go off when the amount of time specified completes, and when the timer expires, it invokes the callback.

Here is an example of a long running task and how you can utilize the setTimeout method.

```javascript
console.log('Start script...');

setTimeout(() => {
    task('Download a file.');
}, 1000);

console.log('Done!');
Code language: JavaScript (javascript)
```

In this example, you will see the message `'Start script...'` and `'Done!'` immediately. And after a while, you will see the message `'Download a file'`.

Here is the output:

```text
Start script...
Done!
Download a file
```

### 

### Resources

{% embed url="https://www.macarthur.me/posts/when-dom-updates-appear-to-be-asynchronous" %}

{% embed url="https://www.javascripttutorial.net/javascript-event-loop/" %}

