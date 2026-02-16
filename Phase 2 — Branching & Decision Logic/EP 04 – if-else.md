# EP 04 - if-else Statement

Pada episode ini kita mengembangkan struktur if menjadi dua arah keputusan.

Jika sebelumnya kita hanya menjalankan kode ketika kondisi true,
sekarang kita bisa menentukan apa yang terjadi ketika **true dan false**.

if-else adalah dasar dari hampir semua validasi dan decision flow dalam sistem industri.

---

## 1. Konsep Dasar if-else

Struktur dasar:

```java
if (kondisi) {
    // dijalankan jika true
} else {
    // dijalankan jika false
}
````

Penjelasan:

* Jika kondisi true → blok if dijalankan
* Jika kondisi false → blok else dijalankan
* Salah satu pasti dieksekusi

---

## 2. Contoh Sederhana

```java
public class Main {
    public static void main(String[] args) {
        int age = 15;

        if (age >= 18) {
            System.out.println("Dewasa");
        } else {
            System.out.println("Belum Dewasa");
        }
    }
}
```

Output:

```text
Belum Dewasa
```

Karena 15 >= 18 adalah false.

---

## 3. if-else dengan Boolean

```java
public class Main {
    public static void main(String[] args) {
        boolean isMember = true;

        if (isMember) {
            System.out.println("Diskon 20%");
        } else {
            System.out.println("Tidak ada diskon");
        }
    }
}
```

Output:

```text
Diskon 20%
```

---

## 4. if-else dengan Operator Logika

Kita bisa menggabungkan beberapa kondisi.

```java
public class Main {
    public static void main(String[] args) {

        int balance = 5000;
        int withdraw = 7000;

        if (balance >= withdraw) {
            System.out.println("Transaksi berhasil");
        } else {
            System.out.println("Saldo tidak cukup");
        }
    }
}
```

Output:

```text
Saldo tidak cukup
```

Contoh ini sering digunakan dalam sistem keuangan.

---

## 5. Perbedaan Dua if Terpisah vs if-else

Perhatikan perbedaan ini.

Versi if-else:

```java
int score = 60;

if (score >= 75) {
    System.out.println("Lulus");
} else {
    System.out.println("Tidak Lulus");
}
```

Hanya satu output yang muncul.

Versi dua if terpisah:

```java
int score = 60;

if (score >= 75) {
    System.out.println("Lulus");
}

if (score < 75) {
    System.out.println("Tidak Lulus");
}
```

Secara logika bisa sama, tetapi lebih berisiko jika kondisi tidak saling eksklusif.

Dalam industri, gunakan if-else jika memang hanya ada dua kemungkinan.

---

## 6. Nested if-else

Kita bisa menaruh if di dalam if.

```java
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

```text
Tidak punya ID
```

Ini disebut nested decision.

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
        } else {
            System.out.println("Login gagal");
        }
    }
}
```

Output:

```text
Login berhasil
```

Dalam sistem nyata, pengecekan akan dilakukan ke database.

---

## 8. Best Practice Industri

* Gunakan kurung kurawal meskipun satu baris
* Hindari nested terlalu dalam karena sulit dibaca
* Gunakan early return pada method jika logika terlalu kompleks
* Gunakan nama variabel boolean yang jelas seperti isValid, hasAccess

Contoh yang lebih clean:

```java
boolean isValid = username.equals("admin") && password.equals("1234");

if (isValid) {
    System.out.println("Login berhasil");
} else {
    System.out.println("Login gagal");
}
```

---

## Ringkasan EP 04

* if-else digunakan untuk dua kemungkinan hasil
* Salah satu blok pasti dieksekusi
* Cocok untuk validasi dan rule bisnis
* Bisa digabung dengan operator logika
* Hindari nested berlebihan

---

## Target Setelah Episode Ini

* Bisa membuat dua arah keputusan
* Mengerti perbedaan if terpisah dan if-else
* Bisa membuat validasi sederhana
* Siap lanjut ke else-if ladder pada episode berikutnya

```
```

