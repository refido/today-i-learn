# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/12/05 / Week 8

![image](/images/36.png)

We separate jobs and work on them, beginning with the backend frontend and scraping data. We do our best to keep it as similar to the original as possible.

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

Databases are an essential component of many websites and apps, and they are important to how data is saved and transmitted over the internet. The technique of obtaining data from a database, whether ad hoc or as part of a procedure integrated into an application, is one of the most significant components of database administration. There are various techniques for retrieving information from a database, but one of the most frequent is to make queries via the command line.

A query is any command used to get data from a table in relational database management systems. The SELECT statement is nearly often used in Structured Query Language (SQL) queries.

```js
getAllPosts = (data, callback) => {
    db.query(
      `SELECT p.id AS postId, p.description, p.datetimeCreated, 
      p.likeCount, p.dislikeCount, p.addedByUserId, u.firstName, u.lastName 
      FROM posts AS p INNER JOIN users AS u ON p.addedByUserId = u.id`,
      [],
      (error, results, fields) => {
        if (error) {
          return callback(error);
        }
        return callback(null, results);
      }
    );
};

addPost = (data, callback) => {
  db.query(
    `INSERT INTO posts (description, imagePath, datetimeCreated, addedByUserId)
    VALUES (?, ?, ?, ?)`,
    [data.description, data.imagePath, new Date(), data.addedByUserId],
    (error, results, fields) => {
      if (error) {
        return callback(error);
      }
      return callback(null, "Post added successfully");
    }
  );
};
```

- What needs to improve?

**Cookies**, Because HTTP is a stateless protocol, no user information is stored on its servers. Cookies are a great method for accomplishing this goal. It enables us to save information on the user's computer and monitor the status of any running apps.

**Sessions** are used to securely keep information on the server, such as the User ID, where it cannot be modified. This prevents tampering with the data. Furthermore, sessions can transport value-based information from one web page to another. Sessions can be used in web browsers that do not support cookies to substitute cookies, allowing for more secure variable storage.
