# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/29 / Week 7

![image](/images/32.png)

There is still a lot to learn this week. We also have mentorship meetings with Mentor Justin, and we have A LOT to talk about. Such as try-catch, Throw, and many others.

- What did I learn today?

The event loop allows Node.js to perform non-blocking I/O activities despite the fact that JavaScript is single-threaded, by offloading actions to the system kernel whenever possible.

Because most modern kernels are multi-threaded, they can withstand a large number of background activities. When one of these operations is done, the kernel tells Node.js, allowing the corresponding callback to be added to the poll queue and eventually performed. This will be discussed in more detail later in this topic.

Node.js starts by initializing the event loop, processing the supplied input script (or entering the REPL, which is not discussed in this article), and performing async API calls, scheduling timers, or calling processes. The event loop is then launched by using nextTick ().

- What did I do well?

Difference between PATCH and PUT

The main difference between PUT and PATCH in REST API is that PUT handles updates by replacing the entire entity, while PATCH only updates the fields that you give it. The HTTP PUT request method is used to create a new resource or replace an existing one, and the HTTP PATCH method is used to change or add data to existing resources.

    - **Advantages of using PUT**
      - We don't have to re-fetch the entity after successfully updating it. Since PUT sends the entire entity, it'll replace whatever is there with what we send.
      - We can always overwrite the complete entity if we send down all fields and do not include any delta modification to existing fields.
      - PUT creates a resource if one doesn't exist.
    - **Advantages of using PATCH**
      - The client doesn't need to know the complete state of the resource before sending an update request.
      - PATCH makes it easier to track update intent to see what changed with each request.
      - PATCH saves bandwidth by allowing partial updates.

- What needs to improve?

**Cookies**, Because HTTP is a stateless protocol, no user information is stored on its servers. Cookies are a great method for accomplishing this goal. It enables us to save information on the user's computer and monitor the status of any running apps.

**Sessions** are used to securely keep information on the server, such as the User ID, where it cannot be modified. This prevents tampering with the data. Furthermore, sessions can transport value-based information from one web page to another. Sessions can be used in web browsers that do not support cookies to substitute cookies, allowing for more secure variable storage.
