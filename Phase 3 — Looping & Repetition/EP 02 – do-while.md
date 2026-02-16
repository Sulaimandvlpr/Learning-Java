# EP 02 - do-while Loop

Pada episode ini kita membahas variasi dari while, yaitu do-while.

Perbedaan utama:

- while mengecek kondisi terlebih dahulu
- do-while menjalankan blok dulu, baru mengecek kondisi

Artinya, do-while pasti dijalankan minimal satu kali.

Dalam sistem industri, do-while sering digunakan untuk:

- Menu interaktif
- Validasi input minimal satu kali
- Retry yang harus terjadi minimal sekali
- Loop berbasis konfirmasi user

---

## 1. Struktur Dasar do-while

Struktur umum:

```java
do {
    // kode dijalankan
} while (kondisi);
````

Perhatikan tanda titik koma setelah while.
Itu wajib.

Alur:

* Blok dijalankan terlebih dahulu
* Setelah itu kondisi dicek
* Jika true, ulangi
* Jika false, berhenti

---

## 2. Perbedaan while vs do-while

Contoh while:

```java
int x = 5;

while (x < 3) {
    System.out.println("Hello");
}
```

Output:

Tidak ada output karena kondisi sudah false sejak awal.

Contoh do-while:

```java
public class Main {
    public static void main(String[] args) {

        int x = 5;

        do {
            System.out.println("Hello");
        } while (x < 3);
    }
}
```

Output:

```text
Hello
```

Karena blok dijalankan dulu sebelum pengecekan.

---

## 3. Contoh Perulangan Angka

```java
public class Main {
    public static void main(String[] args) {

        int i = 1;

        do {
            System.out.println(i);
            i++;
        } while (i <= 5);
    }
}
```

Output:

```text
1
2
3
4
5
```

---

## 4. Simulasi Menu Sederhana

Contoh sistem menu yang berjalan minimal sekali.

```java
public class Main {
    public static void main(String[] args) {

        int choice = 1;

        do {
            System.out.println("1. Lihat saldo");
            System.out.println("2. Keluar");

            choice = 2;

        } while (choice != 2);

        System.out.println("Program selesai");
    }
}
```

Output:

```text
1. Lihat saldo
2. Keluar
Program selesai
```

Ini pola umum di aplikasi berbasis CLI.

---

## 5. Simulasi Retry Minimal Sekali

```java
public class Main {
    public static void main(String[] args) {

        int retry = 0;

        do {
            System.out.println("Mencoba koneksi...");
            retry++;
        } while (retry < 3);

        System.out.println("Selesai mencoba");
    }
}
```

Output:

```text
Mencoba koneksi...
Mencoba koneksi...
Mencoba koneksi...
Selesai mencoba
```

---

## 6. Risiko Infinite Loop pada do-while

Sama seperti while, jika kondisi tidak pernah menjadi false, loop tidak akan berhenti.

Contoh berbahaya:

```java
do {
    System.out.println("Looping...");
} while (true);
```

Ini akan berjalan tanpa henti.

Dalam sistem nyata, infinite loop tanpa kontrol bisa menyebabkan server overload.

---

## 7. Kapan Menggunakan do-while

Gunakan do-while jika:

* Proses harus dijalankan minimal satu kali
* Validasi input awal
* Konfirmasi user
* Menu interaktif

Gunakan while jika:

* Bisa jadi tidak perlu dijalankan sama sekali

---

## Ringkasan EP 02

* do-while selalu berjalan minimal satu kali
* Kondisi dicek setelah blok dijalankan
* Cocok untuk menu dan validasi input
* Tetap harus memastikan kondisi bisa berubah

---

## Target Setelah Episode Ini

* Mengerti perbedaan while dan do-while
* Bisa memilih loop yang tepat
* Menghindari infinite loop
* Siap lanjut ke for loop pada episode berikutnya

```
```

