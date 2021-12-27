# Event-Loop-in-Javascript


JavaScript is a single-threaded synchronous programming language

It means that the main thread where JavaScript code is run, runs in one line at a time manner and there is no possibility of running code in parallel.
Memory allocation in JavaScript:

1) Heap memory: Data stored randomly and memory allocated.
2) 2) Stack memory: Memory allocated in the form of stacks. Mainly used for functions.

Function call stack: The function stack is a function which keeps track of all other functions executed in run time. Ever seen a stack trace being printed when you ran into an error in JavaScript. That is nothing but a snapshot of the function stack at that point when the error occurred.
Event loop: An event loop is something that pulls stuff out of the queue and places it onto the function execution stack whenever the function stack becomes empty.
Here the callback function in the event queue has not yet run and is waiting for its time into the stack when the SetTimeOut() is being executed and the Web API is making the mentioned wait. When the function stack becomes empty, the function gets loaded onto the stack as shown below:That is where the event loop comes into picture, it takes the first event from the Event Queue and places it onto the stack i.e in this case the callback function. From here, this function executes calling other functions inside it, if any.
