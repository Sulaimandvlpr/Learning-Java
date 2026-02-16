# EP 04 — Operator di Java (Aritmatika, Perbandingan, Logika, dan Penugasan)

Operator adalah simbol yang digunakan untuk melakukan operasi terhadap nilai atau variable. 
Memahami operator sangat penting karena hampir semua logika program bergantung pada operator.

---

## 1. Operator Aritmatika

Digunakan untuk operasi matematika dasar.

Daftar operator aritmatika:

- +  penjumlahan
- -  pengurangan
- *  perkalian
- /  pembagian
- %  modulus (sisa bagi)

Contoh:

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 3;

        System.out.println(a + b);
        System.out.println(a - b);
        System.out.println(a * b);
        System.out.println(a / b);
        System.out.println(a % b);
    }
}
````

Output:

```text
13
7
30
3
1
```

Penjelasan:

* 10 / 3 menghasilkan 3 karena pembagian int menghilangkan desimal
* 10 % 3 menghasilkan 1 karena sisa pembagian adalah 1

Jika ingin hasil desimal, salah satu operand harus bertipe double:

```java
double result = 10.0 / 3;
System.out.println(result);
```

Output:

```text
3.3333333333333335
```

---

## 2. Operator Penugasan (Assignment)

Digunakan untuk memberi nilai pada variable.

Operator penugasan dasar:

* =

Contoh:

```java
int x = 5;
```

Operator penugasan gabungan:

* +=
* -=
* *=
* /=
* %=

Contoh:

```java
public class Main {
    public static void main(String[] args) {
        int x = 10;

        x += 5;
        System.out.println(x);

        x *= 2;
        System.out.println(x);
    }
}
```

Output:

```text
15
30
```

Penjelasan:

* x += 5 sama dengan x = x + 5
* x *= 2 sama dengan x = x * 2

---

## 3. Operator Increment dan Decrement

Digunakan untuk menambah atau mengurangi nilai 1.

Operator:

* ++

---

Contoh:

```java
public class Main {
    public static void main(String[] args) {
        int x = 5;

        x++;
        System.out.println(x);

        x--;
        System.out.println(x);
    }
}
```

Output:

```text
6
5
```

Perbedaan prefix dan postfix:

```java
int a = 5;
int b = a++;
System.out.println(a);
System.out.println(b);
```

Output:

```text
6
5
```

Penjelasan:

* a++ artinya nilai lama dipakai dulu, lalu ditambah

Contoh prefix:

```java
int a = 5;
int b = ++a;
System.out.println(a);
System.out.println(b);
```

Output:

```text
6
6
```

Penjelasan:

* ++a artinya ditambah dulu, lalu digunakan

---

## 4. Operator Perbandingan

Digunakan untuk membandingkan dua nilai.
Hasilnya selalu boolean.

Daftar operator perbandingan:

* ==
* !=
* >
* <
* > =
* <=

Contoh:

```java
public class Main {
    public static void main(String[] args) {
        int a = 10;
        int b = 5;

        System.out.println(a == b);
        System.out.println(a != b);
        System.out.println(a > b);
        System.out.println(a < b);
    }
}
```

Output:

```text
false
true
true
false
```

Catatan penting:

* == digunakan untuk membandingkan nilai
* = digunakan untuk assignment

---

## 5. Operator Logika

Digunakan untuk menggabungkan kondisi boolean.

Daftar operator logika:

* &&  logical AND
* ||  logical OR
* !   logical NOT

Contoh:

```java
public class Main {
    public static void main(String[] args) {
        int age = 20;
        boolean hasId = true;

        boolean canEnter = age >= 18 && hasId;
        System.out.println(canEnter);
    }
}
```

Output:

```text
true
```

Contoh OR:

```java
boolean result = false || true;
System.out.println(result);
```

Output:

```text
true
```

Contoh NOT:

```java
boolean active = true;
System.out.println(!active);
```

Output:

```text
false
```

---

## 6. Operator Relasional + Logika dalam Satu Contoh

```java
public class Main {
    public static void main(String[] args) {

        int score = 85;
        boolean isPassing = score >= 75 && score <= 100;

        System.out.println("Lulus: " + isPassing);
    }
}
```

Output:

```text
Lulus: true
```

---

## 7. Operator Ternary

Operator singkat untuk if-else sederhana.

Struktur:

kondisi ? nilaiJikaTrue : nilaiJikaFalse

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        int age = 17;
        String status = age >= 18 ? "Dewasa" : "Belum Dewasa";

        System.out.println(status);
    }
}
```

Output:

```text
Belum Dewasa
```

---

## 8. Ringkasan EP 04

* Operator aritmatika digunakan untuk operasi matematika
* Operator penugasan digunakan untuk memberi dan memperbarui nilai
* Operator perbandingan menghasilkan boolean
* Operator logika menggabungkan kondisi
* Prefix dan postfix increment berbeda perilaku
* Operator ternary adalah bentuk singkat if-else

---

## Target Pemahaman Setelah EP 04

* Mampu menggunakan semua operator dasar
* Memahami perbedaan == dan =
* Memahami logika boolean
* Mengerti cara kerja increment prefix dan postfix
* Siap masuk ke percabangan dan kontrol alur pada EP berikutnya

```
```

