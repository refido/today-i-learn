# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/18 / Week 6

![image](/images/25.png)

Today, Justin's mentor explains and demonstrates how to use redux in React. by utilizing all of the previously taught packages, such as redux, react-redux, redux-thunk, axios, bootstrap@4.6.0, react-router-dom, @redux-devtools/extension, and others. Even though I understand the material explained by mentor Justin, I occasionally forget because it appears that I need to repeat the exemplary steps many times in order to remember it better.

- What did I learn today?

Debug application state changes using Redux DevTools. Redux development workflow is enhanced by extensions. Aside from Redux, it can be used with other state-management architectures. This can assist us in identifying bugs and errors as they occur in the state.

- What did I do well?

Axios is introduced as a node.js and browser-based promise-based http client. In other words, consider it a package used to communicate with the server via http.

```js
import React, { useEffect, useState } from "react";
import axios from "axios"; // import axios 

const App = () => {
  const [todos, setTodos] = useState(null);

 // Create a function that makes a get request through axios.
 // Since we need to do asynchronous processing, we process it through async/await syntax.
  const fetchTodos = async () => {
    const { data } = await axios.get("http://localhost:3001/todos");
    setTodos(data); // Set the data fetched from the server as the state of useState.
  };
 
 // Use useEffect to execute the created function when the component is mounted.
  useEffect(() => {
  // Put the created function in the effect statement and execute it.
    fetchTodos();
  }, []);

 // Check through the console whether data fetching is normal.
  console.log(todos); // App.js:16
  return <div>App</div>;
};

export default App;
```

- What needs to improve?

Learn how to use API. The API uses /fakeApi as the base URL for the endpoints and supports the standard GET/POST/PUT/DELETE HTTP methods for /fakeApi/posts, /fakeApi/users, and fakeApi/notifications. It is defined in src/api/server.js. There are various types of async middleware for Redux, each of which allows you to write your logic in a different syntax. The most common async middleware is redux-thunk, which allows you to write plain functions that may contain async logic directly. The configureStore function of Redux Toolkit automatically configures the thunk middleware by default, and we recommend using thunks as the standard approach for writing async logic with Redux.
