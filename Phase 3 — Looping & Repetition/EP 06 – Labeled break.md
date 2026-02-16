# EP 06 - Labeled break

Pada episode ini kita membahas Labeled break.

Ini adalah fitur lanjutan dari break yang digunakan pada nested loop.

Di industri, ini jarang dipakai dalam kode sehari-hari, tetapi penting untuk dipahami agar kamu benar-benar menguasai kontrol alur program.

---

## 1. Masalah pada Nested Loop

Pada nested loop, break biasa hanya menghentikan loop terdalam.

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 3; i++) {

            for (int j = 1; j <= 3; j++) {

                if (j == 2) {
                    break;
                }

                System.out.println("i=" + i + " j=" + j);
            }
        }
    }
}
````

Output:

```text
i=1 j=1
i=2 j=1
i=3 j=1
```

Penjelasan:

* Saat j == 2, loop dalam berhenti
* Loop luar tetap lanjut
* Hanya loop terdalam yang dihentikan

---

## 2. Apa itu Label

Label adalah penanda yang kita berikan pada sebuah loop.

Format:

```java
labelName:
for (...) {
    ...
}
```

Label diletakkan tepat sebelum loop.

---

## 3. Labeled break

Dengan labeled break, kita bisa menghentikan loop tertentu, bukan hanya loop terdalam.

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        outerLoop:
        for (int i = 1; i <= 3; i++) {

            for (int j = 1; j <= 3; j++) {

                if (j == 2) {
                    break outerLoop;
                }

                System.out.println("i=" + i + " j=" + j);
            }
        }

        System.out.println("Selesai");
    }
}
```

Output:

```text
i=1 j=1
Selesai
```

Penjelasan:

* outerLoop adalah label untuk loop luar
* Saat j == 2
* break outerLoop menghentikan seluruh nested loop
* Program langsung lanjut ke baris setelah loop

---

## 4. Cara Kerja Labeled break

Langkah eksekusi:

* Loop luar mulai
* Loop dalam mulai
* Saat kondisi terpenuhi
* break label dijalankan
* Semua loop yang termasuk dalam label langsung dihentikan

---

## 5. Contoh Kasus Industri

Misalnya kamu sedang mencari data dalam matriks 2D.

Tanpa labeled break:

* Kamu harus pakai flag boolean
* Atau kondisi tambahan

Dengan labeled break:

```java
public class Main {
    public static void main(String[] args) {

        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int target = 5;

        search:
        for (int i = 0; i < matrix.length; i++) {

            for (int j = 0; j < matrix[i].length; j++) {

                if (matrix[i][j] == target) {
                    System.out.println("Ditemukan di posisi [" + i + "," + j + "]");
                    break search;
                }
            }
        }
    }
}
```

Output:

```text
Ditemukan di posisi [1,1]
```

Loop langsung berhenti setelah ditemukan.

Lebih efisien dan tidak perlu variabel tambahan.

---

## 6. Labeled continue

Selain break, label juga bisa digunakan dengan continue.

Contoh:

```java
public class Main {
    public static void main(String[] args) {

        outer:
        for (int i = 1; i <= 3; i++) {

            for (int j = 1; j <= 3; j++) {

                if (j == 2) {
                    continue outer;
                }

                System.out.println("i=" + i + " j=" + j);
            }
        }
    }
}
```

Output:

```text
i=1 j=1
i=2 j=1
i=3 j=1
```

Penjelasan:

Saat j == 2:

* continue outer dijalankan
* Loop luar langsung lanjut ke iterasi berikutnya
* Loop dalam tidak dilanjutkan

---

## 7. Apakah Labeled break Direkomendasikan?

Secara praktik industri:

* Bisa digunakan
* Tapi jarang dipakai
* Biasanya kode direfaktor menjadi method terpisah

Contoh lebih bersih:

Daripada:

* Menggunakan labeled break kompleks

Lebih baik:

* Pindahkan nested loop ke method
* Gunakan return untuk keluar

Itu lebih clean dan mudah dibaca.

---

## 8. Best Practice

* Gunakan labeled break hanya jika memang diperlukan
* Jangan gunakan terlalu banyak label
* Jika logika terlalu kompleks, refactor ke method
* Prioritaskan readability

---

## Ringkasan EP 06

* break biasa menghentikan loop terdalam
* labeled break bisa menghentikan loop tertentu
* labeled continue bisa melompat ke iterasi tertentu
* Jarang dipakai di industri modern
* Tetap penting untuk dipahami

---

## Target Setelah Episode Ini

* Menguasai kontrol alur penuh dalam looping
* Siap masuk ke Stage berikutnya yaitu Methods & Modular Programming

```
```

