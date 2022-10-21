# today-i-learn

[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://wajahatkarim.com)[![forthebadge](https://forthebadge.com/images/badges/makes-people-smile.svg)](https://wajahatkarim.com)

A collection of concise write-ups on small things I learn day to day.

---

## Day 5 (21 october 2022)

![image](/images/4.png)

- New Team

I've made a new friend who appears to be cool and nice.

- What I have done so far

Learn the Javascript programming language for later development in order to learn React.

- New things that I learned / error

Scope Chain Example:

```js
<script>
    // Global variable
    var global_variable = 20;

    function main_function() {
        // Local Variable
        var local_variable = 30;

        var nested_function = function () {

            // Display the value inside the local variable
            console.log(local_variable);
        }

        var another_nested_function = function () {
            
            // Displays the value inside the global variable
            console.log(global_variable);
        }

        nested_function();
        another_nested_function();
    }

    main_function();
</script>
```

Some Exercise:

```js
let a = 1;
    let b = 1;

    function hi () {

    const a = 1;

    let b = 100;

    b++;

    console.log(a,b);

    }

    console.log(a);

    console.log(b);

    hi();

    console.log(b);
```

- My reflection

There is a lot to remember and understand about the Javascript programming language and how to use it.
