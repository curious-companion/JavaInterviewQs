### Q1 What is the difference between JDK, JRE and JVM?
**Answer:** JVM, JRE and JDK serve different roles in the Java ecosystem.

JVM (Java Virtual Machine) is responsible for executing Java bytecode. It handles class loading, memory management, garbage collection and uses JIT compilation to convert bytecode into native machine code.

JRE(Java Runtime Environment) provides the environment to run Java application. It includes the JVM along with core Java libraries and runtime dependencies, but it does not include development tools like the compiler.

JDK (Java Development Kit) is used for developing Java application. It includes the JRE plus tools such as the Java compiler (javac), debugger, and other utiliies required to build, test and run Java programs.

In short, JDK is for development, JRE is for running, and JVM is the engine that executes the code.

### Q2 Why is Java called platform-independepent?
**Answer:** Java is called platform independent because Java source code is compiled into an intermediate form called bytecode, which is not tied to any specific operating system or hardware,

This bytecode can run on any platform that has a compatible Java Virtual Machine(JVM).

Since each operating system has its own JVM implementation, the same bytecode can be executed without modification across different platforms like Windows, Linux or macOS.

This concepts is known as "Write Once, Run Anywhere"

### Q3  what happens internally when you run a Java program?
**Answer:** When Java program is run, the process involves compilation, class loading, bytecode verification, and execution inside the JVM.

First, the Java source code (.java) is compiled by the Java compiler (javac) into bytecode(.class), which is platform independent.

When the program is executed using the java command, the JVM starts and loads the required classes using the Class Loader subsystem.

The Bytecode Verifier checks the bytecode for security and correctness to ensure it does not violate JVM constraints.

The JVM then executes the bytecode using the Execution Enginem, which initially interprets the code and later uses Just-In-Time (JIT) compilation to convert frequently executed bytecode into native machine code for better performance.

During execution, the JVM manages memory through runtime data areas like the Heap, Stack, Method Area, and PC register, and performs Garbage collection automatically free unused memory.

## Q4 Difference between == and equals()?
**Answer:** In Java == and equals() are used for comparison, but they serve different purposes.

The == operator compares references when used with objects, meaning it checks whether two refernces point to the same memory location. For primitive data types, == compares actual values.

The equals() method is used to compare the logical content or values of objects. By default, equals() behaves like == because it is inherited from the Object class, but many classes such as String override it to compare th actual data inside the objects.

Therefore, == checks references equality, while equals() checks content equality depending on its implementation.

## Q5 why a String immutable in Java?
**Answer:** Strings in Java are immutable, meaning once a String object is created, its value cannot be changed.

This design was choses mainly for security, performance, memory efficiency, and thread safety.

Immutability also enables the String Constant Pool, allowing multiple references to share the same object, which improves memory usage and performance.

Additionally, immutable strings are thread-safe by default, and their hashCode is cached, making them efficient keys in hash-based collections like HashMap.


## Q6 Difference between String, StringBuilder, and StringBuffer?
**Answer:** In Java, String, StringBuilder and StringBuffer differ mainly in mutability and thread safety.

String is immutable, meaning once created its value cannot be changed. Any modification results in a new object. This make String thread-safe and memory-efficient through the String Constant Pool, but inefficient for frequent modifications.

StringBuilder is mutabvle and not thread-safe. It allows in-place modification of characters, making it fast and efficient for single-threaded or local operations where frequent string changes are required.

StringBuffer is mutable and thread-safe because its methods are synchronized. This makes it safe in multi-threaded environments, but slightly slower than StringBuilder due to synchronization overhead.

