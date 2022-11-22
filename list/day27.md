# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/22 / Week 6

![image](/images/27.png)

Today, we finished the team tasks that had been assigned to us, then we talked about finishing the personal tasks that had been assigned to us, by asking about the challenges that each of us faced and then looking for solutions to these challenges.

- What did I learn today?

We will now connect MongoDB to the API to send and receive data!

To accomplish this, the code requires a DB client to connect to the database.
We'll use a tool called 'mongoose' to connect to the database.

In MongoDB, every piece of data is defined as a **document**.

One or more **Key-Value** pairs

```js
{
    "_id": ObjectId("6682192a1c155bd2f27881"),
    "name": "test",
}
```

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
