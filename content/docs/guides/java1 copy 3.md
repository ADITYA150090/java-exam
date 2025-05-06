---
title: " 1.4 🔧. Methods and Constructors"
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
## Method Syntax
In Java, methods are blocks of code that perform a specific task. A method must be defined with a return type, method name, and optional parameters.

### Example:
```java
public class MethodSyntaxExample {
    public static void main(String[] args) {
        sayHello(); // Calling the method
    }

    // Method definition
    public static void sayHello() {
        System.out.println("Hello, World!");
    }
}
```

## Method Overloading
Method overloading occurs when multiple methods have the same name but differ in the number or type of parameters.

### Example:
```java
public class MethodOverloadingExample {
    public static void main(String[] args) {
        System.out.println(add(5, 10));       // Calls method with two integers
        System.out.println(add(5.5, 10.5));   // Calls method with two double values
    }

    // Overloaded methods
    public static int add(int a, int b) {
        return a + b;
    }

    public static double add(double a, double b) {
        return a + b;
    }
}
```

## Constructor and Its Types
A constructor is a special method used to initialize objects. There are two types of constructors:
1. **Default Constructor**: A constructor with no parameters.
2. **Parameterized Constructor**: A constructor that accepts parameters to initialize object properties.

### Example:
```java
public class ConstructorExample {
    String name;

    // Default constructor
    public ConstructorExample() {
        name = "Default Name";
    }

    // Parameterized constructor
    public ConstructorExample(String name) {
        this.name = name;
    }

    public static void main(String[] args) {
        ConstructorExample obj1 = new ConstructorExample();
        ConstructorExample obj2 = new ConstructorExample("John");
        System.out.println("Name: " + obj1.name);  // Default Name
        System.out.println("Name: " + obj2.name);  // John
    }
}
```

## Constructor Overloading
Constructor overloading occurs when multiple constructors are defined within the same class, each having a different parameter list.

### Example:
```java
public class ConstructorOverloadingExample {
    String name;
    int age;

    // Constructor with one parameter
    public ConstructorOverloadingExample(String name) {
        this.name = name;
    }

    // Constructor with two parameters
    public ConstructorOverloadingExample(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public static void main(String[] args) {
        ConstructorOverloadingExample obj1 = new ConstructorOverloadingExample("Alice");
        ConstructorOverloadingExample obj2 = new ConstructorOverloadingExample("Bob", 25);
        System.out.println(obj1.name + " | " + obj2.age);
    }
}
```

## this Keyword
The `this` keyword refers to the current object within an instance method or constructor. It can also be used to differentiate between instance variables and method parameters with the same name.

### Example:
```java
public class ThisKeywordExample {
    int age;

    // Constructor using 'this' keyword
    public ThisKeywordExample(int age) {
        this.age = age;  // Refers to the instance variable
    }

    public static void main(String[] args) {
        ThisKeywordExample obj = new ThisKeywordExample(30);
        System.out.println("Age: " + obj.age);
    }
}
```

## static Keyword
The `static` keyword is used to indicate that a particular field or method belongs to the class itself, rather than to instances of the class. It can be used with variables, methods, blocks, and nested classes.

### Example:
```java
public class StaticKeywordExample {
    static int count = 0;

    // Static method to increment count
    public static void incrementCount() {
        count++;
    }

    public static void main(String[] args) {
        System.out.println("Count: " + count);  // Initially 0
        incrementCount();  // Call static method
        System.out.println("Count after increment: " + count);  // Now 1
    }
}
```

