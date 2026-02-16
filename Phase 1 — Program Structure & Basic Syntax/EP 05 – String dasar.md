# EP 05 — String Dasar

Pada episode ini kita membahas String secara fundamental. 
String sangat penting karena hampir semua aplikasi industri memproses teks seperti username, email, token, JSON, log, dan query.

Di Java, String bukan tipe primitif, melainkan class dari package java.lang.

---

## 1. Deklarasi String

String dideklarasikan menggunakan tanda kutip dua.

```java
public class Main {
    public static void main(String[] args) {
        String name = "Eman";
        System.out.println(name);
    }
}
````

Output:

```text
Eman
```

Penjelasan:

* String adalah class
* name adalah reference variable
* "Eman" adalah object String

---

## 2. String adalah Object

Berbeda dengan int atau double, String adalah object.

Artinya:

* Disimpan di heap memory
* Memiliki method
* Memiliki perilaku khusus seperti immutability

Contoh membuat String dengan constructor:

```java
public class Main {
    public static void main(String[] args) {
        String text = new String("Hello");
        System.out.println(text);
    }
}
```

Output:

```text
Hello
```

Dalam praktik modern, cara pertama lebih direkomendasikan karena lebih efisien.

---

## 3. Menggabungkan String (Concatenation)

String bisa digabung menggunakan operator +.

```java
public class Main {
    public static void main(String[] args) {
        String firstName = "Eman";
        String lastName = "Rahman";

        String fullName = firstName + " " + lastName;
        System.out.println(fullName);
    }
}
```

Output:

```text
Eman Rahman
```

Operator + pada String berarti concatenation, bukan penjumlahan.

---

## 4. Panjang String

Untuk mengetahui jumlah karakter gunakan method length().

```java
public class Main {
    public static void main(String[] args) {
        String text = "Java";
        System.out.println(text.length());
    }
}
```

Output:

```text
4
```

---

## 5. Mengakses Karakter

Gunakan charAt(index).

Index dimulai dari 0.

```java
public class Main {
    public static void main(String[] args) {
        String text = "Java";
        System.out.println(text.charAt(0));
        System.out.println(text.charAt(1));
    }
}
```

Output:

```text
J
a
```

Jika index melebihi panjang string, akan terjadi error.

---

## 6. Membandingkan String yang Benar

Jangan gunakan == untuk membandingkan isi String.

Salah:

```java
String role = "ADMIN";
if (role == "ADMIN") {
    System.out.println("Match");
}
```

Benar:

```java
public class Main {
    public static void main(String[] args) {
        String role = "ADMIN";

        if (role.equals("ADMIN")) {
            System.out.println("Match");
        }
    }
}
```

Output:

```text
Match
```

Penjelasan:

* == membandingkan alamat memory
* equals() membandingkan isi

Untuk mengabaikan huruf besar kecil:

```java
role.equalsIgnoreCase("admin");
```

---

## 7. Mengubah Huruf Besar dan Kecil

```java
public class Main {
    public static void main(String[] args) {
        String text = "Java";

        System.out.println(text.toUpperCase());
        System.out.println(text.toLowerCase());
    }
}
```

Output:

```text
JAVA
java
```

---

## 8. Mengambil Sebagian String

Gunakan substring().

```java
public class Main {
    public static void main(String[] args) {
        String text = "Programming";

        System.out.println(text.substring(0, 7));
    }
}
```

Output:

```text
Program
```

Parameter pertama adalah index awal.
Parameter kedua adalah index akhir dan tidak termasuk.

---

## 9. Mengecek Isi String

Beberapa method penting:

* contains()
* startsWith()
* endsWith()

Contoh:

```java
public class Main {
    public static void main(String[] args) {
        String email = "eman@gmail.com";

        System.out.println(email.contains("@"));
        System.out.println(email.startsWith("eman"));
        System.out.println(email.endsWith(".com"));
    }
}
```

Output:

```text
true
true
true
```

Ini sering digunakan untuk validasi sederhana.

---

## 10. Immutability pada String

String di Java bersifat immutable.

Artinya:

* Nilai String tidak bisa diubah
* Jika diubah, sebenarnya dibuat object baru

Contoh:

```java
public class Main {
    public static void main(String[] args) {
        String text = "Java";
        text = text + " 21";

        System.out.println(text);
    }
}
```

Output:

```text
Java 21
```

Object lama tetap ada, lalu dibuat object baru.

Karena itu, untuk manipulasi string berat, nanti akan digunakan StringBuilder.

---

## 11. Contoh Kasus Industri Sederhana

Simulasi validasi email:

```java
public class Main {
    public static void main(String[] args) {

        String email = "user@gmail.com";

        if (email.contains("@") && email.endsWith(".com")) {
            System.out.println("Email valid");
        } else {
            System.out.println("Email tidak valid");
        }
    }
}
```

Output:

```text
Email valid
```

---

## Ringkasan EP 05

* String adalah object, bukan tipe primitif
* Perbandingan isi harus menggunakan equals()
* String bersifat immutable
* Memiliki banyak method seperti length(), substring(), contains()
* Digunakan luas untuk validasi, parsing, dan manipulasi teks

---

## Target Pemahaman Setelah EP 05

* Mengerti bahwa String adalah object
* Bisa membandingkan String dengan benar
* Bisa menggunakan method dasar String
* Mengerti konsep immutability
* Siap masuk ke operator perbandingan dan logika pada Phase berikutnya

```
```
