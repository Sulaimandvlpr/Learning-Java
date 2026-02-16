````md
# EP 01 — Apa itu Java, JVM, JDK

## 1. Apa itu Java

Java adalah bahasa pemrograman tingkat tinggi yang dirancang untuk membangun aplikasi yang stabil, aman, dan scalable. Java bersifat object-oriented, strongly typed, dan berjalan di atas JVM sehingga dapat dijalankan di berbagai sistem operasi tanpa perlu ditulis ulang.

Karakteristik utama Java:

- Object-Oriented Programming (OOP)
- Strongly typed
- Garbage collected
- Portable melalui JVM
- Digunakan luas di backend enterprise, fintech, e-commerce, dan distributed systems

Pada industri 2026, Java tetap dominan karena stabilitas, ekosistem framework seperti Spring, serta dukungan Long Term Support seperti Java 17 dan Java 21.

---

## 2. Apa itu JVM

JVM adalah Java Virtual Machine. JVM adalah mesin virtual yang menjalankan bytecode hasil kompilasi Java.

Alur kerja Java:

- Kita menulis file dengan ekstensi .java
- Compiler (javac) mengubahnya menjadi bytecode (.class)
- JVM membaca dan mengeksekusi bytecode tersebut

Ilustrasi sederhana:

Source Code (.java)  
- javac  
- Bytecode (.class)  
- JVM  
- Program berjalan  

JVM bertanggung jawab atas:

- Manajemen memori (heap dan stack)
- Garbage Collection
- Eksekusi bytecode
- Thread management
- Keamanan runtime

Inilah alasan Java disebut portable, karena yang berbeda antar sistem operasi adalah JVM-nya, bukan programnya.

---

## 3. Apa itu JDK

JDK adalah Java Development Kit. JDK adalah paket lengkap untuk mengembangkan aplikasi Java.

Isi JDK:

- Compiler (javac)
- JVM
- Standard Library
- Tools debugging
- Tools packaging

Perbedaannya:

- JVM hanya menjalankan program
- JDK digunakan untuk membuat dan menjalankan program

Tanpa JDK, kita tidak bisa meng-compile kode Java.

---

## 4. Struktur Program Java Dasar

Contoh program sederhana:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, Java!");
    }
}
````

Output:

```text
Hello, Java!
```

Sekarang kita bedah setiap bagian kode tersebut secara teknis dan benar.

### public class Main

Penjelasan:

* class adalah blueprint atau cetakan untuk membuat object
* Main adalah nama class
* public adalah access modifier yang berarti class ini dapat diakses dari mana saja
* Nama file harus sama dengan nama class jika class tersebut public, sehingga file harus bernama Main.java

Struktur umum deklarasi class:

```java
access_modifier class NamaClass {
}
```

Contoh lain:

```java
public class Calculator {
}
```

---

### public static void main(String[] args)

Ini adalah method utama yang menjadi entry point program Java.

Penjelasan tiap kata:

* public berarti method ini dapat diakses oleh JVM
* static berarti method ini milik class, bukan object
* void berarti method ini tidak mengembalikan nilai
* main adalah nama method yang dicari JVM saat program dijalankan
* String[] args adalah parameter berupa array String untuk menerima argumen dari command line

Tanpa method main, program tidak bisa dijalankan secara langsung.

Contoh variasi argumen:

```java
public class Main {
    public static void main(String[] args) {
        System.out.println(args[0]);
    }
}
```

Jika dijalankan dengan:

```bash
java Main Halo
```

Output:

```text
Halo
```

---

### System.out.println()

Ini adalah perintah untuk mencetak output ke console.

Penjelasan detail:

* System adalah class bawaan Java dari package java.lang
* out adalah objek static bertipe PrintStream
* println() adalah method untuk mencetak teks dan pindah baris

Struktur dasarnya:

```java
System.out.println("Teks");
```

Jika tidak ingin pindah baris:

```java
System.out.print("Teks");
```

Contoh:

```java
public class Main {
    public static void main(String[] args) {
        System.out.print("Halo ");
        System.out.println("Dunia");
    }
}
```

Output:

```text
Halo Dunia
```

---

## 5. Proses Kompilasi dan Eksekusi

Langkah 1 — Kompilasi

```bash
javac Main.java
```

File yang dihasilkan:

Main.class

Langkah 2 — Eksekusi

```bash
java Main
```

Output:

```text
Hello, Java!
```

Penjelasan teknis:

* javac mengubah source code menjadi bytecode
* java memanggil JVM untuk menjalankan bytecode tersebut

---

## 6. Contoh Dengan Variabel

```java
public class Main {
    public static void main(String[] args) {
        int age = 21;
        String name = "Eman";

        System.out.println("Nama: " + name);
        System.out.println("Umur: " + age);
    }
}
```

Output:

```text
Nama: Eman
Umur: 21
```

Penjelasan:

* int adalah tipe data primitif untuk bilangan bulat
* String adalah class untuk teks
* Tanda + digunakan untuk menggabungkan string dengan variabel

---

## 7. Ringkasan Konsep Penting

* Java adalah bahasa OOP yang berjalan di atas JVM
* JVM menjalankan bytecode
* JDK digunakan untuk mengembangkan aplikasi
* Program Java selalu memiliki method main sebagai entry point
* System.out.println digunakan untuk menampilkan output

---

## 8. Target Pemahaman Setelah EP 01

* Memahami perbedaan Java, JVM, dan JDK
* Mengerti struktur dasar program Java
* Mengetahui fungsi public, class, static, void, dan main
* Mengerti bagaimana program dikompilasi dan dijalankan
* Mampu menulis dan menjalankan program sederhana

```
```
