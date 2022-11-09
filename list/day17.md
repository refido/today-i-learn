# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/08 / Week 4

![image](/images/17.png)

We discussed our plans and worked on the team project we discussed at the previous meeting. We'll make a Place Advisory so that this application displays comments from places that have been visited, and then other people can comment on these comments.

- What did I learn today?

So far, I've figured out how to use json-server to create a fake API or a temporary database.

```js
{
  "todos": [
    {
      "id": 1,
      "title": "json-server",
      "content": "Let's learn json-server."
    }
  ]
}
```

We can also dispatch API request promises as Redux actions, which are stored in your application's state under an API key.

```js
//get
const fetchTodos = async () => {
    const { data } = await axios.get("http://localhost:3001/todos");
    setTodos(data);
};
//post
const onSubmitHandler = (todo) => {
    axios.post("http://localhost:3001/todos", todo);
};
//delete
const onClickDeleteButtonHandler = (todoId) => {
    axios.delete(`http://localhost:3001/todos/${todoId}`);
};
//patch
 const onClickEditButtonHandler = (todoId, edit) => {
    axios.patch(`http://localhost:3001/todos/${todoId}`, edit);
  };
```

- What did I do well?

How to use json-server to create and manipulate fake api data or a temporary database.

- What needs to improve?

How to use the reducer from redux and thunk redux.
