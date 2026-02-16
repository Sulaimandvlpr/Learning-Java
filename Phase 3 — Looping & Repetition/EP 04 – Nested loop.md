# EP 04 - Nested Loop

Pada episode ini kita membahas perulangan bertingkat.

Nested loop adalah loop di dalam loop.

Digunakan ketika kita bekerja dengan:

- Tabel atau matriks
- Data dua dimensi
- Pola (pattern)
- Kombinasi data
- Perbandingan antar elemen

Dalam industri, nested loop sering muncul pada:

- Proses matrix
- Data grid
- Algoritma sederhana
- Pencarian kombinasi

---

## 1. Struktur Dasar Nested Loop

Struktur umum:

```java
for (inisialisasi1; kondisi1; update1) {
    for (inisialisasi2; kondisi2; update2) {
        // kode dijalankan
    }
}
````

Penjelasan:

* Loop luar berjalan terlebih dahulu
* Untuk setiap iterasi loop luar, loop dalam dijalankan penuh

---

## 2. Contoh Sederhana

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 3; i++) {
            for (int j = 1; j <= 2; j++) {
                System.out.println("i=" + i + " j=" + j);
            }
        }
    }
}
```

Output:

```text
i=1 j=1
i=1 j=2
i=2 j=1
i=2 j=2
i=3 j=1
i=3 j=2
```

Penjelasan alur:

* i = 1 → j berjalan dari 1 sampai 2
* i = 2 → j berjalan lagi dari 1 sampai 2
* i = 3 → j berjalan lagi dari 1 sampai 2

---

## 3. Visualisasi Pola Bintang

Nested loop sering digunakan untuk membuat pola.

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 3; i++) {
            for (int j = 1; j <= 4; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }
    }
}
```

Output:

```text
* * * * 
* * * * 
* * * * 
```

Loop luar menentukan baris.
Loop dalam menentukan kolom.

---

## 4. Nested Loop dengan while

Nested loop tidak hanya untuk for.

```java
public class Main {
    public static void main(String[] args) {

        int i = 1;

        while (i <= 2) {
            int j = 1;

            while (j <= 3) {
                System.out.println("i=" + i + " j=" + j);
                j++;
            }

            i++;
        }
    }
}
```

Output:

```text
i=1 j=1
i=1 j=2
i=1 j=3
i=2 j=1
i=2 j=2
i=2 j=3
```

---

## 5. Kompleksitas Nested Loop

Jika satu loop berjalan n kali,
dan di dalamnya ada loop lain yang juga n kali,
maka total operasi menjadi n × n.

Ini disebut kompleksitas O(n²).

Contoh:

```java
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        // operasi
    }
}
```

Jika n besar, performa bisa menurun drastis.

Dalam industri, nested loop harus diperhatikan karena bisa menyebabkan sistem lambat.

---

## 6. Contoh Kasus Industri Sederhana

Simulasi pencocokan dua daftar:

```java
public class Main {
    public static void main(String[] args) {

        int[] listA = {1, 2, 3};
        int[] listB = {2, 3, 4};

        for (int i = 0; i < listA.length; i++) {
            for (int j = 0; j < listB.length; j++) {
                if (listA[i] == listB[j]) {
                    System.out.println("Match: " + listA[i]);
                }
            }
        }
    }
}
```

Output:

```text
Match: 2
Match: 3
```

Ini contoh pencarian sederhana dengan kompleksitas O(n²).

Di sistem besar, pendekatan seperti ini bisa diganti dengan struktur data yang lebih efisien.

---

## 7. Kesalahan Umum

* Lupa mereset variabel loop dalam
* Terlalu banyak nested level
* Tidak sadar dampak performa
* Logika sulit dibaca

Jika nested lebih dari 3 level, biasanya perlu refactor.

---

## 8. Best Practice Industri

* Gunakan nested loop hanya jika perlu
* Perhatikan kompleksitas
* Pertimbangkan struktur data seperti Set atau Map
* Pecah menjadi method jika terlalu kompleks

---

## Ringkasan EP 04

* Nested loop adalah loop di dalam loop
* Loop dalam dijalankan penuh setiap iterasi loop luar
* Digunakan untuk tabel, matriks, dan kombinasi
* Bisa menyebabkan kompleksitas O(n²)
* Harus berhati-hati dalam sistem produksi

---

## Target Setelah Episode Ini

* Bisa membuat nested loop
* Mengerti cara kerja iterasi bertingkat
* Mengerti dampak performa dasar
* Siap lanjut ke break dan continue pada episode berikutnya

```
```

