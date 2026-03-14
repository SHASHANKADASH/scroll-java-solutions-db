---
layout: default
title: Why the main method is public, static and void?
nav_order: 2
parent: Beginner
---

# Question

Why is the `main` method declared as **public**, **static**, and **void** in Java?

# Code

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

# Answer

The `main` method is declared as **public**, **static**, and **void** so that the **Java Virtual Machine (JVM)** can locate and execute it as the **entry point of a Java program**.

* **public** → JVM must be able to access the method from outside the class.
* **static** → JVM can call the method without creating an object of the class.
* **void** → The method does not return any value to the JVM.

# Explanation

### 1. Why `public`?

The `main` method must be **public** because the JVM calls it from outside the class.

If it were `private`, `protected`, or default access, the JVM would not be able to invoke it.

Example (Invalid):

```java
private static void main(String[] args)
```

### 2. Why `static`?

The `main` method is **static** so the JVM can call it **without creating an object** of the class.

When a Java program starts, no objects exist yet. The JVM directly calls:

```java
ClassName.main()
```

If `main` were not static, the JVM would first need to create an object of the class before calling the method.

### 3. Why `void`?

The `main` method returns **void** because the JVM does not expect any return value after the program finishes execution.

The program simply starts from `main` and terminates when the method completes.

# Concept

* Entry point of a Java program
* JVM method invocation
* Access modifiers
* Static methods
* Program execution lifecycle

The JVM specifically looks for this signature:

```java
public static void main(String[] args)
```

# Further Reading

[Java main Method - Official Documentation](https://docs.oracle.com/javase/tutorial/getStarted/application/index.html)
