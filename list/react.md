# React Introductory

learning a javascript

## QnA

1. What is loosely typed dynamic language?
   - Because JavaScript is a loosely typed language, we don't have to specify what type of information will be stored in a variable in advance. JavaScript automatically types variables based on the information we assign to them (for example, that " or " " to indicate string values).
2. What is JavaScript Type Casting?
   - Typecasting in JavaScript means converting one data type to another data type i.e., the conversion of a string data type to Boolean or the conversion of an integer data type to string data type. The typecasting in JavaScript is also known as type conversion or type coercion.
3. What is difference between == and === in Javascript?
   - The main difference between the == and === operators in javascript is that the == operator converts the operands' types before comparing them, whereas the === operator compares the operands' values as well as their data types.
4. What is the **problem** of a loosely typed dynamic language, and what are the ways to **supplement** it?
   - These Javascripts frequently produce unexpected results. For example, an operation was designed to be performed on an integer data type, but if a string is passed, the result is random and unpredictable. As a result, developers must exercise extreme caution when working with these types of languages.
5. Compare the difference between undefined and null.
   - Null: The value is intentionally not present. It is one of JavaScript's primitive values.
   - Undefined: It indicates that the value does not exist in the compiler. It is the universal object.
6. Primitive type data, and Reference type data.
   - When we create a variable in JavaScript, we can store either a primitive value or a reference value. It's a primitive value if the value is a number, string, boolean, undefined, null, or symbol. It's a reference value if it's anything else (i.e. typeof object).
7. JavaScript Type Casting
   - In JavaScript, typecasting refers to the process of converting one data type to another, such as converting a string data type to a Boolean data type or an integer data type to a string data type. Typecasting is also known as type conversion or type coercion in JavaScript.
8. How to make Immutable Object?
   - To make an object immutable, freeze each property of type object recursively (deep freeze). When you know the object contains no cycles in the reference graph, use the pattern on a case-by-case basis based on your design; otherwise, an endless loop will be triggered. example:

    ```js
    const supportedLanguages = {
    'af': 'Afrikaans',
    'bn': 'Bengali',
    'de': 'German',
    'en': 'English',
    'fr': 'French'
    }
    const frozenSupportedLanguages = Object.freeze(supportedLanguages);

    // The supportedLanguages and frozenSupportedLanguages are same

    frozenSupportedLanguages === supportedLanguages; // returns true
    // Add a new property
    supportedLanguages['kn'] = 'Kannada';

    // Modify an existing property
    supportedLanguages["af"] = 'something else';

    // Delete a property
    delete supportedLanguages.bn; // returns false

    // log the object to the console
    console.log(supportedLanguages); // Unchanged => {af: "Afrikaans", bn: "Bengali", en: "English", fr: "French"}
    ```

9. What are shallow copy and deep copy. What are the differences?
   - Shallow copy stores a copy of the original object and only the reference address is finally copied.
   - Deep copy stores both the original object and the repetitive copies.
10. Scope, Hoisting, and TDZ
    - In JavaScript, scope refers to the current context of code, which determines whether variables are accessible to JavaScript. There are two kinds of scope: local and global: Outside of a block, global variables are declared. Local variables are variables declared within a block.
    - JavaScript Hoisting is the process by which the interpreter appears to move the declaration of functions, variables, or classes to the top of their scope prior to executing the code. Hoisting allows functions to be safely used in code before they are declared.
    - A temporal dead zone (TDZ) is the area of a block where a variable is inaccessible until the computer completely initializes it with a value. A block is a pair of braces ( {...} ) used to group multiple statements together.
11. Different ways of hoisting in Function Declarations and Function Expressions.
    1. Function Declarations
        - Function declarations must begin with the phrase "function."
        - Function declarations must be named.
        - Function declarations are being executed during the compilation phase ( Function declarations load before any code is executed )

        ```js
        function multiply(a,b){
            return a*b;
        }
        ```

    2. Function Expressions
        - Function expressions are functions that are stored in a variable.
        - Function expressions do not require a name.
        - On the execution phase of the JS engine, function expressions are executed ( Function expressions load only when the interpreter reaches that line of code )  

         ```js
        var multiply = function(a,b){
            return a*b
        }
        ```

    3. Hoisting
       - JavaScript's default behavior for allocating memory for declarations during the compilation phase is hoisting.
       - Variable declarations and function declarations are both hoisted (Function declarations are hoisted first), but Function expressions are not fully hoisted.

        ```js
        var foo = function(){
            return 3;
        }
        ```

12. Execution Context and Call Stack
    1. Execution Context
        - The environment in which a piece of JavaScript is executed is referred to as the Execution Context. It stores all of the information required to execute some code, such as local variables or arguments passed into a function. JavaScript code is always executed inside an execution context (the computer CPU processing the received machine code).
    2. Call Stack
       - Remember that the call stack, along with the memory heap, comprise the JavaScript engine. The call stack is a "place" where execution contexts are stacked on top of each other to keep track of where we are in the program's execution (the order of execution).
13. Scope Chain and Information Hiding
    1. Scope Chain
       - The Scope Chain process is used by the JavaScript engine to determine the precise location or accessibility of variables.
       - Scope Chain means that one variable with a scope (global or local/function or block scope) is used by another variable or function with a different scope (global or local/function or block scope).
       - This complete chain formation continues until the user instructs it to stop.

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

    2. Information Hiding
       - The private keyword is used in Java programming to hide data - a field or method marked as private is not visible outside of the classes or subclasses.

       ```js
        var MYCLASS = function(){

            var priv_var = 0; //private var

            this.addToVar = function(){
                priv_var++;
            }

            this.showVar = function(){
                return priv_var;
            }

        }

        var mc = new MYCLASS;

        mc.addTovar();
        alert(mc.showVar()); //"1"
       ```

## Exercise

1. What would be the “b” value printed on the console?
   - The result is the number one.
2. Which “b” value would be printed from which line of console.log? Explain why.
   - Because b is a variable that exists outside of the function
3. What would be `//console.log(a);` in the comment? If there’s an error, explain why and fix the error.

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
