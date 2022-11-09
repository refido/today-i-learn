# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/07 / Week 4

![image](/images/16.png)

We talked about what we were going to do, and then we went to Zoom to go over last week's test material, which will be brought by several students, including myself.

- What did I learn today?

Middleware is a tool that transforms the result of a request before it is sent as a response. In this case, chunks, a redux library that allows us to interact with any API declaratively, enables us to define API endpoints across chunks in the webpack chunked application. As a result, we can apply some 'logic' to, say, redux actions.

We can import the API endpoint constant and perform API actions after adding the redux-chunk reducer to the Redux store and creating an API helper file.

```js
// GET https://api.example.com/items/12
api.getItem({ id: 12 });

// GET https://api.example.com/items/12?custom=query
api.getItem({ id: 12, custom: 'query' });

// POST https://api.example.com/items
api.createItem({ name: 'my-item', price: 100 });

// PATCH https://api.example/items/12
api.updateItem({ id: 12 }, { price: 200 });

// DELETE https://api.example.com/items/12
api.deleteItem({ id: 12 });
```

We can also dispatch API request promises as Redux actions, which are stored in your application's state under an API key.

```js
const getItem = id => {
    return api.getItem({ id });
};
```

- What did I do well?

Learn how to create APIs and how to use them in React.

- What needs to improve?

Consume the API so that creating the frontend is simple.
