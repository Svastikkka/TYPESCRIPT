# TypeScript Tutorial

- TypeScript is Typed JavaScript.
- TypeScript adds types to JavaScript to help you speed up the development by catching errors before you even run the JavaScript code.
- TypeScript is an open-source programming language that builds on top of JavaScript. 
- It works on any browser, any OS, any environment that JavaScript runs.

## What is TypeScript
* TypeScript is a super set of JavaScript.
* TypeScript builds on top of JavaScript. First, you write the TypeScript code and then you compile the TypeScript code into plain JavaScript code using a TypeScript compiler.
* Once you have the plain JavaScript code, you can deploy it to any environments that JavaScript runs.
* TypeScript files use the ```.ts``` extension rather than the ```.js``` extension of JavaScript files.
* TypeScript uses the JavaScript syntaxes and adds additional syntaxes for supporting Types.

## Why TypeScript
The main goals of TypeScript are:
  * ### TypeScript improves your productivity while helping avoid bugs
  
    Types increase productivity by helping you avoid many mistakes. By using types, you can catch bugs at the compile-time instead of having them occurring at runtime
    The following function adds two numbers x and y:
    
    ```
    function add(x, y) {
      return x + y;
      }
    ```
    If you get the values from HTML input elements and pass them into the function, you may get an unexpected result:
    
    ```
    let result = add(input1.value, input2.value);
    console.log(result); // result of concatenating strings
    ```
    For example, if users entered `10` and `20`, the ```add()``` function would return `1020`, instead of `30`.
    The reason is that the ```input1.value``` and ```input2.value``` are strings, not numbers. When you use the operator ```+``` to add two strings, it concatenates them into a single string.
    
    When you use TypeScript to explicitly specify the type for the parameters like this:
    
    ```
    function add(x: number, y: number) {
      return x + y;
      }
    ```
    
    In this function, we added the number types to the parameters. The function  ```add()``` will accept only numbers, not any other values.
    When you invoke the function as follows:
    
    ```
    let result = add(input1.value, input2.value);
    ```
    the TypeScript compiler will issue an error if you compile the TypeScript code into JavaScript. Hence, you can prevent the error from happening at runtime.
    
  * ### TypeScript brings the future JavaScript to today
  
    TypeScript supports the upcoming features planned in the ES Next for the current JavaScript engines. It means that you can use the new JavaScript features before web browsers (or other environments) fully support them.
    Every year, TC39 releases a number of new features for ECMAScript which is the standard of JavaScript. The feature proposals typically go through five stages:
    
    * Stage 0: Strawperson
    * Stage 1: Proposal
    * Stage 2: Draft
    * Stage 3: Candidate
    * Stage 4: Finished
    
