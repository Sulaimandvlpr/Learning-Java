# EP 06 - Nested if

Pada episode ini kita membahas percabangan bertingkat.

Nested if adalah kondisi if yang berada di dalam blok if lainnya.

Digunakan ketika keputusan memiliki beberapa level atau tahapan validasi.

Dalam sistem industri, nested if sering muncul pada:

- Validasi login + role
- Validasi transaksi + limit
- Permission checking
- Multi-step verification

---

## 1. Struktur Dasar Nested if

Struktur umum:

```java
if (kondisi1) {
    if (kondisi2) {
        // dijalankan jika kondisi1 dan kondisi2 true
    }
}
````

Artinya:

* Kondisi kedua hanya dicek jika kondisi pertama true

---

## 2. Contoh Sederhana

```java
public class Main {
    public static void main(String[] args) {

        int age = 20;
        boolean hasId = true;

        if (age >= 18) {
            if (hasId) {
                System.out.println("Boleh masuk");
            }
        }
    }
}
```

Output:

```text id="kq7v1m"
Boleh masuk
```

Jika age < 18, maka kondisi kedua tidak pernah dicek.

---

## 3. Nested if dengan else

```java id="h3lp9r"
public class Main {
    public static void main(String[] args) {

        int age = 20;
        boolean hasId = false;

        if (age >= 18) {
            if (hasId) {
                System.out.println("Boleh masuk");
            } else {
                System.out.println("Tidak punya ID");
            }
        } else {
            System.out.println("Terlalu muda");
        }
    }
}
```

Output:

```text id="b0sk92"
Tidak punya ID
```

Alur logika:

* Cek umur
* Jika cukup umur, cek ID
* Jika tidak cukup umur, langsung tolak

---

## 4. Nested if vs Operator Logika

Nested if sering bisa diganti dengan operator logika.

Versi nested:

```java id="k9v3dx"
if (age >= 18) {
    if (hasId) {
        System.out.println("Boleh masuk");
    }
}
```

Versi lebih ringkas:

```java id="d2r8zf"
if (age >= 18 && hasId) {
    System.out.println("Boleh masuk");
}
```

Kapan gunakan nested?

* Jika ada pesan berbeda di tiap level validasi
* Jika setiap level memiliki aksi berbeda
* Jika logika terlalu kompleks untuk satu baris

---

## 5. Contoh Kasus Industri

Simulasi sistem ATM sederhana:

```java id="r6u1kd"
public class Main {
    public static void main(String[] args) {

        boolean cardValid = true;
        boolean pinCorrect = true;
        double balance = 5000;
        double withdraw = 2000;

        if (cardValid) {
            if (pinCorrect) {
                if (balance >= withdraw) {
                    System.out.println("Transaksi berhasil");
                } else {
                    System.out.println("Saldo tidak cukup");
                }
            } else {
                System.out.println("PIN salah");
            }
        } else {
            System.out.println("Kartu tidak valid");
        }
    }
}
```

Output:

```text id="u3q8nt"
Transaksi berhasil
```

Ini adalah contoh validasi bertingkat yang realistis.

---

## 6. Masalah Nested if Terlalu Dalam

Jika nested terlalu dalam, kode menjadi sulit dibaca.

Contoh yang kurang baik:

```java
if (a) {
    if (b) {
        if (c) {
            if (d) {
                // terlalu dalam
            }
        }
    }
}
```

Dalam industri, ini disebut pyramid of doom.

Solusi yang lebih baik adalah menggunakan early return di dalam method, atau memecah logika menjadi method terpisah.

---

## 7. Refactor Nested if Menjadi Lebih Bersih

Contoh lebih clean menggunakan validasi bertahap:

```java id="t8p2az"
public class Main {
    public static void main(String[] args) {

        boolean cardValid = true;
        boolean pinCorrect = true;

        if (!cardValid) {
            System.out.println("Kartu tidak valid");
            return;
        }

        if (!pinCorrect) {
            System.out.println("PIN salah");
            return;
        }

        System.out.println("Akses diberikan");
    }
}
```

Output:

```text id="x9r1mv"
Akses diberikan
```

Ini lebih mudah dibaca dan lebih profesional.

---

## 8. Ringkasan EP 06

* Nested if adalah if di dalam if
* Digunakan untuk keputusan bertingkat
* Kondisi kedua hanya dicek jika kondisi pertama true
* Bisa diganti operator logika jika sederhana
* Hindari nested terlalu dalam
* Gunakan early return untuk kode lebih bersih

---

## Target Setelah Episode Ini

* Bisa membuat percabangan bertingkat
* Mengerti kapan gunakan nested
* Bisa membedakan nested vs operator logika
* Siap lanjut ke switch statement pada episode berikutnya

```
```
