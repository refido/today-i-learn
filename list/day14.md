# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/03 / Week 3

![image](/images/13.png)

Today's quiz was particularly difficult because I had to solve the error and explain why it occurred. The worst-case scenario is when the error does not appear explicitly, forcing me to search very carefully, even if it means reading a line of code.

- What did I learn today?

Accuracy is the most important lesson I learned today, because if I'm not careful, I'll have a hard time finding errors or bugs, and it can even affect the development of apps later on.

an example is when the correct data will not load when entering the card details page marked complete.

The error occurred because the id was not sent to Detail.jsx; this was caused by the index filling the position of the id; as a result, the data sent was 0 rather than the desired id; to resolve this, we must delete the index and replace it with todo.id, as shown below.

before:

```js
todos.map((todo, index) => { //delete index
          if (todo.isDone) {
            returns (
              <StTodoContainer key={todo.id}>
                <StLink to={`/${index}`} key={todo.id}> //change this
                  <div>상세보기</div>
                </StLink>
                <div>
                  <h2 className="todo-title">{todo.title}</h2>
                  <div>{todo.body}</div>
                </div>
                <StDialogFooter>
                  <StButton
                    borderColor="red"
                    onClick={() => onDeleteTodo(todo.id)}
                  >
                    ️
                  </StButton>
                  <StButton
                    borderColor="green"
                    onClick={() => onToggleStatusTodo(todo.id)}
                  >
                    {todo.isDone ? "취소!" : "완료!"}
                  </StButton>
                </StDialogFooter>
              </StTodoContainer>
            );
          } else {
            return null;
          }
        }
```

```js
after:
todos.map((todo) => {
          if (todo.isDone) {
            returns (
              <StTodoContainer key={todo.id}>
                <StLink to={`/${todo.id}`} key={todo.id}> //todo.id
                  <div>상세보기</div>
                </StLink>
                <div>
                  <h2 className="todo-title">{todo.title}</h2>
                  <div>{todo.body}</div>
                </div>
                <StDialogFooter>
                  <StButton
                    borderColor="red"
                    onClick={() => onDeleteTodo(todo.id)}
                  >
                    ️
                  </StButton>
                  <StButton
                    borderColor="green"
                    onClick={() => onToggleStatusTodo(todo.id)}
                  >
                    {todo.isDone ? "취소!" : "완료!"}
                  </StButton>
                </StDialogFooter>
              </StTodoContainer>
            );
          } else {
            return null;
          }
        }
```

- What did I do well?

Because I already know which functions to use, it aids me in reducing the amount of code that contains errors or bugs. The cancel button, for example, will not function.

The cancel button will not work because the onToggleStatusTodo function does not have an id parameter. Because the function requires a parameter, as shown below, we must add the parameter id to the onToggleStatusTodo function.

```js
onClick=() => onToggleStatusTodo(id)
```

- What needs to improve?

Looking for bugs and errors is something that should be considered and studied more thoroughly, because bugs and errors are frequently found during the development of an application.
