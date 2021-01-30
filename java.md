# Java Interview Questions

1. What is JVM and what are some advantages and disadvantages of it?

Java source code are compiled into byte code which is platform independent
instruction set. JVM is an interpreter which interprets this byte code.

Advantage: It is platform independent
Disadvantage: It is slow due to added layer of indirection

2. What is the difference between checked and unchecked exceptions? List five
   commonly used standard exceptions.

Checked exceptions are enforced by compiler meaning they must either be handled
or propagated up in the call hierarchy. Unchecked exceptions are not enforced by
compiler. Compiler won't complain at compile time if an unchecked exception is
not handled.

Some common exceptions:

- FileNotFound
- NullPointer
- IllegalArgumentException
- IOException

3. What are Final, Finally, Finalizer

They all are key words.

Final with a variable name means that the variable can only be assigned once
either when it is declared or inside constructor. 

Finally is used with try catch block to free resources.

Finalizer is inherited from the Object class. This method is called when object
is garbage collected. Overriding this method is not a good practice.

4. What is the difference between Equal() and == ?

For primitive types we can only use `==`. 

`==` checkes if the value of the object is equal. In case of reference type
object the value of the object is the memory address. If we want to compare
objects based on the contents, we need to override the `equals()` method
inherited from Object class.

5. Difference between `hashcode()` and `equals()`

`hashcode()` is used when we put objects in a hash based container and use the
`contains()` method. If we override the `equals()` method we also need to
override `hashcode()` method.

6. String vs StringBuilder

String is immutable which brings several benefits like -

- Thread safe
- Cachable

This also creates some drawbacks like -

- Every time a string is modified a new object is created

StringBuilder on the other hand is mutable.

