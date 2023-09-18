<h1>♛ Nodejs FAQ interviews repository ♛ </h1>

<h2>Motivation</h2>

<p>Having a tracking log list for all the questions, projects and stuff for over the interviews of Nodejs. </p>

- What is NodeJs? 
<pre>Nodejs is a very popular scripting languaje that is primarily used for a server-side scripting requirements</pre>

- What is the difference between  Nodejs and JavaScript? 
<pre>Javascript is the entirely programming language and Node Js is a scripting language as interpreter of Javascript</pre>

- Can you briefly explain the working of Nodejs? 
<pre>Nodejs is an entity that runs in a virtual environment, using Javascript as the primary scripting language.
It uses a simple V8 environment to run on, which helps in the provision of features like the non-blocking I/O and a single-threaded event loop</pre>

- Where is Nodejs used? 
<pre>Nodejs is used in a variety of domains. But, it is very well regarded in the design of the following concepts:
- Network application 
- Distributed computing
- Responsive web apps
- Server-Client applications </pre>

- What is the difference between Nodejs and Angular? 
<pre>Nodejs is used in:
- Situations where scalability is a requirement
- Ability to generate queries in a database 
- Mainly used to develop small/medium-sized applications 
- Provides many frameworks such as Sails, partial, and express

Angular is used in:
- Best fit for the development of real-time applications 
- Ability to simplify an application into the MVC architecture
- Mainly used to develop real-time interactive web applications 
- Coded in TypeScript </pre>

- Why is Nodejs single-threaded? 
<pre>Nodejs works on the single-threaded model to ensure that there is support for asynchronous proccesing.

With this, it makes it scalable and efficient for applications to provide high performance and efficiency under high amounts of load.</pre>

- What is the meaning of control flow function? 
<pre>The control flow function is a common code snippet, which executes whenever there are any asynchronous function calls made

They are used to evaluate the order in which these functions are executed in Nodejs</pre>

- Why is Nodejs so popular these days? 
<pre>Nodejs has gained an immense amount of traction as it mainly uses Javascript. It provides programmers with the following options:
- Writing Javascript on the server
- Access to the HTTP stack
- TCP and other protocols
- Direct database access
</pre>

- What is an event loop in Nodejs? 
<pre>The working of an event loop begins with the occurrence of a callback wherever an event begins. This is usually run by a specific listener. Nodejs will keep executing the code after the functions have been called, without expecting the output prior to the beginning.</pre>

- Explain REPL in the context of Nodejs 
<pre>
- Read: reads the user's input, parses it into Javascript data-structure and then stores it in the memory.
- Eval: Receives and evaluates the data structure.
- Print: Prints the final result
- Loop: loops the provided command until CTRL+C is pressed twice 
</pre>

- What do you understand by a test pyramid? 
<pre> Unit tests -> Integration tests -> End to end </pre>

- Explain the purpose of module.exports? 
<pre>A module in Nodejs is used to encapsulate all the related codes into a single unit of code which can be interpreted by shifting all related functions into a single file</pre>


- What do you understand by Reactor Pattern in Nodejs? 
<pre> Reactor Pattern in Nodejs is basically a concept of non-blocking I/O operations, this pattern povides a handler that is associated with each I/O operation, As soon as an I/O request is generated, it is then submitted to a demultiplexer, this demultiplexer is a notification interface which is capable of handling concurrency in non-blocking I/O mode, it also helps in collecting each and every request in the form of an event and then place each event in a queue, the resulting in the generation of the Event Queue</pre>


- Explain the concept of middleware in Nodejs? 
<pre>Middleware is a function receives the request and response objects
- Commonly performed tasks
- Execute any type of code
- Update or modify the request and the response objects
- Finish the request-response cycle 
- Invoke the next middleware in the stack 
</pre>


- Differentiate between spawn() and fork() methods in Nodejs? 
<pre>
- The spawn() is used to launch a new process with the provided set of commands.
- Fork() it is a special instance of spawn() that executes a new instance of the V8 engine.
</pre>


- Explain the concept of stub in Nodejs 
<pre>Stubs are basically the programs or functions that are used for stimulating the module or component behavior, during any test cases, stubs provide the canned answers of the functions</pre>


- How assert works in Nodejs? 
<pre>Assert is used to write tests, it only provides feedback only when any of the running test cases fails, this module gives you a set of assertion tests which are then used for testing invariants, it is basically used internally by Nodejs but using require('assert') code, it can be used in other applications as well </pre>


- Differentiate between process.nextTick() and setImmediate()? 
<pre>process.nextTick() and setImmediate(), both are functions of the Timers module which help in executing the code after a predefined period 

- process.nextTick():
it waits for the execution of action till the next pass around in the event loop or once the event loop is completed only then it will invoke the callback function

- setImmediate()
It waits for the execution of action till the next pass around in the event loop or once the event loop is completed only then it will invoke the callback function</pre>


- Explain the usage of a buffer class in Nodejs ? 
<pre>Buffer class in Nodejs is used for storing the raw data in a similar manner of an array of integers, but it corresponds to a raw memory allocation that is located outside the V8 heap, it is global class that is easily accessible can be accessed in an application without importing a buffer module.

Buffer class is used because pure Javascript is not compatible with binary date</pre>


- How does Nodejs handle the child threads ? 
<pre>Nodejs is a single threaded process and doesn't expose the child threads or thread management methods</pre>


- What is the use of NODE_ENV? 
<pre>If the project is in the production stage, Nodejs promotes the convention of making use of NODE_ENV variable to flag it</pre>


- Differentiate between Nodejs vs Ajax? 
<pre>
- Nodejs is a server-side technology
- Required to develop the server software that are typically executed by the servers instead of the web browsers

- Ajax is client-side technology
- Required for updating or modifying the webpage contents wihout having to refresh it </pre>

- What do you understand by an Event Emitter in Nodejs ? 
<pre>
    const EventEmitter = require('events');
    class MyEmitter extends EventEmitter{ }
    const myEmitter = new MyEmitter();

    myEmitter.on('event', () => {
        console.log('an event ocurred!');

    });

    myEmitter.emit('event');
</pre>
- What is the call stack, callback queue and how they interact within the event loop?
  <pre>
    Call stack: In Node.js, the call stack is used to keep track of the execution of synchronous functions. When a function is called synchronously, it is added to the top of the call stack, and when it returns, it is       removed from the stack. This means that if a function is blocking or takes a long time to complete, it will block the execution of other functions until it returns.

    Callback Queue: In Node.js, when an asynchronous operation completes, the callback function is not executed immediately. Instead, it is placed in a queue called the callback queue. The callback queue holds all the       completed callback functions that are waiting to be executed. By using callbacks and the callback queue, you can avoid blocking the event loop and ensure that your code can handle multiple requests simultaneously.

    Event loop: The event loop is a fundamental concept in Node.js that allows for asynchronous programming. It is a continuously running process that monitors the call stack and the callback queue, and executes tasks       when the call stack is empty.

    The event loop works in a cycle, repeatedly checking the call stack and the callback queue. When the call stack is empty, the event loop looks for the next task in the callback queue to execute. When a task is           picked up from the queue, it is added to the call stack and executed
  </pre>



<br>

## Authors

* **Aldair Bernal** - *Full work* - [Aldair47x](https://github.com/Aldair47x)

Follow me! – [aldair47x@Twitter](https://twitter.com/aldair47x) – aldair47x@gmail.com

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
