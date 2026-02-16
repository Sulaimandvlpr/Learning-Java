# EP 03 - if Statement

Pada episode ini kita mulai menggunakan operator perbandingan dan operator logika untuk membuat keputusan dalam program.

if adalah struktur kontrol yang digunakan untuk menjalankan kode hanya jika suatu kondisi bernilai true.

if adalah fondasi semua sistem backend, validasi, autentikasi, filtering, dan business rule di industri.

---

## 1. Konsep Dasar if

Struktur dasar:

```java
if (kondisi) {
    // kode dijalankan jika kondisi true
}
````

Penjelasan:

* kondisi harus bertipe boolean
* jika kondisi bernilai true maka blok kode dijalankan
* jika false maka dilewati

Contoh paling sederhana:

```java
public class Main {
    public static void main(String[] args) {
        int age = 20;

        if (age >= 18) {
            System.out.println("Dewasa");
        }
    }
}
```

Output:

```text
Dewasa
```

Karena 20 >= 18 bernilai true.

Jika kondisi false, tidak ada output.

---

## 2. if dengan Boolean Langsung

Kondisi tidak harus berupa perbandingan.
Bisa langsung menggunakan variabel boolean.

```java
public class Main {
    public static void main(String[] args) {
        boolean isActive = true;

        if (isActive) {
            System.out.println("User aktif");
        }
    }
}
```

Output:

```text
User aktif
```

---

## 3. if dengan Operator Logika

Kita bisa menggabungkan beberapa kondisi.

```java
public class Main {
    public static void main(String[] args) {

        int age = 25;
        boolean hasId = true;

        if (age >= 18 && hasId) {
            System.out.println("Boleh masuk");
        }
    }
}
```

Output:

```text
Boleh masuk
```

Penjelasan:

* age >= 18 → true
* hasId → true
* true && true → true
* Maka blok dijalankan

---

## 4. Block Scope pada if

Variabel yang dibuat di dalam blok if hanya bisa digunakan di dalam blok tersebut.

```java
public class Main {
    public static void main(String[] args) {

        int score = 90;

        if (score > 80) {
            String grade = "A";
            System.out.println(grade);
        }

        // System.out.println(grade); // error
    }
}
```

Output:

```text
A
```

Variabel grade tidak bisa diakses di luar blok.

Ini disebut block scope.

---

## 5. if Tanpa Kurung Kurawal

Jika hanya satu baris, kurung kurawal boleh dihilangkan.

```java
public class Main {
    public static void main(String[] args) {

        int number = 5;

        if (number > 0)
            System.out.println("Positif");
    }
}
```

Output:

```text
Positif
```

Namun dalam industri profesional, sangat disarankan tetap menggunakan kurung kurawal untuk menghindari bug.

---

## 6. Kesalahan Umum Pemula

Kesalahan menggunakan assignment (=) alih-alih perbandingan (==).

Salah:

```java
boolean isActive = true;

if (isActive = false) {
    System.out.println("Aktif");
}
```

Ini bukan perbandingan.
Ini mengubah nilai isActive menjadi false.

Benar:

```java
boolean isActive = true;

if (isActive == false) {
    System.out.println("Tidak aktif");
}
```

Atau lebih bersih:

```java
if (!isActive) {
    System.out.println("Tidak aktif");
}
```

---

## 7. Contoh Kasus Industri

Validasi login sederhana:

```java
public class Main {
    public static void main(String[] args) {

        String username = "admin";
        String password = "1234";

        if (username.equals("admin") && password.equals("1234")) {
            System.out.println("Login berhasil");
        }
    }
}
```

Output:

```text
Login berhasil
```

Di dunia nyata, logika ini akan terhubung ke database.

---

## 8. if Bertingkat Tanpa else

Kadang kita ingin beberapa pengecekan terpisah.

```java
public class Main {
    public static void main(String[] args) {

        int score = 95;

        if (score > 90) {
            System.out.println("Excellent");
        }

        if (score > 70) {
            System.out.println("Passed");
        }
    }
}
```

Output:

```text
Excellent
Passed
```

Karena kedua kondisi bernilai true.

---

## Ringkasan EP 03

* if digunakan untuk menjalankan kode jika kondisi true
* Kondisi harus boolean
* Bisa menggunakan operator perbandingan dan logika
* Memiliki block scope
* Disarankan selalu menggunakan kurung kurawal
* Fondasi utama semua sistem decision logic

---

## Target Setelah Episode Ini

* Bisa membuat keputusan sederhana
* Bisa menggabungkan kondisi
* Mengerti scope dalam blok
* Siap lanjut ke if-else pada episode berikutnya

```
```
