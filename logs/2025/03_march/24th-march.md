24-03-2025

## Progress: 
* Object contructor.
* `this` and `new` keyword
* Difference between `Object.getPrototypeOf()` vs. 
`.__proto__` vs. `[[Prototype]]`.
* Prototypal Inheritance.
* In JavaScript: Made a new repo `Library`.
* In `Library`'s `script.js` made constructor for making `Book` objects with an inner function `info` that can report the book information.

## Challenges:
* How the prototype works- especially, what does defining 'on the `prototype`' mean?


## Key Takeaways:
* Methods vs. Properties – A method (like info()) needs to be defined as a function inside the constructor using this.info = function() {} so that each book object can call it. If you just assign a function without this, it won't be part of the object.

## Next Steps:
* Build on the `Library` project - array to store all books, generate unique id with `crypto.randomUUID()`.
* State in React.