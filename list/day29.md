# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/24 / Week 6

![image](/images/29.png)

Today, we completed the personal assignments that had been assigned to us, followed by a discussion of the questions that had been assigned to us, and we also assisted each other in resolving some personal assignment issues. And if you want to see the results of the API that has been created, click [here]([list/day29.md](https://evening-castle-44105.herokuapp.com/api/posts)).

- What did I learn today?

API that fetches the entire list of users.

```js
{
router.get('/user', async (req, res) => {
    const user = await Posts.find({}, { name: 1, ID: 1, pw: 1 })
    const result = users.map(user => {
        return user
    })
   
   if (users.length === 0) {
        return res.status(400).json({
            success: true,
            errorMessage: 'Failed to Fetch User List'
        })
    }

    res.json({ data: result })
})
}
```

API that fetches user information when a particular user id is given

```js
router.get('/user/:userid', async (req, res) => {
    const { userid } = req.params
    const user = await Posts.find({ userid: +userid }, { name: 1, ID: 1, pw: 1 })

    if (user.length === 0) {
        return res.status(400).json({
            success: true,
            errorMessage: 'User Information Not Found'
        })
    }

    res.json({ data: user })
})
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
