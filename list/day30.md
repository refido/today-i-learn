# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/11/25 / Week 7

![image](/images/30.png)

We are studying new material today, watching it together, and discussing it. We will be studying object literals, destructuring allocation, error handling, classes, and hoisting. For the time being, that's all we don't fully understand.

- What did I learn today?

Restful API

A RESTful API is an interface that allows two computer systems to safely exchange data over the internet. To accomplish various functions, most business apps must interface with other internal and third-party applications. To create monthly payslips, for example, your internal accounting system must share data with your customer's banking system in order to automate invoicing and connect with an internal timesheet application. RESTful APIs facilitate this information flow because they adhere to software communication standards that are safe, trustworthy, and efficient.

RESTful APIs include the following benefits:

Scalability

Because REST improves client-server interactions, systems that employ REST APIs may scale efficiently. Because the server does not need to keep previous client request information, statelessness reduces server load. Some client-server exchanges are reduced or eliminated entirely when caching is properly managed. All of these characteristics promote scalability without introducing communication bottlenecks that degrade performance.

Flexibility

RESTful web services allow for complete client-server separation. They simplify and decouple distinct server components, allowing each component to evolve independently. Changes to the server application's platform or technology have no effect on the client application. The ability to overlay application functions adds even more versatility. Developers, for example, may make changes to the database layer without having to rewrite the application logic.

Independence

REST APIs are unaffected by the technology employed. Client and server applications may be written in a variety of programming languages without compromising the API architecture. You may also modify the underlying technology on either side without disrupting communication.

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

**Error handling** is a method of dealing with errors and dealing with unforesen occurrences.

Errors are classified as **predictable errors** or **unexpected errors**, and when developing a normal application, it should be considered that **unexpected error** circumstances will occur more frequently.

**Exceptions are processed to prevent problems from occuring on the server.**

**Exception handling** is commonly done using a 'try... catch' statement.

If data other than a **string** is supplied while attempting to transform the names in users to uppercase with 'String.toUpperCase(),' an error occurs.

```jsx
const users = ["Lee", "Kim", "Park", 2];

try {
  for (const user of users) {
    console.log(user.toUpperCase());
  }
} catch (err) {
  console.error(`Error: ${err.message}`);
}

// LEE
// KIM
// PARK
// Error: user.toUpperCase is not a function
```
