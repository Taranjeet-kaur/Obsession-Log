08-07-2025

## Progress:
* Learned how equals() checks content when overridden, and otherwise checks reference equality.
* Understood that hashCode() works with equals() to maintain consistency in hash-based collections.
* Explored getClass() as a way to get the actual object type at runtime, regardless of reference.
* Practiced variable hiding: same field name in parent and child → resolved using reference type at compile-time.

## Challenges:
* Confused equals() vs == at first.
* Initially expected getClass() or field access to use actual object type — had to unlearn that for fields.


## Key Takeaways:
* equals() and hashCode() must be overridden together for correct behavior in sets/maps.
* getClass() shows true object type, not reference type.
* Variables are not overridden, only hidden — Java uses reference type to resolve fields at compile-time.
* Method behavior (overridden vs hidden) depends on instance vs static.

