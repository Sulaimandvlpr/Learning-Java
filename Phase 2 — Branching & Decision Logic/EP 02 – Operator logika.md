# EP 02 - Operator Logika (Logical Operators)

Pada episode ini kita membahas bagaimana menggabungkan beberapa kondisi menjadi satu keputusan.

Jika operator perbandingan menghasilkan boolean, maka operator logika digunakan untuk menggabungkan nilai boolean tersebut.

Operator logika sangat penting dalam:

- Validasi login
- Filtering data
- Rule bisnis (business rules)
- Sistem keamanan
- Permission & role checking

---

## 1. Jenis Operator Logika di Java

Java memiliki beberapa operator logika utama:

- &&  Logical AND  
- ||  Logical OR  
- !   Logical NOT  

Semua operator ini bekerja pada nilai boolean.

---

## 2. Logical AND (&&)

Operator AND akan menghasilkan true hanya jika kedua kondisi bernilai true.

Struktur dasar:

```java
kondisi1 && kondisi2
````

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        int age = 20;
        boolean hasId = true;

        System.out.println(age >= 18 && hasId);
    }
}
```

Output:

```text
true
```

Penjelasan:

* age >= 18 → true
* hasId → true
* true && true → true

Jika salah satu false, hasilnya false.

---

## 3. Logical OR (||)

Operator OR menghasilkan true jika salah satu kondisi true.

Struktur:

```java
kondisi1 || kondisi2
```

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        boolean isAdmin = false;
        boolean isManager = true;

        System.out.println(isAdmin || isManager);
    }
}
```

Output:

```text
true
```

Karena salah satu bernilai true.

---

## 4. Logical NOT (!)

Operator NOT membalik nilai boolean.

Struktur:

```java
!kondisi
```

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        boolean isActive = false;

        System.out.println(!isActive);
    }
}
```

Output:

```text
true
```

Karena false dibalik menjadi true.

---

## 5. Kombinasi Beberapa Operator

Kita bisa menggabungkan beberapa kondisi sekaligus.

Contoh validasi login:

```java
public class Main {
    public static void main(String[] args) {

        String username = "admin";
        String password = "1234";
        boolean isBlocked = false;

        boolean isValid = username.equals("admin")
                          && password.equals("1234")
                          && !isBlocked;

        System.out.println(isValid);
    }
}
```

Output:

```text
true
```

Penjelasan:

* Username benar
* Password benar
* User tidak diblokir
* Semua true → hasil true

---

## 6. Short Circuit Behavior

Java menggunakan short-circuit evaluation pada && dan ||.

Artinya:

* Pada AND, jika kondisi pertama false, kondisi kedua tidak dicek.
* Pada OR, jika kondisi pertama true, kondisi kedua tidak dicek.

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        int x = 5;

        if (x > 10 && x++ > 3) {
        }

        System.out.println(x);
    }
}
```

Output:

```text
5
```

Karena x > 10 adalah false, maka x++ tidak dijalankan.

Ini penting untuk efisiensi dan mencegah error.

---

## 7. Perbedaan && dan &

&& adalah logical AND dengan short-circuit.
& adalah bitwise AND dan tidak short-circuit.

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        int x = 5;

        if (x > 10 & x++ > 3) {
        }

        System.out.println(x);
    }
}
```

Output:

```text
6
```

Karena operator & tetap mengevaluasi kedua sisi.

Dalam industri, hampir selalu gunakan && untuk logika kondisi.

---

## 8. Contoh Kasus Industri

Validasi transaksi:

```java
public class Main {
    public static void main(String[] args) {

        double balance = 5000;
        double withdraw = 2000;
        boolean isVerified = true;

        boolean canWithdraw = balance >= withdraw && isVerified;

        System.out.println(canWithdraw);
    }
}
```

Output:

```text
true
```

Ini adalah contoh sederhana rule keuangan.

---

## 9. Urutan Evaluasi

Prioritas operator:

* ! dievaluasi terlebih dahulu
* kemudian &&
* terakhir ||

Gunakan tanda kurung untuk memperjelas logika.

Contoh:

```java
boolean result = (true || false) && false;
```

Tanpa tanda kurung bisa membingungkan.

---

## Ringkasan EP 02

* && untuk semua kondisi harus true
* || untuk minimal satu true
* ! untuk membalik boolean
* Java menggunakan short-circuit
* Gunakan tanda kurung untuk memperjelas logika
* Sangat penting untuk validasi dan business logic

---

## Target Pemahaman Setelah Episode Ini

* Bisa menggabungkan banyak kondisi
* Mengerti short-circuit
* Bisa membaca logika kompleks
* Siap masuk ke if pada EP berikutnya

```
```
