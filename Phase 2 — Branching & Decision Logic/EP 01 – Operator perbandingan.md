# Phase 2 — EP 01  
# Operator Perbandingan (Comparison Operators)

Pada episode ini kita masuk ke dasar logika pengambilan keputusan.

Operator perbandingan digunakan untuk membandingkan dua nilai dan menghasilkan nilai boolean.

Boolean hanya memiliki dua nilai:

- true
- false

Operator ini akan sangat sering digunakan dalam if, loop, validasi data, filtering, dan business rule di sistem industri.

---

## 1. Daftar Operator Perbandingan

Di Java terdapat operator berikut:

- ==  sama dengan  
- !=  tidak sama dengan  
- >   lebih besar  
- <   lebih kecil  
- >=  lebih besar sama dengan  
- <=  lebih kecil sama dengan  

Semua operator ini menghasilkan boolean.

---

## 2. Operator == (Sama Dengan)

Digunakan untuk membandingkan nilai numerik atau boolean.

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 10;

        System.out.println(a == b);
    }
}
````

Output:

```text
true
```

Karena nilai a dan b sama.

---

## 3. Operator != (Tidak Sama Dengan)

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 5;

        System.out.println(a != b);
    }
}
```

Output:

```text
true
```

Karena 10 tidak sama dengan 5.

---

## 4. Operator Lebih Besar dan Lebih Kecil

```java
public class Main {
    public static void main(String[] args) {
        int score = 85;

        System.out.println(score > 70);
        System.out.println(score < 50);
    }
}
```

Output:

```text
true
false
```

Penjelasan:

* 85 lebih besar dari 70
* 85 tidak lebih kecil dari 50

---

## 5. Operator >= dan <=

```java
public class Main {
    public static void main(String[] args) {
        int age = 18;

        System.out.println(age >= 18);
        System.out.println(age <= 17);
    }
}
```

Output:

```text
true
false
```

Operator ini sering digunakan untuk validasi umur, batas transaksi, dan rule bisnis.

---

## 6. Perbandingan pada Tipe double

Hati-hati ketika membandingkan angka desimal.

```java
public class Main {
    public static void main(String[] args) {
        double a = 0.1 + 0.2;
        System.out.println(a == 0.3);
    }
}
```

Output:

```text
false
```

Penjelasan:

Tipe floating point memiliki keterbatasan presisi.
Di sistem keuangan industri, perhitungan uang tidak menggunakan double, melainkan BigDecimal.

---

## 7. Perbandingan char

char juga bisa dibandingkan karena disimpan sebagai angka Unicode.

```java
public class Main {
    public static void main(String[] args) {
        char a = 'A';
        char b = 'B';

        System.out.println(a < b);
    }
}
```

Output:

```text
true
```

Karena secara Unicode, nilai 'A' lebih kecil dari 'B'.

---

## 8. Perbandingan String

Untuk String tidak boleh menggunakan ==.

Salah:

```java
String text = "Java";
System.out.println(text == "Java");
```

Benar:

```java
public class Main {
    public static void main(String[] args) {
        String text = "Java";
        System.out.println(text.equals("Java"));
    }
}
```

Output:

```text
true
```

Karena equals() membandingkan isi.

---

## 9. Contoh Kasus Industri

Simulasi validasi login sederhana:

```java
public class Main {
    public static void main(String[] args) {

        int userInputPin = 1234;
        int savedPin = 1234;

        System.out.println(userInputPin == savedPin);
    }
}
```

Output:

```text
true
```

Contoh validasi umur minimum:

```java
public class Main {
    public static void main(String[] args) {

        int age = 20;
        System.out.println(age >= 18);
    }
}
```

Output:

```text
true
```

---

## 10. Ringkasan EP 01

* Operator perbandingan menghasilkan boolean
* Digunakan dalam logika keputusan
* == untuk nilai primitif
* equals() untuk String
* Hindari membandingkan double untuk keuangan
* Sangat penting untuk validasi dan business rule

---

## Target Pemahaman Setelah Episode Ini

* Memahami semua operator perbandingan
* Mengerti hasilnya selalu boolean
* Siap masuk ke operator logika pada EP 02

```
```

