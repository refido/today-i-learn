# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/11 / Week 5

![image](/images/20.png)

Today we want to clone the page we like and recreate it. We can learn what skills we will need to create our own projects by remaking popular services!

- What did I learn today?

A higher-order component (HOC) is a function that takes one component and returns another. The component converts props to UI, and a higher-order component transforms one component into another. Example:

```js
// HOC.js
import React, {Component} from 'react';

export default function Hoc(HocComponent){
    return class extends Component{
        render(){
            return (
                <div>
                    <HocComponent></HocComponent>
                </div>

            );
        }
    } 
}
```

```js
/// App.js
import React, { Component } from 'react';
import Hoc from './HOC';

class App extends Component {
  
  render() {
    return (
      <div>
        Higher-Order Component Tutorial
      </div>
    )
  }
}
App = Hoc(App);
export default App;

```

- What did I do well?

Code splitting is the process of dividing code into various bundles or components that can then be loaded on demand or in parallel. CSS and JavaScript files or bundles grow in byte size as an application's complexity or maintenance increases, particularly as the number and size of included third-party libraries grow. Example:

**Before:**

```js
import { add } from './math';

console.log(add(16, 26));
```

**After:**

```js
import("./math").then(math => {
  console.log(math.add(16, 26));
});
```

- What needs to improve?

Redux Thunk is middleware that allows Redux to return functions rather than simple actions. This enables delayed activities, such as dealing with promises. One of the major applications for this middleware is to handle asynchronous activities, such as using Axios to submit a GET request. We may use Redux Thunk to dispatch those actions asynchronously and resolve each promise that is returned.
