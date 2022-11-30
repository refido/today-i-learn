# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/30 / Week 7

![image](/images/33.png)

There is still a lot to learn this week. We also have mentorship meetings with Mentor Justin, and we have A LOT to talk about. Such as try-catch, Throw, and many others.

- What did I learn today?

The event loop allows Node.js to perform non-blocking I/O activities despite the fact that JavaScript is single-threaded, by offloading actions to the system kernel whenever possible.

Because most modern kernels are multi-threaded, they can withstand a large number of background activities. When one of these operations is done, the kernel tells Node.js, allowing the corresponding callback to be added to the poll queue and eventually performed. This will be discussed in more detail later in this topic.

Node.js starts by initializing the event loop, processing the supplied input script (or entering the REPL, which is not discussed in this article), and performing async API calls, scheduling timers, or calling processes. The event loop is then launched by using nextTick ().

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
