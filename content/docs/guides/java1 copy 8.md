---
title: " 9 📄 . File Handling & Streams "
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
Java provides rich APIs for file input and output (I/O) using streams. These streams handle both binary (byte-based) and character (text-based) data.

### 🔹 Byte Stream

Byte streams are used to perform input and output of 8-bit bytes. These are mainly used to handle binary data like images, audio, video, etc.

Example:
```java
import java.io.FileInputStream;
import java.io.FileOutputStream;

public class ByteStreamExample {
    public static void main(String[] args) {
        try {
            FileInputStream in = new FileInputStream("input.txt");
            FileOutputStream out = new FileOutputStream("output.txt");
            int i;
            while ((i = in.read()) != -1) {
                out.write(i);
            }
            in.close();
            out.close();
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
🔹 FileInputStream & FileOutputStream

FileInputStream: Reads data from a file byte by byte.

FileOutputStream: Writes byte data to a file.

Already shown in Byte Stream example.
##🔸 Character Stream

Character streams use 16-bit Unicode and are used for handling text files.

Example:
```java
import java.io.FileReader;
import java.io.FileWriter;

public class CharStreamExample {
    public static void main(String[] args) {
        try {
            FileReader fr = new FileReader("input.txt");
            FileWriter fw = new FileWriter("output.txt");
            int i;
            while ((i = fr.read()) != -1) {
                fw.write(i);
            }
            fr.close();
            fw.close();
        } catch (Exception e) {
            System.out.println(e);
        }
    }
}
```
🔸 FileReader & FileWriter

FileReader: Reads character data from files.

FileWriter: Writes character data to files.

Already shown above.
##💨 Buffered Streams

Buffered classes increase efficiency by reducing I/O operations.

BufferedInputStream

BufferedOutputStream

BufferedReader

BufferedWriter

Example:
```java
import java.io.*;

public class BufferedExample {
    public static void main(String[] args) {
        try {
            BufferedReader br = new BufferedReader(new FileReader("input.txt"));
            BufferedWriter bw = new BufferedWriter(new FileWriter("output.txt"));
            String line;
            while ((line = br.readLine()) != null) {
                bw.write(line);
                bw.newLine();
            }
            br.close();
            bw.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

##🔄 InputStreamReader & OutputStreamWriter

They bridge byte streams and character streams.

Example:
```java
import java.io.*;

public class StreamReaderWriterExample {
    public static void main(String[] args) {
        try {
            InputStreamReader isr = new InputStreamReader(new FileInputStream("input.txt"));
            OutputStreamWriter osw = new OutputStreamWriter(new FileOutputStream("output.txt"));
            int data;
            while ((data = isr.read()) != -1) {
                osw.write(data);
            }
            isr.close();
            osw.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

## 🗂️ Stream Hierarchy Overview
```php
            InputStream              OutputStream
                |                          |
     ------------------------    ------------------------
    |                        |  |                        |
FileInputStream     BufferedInputStream     FileOutputStream     BufferedOutputStream

            Reader                     Writer
                |                          |
     ------------------------    ------------------------
    |                        |  |                        |
FileReader          BufferedReader     FileWriter         BufferedWriter
```

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
```java

```


