---
title: "1.7 📦 . Packages in Java"
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


A **package** in Java is a namespace that organizes a set of related classes and interfaces. Conceptually, it's similar to different folders on your computer. Packages help:
- Prevent class name conflicts
- Control access with visibility modifiers
- Make locating and using classes easier

---

## 📁 1. Built-in vs User-defined Packages

### ✅ Built-in Packages
Java provides a rich set of standard packages in the `java.*` namespace.

**Examples:**
- `java.lang` – Fundamental classes (automatically imported)
- `java.util` – Data structures like ArrayList, HashMap
- `java.io` – Input/output functionalities
- `java.sql` – Database handling

```java
import java.util.Scanner;

public class BuiltInDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter name: ");
        String name = sc.nextLine();
        System.out.println("Hello " + name);
    }
}

🛠️ User-defined Packages
You can create your own packages to group related classes.

Steps to create:

Use package keyword at the top.

Save the file inside a folder with the same name as the package.

📄 MyPackage/Hello.java

```java
package MyPackage;

public class Hello {
    public void display() {
        System.out.println("Hello from user-defined package!");
    }
}

```
📄 Test.java
```java
import MyPackage.Hello;

public class Test {
    public static void main(String[] args) {
        Hello h = new Hello();
        h.display();
    }
}

```
📥 2. Importing Packages
To use classes from another package, you use the import keyword:
```java
import java.util.*;           // Imports all classes from java.util
import java.util.Scanner;     // Imports only Scanner

```
No import needed for classes in the same package.
## 🏗️ 3. Creating and Using Packages
Create a package:
```java
package mypack;

public class Message {
    public static void printMessage() {
        System.out.println("Package created and accessed!");
    }
}

```
Use it:
```java
import mypack.Message;

public class UsePackage {
    public static void main(String[] args) {
        Message.printMessage();
    }
}

```
## 🔐 4. Access Levels (public, private, protected)
Java uses access modifiers to restrict the scope of classes, variables, methods, and constructors.

Modifier	Class	Package	Subclass	World
public	✔	✔	✔	✔
protected	✔	✔	✔	✖
(default)	✔	✔	✖	✖
private	✔	✖	✖	✖
```java
package demo;

public class AccessExample {
    public int pub = 1;
    protected int prot = 2;
    int def = 3;
    private int priv = 4;

    public void showAccess() {
        System.out.println("Public: " + pub);
        System.out.println("Protected: " + prot);
        System.out.println("Default: " + def);
        System.out.println("Private: " + priv);
    }
}

```
##
```java

```
