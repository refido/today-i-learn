# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/02 / Week 3

![image](/images/12.png)

Today, we finish a personal task and assist one another; this week's personal task is much more difficult than the previous week's.

- What did I learn today?

Ducks is a modular pattern that groups actions, action types, and reducers.

According to the Ducks' proposal:

1. A function called reducer MUST be exported by default ()

2. MUST export its action creators as functions

3. Action types must be in the form npm-module-or-app/reducer/ACTION TYPE.

4. MAY export its action types as UPPER SNAKE CASE if an external reducer needs to listen for them or if it is a published reusable library.

- What did I do well?

By far my most familiar pattern is the duck. I was in the middle of putting Redux into action on a large React SPA. I had already created the file structure because I had seen and used it on smaller applications before. However, as the application grew in size, I began to wonder if my setup would scale well. A coworker advised me to look into 'Redux Ducks.' 'That's a ridiculous name,' I thought.

- What needs to improve?

I need to improve my understanding of how to use functional updates in useState. The state is a React built-in object that stores data or information about the component. The state of a component can change over time, and when it does, the component re-renders.
