# Question
What is the output?

# Code
```java
int a = 10;
System.out.println(a++ + ++a);
```

# Answer
22

# Explanation

Initial value:

a = 10

Expression being evaluated:

a++ + ++a

Java evaluates expressions **from left to right**.

Step 1 — Evaluate `a++`  
`a++` is the **post-increment operator**.  
It returns the current value first and then increments the variable.

Value used = 10  
a becomes = 11

Step 2 — Evaluate `++a`  
`++a` is the **pre-increment operator**.  
It increments the variable first and then returns the new value.

a becomes = 12  
Value used = 12

Step 3 — Final calculation

10 + 12 = 22

Final output:

22

# Concept

**Post-increment (`a++`)**
- Returns the current value
- Then increments the variable

Example:

```java
int a = 5;
System.out.println(a++); // prints 5
System.out.println(a);   // prints 6
```

**Pre-increment (`++a`)**
- Increments the variable first
- Then returns the updated value

Example:

```java
int a = 5;
System.out.println(++a); // prints 6
```

Java evaluates expressions **from left to right**, which determines how mixed increment operators behave inside expressions.

# Further Reading
[Link Text](https://www.geeksforgeeks.org/cpp/increment-and-decrement-operators-in-programming/#increment-operators-in-java)
