from::
url::[Strings Just Got Faster – Inside.java](https://inside.java/2025/05/01/strings-just-got-faster/)
on:: 2025-05-03 15:42

- JDK 25 improves `String` performance by making `String::hashCode` mostly constant foldable.
- This optimization significantly benefits immutable `Map<String, V>` lookups, potentially improving performance by over 8x in certain scenarios.
- The improvement works by caching the `String`'s hashcode internally after the first calculation.
- A `@Stable` annotation signals to the virtual machine that a field’s value won't change, enabling constant folding.
- Strings with a hashcode of zero are not currently optimized, though a fix is anticipated.
- User code can indirectly benefit from similar optimizations via the upcoming JEP 502 (Stable Values).