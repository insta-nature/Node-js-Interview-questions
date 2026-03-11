## 9.Why is Node.js single-threaded?
Node.js was created explicitly as an experiment in async processing. This was to try a new theory of doing async processing on a single thread over the existing thread-based implementation of scaling via different frameworks.

## 10. What are the advantages of using promises instead of callbacks?
The main advantage of using promise is you get an object to decide the action that needs to be taken after the async task completes. This gives more manageable code and avoids callback hell.

## 11. What is control flow in NodeJS?
In Node.js, control flow refers to the order in which asynchronous operations (like file reads, API calls, DB queries) are executed and how their results are handled.

Because, Node.js is non-blocking and event-driven, tasks don’t always finish in the order they start. Control flow ensures they are managed correctly.

## 12. What do you mean by event loop in NodeJS?
Event loops handle asynchronous callbacks in Node.js. It is the foundation of Node.js's non-blocking input/output in Node.js, making it one of the most important environmental features.

## 13. What is the order in which control flow statements get executed?

The order in which the statements are executed is as follows:

- Execution and queue handling
- Collection of data and storing it
- Handling concurrency
- Executing the next lines of code

## 14. main disadvantages of NodeJS?
Here are some main disadvantages of NodeJS listed below:

- Single-threaded nature: It may not fully utilize multi-core CPUs, limiting performance.
- NoSQL preference: Relational databases like MySQL aren't commonly used.
- Rapid API changes: Frequent updates can introduce instability and compatibility issues.

## 15. What is REPL in NodeJS?
REPL in NodeJS stands for Read, Evaluate, Print, and Loop. It is a computer environment similar to the shell which is useful for writing and debugging code as it executes the code in on go.

- Read: It reads the input provided by the user (JavaScript expressions or commands).
- Eval: It evaluates the input (executes the code).
- Print: It prints the result of the evaluation to the console.
- Loop: It loops back, allowing you to enter more code and get immediate results.

## 18. What is package.json in NodeJS?
package.json in NodeJS is a metadata file that contains project-specific information such as dependencies, scripts, version, author details, and other configuration settings required for managing and building the project.

## 19. How to create the simple HTTP server in NodeJS?
You can create a simple HTTP server in NodeJS using the built-in http module:

```
const http = require('http');

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Hello, World!');
});
server.listen(3000, () => {
  console.log('Server is running at http://localhost:3000/');
});
```

## 21. What are promises in NodeJS?
A promise is an advancement of callbacks in NodeJS. In other words, a promise is a JavaScript object that is used to handle all the asynchronous data operations. While developing an application, you may encounter that you are using a lot of nested callback functions, which causes a problem of callback hell. Promises solve this problem of callback hell.\

## 28. What is callback hell?
Callback hell is an issue caused by a nested callback. This causes the code to look like a pyramid and makes it unable to read To overcome this situation, we use promises.

## 31. What are the different types of HTTP requests?
The different types of HTTP requests are mentioned below:

- GET: Retrieve data.
- POST: Create new resource.
- PUT: Update an entire resource.
- PATCH: Partially update a resource.
- DELETE: Remove a resource.

## 33. Explain the use of the passport module in NodeJS
The passport module is used for adding authentication features to our website or web app. It implements authentication measure which helps to perform sign-in operations.

## 34. What is a, fork in NodeJS?
Fork is a method in NodeJS that is used to create child processes. It helps to handle the increasing workload. It creates a new instance of the engine which enables multiple processes to run the code.

## 35. What are the three methods to avoid callback hell?
The three methods to avoid callback hell are:

- Using async/await()
- Using promises
- Using generators

## 37. What is CORS in NodeJS?
The word CORS stands for “Cross-Origin Resource Sharing”. Cross-Origin Resource Sharing is an HTTP-header based mechanism implemented by the browser which allows a server or an API to indicate any origins (different in terms of protocol, hostname, or port) other than its origin from which the unknown origin gets permission to access and load resources. The cors package available in the npm registry is used to tackle CORS errors in a NodeJS application.

## 40. How do you manage packages in your NodeJS project?
In a NodeJS project, package management is handled through npm (Node Package Manager), which is the default package manager for NodeJS, which allows you to install and manage third-party packages and create and publish your packages. 

## 41. What is the purpose of NODE_ENV?
The `NODE_ENV` environment variable in NodeJS is used to specify the environment in which the NodeJS application is running. It helps in distinguishing between different stages of the application's lifecycle, such as development, testing, or production, and allows you to customize the behavior of the application based on that environment.

## 44. What is a cluster in NodeJS?
Due to a single thread in NodeJS, it handles memory more efficiently because there are no multiple threads due to which no thread management is needed. Now, to handle workload efficiently and to take advantage of computer multi-core systems, cluster modules are created that provide us the way to make child processes that run simultaneously with a single parent process.

## 45. Explain some of the cluster methods in NodeJS
Fork(): It creates a new child process from the master. The isMaster returns true if the current process is master or else false.
isWorker: It returns true if the current process is a worker or else false.
process: It returns the child process which is global.
send(): It sends a message from worker to master or vice versa. 
kill(): It is used to kill the current worker.

## 46. How to manage sessions in NodeJS?
Session management can be done in NodeJS by using the express-session module. It helps in saving the data in the key-value form. In this module, the session data is not saved in the cookie itself, just the session ID.

## 47. How many types of API functions are there in Node.js?
There are two types of API functions:

Asynchronous, non-blocking functions - mostly I/O operations which can be fork out of the main loop.
Synchronous, blocking functions - mostly operations that influence the process running in the main loop.

## 48. How can we implement authentication and authorization in NodeJS?
Authentication is the process of verifying a user’s identity, while Authorization determines what actions or resources that user is allowed to access. In Node.js, these can be implemented using packages such as Passport (for strategies like OAuth, Google, GitHub, etc.) and JWT(jsonwebtoken) for token-based authentication and role-based authorization.

## 49. How to Connect NodeJS to a MongoDB Database?
To connect to the MongoDB database write the following code after installing the Mongoose package:

```
const mongoose = require("mongoose");

mongoose.connect("DATABASE_URL_HERE", {
   useNewUrlParser: true,
   useUnifiedTopology: true
});
```

## 54. What is web socket?
Web Socket is a protocol that provides full-duplex (multiway) communication i.e. allows communication in both directions simultaneously. Web Socket is a modern web technology in which there is a continuous connection between the user’s browser (client) and the server. In this type of communication, between the web server and the web browser, both of them can send messages to each other at any point in time.

## 58. What is an Event Emitter in Node.js?
In Node.js, an Event Emitter is a class that allows objects to emit events and register listeners (callbacks) to handle those events. It is part of the events module and is commonly used to handle asynchronous events and to implement an observer pattern, where an object (the emitter) triggers events, and other objects (listeners) respond to those events.
