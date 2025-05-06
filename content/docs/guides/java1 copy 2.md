---
title: " 1.3 📦. Control Flow Statements"
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
### if-else

The `if-else` statement is used to make decisions based on a condition. If the condition is `true`, the first block of code is executed; otherwise, the `else` block is executed.

**Example:**
```java
public class IfElseExample {
    public static void main(String[] args) {
        int num = 10;
        if (num > 5) {
            System.out.println("Number is greater than 5");
        } else {
            System.out.println("Number is less than or equal to 5");
        }
    }
}
```

### switch-case

The `switch` statement executes one out of many possible blocks of code based on the value of a variable or expression.

**Example:**
```java
public class SwitchCaseExample {
    public static void main(String[] args) {
        int day = 3;
        switch (day) {
            case 1:
                System.out.println("Monday");
                break;
            case 2:
                System.out.println("Tuesday");
                break;
            case 3:
                System.out.println("Wednesday");
                break;
            case 4:
                System.out.println("Thursday");
                break;
            default:
                System.out.println("Invalid Day");
        }
    }
}
```

### loops (for, while, do-while)

Loops are used to execute a block of code multiple times. Java has three types of loops: `for`, `while`, and `do-while`.

**for loop example:**
```java
public class ForLoopExample {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Iteration: " + i);
        }
    }
}
```

**while loop example:**
```java
public class WhileLoopExample {
    public static void main(String[] args) {
        int i = 1;
        while (i <= 5) {
            System.out.println("Iteration: " + i);
            i++;
        }
    }
}
```

**do-while loop example:**
```java
public class DoWhileLoopExample {
    public static void main(String[] args) {
        int i = 1;
        do {
            System.out.println("Iteration: " + i);
            i++;
        } while (i <= 5);
    }
}
```

### break and continue

- `break`: Exits from the loop or `switch` statement.
- `continue`: Skips the current iteration of the loop and moves to the next iteration.

**Example:**
```java
public class BreakContinueExample {
    public static void main(String[] args) {
        for (int i = 1; i <= 5; i++) {
            if (i == 3) {
                continue; // Skips iteration when i is 3
            }
            if (i == 4) {
                break; // Exits the loop when i is 4
            }
            System.out.println("Iteration: " + i);
        }
    }
}
```

### nested loops

A nested loop is a loop inside another loop. It is used when you need to perform operations that require multiple iterations within each iteration.

**Example:**
```java
public class NestedLoopsExample {
    public static void main(String[] args) {
        for (int i = 1; i <= 3; i++) {
            for (int j = 1; j <= 2; j++) {
                System.out.println("i: " + i + ", j: " + j);
            }
        }
    }
}
```

---

This Markdown file provides an overview of Control Flow Statements in Java, with code examples for each subtopic.

