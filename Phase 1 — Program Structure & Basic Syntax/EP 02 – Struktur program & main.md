# EP 02 — Struktur Program Java & main() Method (Deep Dive)

Pada episode ini kita membedah struktur program Java secara lebih dalam dan teknis. Fokus utama adalah memahami bagaimana sebuah file Java dibangun, bagaimana JVM menemukan titik awal eksekusi, serta aturan penting yang berlaku dalam penulisan kode Java.

---

## 1. Struktur Dasar File Java

Struktur umum file Java:

- Package declaration (opsional)
- Import statements (opsional)
- Class declaration
- Fields dan methods

Contoh lengkap:

```java
package com.example.app;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        System.out.println("Program berjalan");
    }
}
````

Penjelasan:

* package digunakan untuk mengelompokkan class
* import digunakan untuk menggunakan class dari package lain
* public class Main adalah deklarasi class
* main() adalah entry point program

Jika file memiliki package, maka struktur folder harus sesuai dengan nama package.

Contoh:
package com.example.app berarti file harus berada di:

com/example/app/Main.java

---

## 2. Aturan Penamaan Class

Aturan penting:

* Nama class harus diawali huruf besar (konvensi)
* Nama file harus sama dengan nama class jika class tersebut public
* Satu file hanya boleh memiliki satu public class

Contoh valid:

```java
public class UserService {
}
```

File harus bernama:

UserService.java

Contoh tidak valid:

```java
public class UserService {
}

public class ProductService {
}
```

Error karena ada dua public class dalam satu file.

---

## 3. Entry Point: main() Method

Method main adalah titik awal eksekusi program Java.

Struktur resmi:

```java
public static void main(String[] args)
```

Penjelasan detail:

* public agar bisa diakses oleh JVM
* static karena dipanggil tanpa membuat object
* void karena tidak mengembalikan nilai
* main adalah nama yang wajib
* String[] args adalah parameter untuk menerima argumen dari command line

Tanpa method main, program tidak bisa dijalankan langsung.

---

## 4. Memahami static Secara Konseptual

static berarti milik class, bukan milik object.

Artinya:

* Bisa dipanggil tanpa membuat object
* Dibagi ke seluruh instance

Contoh:

```java
public class Counter {

    static int count = 0;

    public static void main(String[] args) {
        count++;
        System.out.println(count);
    }
}
```

Output:

```text
1
```

Variabel static hanya ada satu di memory.

---

## 5. Apa yang Terjadi Jika main Tidak Static

Contoh:

```java
public class Main {

    public void main(String[] args) {
        System.out.println("Halo");
    }
}
```

Program tidak akan berjalan karena JVM mencari method main yang static.

---

## 6. Scope Kurung Kurawal

Java menggunakan {} untuk menentukan blok kode.

Contoh:

```java
public class Main {

    public static void main(String[] args) {

        if (true) {
            System.out.println("Di dalam blok");
        }

        System.out.println("Di luar blok");
    }
}
```

Output:

```text
Di dalam blok
Di luar blok
```

Blok menentukan scope variable dan eksekusi.

---

## 7. Multiple Method dalam Satu Class

Satu class dapat memiliki banyak method.

Contoh:

```java
public class Main {

    public static void main(String[] args) {
        greet();
    }

    public static void greet() {
        System.out.println("Halo dari method greet");
    }
}
```

Output:

```text
Halo dari method greet
```

JVM memulai dari main(), lalu method lain dipanggil dari sana.

---

## 8. Comment dalam Java

Java memiliki tiga jenis komentar.

Single line:

```java
// Ini komentar satu baris
```

Multi-line:

```java
/*
   Ini komentar
   lebih dari satu baris
*/
```

Documentation comment:

```java
/**
 * Ini komentar dokumentasi
 */
```

Komentar tidak dieksekusi oleh JVM.

---

## 9. Contoh Struktur Program Lebih Realistis

```java
package app;

public class Main {

    static String appName = "Learning Java";

    public static void main(String[] args) {
        printAppName();
        printVersion();
    }

    public static void printAppName() {
        System.out.println("App: " + appName);
    }

    public static void printVersion() {
        System.out.println("Version: 1.0");
    }
}
```

Output:

```text
App: Learning Java
Version: 1.0
```

Struktur ini mulai mendekati praktik nyata aplikasi kecil.

---

## 10. Ringkasan EP 02

* File Java terdiri dari package, import, dan class
* Nama file harus sama dengan public class
* main() adalah entry point program
* static berarti milik class
* JVM mencari method public static void main(String[] args)
* {} menentukan blok dan scope

---

## Target Pemahaman Setelah EP 02

* Mengerti struktur file Java
* Mengerti kenapa main harus static
* Mengerti aturan penamaan class
* Mengerti bagaimana JVM memulai program
* Mampu membuat program dengan beberapa method

```
```
