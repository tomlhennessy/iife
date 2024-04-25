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
