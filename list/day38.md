# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/12/07 / Week 8

![image](/images/38.png)

We did our best to finish the clone code project; there are two more functions and pages that must be completed. We keep track of all the chores we need to perform for our project in our notes to stay organized. Members should communicate with one another about their work progress, deadlines, and any problems they are having with the project. Communication is essential when working since it prevents problems and blunders that stymie efforts.

- What did I learn today?

  1. Can’t connect all APIs.

        Routes must be defined in index.js.

        ```js
        const posts = require("./posts");
        const comments = require("./comments");
        const signup = require("./signup");
        const login = require("./login");
        const likes = require("./likes");

        module.exports = [posts, comments, signup, login, likes];
        ```

  2. In AuthMiddleware, Cookie data is not received properly.

        We are unable to get cookie data since we are not using the cookieParser middleware; therefore, in order to resolve this issue, we must employ it.

        ```js
        app.use(cookieParser());
        ```

  3. Can find jwt authentication error in AuthMiddleware.
  
        There is an issue with jwt.sign() since we do not use the secret key that we have in.env when we login. As a result of the mistake, we must change it from.env to secret key in order to solve it.

        ```js
        const token = jwt.sign(
                { userId: user.userId },
                process.env.SECRET_KEY,
                { expiresIn: "10s" }
            );
        ```

  4. When calling API with POST Method, Request data is not received properly.
  
        That occurred because we are not utilizing any middleware to handle the request data, to solved it thus we must use bodyParser or express. json

        ```js
        app.use("/", bodyParser.json(), router);
        ```

  5. Error is found when requesting /posts/like API using GET Method.

        When we request this route, we receive the error "GET /posts/like: Cannot access 'getLikePostIdByLikes' before initialization," which occurs because we call the getLikePostIdByLikes method before we initialize.
        So all we have to do is relocate the function before calling it.

        ```js
        const getLikePostIdByLikes = (likes) => {
                let likePostIdArray = [];
                for (const like of likes) {
                    likePostIdArray.push(like.postId);
                }
                return likePostIdArray;
                }
                let likePostIdArray = getLikePostIdByLikes(userLikes);
        ```

- What did I do well?

Cross-Origin Resource Sharing (CORS) is an HTTP-header-based system that enables a server to specify any origins (domain, scheme, or port) other than its own from which a browser should allow resources to be loaded. CORS additionally makes use of a technique that allows browsers to send a "preflight" request to the server hosting the cross-origin resource to ensure that the server will allow the real request. The browser transmits headers indicating the HTTP method as well as headers that will be used in the actual request during that preflight.

An example of a cross-origin request: the front-end JavaScript code served from <https://domain-a.com> uses XMLHttpRequest to make a request for <https://domain-b.com/data.json>.

Cross-origin HTTP requests launched by scripts are restricted by browsers for security concerns. The same-origin policy, for example, is followed by XMLHttpRequest and the Fetch API. This implies that a web application that uses those APIs can only request resources from the origin from which the application was loaded, unless the answer from other origins includes the appropriate CORS headers.

- What needs to improve?

Using **redux-thunk** and **redux-promise**

It's vital to note that each third-party library has its own learning curve as well as possible scalability difficulties. However, of all the Redux community libraries for handling side effects, those that function like **redux-thunk** and **redux-promise** are the simplest to learn.

The concept is straightforward. A **thunk** is a piece of code that does some delayed job, or, to put it another way, it is the logic needed to update a state later.

You design an action creator for **redux-thunk** that does not "create" an object but returns a function. Redux's **getState** and **dispatch** methods are provided for this function.
