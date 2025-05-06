---
title: "1.5 🧱. Object-Oriented Programming "
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
# 🧱 5. Object-Oriented Programming (OOP) in Java

Object-Oriented Programming is a paradigm that organizes software design around data, or objects, rather than functions and logic. Here are the 10 core concepts with examples:

---

## 1. Class and Object

A **class** is a blueprint. An **object** is an instance of a class.

```java
class Car {
    String color = "Red";
    void drive() {
        System.out.println("Driving the car...");
    }
}

public class Main {
    public static void main(String[] args) {
        Car myCar = new Car(); // Object creation
        myCar.drive();         // Method call
        System.out.println(myCar.color); // Accessing property
    }
}
```
### 2. Access Modifiers
Control visibility: public, private, protected, and default (no modifier).

```java
class Test {
    public int a = 10;
    private int b = 20;
    protected int c = 30;
    int d = 40; // default
}
```
### 3. Inheritance
extends keyword allows a class to inherit properties and methods.
```java
class Animal {
    void eat() {
        System.out.println("This animal eats food");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.eat(); // Inherited
        d.bark();
    }
}
```

### 4. Method Overriding
A subclass provides its own version of a method defined in its superclass.

```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}

```

### 5. Polymorphism
One method behaves differently based on the object type.
```java
class Shape {
    void draw() {
        System.out.println("Drawing shape");
    }
}

class Circle extends Shape {
    void draw() {
        System.out.println("Drawing circle");
    }
}

class Square extends Shape {
    void draw() {
        System.out.println("Drawing square");
    }
}

public class Main {
    public static void main(String[] args) {
        Shape s1 = new Circle();
        Shape s2 = new Square();
        s1.draw();
        s2.draw();
    }
}

```




### 6. Abstraction
Hide implementation using abstract classes or interfaces.
```java
abstract class Vehicle {
    abstract void start();
}

class Bike extends Vehicle {
    void start() {
        System.out.println("Bike starts with a kick");
    }
}

```





### 7. Abstract Class
A class that cannot be instantiated and may have abstract methods.

```java
abstract class Animal {
    abstract void makeSound();
    void sleep() {
        System.out.println("Sleeping...");
    }
}

```



### 8. Interface
Used to define a contract that implementing classes must follow.



```java
interface Drawable {
    void draw();
}

class Rectangle implements Drawable {
    public void draw() {
        System.out.println("Drawing rectangle");
    }
}

```




### 9. Encapsulation
Wrap fields and methods into a class and restrict access using getters/setters.

```java
class Student {
    private String name;

    public void setName(String n) {
        name = n;
    }

    public String getName() {
        return name;
    }
}

```


### 10. Dynamic Method Dispatch
Superclass reference is used to call overridden methods at runtime.

```java
class Animal {
    void sound() {
        System.out.println("Some sound");
    }
}

class Dog extends Animal {
    void sound() {
        System.out.println("Bark");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a = new Dog(); // Superclass reference
        a.sound(); // Executes Dog's sound
    }
}

```
