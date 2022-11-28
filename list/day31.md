# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/28 / Week 7

![image](/images/31.png)

There is still a lot to learn this week. We also have mentorship meetings with Mentor Justin, and we have A LOT to talk about. Such as try-catch, Throw, and many others.

- What did I learn today?

The event loop allows Node.js to perform non-blocking I/O activities despite the fact that JavaScript is single-threaded, by offloading actions to the system kernel whenever possible.

Because most modern kernels are multi-threaded, they can withstand a large number of background activities. When one of these operations is done, the kernel tells Node.js, allowing the corresponding callback to be added to the poll queue and eventually performed. This will be discussed in more detail later in this topic.

Node.js starts by initializing the event loop, processing the supplied input script (or entering the REPL, which is not discussed in this article), and performing async API calls, scheduling timers, or calling processes. The event loop is then launched by using nextTick ().

- What did I do well?

Package.json contains vital project information. It comprises both human-readable metadata about the project (such as the project name and description) and functional metadata about the package, such as the package version number and a list of dependencies required by the application.

```js
{
  "name": "my-project",
  "version": "1.5.0",
  "description": "Express server project using compression",
  "main": "src/index.js",
  "scripts": {
      "start": "node index.js",
   "dev": "nodemon",
   "lint": "eslint **/*.js"
        },
        "dependencies": {
            "express": "^4.16.4",
   "compression": "~1.7.4"
        },
        "devDependencies": {
   "eslint": "^5.16.0",
            "nodemon": "^1.18.11"
        },
  "repository": {
   "type": "git",
   "url": "https://github.com/osiolabs/example.git"
  },
  "author": "Jon Church",
  "contributors": [{
   "name": "Amber Matz",
   "email": "example@example.com",
   "url": "https://www.osiolabs.com/#team"
  }],
  "keywords": ["server", "osiolabs", "express", "compression"]
    }
```

- What needs to improve?

**Cookies**, Because HTTP is a stateless protocol, no user information is stored on its servers. Cookies are a great method for accomplishing this goal. It enables us to save information on the user's computer and monitor the status of any running apps.

**Sessions** are used to securely keep information on the server, such as the User ID, where it cannot be modified. This prevents tampering with the data. Furthermore, sessions can transport value-based information from one web page to another. Sessions can be used in web browsers that do not support cookies to substitute cookies, allowing for more secure variable storage.
