# EP 01 - while Loop

Pada episode ini kita masuk ke konsep perulangan.

Loop digunakan ketika kita ingin menjalankan blok kode berulang kali selama suatu kondisi bernilai true.

Dalam sistem industri, loop digunakan untuk:

- Memproses data dalam jumlah banyak
- Membaca file baris demi baris
- Mengiterasi array dan collection
- Melakukan retry request
- Polling sistem eksternal

while adalah bentuk loop paling dasar dan paling fleksibel.

---

## 1. Struktur Dasar while

Struktur umum:

```java
while (kondisi) {
    // kode dijalankan selama kondisi true
}
````

Penjelasan:

* Kondisi dicek sebelum eksekusi
* Jika kondisi false sejak awal, blok tidak pernah dijalankan
* Jika kondisi selalu true, akan terjadi infinite loop

---

## 2. Contoh Sederhana

```java
public class Main {
    public static void main(String[] args) {

        int i = 1;

        while (i <= 5) {
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
4
5
```

Penjelasan alur:

* i mulai dari 1
* Selama i <= 5, cetak i
* Setelah itu i ditambah 1
* Berhenti saat i menjadi 6

---

## 3. Pentingnya Update Variable

Jika kita lupa mengubah nilai variabel di dalam loop, program bisa berjalan tanpa henti.

Contoh berbahaya:

```java
int i = 1;

while (i <= 5) {
    System.out.println(i);
}
```

Ini menyebabkan infinite loop karena i tidak pernah berubah.

Dalam sistem nyata, infinite loop bisa menyebabkan:

* CPU 100%
* Memory leak
* Server crash

---

## 4. while dengan Kondisi Boolean

```java
public class Main {
    public static void main(String[] args) {

        boolean isRunning = true;
        int counter = 0;

        while (isRunning) {
            System.out.println("Running...");
            counter++;

            if (counter == 3) {
                isRunning = false;
            }
        }
    }
}
```

Output:

```text
Running...
Running...
Running...
```

Loop berhenti karena kondisi berubah menjadi false.

---

## 5. Pola Umum while di Industri

Struktur umum while dalam sistem nyata biasanya seperti ini:

```java
while (condition) {
    // proses
    // update condition
}
```

Contoh retry sederhana:

```java
public class Main {
    public static void main(String[] args) {

        int retry = 0;

        while (retry < 3) {
            System.out.println("Mencoba koneksi...");
            retry++;
        }

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

## 6. while untuk Validasi Input (Simulasi)

Contoh simulasi PIN ATM:

```java
public class Main {
    public static void main(String[] args) {

        int correctPin = 1234;
        int inputPin = 1111;
        int attempt = 0;

        while (inputPin != correctPin && attempt < 3) {
            System.out.println("PIN salah");
            attempt++;
            inputPin = 1234;
        }

        if (inputPin == correctPin) {
            System.out.println("Akses diberikan");
        }
    }
}
```

Output:

```text
PIN salah
Akses diberikan
```

---

## 7. Kapan Menggunakan while

Gunakan while jika:

* Jumlah perulangan tidak diketahui di awal
* Loop tergantung pada kondisi dinamis
* Menggunakan sistem event atau polling

Gunakan for jika:

* Jumlah perulangan sudah jelas

for akan dibahas di episode berikutnya.

---

## 8. Best Practice Industri

* Pastikan kondisi loop bisa berubah
* Hindari infinite loop tanpa kontrol
* Gunakan logging untuk debugging loop kompleks
* Gunakan break jika perlu keluar lebih awal
* Gunakan while untuk kondisi berbasis status

---

## Ringkasan EP 01

* while adalah loop berbasis kondisi
* Kondisi dicek sebelum eksekusi
* Bisa tidak dijalankan sama sekali
* Wajib memastikan kondisi berubah
* Digunakan luas dalam sistem backend

---

## Target Setelah Episode Ini

* Mengerti konsep perulangan
* Bisa membuat while loop sederhana
* Menghindari infinite loop
* Siap lanjut ke do-while pada episode berikutnya

```
```
