## Q1 What is abstraction and How it is different from Encapsulation?
**Answer:**
Abstraction and Encapsulation are both core OOP concepts, but they solve different problems.

Abstraction focuses on what an object does, not how it does it. It hides implementation details and exposes only the essential features to the user. In Java, abstraction is achieved using interfaces and abstract classes.

Encapsulation focuses on how data is protected and accessed. It bundles data and methods together in a class and restricts direct access to data using access modifiers, exposing controlled access through getters and setters.

In short, abstraction is about design and simplicity, while encapsulation is about data protection and integrity.

## Q2 Can an interface have method implementations?
Yes, since JAva 8, interfaces can have method implementations.

Java introduced default methods to allow interface to provide method implementations without breaking existing implementing classes.

Interfaces can also have static methods with implementations, which belong to the interface itself and cannot be overridden by implementing classes.

However, interfaces still cannot have instance variables or constructors and methods are public by default.

## Q3 Difference between Abstract class and Interface?
**Answer** Abstract classes and interfaces are both used to achieve abstraction in Java, but they differ in design and usage.

An abstract class can have both abstract and concrete methods, can contain instance variables, and can have constructors. It represents an “is-a” relationship with shared state and behavior. A class can extend only one abstract class due to Java’s single inheritance rule.

An interface defines a contract. It supports multiple inheritance, cannot have instance variables or constructors, and from Java 8 onwards can have default and static methods with implementations. Interfaces focus on what a class can do, not how it stores state.

In short, use an abstract class when classes share common state or base functionality, and use an interface when you need multiple inheritance or to define a capability.

## Q4 Can we achieve multiple inheritance in Java? How?
**Answer** Java does not support multiple inheritance using classes to avoid ambiguity, such as the Diamond Problem.

However, Java achieves multiple inheritance through interfaces. A class can implement multiple interfaces, allowing it to inherit multiple behaviors without inheriting state.

From Java 8 onwards, interfaces can also contain default methods, and if multiple interfaces provide the same default method, the implementing class must override the method to resolve the conflict.

## Q5 What is Polymorphisma and give a real world example?
**Answer**Polymorphism is an OOP concept where one interface or method can take multiple forms, meaning the same method call behaves differently based on the object it is acting upon.

In Java, polymorphism is mainly achieved through method overriding and method overloading, with runtime polymorphism being more important in real applications.

Polymorphism allows code to be flexible, extensible, and loosely coupled, making it easier to add new implementations without changing existing code.
