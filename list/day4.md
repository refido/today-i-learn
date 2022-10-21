# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## Day 4 (20 october 2022)

![image](/images/3.png)

- TEAM PROGRESS

finish all of the task and submitted our project to LearningX Bootcamp

- What I have done so far

Add search bar to our project that can search depends on what you input on search bar

```js
$(document).ready(function () {
    show_item();
    $('#myInput').on("keyup", function () {
      var value = $(this).val().toLowerCase();
      $('#item-list #cardBox').filter(function () {
        $(this).toggle($(this).text().toLowerCase().indexOf(value) > -1)
      })
    })
  });
```

- New things that I learned / error

I discovered that I can use keyup functions to send data or perform interactive tasks without using a button.

- My reflection

I need to learn more about Javascript.
