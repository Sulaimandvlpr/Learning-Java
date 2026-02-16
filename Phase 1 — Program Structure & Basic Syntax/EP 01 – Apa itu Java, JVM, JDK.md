````md
# EP 01 — Apa itu Java, JVM, JDK

## 1. Apa itu Java?

Java adalah bahasa pemrograman tingkat tinggi yang:

- Berbasis Object-Oriented Programming (OOP)
- Bersifat strongly typed
- Menggunakan konsep Write Once, Run Anywhere (WORA)
- Didesain untuk sistem besar, scalable, dan maintainable

Java sangat relevan di industri 2026 karena:

- Digunakan luas pada backend enterprise (banking, fintech, e-commerce)
- Dominan di sistem microservices berbasis Spring Boot
- Banyak dipakai di sistem high-traffic dan distributed system
- Stabil dan memiliki Long Term Support (LTS) release seperti Java 17 dan Java 21

Java bukan hanya bahasa, tetapi bagian dari ekosistem besar yang terdiri dari JVM, JDK, dan berbagai tools build.

---

## 2. Apa itu JVM?

JVM adalah Java Virtual Machine.

JVM adalah mesin virtual yang menjalankan bytecode hasil kompilasi Java.

Alur kerja Java adalah:

- Kita menulis kode Java (.java)
- Kode dikompilasi oleh compiler menjadi bytecode (.class)
- Bytecode dijalankan oleh JVM

Karena JVM tersedia di berbagai sistem operasi, maka program Java bisa dijalankan di Windows, Linux, dan macOS tanpa perlu ditulis ulang.

Contoh ilustrasi alur:

Source Code (.java)
        ↓
Compiler (javac)
        ↓
Bytecode (.class)
        ↓
JVM
        ↓
Program berjalan

JVM bertanggung jawab atas:

- Memory management
- Garbage Collection
- Keamanan runtime
- Eksekusi bytecode
- Thread management

Di industri, pemahaman JVM penting untuk:

- Optimasi performa
- Debugging memory leak
- Tuning garbage collection
- Menangani aplikasi high-load

---

## 3. Apa itu JDK?

JDK adalah Java Development Kit.

JDK adalah paket lengkap untuk mengembangkan aplikasi Java.

JDK berisi:

- Compiler (javac)
- JVM
- Standard library
- Tools debugging
- Tools packaging

Tanpa JDK, kita tidak bisa mengembangkan program Java.

Perbedaan singkat:

- JVM hanya untuk menjalankan
- JDK untuk mengembangkan
- JRE adalah runtime environment (sudah deprecated secara terpisah, sekarang terintegrasi dalam JDK modern)

---

## 4. Contoh Program Java Sederhana

Berikut contoh program paling dasar.

Contoh 1 — Program Hello World

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, Java 2026!");
    }
}
````

Output:

```
Hello, Java 2026!
```

Penjelasan:

* public class Main adalah deklarasi kelas
* main adalah entry point program
* System.out.println() digunakan untuk mencetak output ke console

---

## 5. Contoh Proses Kompilasi dan Eksekusi

Jika file bernama Main.java, maka jalankan:

```bash
javac Main.java
```

Perintah ini menghasilkan file:

```
Main.class
```

Lalu jalankan dengan:

```bash
java Main
```

Output:

```
Hello, Java 2026!
```

Ini menunjukkan bahwa:

* javac mengubah source code menjadi bytecode
* java menjalankan bytecode menggunakan JVM

---

## 6. Contoh Program dengan Variabel

Contoh 2 — Menggunakan Variabel

```java
public class Main {
    public static void main(String[] args) {
        int age = 20;
        String name = "Eman";

        System.out.println("Nama: " + name);
        System.out.println("Umur: " + age);
    }
}
```

Output:

```
Nama: Eman
Umur: 20
```

Penjelasan:

* int adalah tipe data bilangan bulat
* String adalah tipe data teks
* Tanda + digunakan untuk menggabungkan string

---

## 7. Kenapa Java Masih Relevan di 2026?

Java tetap kuat karena:

* Stabil dan backward compatible
* Banyak digunakan di enterprise
* Mendukung microservices dan cloud-native
* Mendukung concurrency tingkat tinggi
* Memiliki Virtual Threads (Java 21)
* Ekosistem framework sangat matang

Contoh penggunaan nyata di industri:

* Sistem transaksi bank
* API backend e-commerce
* Sistem pembayaran
* Distributed systems
* Platform data processing

---

## 8. Ringkasan EP 01

* Java adalah bahasa OOP untuk sistem besar
* JVM menjalankan bytecode
* JDK digunakan untuk mengembangkan aplikasi
* Java bersifat portable karena JVM
* Program Java dikompilasi menjadi .class sebelum dijalankan
