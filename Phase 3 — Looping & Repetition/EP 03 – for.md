# EP 03 - for Loop

Pada episode ini kita membahas loop yang paling sering digunakan dalam pemrograman profesional, yaitu for.

Jika while digunakan ketika jumlah perulangan tidak pasti,
maka for digunakan ketika jumlah iterasi sudah diketahui dengan jelas.

Dalam industri, for sangat sering digunakan untuk:

- Iterasi array
- Iterasi collection
- Proses batch data
- Perhitungan numerik
- Pagination logic

---

## 1. Struktur Dasar for

Struktur umum:

```java
for (inisialisasi; kondisi; update) {
    // kode dijalankan
}
````

Penjelasan:

* inisialisasi dijalankan sekali di awal
* kondisi dicek sebelum setiap iterasi
* update dijalankan setelah setiap iterasi
* Jika kondisi false, loop berhenti

---

## 2. Contoh Dasar

```java id="m3x7qa"
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i <= 5; i++) {
            System.out.println(i);
        }
    }
}
```

Output:

```text id="8ltz4w"
1
2
3
4
5
```

Alur eksekusi:

* int i = 1
* Cek i <= 5
* Jalankan blok
* i++
* Ulangi

---

## 3. for Mundur

for tidak harus naik, bisa juga turun.

```java id="k9p4sd"
public class Main {
    public static void main(String[] args) {

        for (int i = 5; i >= 1; i--) {
            System.out.println(i);
        }
    }
}
```

Output:

```text id="p2vd6z"
5
4
3
2
1
```

---

## 4. for dengan Increment Lebih dari 1

```java id="x6qn2f"
public class Main {
    public static void main(String[] args) {

        for (int i = 0; i <= 10; i += 2) {
            System.out.println(i);
        }
    }
}
```

Output:

```text id="y8fh3k"
0
2
4
6
8
10
```

---

## 5. Perbandingan for dan while

Versi while:

```java id="r7sw8n"
int i = 1;

while (i <= 5) {
    System.out.println(i);
    i++;
}
```

Versi for:

```java id="a5n3wt"
for (int i = 1; i <= 5; i++) {
    System.out.println(i);
}
```

for lebih ringkas dan lebih mudah dibaca ketika jumlah iterasi jelas.

Dalam industri, hampir semua iterasi berbasis index menggunakan for.

---

## 6. Scope Variable pada for

Variabel yang dibuat di dalam for hanya berlaku di dalam loop.

```java id="h8qlx2"
for (int i = 0; i < 3; i++) {
    System.out.println(i);
}

// System.out.println(i); // error
```

Ini disebut block scope.

---

## 7. Infinite Loop dengan for

Sama seperti while, for juga bisa menjadi infinite loop.

```java id="b7txra"
for (;;) {
    System.out.println("Loop tanpa henti");
}
```

Karena tidak ada kondisi yang menghentikan.

Dalam sistem server, ini sangat berbahaya jika tidak terkontrol.

---

## 8. Contoh Kasus Industri

Simulasi proses batch data:

```java id="t2kp9m"
public class Main {
    public static void main(String[] args) {

        int totalData = 5;

        for (int i = 1; i <= totalData; i++) {
            System.out.println("Memproses data ke-" + i);
        }

        System.out.println("Selesai memproses");
    }
}
```

Output:

```text id="v4mz9p"
Memproses data ke-1
Memproses data ke-2
Memproses data ke-3
Memproses data ke-4
Memproses data ke-5
Selesai memproses
```

---

## 9. Best Practice Industri

* Gunakan for jika jumlah iterasi jelas
* Gunakan nama variabel yang jelas jika loop kompleks
* Hindari logika terlalu kompleks di dalam header for
* Jangan buat infinite loop tanpa kontrol
* Untuk koleksi modern, nanti kita akan belajar enhanced for dan Stream

---

## Ringkasan EP 03

* for digunakan untuk iterasi dengan jumlah pasti
* Memiliki tiga bagian: inisialisasi, kondisi, update
* Lebih ringkas dari while
* Memiliki scope terbatas
* Sangat sering digunakan dalam produksi

---

## Target Setelah Episode Ini

* Bisa menggunakan for dengan benar
* Mengerti perbedaan for dan while
* Bisa membuat loop maju dan mundur
* Siap lanjut ke Nested loop pada episode berikutnya

```
```

