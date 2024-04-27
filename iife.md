# Immediately-Invoked Function Expressions (IIFEs)

1. Defition:
    - IIFEs (pronounced "iffy") in JavaScript are anonymous functions that are executed immediately after being defined

2. Syntax:
    - Define an anonymous function
    - Wrap the function in parentheses to make it an expression
    - Immediately invoke the function by adding another pair of parentheses after it

3. Example:
```javascript
(function() {
    console.log("run me immediately!");
})();
```
4. Purpose:
    - Execute a function once without assigning it a name
    - Keep variables and functions private, preventing pollution of the global namespace
    - Protect global variables from being accessed or overwritten

5. Advantages:
    - Prevents repeated function invocation
    - Ensures encapsulation by hiding function and variable declarations


# Unassigned Variables in JavaScript

* Default Values in JavaScript variables:
    - Variables declared with 'let' or 'var' have a default value of 'undefined' if not expllicity assigned

    Example:
    ```javascript
    var hello;
    console.log(hello); // prints undefined
    ```

* Const Variables Exception:
    - __'const'__ variables must be assigned a value upon declaration, otherwise, it throws a 'SyntaxError'
    - Reason: 'const' variables cannot be reassigned, ensuring that they always have a value

    Example:
    ```javascript
    const goodbye;
    // SyntaxError: Missing initialiser in const declaration
    ```

* Hoisting and Default Values:
    - Variables declared with __'var'__ have their names hoisted to the top with a default value of undefined

    Example:
    ```javascript
    function hoistBuddy() {
        console.log(hello); // prints undefined
        var hello;
    }
    ```

* Difference in Hoisting with 'let':
    - __'let'__ variables are also hoisted but with a strict behaviour; accessing them before assignment results in an error

    Example:
    ```javascript
    function hoistBuddy() {
        console.log(hello); // ReferenceError: Cannot access 'hello' before initialisation
        let hello;
    }
    ```

* Summary:
    - Variables with 'let' or 'var' default to 'undefined'.
    - 'Const' variables require immediate assignment to be valid
