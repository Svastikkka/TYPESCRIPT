# Why use TypeScript

## There are two main reasons to use TypeScript:
  - TypeScript adds a type system to help you avoid many problems with dynamic types in JavaScript.
  - TypeScript implements the future features of JavaScript a.k.a ES Next so that you can use them today.
  
  ***Note*** This tutorial focuses on the first reason.
  
## Understanding dynamic type in JavaScript
  - JavaScript is `dynamically typed`. Unlike statically-typed languages such as Java or C#, values have types instead of variables. For example:
  ```
    "Hello"
  ```
  From the value, you can tell that its type is string. Also, the following value is a number:
  ```
    2020
  ```
  See the following example:
  ```
    let box;
    console.log(typeof(box)); // undefined

    box = "Hello";
    console.log(typeof(box)); // string

    box = 100;
    console.log(typeof(box)); // number
  ```
  As you can see, as soon as the value is assigned, the type of the variable changes.
  And you don’t need to explicitly tell JavaScript the type. JavaScript will automatically infer the type from the value.
  
  ***Note*** Dynamic types offer flexibility. However, they also leads to problems.
  
## Problems with dynamic types
  Suppose you have a function that returns a product object based on an id:
  ```
    function getProduct(id){
      return {
        id: id,
        name: `Awesome Gadget ${id}`,
        price: 99.5
      }
    }
  ```
  The following uses the `getProduct()` function to retrieve the product with id 1 and shows its data:
  ```
    const product = getProduct(1);
    console.log(`The product ${product.Name} costs $${product.price}`);
  ```
  Output
  ```
    The product undefined costs $99.5
  ```
  It isn’t what we expected.
  The issue with this code is that the product object doesn’t have the `Name` property. It has the `name` property with the first letter `n` in lowercase.
  However, you can only know it until you run the script.
  Referencing a property that doesn’t exist on the object is a common issue when working in JavaScript
  
  The following example defines a new function that outputs the product information to the Console:
  And the following uses the `getProduct()` and `showProduct()` functions:
  
  ```
     function getProduct(id){
        return {
            id: id,
            name: `Awesome Gadget ${id}`,
            price: 99.5
          }
    }

    const showProduct2 = (name, price)  => {
        console.log(`The product ${name} costs ${price}$.`);
      };

    const product = getProduct(1);
    showProduct2(product.price, product.name);
  ```
  
  Output:
  ```
  The product 99.5 costs $Awesome Gadget 1
  ```
  This time we pass the arguments in the wrong order to the showProduct() function. This is another common problem that you often have when working with JavaScript.
  This is why the TypeScript comes into play.






  
