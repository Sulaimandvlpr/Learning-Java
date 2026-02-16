# EP 05 - break dan continue

Pada episode ini kita membahas dua keyword penting dalam looping:

- break
- continue

Keduanya digunakan untuk mengontrol alur perulangan.

Dalam industri, penggunaan yang tepat membuat kode lebih efisien dan mudah dibaca.

---

## 1. break

break digunakan untuk menghentikan loop secara langsung.

Ketika break dijalankan:

- Loop langsung berhenti
- Eksekusi keluar dari blok loop
- Program lanjut ke baris setelah loop

---

## 2. Contoh break pada for

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 10; i++) {

            if (i == 5) {
                break;
            }

            System.out.println(i);
        }
    }
}
````

Output:

```text
1
2
3
4
```

Penjelasan:

Saat i bernilai 5, kondisi terpenuhi.
break dieksekusi.
Loop berhenti total.
Angka 5 tidak dicetak.

---

## 3. break pada while

```java
public class Main {
    public static void main(String[] args) {

        int i = 1;

        while (true) {

            if (i > 3) {
                break;
            }

            System.out.println(i);
            i++;
        }
    }
}
```

Output:

```text
1
2
3
```

while(true) berarti loop tak terbatas.
break digunakan sebagai mekanisme keluar.

Ini sering digunakan pada:

* Sistem menu
* Game loop
* Server listener

---

## 4. continue

continue digunakan untuk melewati sisa kode dalam iterasi saat ini.

Loop tidak berhenti.
Loop lanjut ke iterasi berikutnya.

---

## 5. Contoh continue

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {

            if (i == 3) {
                continue;
            }

            System.out.println(i);
        }
    }
}
```

Output:

```text
1
2
4
5
```

Penjelasan:

Saat i bernilai 3,
continue dijalankan,
System.out.println(i) dilewati,
loop lanjut ke i berikutnya.

---

## 6. Perbedaan break dan continue

break:

* Menghentikan loop sepenuhnya

continue:

* Melewati satu iterasi saja

Ilustrasi logika:

break:
1 2 3 STOP

continue:
1 2 skip 3 4 5

---

## 7. Penggunaan pada Nested Loop

break hanya menghentikan loop terdalam.

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
```

Output:

```text
i=1 j=1
i=2 j=1
i=3 j=1
```

Penjelasan:

Saat j == 2,
loop dalam berhenti,
loop luar tetap lanjut.

---

## 8. Kapan break digunakan di industri

* Saat menemukan data yang dicari
* Validasi gagal
* Early exit untuk efisiensi
* Menghentikan loop tak terbatas

Contoh pencarian:

```java
public class Main {
    public static void main(String[] args) {

        int[] numbers = {4, 7, 9, 2, 5};
        int target = 9;

        for (int i = 0; i < numbers.length; i++) {

            if (numbers[i] == target) {
                System.out.println("Ditemukan di index " + i);
                break;
            }
        }
    }
}
```

Output:

```text
Ditemukan di index 2
```

Loop berhenti setelah data ditemukan.
Ini lebih efisien dibanding terus berjalan.

---

## 9. Kesalahan Umum

* Menggunakan continue berlebihan sehingga kode sulit dibaca
* Menggunakan break tanpa memahami alur
* Membuat loop tak terbatas tanpa break

---

## 10. Best Practice

* Gunakan break untuk early exit
* Gunakan continue untuk menyederhanakan kondisi
* Jangan membuat logika terlalu bercabang dalam loop
* Jika terlalu kompleks, refactor ke method

---

## Ringkasan EP 05

* break menghentikan loop sepenuhnya
* continue melewati satu iterasi
* break penting untuk efisiensi
* continue membantu menjaga kode tetap bersih
* Sangat sering digunakan dalam sistem produksi

---

## Target Setelah Episode Ini

* Menguasai kontrol alur dalam looping
* Memahami early termination
* Siap lanjut ke Labeled break pada episode berikutnya

```
```

