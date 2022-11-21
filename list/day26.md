# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/21 / Week 6

![image](/images/26.png)

Today, Justin's mentor explains Monolithic and Microservices. A monolithic application is composed of a single unified unit, whereas a microservices architecture is composed of smaller, independently deployable services.

![image](/images/Monolithic-vs-Microservices-1024x473.png)

A monolithic architecture is a traditional model of a software program that is built as a unified unit that is self-contained and independent of other applications. The term "monolith" is frequently associated with something large and glacial, which is not far from the truth of a monolith architecture for software design.

A microservices architecture, also known simply as microservices, is a design method that is based on a series of independently deployable services. These services each have their own business logic and database, and they all serve a specific purpose. Each service undergoes updating, testing, deployment, and scaling. Microservices divide major business concerns into separate, independent code bases.

- What did I learn today?

All computers, just as we can communicate through "words," can communicate through "networks."
In the real world, "language" (for example, Korean) is a method of expression, and "speech" is a means of expression.
In the digital world, "network" is a mode of expression, and "communication protocol (for example, HTTP)" is a method of expression.

- What did I do well?

Express.js is a web framework that allows you to quickly and easily create a Node.js server.

Other web frameworks exist in addition to Express.js, but most Node.js web servers are now built using the Express.js framework.

```js
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(port, () => {
  console.log(port, 'Server is open with port!');
});
```

API Client is a tool that assists us in checking and testing the API requests that we wrote during the development stage. API Client can assist you in accelerating development or avoiding fatal errors.

- What needs to improve?

  - A type of object that enables JavaScript to handle **asynchronous processing** in a synchronous manner. You can easily perform asynchronous processing with this object, even in JavaScript with a **non-blocking model.**
  - Interface for Promise Constructors,  Only functions can be passed to the 'executor,' and the words'resolve' and'reject' are injected as 'arguments.'

```jsx
new Promise(executor);

// example
new Promise((resolve, reject) => {
 // statement
});
```
