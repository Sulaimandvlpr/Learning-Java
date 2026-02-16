# EP 07 - switch Statement

Pada episode ini kita membahas alternatif dari else-if ladder, yaitu switch.

switch digunakan ketika kita ingin membandingkan satu variabel terhadap beberapa kemungkinan nilai tetap.

switch lebih rapi dan lebih mudah dibaca dibandingkan banyak else-if jika kondisinya berbasis nilai diskrit.

Dalam industri, switch sering digunakan untuk:

- Mapping kode status
- Mapping role user
- Mapping menu pilihan
- Mapping enum
- Command handler sederhana

---

## 1. Struktur Dasar switch

Struktur umum:

```java
switch (variable) {
    case nilai1:
        // aksi
        break;
    case nilai2:
        // aksi
        break;
    default:
        // aksi jika tidak ada yang cocok
}
````

Penjelasan:

* variable bisa berupa int, char, String, atau enum
* case adalah nilai yang dibandingkan
* break digunakan untuk menghentikan eksekusi
* default bersifat opsional

---

## 2. Contoh Menggunakan int

```java
public class Main {
    public static void main(String[] args) {

        int day = 3;

        switch (day) {
            case 1:
                System.out.println("Senin");
                break;
            case 2:
                System.out.println("Selasa");
                break;
            case 3:
                System.out.println("Rabu");
                break;
            default:
                System.out.println("Hari tidak valid");
        }
    }
}
```

Output:

```text id="j8v4ap"
Rabu
```

---

## 3. Pentingnya break

Jika tidak menggunakan break, maka akan terjadi fall-through.

Contoh tanpa break:

```java
public class Main {
    public static void main(String[] args) {

        int number = 1;

        switch (number) {
            case 1:
                System.out.println("Satu");
            case 2:
                System.out.println("Dua");
            case 3:
                System.out.println("Tiga");
        }
    }
}
```

Output:

```text id="t9f2lm"
Satu
Dua
Tiga
```

Karena setelah case 1 cocok, eksekusi terus berjalan ke bawah.

Dalam industri, fall-through jarang digunakan dan sering menjadi sumber bug.

---

## 4. switch dengan String

Java modern mendukung String dalam switch.

```java
public class Main {
    public static void main(String[] args) {

        String role = "ADMIN";

        switch (role) {
            case "ADMIN":
                System.out.println("Akses penuh");
                break;
            case "USER":
                System.out.println("Akses terbatas");
                break;
            default:
                System.out.println("Role tidak dikenal");
        }
    }
}
```

Output:

```text id="y6b3xz"
Akses penuh
```

Ini sangat umum dalam sistem authorization.

---

## 5. Multiple Case dalam Satu Blok

Kita bisa menggabungkan beberapa case.

```java
public class Main {
    public static void main(String[] args) {

        int month = 1;

        switch (month) {
            case 12:
            case 1:
            case 2:
                System.out.println("Musim Dingin");
                break;
            default:
                System.out.println("Bukan Musim Dingin");
        }
    }
}
```

Output:

```text id="v4k8qn"
Musim Dingin
```

---

## 6. Perbedaan switch dan else-if

Gunakan switch jika:

* Membandingkan satu variabel
* Nilai tetap atau diskrit
* Banyak cabang sederhana

Gunakan else-if jika:

* Membandingkan rentang nilai
* Menggunakan operator logika kompleks
* Menggabungkan banyak kondisi berbeda

Contoh rentang nilai lebih cocok else-if:

```java
if (score >= 90) {
    System.out.println("A");
} else if (score >= 80) {
    System.out.println("B");
}
```

switch tidak cocok untuk rentang seperti ini.

---

## 7. Contoh Kasus Industri

Mapping status HTTP sederhana:

```java
public class Main {
    public static void main(String[] args) {

        int statusCode = 404;

        switch (statusCode) {
            case 200:
                System.out.println("OK");
                break;
            case 404:
                System.out.println("Not Found");
                break;
            case 500:
                System.out.println("Server Error");
                break;
            default:
                System.out.println("Unknown Status");
        }
    }
}
```

Output:

```text id="q1m8xz"
Not Found
```

---

## 8. Ringkasan EP 07

* switch digunakan untuk banyak pilihan nilai tetap
* break mencegah fall-through
* Bisa digunakan untuk int, char, String, enum
* Lebih rapi dibandingkan else-if untuk nilai diskrit
* Tidak cocok untuk rentang nilai

---

## Target Setelah Episode Ini

* Bisa menggunakan switch dengan benar
* Mengerti fungsi break
* Bisa memilih kapan pakai switch dan kapan pakai else-if
* Siap lanjut ke switch expression modern pada episode berikutnya

```
```
