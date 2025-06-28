28-06-2025

## Progress:
* Learned how to clearly differentiate between instance methods and static methods.
* Learned the 4 major uses of `this` keyword:

> * To resolve variable name conflict.

> * To call another constructor.

> * To pass the current object.

> * To return the current object for method chaining.

* Explored the wrong cases when `this` is not used → understood what Java prefers by default (local variables).

* Learned why `this` cannot be static → it always belongs to the current object, not the class.

* Cleared the difference between passing an object directly (Student s) vs. passing `this` (the current object).

## Challenges:
* Initially struggled to understand why variables or methods are made of the same class type.
* Confusion around why this cannot be used in `main()` or other static methods.


## Key Takeaways:
* `this` is not static because it changes meaning with each object → it always points to "the current speaker" (the current object in action).

* In static methods (like `main`), there’s no “speaker” → `this` is not allowed.

* Methods can accept the same class type as a parameter to compare, copy, or work with other objects.

* Methods can return the same class type to enable method chaining.

* Java always prefers local variables first unless you use `this` to clarify.

* Method chaining works only when the method returns the current object → using `return this;`


## Next Steps:
* Practice some more question on `this`.
* Study next topic -> `Object and Static Initializers (Anonymous Blocks)`.