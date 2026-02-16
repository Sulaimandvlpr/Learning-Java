# EP 08 - switch Expression (Modern Java)

Pada episode ini kita membahas versi modern dari switch.

Mulai Java 14 dan distabilkan di versi setelahnya, Java memperkenalkan switch expression.

Perbedaannya dengan switch lama:

- Bisa langsung mengembalikan nilai
- Tidak perlu break
- Sintaks lebih ringkas
- Lebih aman dari fall-through bug

Switch expression banyak digunakan di kode modern Java 17–21 yang saat ini menjadi standar industri.

---

## 1. Perbedaan switch Lama vs switch Expression

Switch lama:

```java
int day = 2;
String result;

switch (day) {
    case 1:
        result = "Senin";
        break;
    case 2:
        result = "Selasa";
        break;
    default:
        result = "Tidak valid";
}
````

Switch expression:

```java
int day = 2;

String result = switch (day) {
    case 1 -> "Senin";
    case 2 -> "Selasa";
    default -> "Tidak valid";
};
```

Switch expression lebih ringkas dan lebih bersih.

---

## 2. Contoh Dasar switch Expression

```java
public class Main {
    public static void main(String[] args) {

        int day = 3;

        String result = switch (day) {
            case 1 -> "Senin";
            case 2 -> "Selasa";
            case 3 -> "Rabu";
            default -> "Tidak valid";
        };

        System.out.println(result);
    }
}
```

Output:

```text
Rabu
```

Penjelasan:

* Tidak ada break
* Menggunakan tanda panah ->
* Menghasilkan nilai yang bisa langsung disimpan

---

## 3. Multiple Case dalam switch Expression

```java
public class Main {
    public static void main(String[] args) {

        int month = 1;

        String season = switch (month) {
            case 12, 1, 2 -> "Musim Dingin";
            case 3, 4, 5 -> "Musim Semi";
            default -> "Musim Lainnya";
        };

        System.out.println(season);
    }
}
```

Output:

```text
Musim Dingin
```

Lebih bersih dibandingkan switch lama.

---

## 4. Block dalam switch Expression

Jika logic lebih dari satu baris, gunakan block dan yield.

```java
public class Main {
    public static void main(String[] args) {

        int score = 85;

        String grade = switch (score / 10) {
            case 10, 9 -> {
                yield "A";
            }
            case 8 -> {
                yield "B";
            }
            case 7 -> {
                yield "C";
            }
            default -> {
                yield "D";
            }
        };

        System.out.println(grade);
    }
}
```

Output:

```text
B
```

Penjelasan:

* yield digunakan untuk mengembalikan nilai dari block
* Berguna jika ada perhitungan tambahan

---

## 5. switch Expression dengan Enum

Switch expression sangat cocok dengan enum.

Contoh:

```java
enum Role {
    ADMIN,
    USER,
    GUEST
}

public class Main {
    public static void main(String[] args) {

        Role role = Role.ADMIN;

        String access = switch (role) {
            case ADMIN -> "Full Access";
            case USER -> "Limited Access";
            case GUEST -> "Read Only";
        };

        System.out.println(access);
    }
}
```

Output:

```text
Full Access
```

Dalam industri, kombinasi enum + switch expression sangat umum.

---

## 6. Keuntungan Industri

Switch expression memberikan:

* Kode lebih ringkas
* Lebih mudah dibaca
* Lebih aman dari bug break
* Cocok untuk functional style programming

Switch modern sering digunakan dalam:

* Mapping status
* Mapping event type
* API response handler
* Domain logic sederhana

---

## 7. Perbandingan Praktis

Gunakan switch expression jika:

* Ingin mengembalikan nilai
* Logic sederhana
* Menggunakan Java 17 ke atas

Gunakan switch lama jika:

* Menggunakan Java versi lama
* Tidak membutuhkan return value

Dalam standar industri 2026, Java 17 dan 21 adalah LTS yang umum digunakan, sehingga switch expression adalah best practice.

---

## Ringkasan EP 08

* switch expression adalah versi modern dari switch
* Tidak memerlukan break
* Bisa langsung menghasilkan nilai
* Menggunakan -> dan yield
* Lebih aman dan lebih clean
* Direkomendasikan untuk Java modern

---

## Target Setelah Episode Ini

* Mengerti perbedaan switch lama dan modern
* Bisa menggunakan switch expression dengan benar
* Siap masuk ke Phase Looping pada episode berikutnya

```
```
