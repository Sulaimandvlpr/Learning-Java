# EP 05 - else-if Ladder

Pada episode ini kita membahas bagaimana menangani lebih dari dua kemungkinan kondisi.

Jika if-else hanya cocok untuk dua kemungkinan, maka else-if digunakan ketika ada banyak cabang keputusan.

Ini sering digunakan dalam:

- Sistem penilaian
- Validasi level akses
- Kategori produk
- Perhitungan pajak bertingkat
- Business rule kompleks

---

## 1. Struktur Dasar else-if

Struktur umum:

```java
if (kondisi1) {
    // dijalankan jika kondisi1 true
} else if (kondisi2) {
    // dijalankan jika kondisi2 true
} else if (kondisi3) {
    // dan seterusnya
} else {
    // dijalankan jika semua kondisi di atas false
}
````

Penjelasan:

* Kondisi diperiksa dari atas ke bawah
* Begitu satu kondisi bernilai true, blok tersebut dijalankan
* Setelah itu, pengecekan berhenti
* else bersifat opsional tetapi biasanya digunakan sebagai default

---

## 2. Contoh Sistem Penilaian

```java
public class Main {
    public static void main(String[] args) {

        int score = 85;

        if (score >= 90) {
            System.out.println("Grade A");
        } else if (score >= 80) {
            System.out.println("Grade B");
        } else if (score >= 70) {
            System.out.println("Grade C");
        } else {
            System.out.println("Tidak Lulus");
        }
    }
}
```

Output:

```text id="q7zp91"
Grade B
```

Penjelasan:

* score >= 90 → false
* score >= 80 → true
* Program berhenti di sini
* Kondisi berikutnya tidak diperiksa

---

## 3. Urutan Kondisi Sangat Penting

Perhatikan contoh yang salah:

```java
public class Main {
    public static void main(String[] args) {

        int score = 95;

        if (score >= 70) {
            System.out.println("Grade C");
        } else if (score >= 80) {
            System.out.println("Grade B");
        } else if (score >= 90) {
            System.out.println("Grade A");
        }
    }
}
```

Output:

```text id="k1x8dw"
Grade C
```

Walaupun nilainya 95, hasilnya Grade C.

Kenapa?

Karena kondisi pertama sudah true, sehingga yang lain tidak dicek.

Best practice:

* Urutkan dari kondisi paling spesifik atau terbesar ke terkecil

---

## 4. else-if dengan Operator Logika

```java
public class Main {
    public static void main(String[] args) {

        int age = 25;
        boolean hasId = true;

        if (age < 18) {
            System.out.println("Terlalu muda");
        } else if (age >= 18 && hasId) {
            System.out.println("Boleh masuk");
        } else {
            System.out.println("Perlu ID");
        }
    }
}
```

Output:

```text id="r8y2mv"
Boleh masuk
```

---

## 5. else-if Tanpa else

else tidak wajib digunakan.

```java
public class Main {
    public static void main(String[] args) {

        int temperature = 30;

        if (temperature > 35) {
            System.out.println("Panas ekstrem");
        } else if (temperature > 25) {
            System.out.println("Hangat");
        }
    }
}
```

Output:

```text id="n5q3sj"
Hangat
```

Namun jika tidak ada kondisi yang terpenuhi, tidak ada output.

---

## 6. Contoh Kasus Industri

Simulasi kategori pelanggan berdasarkan total belanja:

```java
public class Main {
    public static void main(String[] args) {

        double totalPurchase = 1500000;

        if (totalPurchase >= 5000000) {
            System.out.println("Platinum");
        } else if (totalPurchase >= 2000000) {
            System.out.println("Gold");
        } else if (totalPurchase >= 1000000) {
            System.out.println("Silver");
        } else {
            System.out.println("Regular");
        }
    }
}
```

Output:

```text id="x2h7tm"
Silver
```

Ini adalah contoh tiering system yang umum di e-commerce dan fintech.

---

## 7. else-if vs switch

else-if cocok untuk:

* Rentang nilai
* Kondisi kompleks
* Kombinasi logika

switch cocok untuk:

* Nilai tetap
* Perbandingan satu variabel
* Banyak pilihan diskrit

Kita akan membahas switch di episode berikutnya.

---

## 8. Best Practice Industri

* Urutkan kondisi dari paling spesifik ke paling umum
* Hindari else-if terlalu panjang karena sulit dibaca
* Jika lebih dari 5-6 cabang, pertimbangkan switch atau polymorphism
* Gunakan variabel boolean untuk memperjelas logika

Contoh lebih clean:

```java
boolean isGold = totalPurchase >= 2000000 && totalPurchase < 5000000;

if (isGold) {
    System.out.println("Gold");
}
```

---

## Ringkasan EP 05

* else-if digunakan untuk banyak kemungkinan
* Evaluasi berjalan dari atas ke bawah
* Urutan kondisi sangat penting
* else bersifat default
* Banyak digunakan dalam business rule

---

## Target Setelah Episode Ini

* Bisa membuat percabangan dengan banyak kondisi
* Mengerti pentingnya urutan kondisi
* Bisa menerapkan logika bertingkat
* Siap lanjut ke Nested if pada episode berikutnya

```
```
