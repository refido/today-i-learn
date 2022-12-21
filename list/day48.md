# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## [SpartaCodingClub Full-Stack Bootcamp in Indonesia] 2022/12/21 / Week 10

![image](/images/48.png)

We established a plan today to minimize or decrease bottlenecks such as project work delays. Members should communicate with one another on the status of their work, deadlines, and any issues they experience with the project. Communication is critical while working since it avoids difficulties and faults from slowing down the process. But, in the end, difficulties must be confronted.

- What did I learn today?

  Create syle component

      ```js
      const HeaderWrapper = styled.div`
      display: flex;
      padding: 15px 20px;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      background-color: white;
      z-index: 100;
      top: 0;
      box-shadow: 0px 5px 8px -9px rgba(0, 0, 0, 0.75);
      `

      const HeaderLeft = styled.div`
      display: flex;
      justify-content: space-evenly;
      img {
            height: 40px;
      }
      `

      const HeaderInput = styled.div`
      display: flex;
      align-items: center;
      background-color: #eff2f5;
      padding: 10px;
      margin-left: 10px;
      border-radius: 33px;
      input {
            border: none;
            background-color: transparent;
            outline-width: 0;
      }
      `
      const HeaderCenter = styled.div`
      display: flex;
      flex: 1;
      justify-content: center;
      .header__option{
            display: flex;
            align-items: center;
            padding: 10px 30px;
            cursor: pointer;
            .MuiSvgIcon-root{
                  color: gray;
            }
            &:hover{
                  background-color: #eff2f5;
                  border-radius: 10px;
                  align-items: center;
                  padding: 0 30px;
                  border-bottom: none;
                  .MuiSvgIcon-root{
                  color: #2e81f4;
                  }
            }
      }
      .header__option--active{
            border-bottom: 4px solid #2e81f4;
            .MuiSvgIcon-root{
                  color: #2e81f4;
            }
      }
      `
      const HeaderRight = styled.div`
      display: flex;
      .header__info {
            display: flex;
            align-items: center;
            h4 {
                  margin-left: 10px;
            }
      }
      `
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
