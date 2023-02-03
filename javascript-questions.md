### Explain event delegation.
Event delegation refers to the process of using event propagation (bubbling) to handle events at a higher level in the DOM than the element on which the event originated. It allows us to attach a single event listener for elements that exist now or in the future.

### Explain how **this** works in JavaScript.
In regular functions the "this" keyword represented the object that called the function, which could be the window, the document, a button or whatever.
When the "this" is inside an object method, it will refer to the object.
When the "this" is inside a function, it can have two values:
- it can be the global object when the function is not inside an object
- or it can be linked to the scope when it references the instantiated object

When the "this" is outside a function, it is the global window object.
When the "this" is inside an expression function, it is the global object. But if your code is in a strict mode, this becomes undefined.
When the "this" is inside an arrow function, it is always the global object.
#### Can you give an example of one of the ways that working with this has changed in ES6?
Arrow functions were introduced in ES6 and it's does not have its own "this"

### Explain how prototypal inheritance works.
When we assign something via prototype, it will be generated in inheritance for all objects that are made later. It should be used for content that doesn't change because all changes will be treated as an inheritance.

### What's the difference between a variable that is: null, undefined or undeclared?
According to ECMAScripts' documentation, a variable that is undefined is a variable that has been declared but not assigned a value. A variable that is null will have been explicitly assigned to the null value. It represents no value and is different from undefined in the sense that it has been explicitly assigned. Undeclared variables are created when you assign a value to an identifier that is not previously created using var, let or const.
#### How would you go about checking for any of these states?
To check for null and undefined, compare using the strict equality (===) operator.