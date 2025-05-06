---
title: "1.6 🧰 . Exception Handling"
description: "Guides lead a user through a specific task they want to accomplish, often with a sequence of steps."
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


Exception handling in Java is a mechanism to handle **runtime errors**, so the normal flow of the application can be maintained. It prevents abrupt termination of the program and provides a way to gracefully recover from errors.

---

## ❓ 1. What is an Exception?

An **Exception** is an object that describes an error condition that has occurred in a piece of code. When an exceptional event occurs, Java creates an object and throws it, which can be caught and handled.

Java provides a rich set of built-in exception classes, but you can also create your own custom exceptions.

**Why is exception handling important?**
- Prevents program crashes
- Separates error-handling code from regular code
- Makes code more robust and readable

---

## 📚 2. Types of Exceptions

Java exceptions are divided into **two main categories**:

### ✅ Checked Exceptions
These are exceptions that are **checked at compile-time**. The compiler ensures that your code handles these exceptions using try-catch blocks or the `throws` keyword.

Examples:
- `IOException`
- `SQLException`
- `FileNotFoundException`

### ❌ Unchecked Exceptions
These are **not checked at compile-time**. They usually result from programming errors.

Examples:
- `ArithmeticException`
- `NullPointerException`
- `ArrayIndexOutOfBoundsException`

### ⚠️ Errors
Errors indicate serious problems that a program should not try to catch (e.g., `OutOfMemoryError`).

---

## 🔐 3. try-catch-finally

Java provides a structured way to handle exceptions using these keywords:

- `try`: Defines a block of code in which exceptions can occur.
- `catch`: Defines a block of code that handles the exception.
- `finally`: Defines a block of code that is always executed whether an exception occurred or not.

```java
public class TryCatchExample {
    public static void main(String[] args) {
        try {
            int a = 10 / 0;
        } catch (ArithmeticException e) {
            System.out.println("Caught an ArithmeticException: " + e.getMessage());
        } finally {
            System.out.println("Finally block executed");
        }
    }
}
```


## 🎯 4. throw and throws
throw
Used to explicitly throw an exception object.

```java
throw new ArithmeticException("Cannot divide by zero");

```

throws
Used in method declarations to specify the exceptions that a method may throw.
```java
public class ThrowThrowsDemo {
    static void check(int age) throws ArithmeticException {
        if (age < 18) {
            throw new ArithmeticException("Underage");
        } else {
            System.out.println("Access granted");
        }
    }

    public static void main(String[] args) {
        check(15);
    }
}

```
Example:
```java
public class ThrowThrowsDemo {
    static void check(int age) throws ArithmeticException {
        if (age < 18) {
            throw new ArithmeticException("Underage");
        } else {
            System.out.println("Access granted");
        }
    }

    public static void main(String[] args) {
        check(15);
    }
}

```
## 🧩 5. Custom Exception
You can define your own exception class by extending Exception or RuntimeException.
```java
class MyException extends Exception {
    public MyException(String message) {
        super(message);
    }
}

public class CustomExceptionDemo {
    static void validate(int age) throws MyException {
        if (age < 18)
            throw new MyException("Not eligible");
        else
            System.out.println("Eligible");
    }

    public static void main(String[] args) {
        try {
            validate(16);
        } catch (MyException e) {
            System.out.println("Caught: " + e.getMessage());
        }
    }
}

```
##🧱 6. Exception Class Hierarchy
```php
Throwable
├── Exception
│   ├── IOException
│   ├── SQLException
│   └── ...
├── RuntimeException
│   ├── ArithmeticException
│   ├── NullPointerException
│   └── ...
└── Error
    ├── OutOfMemoryError
    └── StackOverflowError
```
✔ Key Points:
All exceptions are subclasses of Throwable.

Exception is for conditions a program should catch.

Error is for serious problems that should not be handled.
##
```java

```
##
```java

```
##
```java

```
##

