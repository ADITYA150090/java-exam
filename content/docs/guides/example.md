---
title: "1.2 ⚙️. Java Basics"
description: "Guides loda a user through a specific task they want to accomplish, often with a sequence of steps."
summary: ""
date: 2023-09-07T16:04:48+02:00
lastmod: 2023-09-07T16:04:48+02:00
draft: false
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  robots: "" # custom robot tags (optional)
---



---

### Java Program Structure

A basic Java program consists of a class, a `main` method, and statements inside the method. Here is an example:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

### JVM, JDK, JRE

- **JVM**: Java Virtual Machine is responsible for running Java bytecode.
- **JDK**: Java Development Kit provides tools to develop Java programs.
- **JRE**: Java Runtime Environment contains JVM and other libraries for running Java programs.

**Example:**
```java
// JVM is responsible for executing this bytecode
public class Example {
    public static void main(String[] args) {
        System.out.println("JVM executes this program!");
    }
}
```

### Java Architecture

Java Architecture consists of various components like ClassLoader, JVM, Garbage Collector, etc.

- **ClassLoader** loads classes at runtime.
- **JVM** executes bytecode.
- **Garbage Collector** automatically deletes unused objects from memory.

**Example:**
```java
// This Java code is loaded and executed by JVM at runtime.
public class JavaArchitectureExample {
    public static void main(String[] args) {
        System.out.println("Understanding Java Architecture");
    }
}
```

### Keywords in Java

Keywords in Java are reserved words that have a special meaning and cannot be used as identifiers. Some common keywords include `public`, `static`, `void`, `class`, `if`, `else`, etc.

**Example:**
```java
public class KeywordExample {
    public static void main(String[] args) {
        int number = 10;  // 'int' is a keyword for integer data type
        if (number > 5) { // 'if' is a keyword for conditional statement
            System.out.println("Number is greater than 5");
        }
    }
}
```

### Data Types and Variables

Java provides various primitive data types like `int`, `float`, `char`, `boolean`, and more. Variables are used to store values of these data types.

**Example:**
```java
public class DataTypesExample {
    public static void main(String[] args) {
        int num = 10;            // Integer type
        float price = 19.99f;    // Float type
        char grade = 'A';        // Character type
        boolean isActive = true; // Boolean type

        System.out.println("Num: " + num);
        System.out.println("Price: " + price);
        System.out.println("Grade: " + grade);
        System.out.println("Active: " + isActive);
    }
}
```

### Operators in Java

Java provides several types of operators like arithmetic, relational, logical, and assignment operators.

**Example:**
```java
public class OperatorsExample {
    public static void main(String[] args) {
        int a = 10;
        int b = 20;

        // Arithmetic operators
        int sum = a + b;
        int diff = a - b;
        int product = a * b;
        int quotient = b / a;
        int remainder = b % a;

        // Relational operator
        boolean isGreater = b > a;

        // Logical operator
        boolean isTrue = (a < b) && (b > a);

        System.out.println("Sum: " + sum);
        System.out.println("Difference: " + diff);
        System.out.println("Product: " + product);
        System.out.println("Quotient: " + quotient);
        System.out.println("Remainder: " + remainder);
        System.out.println("Is Greater: " + isGreater);
        System.out.println("Logical Operation Result: " + isTrue);
    }
}
```

---

This Markdown file provides an introduction to Java Basics with code examples for each subtopic.


