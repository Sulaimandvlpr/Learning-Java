# EP 03 — Variable & Tipe Data Primitif

Pada episode ini kita membahas fondasi paling penting dalam pemrograman Java yaitu variable dan tipe data. Hampir semua program akan menggunakan variable untuk menyimpan dan memanipulasi data.

---

## 1. Apa itu Variable

Variable adalah tempat penyimpanan data di dalam memory.

Secara sederhana:

- Variable memiliki nama
- Variable memiliki tipe data
- Variable menyimpan nilai

Struktur deklarasi variable:

```java
tipeData namaVariable = nilai;
````

Contoh:

```java
int age = 21;
```

Penjelasan:

* int adalah tipe data
* age adalah nama variable
* 21 adalah nilai yang disimpan

---

## 2. Tipe Data Primitif di Java

Java memiliki 8 tipe data primitif:

* byte
* short
* int
* long
* float
* double
* char
* boolean

Tipe primitif menyimpan nilai secara langsung di memory dan bukan object.

---

## 3. Tipe Data Numerik

### int

Digunakan untuk bilangan bulat.

```java
public class Main {
    public static void main(String[] args) {
        int number = 10;
        System.out.println(number);
    }
}
```

Output:

```text
10
```

Range int adalah -2^31 sampai 2^31-1.

---

### long

Digunakan untuk angka yang lebih besar dari int.

```java
public class Main {
    public static void main(String[] args) {
        long population = 8000000000L;
        System.out.println(population);
    }
}
```

Output:

```text
8000000000
```

Huruf L di akhir angka wajib untuk literal long besar.

---

### float dan double

Digunakan untuk angka desimal.

```java
public class Main {
    public static void main(String[] args) {
        float price = 10.5f;
        double pi = 3.14159;

        System.out.println(price);
        System.out.println(pi);
    }
}
```

Output:

```text
10.5
3.14159
```

Catatan:

* float harus diakhiri huruf f
* double adalah tipe desimal default di Java
* Untuk keuangan sebaiknya gunakan BigDecimal, bukan float/double

---

## 4. Tipe Data Karakter

### char

Digunakan untuk satu karakter.

```java
public class Main {
    public static void main(String[] args) {
        char grade = 'A';
        System.out.println(grade);
    }
}
```

Output:

```text
A
```

Char menggunakan tanda kutip satu.

---

## 5. Tipe Data Boolean

Digunakan untuk nilai benar atau salah.

```java
public class Main {
    public static void main(String[] args) {
        boolean isActive = true;
        System.out.println(isActive);
    }
}
```

Output:

```text
true
```

Boolean hanya memiliki dua nilai:

* true
* false

---

## 6. Tipe Data String

String bukan tipe primitif, melainkan class.

Digunakan untuk menyimpan teks.

```java
public class Main {
    public static void main(String[] args) {
        String name = "Eman";
        System.out.println(name);
    }
}
```

Output:

```text
Eman
```

String menggunakan tanda kutip dua.

---

## 7. Deklarasi Tanpa Inisialisasi

Variable bisa dideklarasikan tanpa langsung diberi nilai.

```java
int age;
age = 25;
System.out.println(age);
```

Namun variable lokal wajib diinisialisasi sebelum digunakan.

Contoh error:

```java
int number;
System.out.println(number);
```

Ini akan menghasilkan compile error karena number belum diberi nilai.

---

## 8. Type Casting

Type casting adalah mengubah satu tipe data menjadi tipe lain.

### Implicit Casting

Terjadi otomatis jika tipe kecil ke besar.

```java
int number = 10;
double result = number;
System.out.println(result);
```

Output:

```text
10.0
```

---

### Explicit Casting

Dilakukan manual jika tipe besar ke kecil.

```java
double pi = 3.99;
int value = (int) pi;
System.out.println(value);
```

Output:

```text
3
```

Bagian desimal akan terpotong.

---

## 9. Aturan Penamaan Variable

Konvensi yang benar:

* camelCase
* Tidak boleh diawali angka
* Tidak boleh menggunakan keyword Java

Contoh benar:

```java
int totalScore;
String firstName;
boolean isLoggedIn;
```

Contoh salah:

```java
int 1score;
int class;
```

---

## 10. Contoh Program Gabungan

```java
public class Main {
    public static void main(String[] args) {

        String name = "Eman";
        int age = 21;
        double height = 170.5;
        boolean isStudent = true;

        System.out.println("Nama: " + name);
        System.out.println("Umur: " + age);
        System.out.println("Tinggi: " + height);
        System.out.println("Mahasiswa: " + isStudent);
    }
}
```

Output:

```text
Nama: Eman
Umur: 21
Tinggi: 170.5
Mahasiswa: true
```

---

## Ringkasan EP 03

* Variable adalah tempat menyimpan data di memory
* Java memiliki 8 tipe data primitif
* String adalah class, bukan tipe primitif
* Casting bisa implicit atau explicit
* Variable harus diinisialisasi sebelum digunakan
* Penamaan mengikuti camelCase

---

## Target Pemahaman Setelah EP 03

* Mengerti perbedaan tipe primitif
* Bisa memilih tipe data yang tepat
* Mengerti casting
* Mengerti aturan deklarasi variable
* Mampu membuat program sederhana dengan berbagai tipe data

```
```

