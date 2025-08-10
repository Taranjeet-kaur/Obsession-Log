10-08-2025

## Progress:
* Topic - Exceptions Handling. 
* Learned what exception propagation means: the process of an exception moving up the call stack until handled.
* Understood the difference between checked and unchecked exceptions in propagation.
* Studied how throws works — it declares potential exceptions for a method, allowing the caller to handle them.

## Challenges:
* Confused between declaring an exception (throws) and throwing an exception (throw).

* Needed to untangle when exactly exception propagation stops (when caught) and when it continues.


## Key Takeaways:
* Exception Propagation = an exception moves up the method call hierarchy until it’s caught or the program ends.
* throws only declares a possibility of an exception, not a guarantee.

* If no exception is thrown, normal execution continues without triggering any catch block.

* Code reusability benefit: core method logic can remain clean and portable, while exception handling is left to the caller.

* Declaring throws shifts handling responsibility, but doesn’t change program flow unless an actual exception occurs.

## Next steps:
* Difference between `throw` and `throws`.

* Difference between `final`, `finally` and `finalize`.

* Exception Handling with method overriding.

*  Custom Exception.