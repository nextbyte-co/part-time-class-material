# Javascript Dasar Chapter #1

![Javascript logo](https://www.schemecolor.com/wp-content/uploads/javascript-logo.png)

## Pengertian Javascript

Javascript adalah bahasa pemograman web yang digunakan untuk memanipulasi elemen-elemen HTML dan membuat website menjadi lebih ineraktif. Javascript juga merupakan *client-side programming language*, yaitu bahasa yang dijalankan dimana *user/client* dapat berinteraksi secara langsung.

---

## Hello World di Javascript

Membuat *Hello World* merupakan 'ritual' yang sering dilakukan ketika mempelajari bahasa pemograman baru

```javascript
console.log("Hello World");
```

---

## Input File Javascript di HTML

Ada Setidaknya tiga cara dalam menaruh kode Javascript untuk dijalankan berbarengan dengan HTML

- ### Inline

```html
<button onclick="alert('Hello World');">Click Here!</button>
```

- ### Internal
```html
<body>
   <p>Belajar JS</p>
   <script>
      console.log("Hello World");
   </script>
</body>
```

- ### External
```html
<script src="helloworld.js"></script>
```

---

## Aturan Dasar Javascript

Secara umum aturan dasar pada Javascript sama hal nya dengan aturan pada bahasa pemograman lainya. Beberapa yang akan dibahas diantaranya adalah *Sattement*, *Case Sensitive*, *Whtespace*, dan *Comments*.

- ### Statement

```html
<script>
   alert("Hello World!");
   console.log("Learning Javascript");
   var a = 12; let b = "aku"; const c= 3.14;
   const elementsBox =
   document.getElementsByClassName("box");
</script>
```

Sebuah baris perintah javascript disebut dengan *Statement*, bisanya diakhiri dengan *semicolon* atau titik koma. Pada contoh diatas terdapat enam *statements*, baris kedua dan ketiga satu *statement*, baris ke empat ada tiga *statement*, dan yang terkahir satu *statement* dalam dua baris (baris kelima dan keenam)

- ### Case Sensitive

Javascript termasuk bahasa pemograman yang *case sensitive*. Artinya, **huruf besar dan huruf kecil dianggap berbeda**. Maka dari itu, jika salah dalam penulusan perintah ataupun variable pada javascript maka program tidak akan berjalan bahkan *error*.

- ### Whitepace

**Whitespace** memiliki arti 'karakter kosong', seperti spasi, tab atau baris baru. Pada dasarnya dalam javascript *whitespace* akan diabaikan. Tidak perlu khawatir seberapa banyak ruang yang terbuang pun, program akan tetap berjalan semestinya.

- ### Comments

*Comments* atau baris komentar merupakan serangkaian teks atau baris perintah dalam bahasa pemograman yang tidak akan dieksekusi. *Comments* biasanya sering digunakan menjelaskan kode program tertentu, menonaktifkan baris program, dan untuk keperluan dokumentasi.

```javascript
// Ini komentar satu baris
// Ini contoh lagi
let nama = "Jajajng Jamudud"; // Bisa juga ditempatkan setelah statement

/* Ini kmentar
yang bisa lebih
dari satu baris
*/

/*
* Biar lebih rapi
* bisa pake tanda bintang
* Beberapa programmer
* Sering menuisnya begini
*/
```

---

## Variable dan Konstatnta

*Variable* adalah sebuah *keyword* yang digunakan untuk menampung data. Agar data dalam variable tersebut bisa digunakan, maka variable mambutuhkan nama.

- ### var, let, const

*var* saat ini sudah mulai jarang digunakan, karena *var* memiliki risiko yang apabila digunakan program dalam skala besar terjadi *hoisting* atau *duplikasi variable*

*let* dan *const* adalah fitur baru ES6. *Let* Sama dengan *var*, namun *let* lebih aman dalam penggunaanya. *Let* tidak memungkinkan menduplikasi variable, *hoisting*, dan *block scope*. Sedangkan *const* atau konstanta, adalah variable yang nialainya tetap dan tidak bisa diubah.

```javascript
// Menggunakan keyword var
var angka;

// [var] mengisi nilai pada variable
var angka; // declaration (mendeklarasikan variable)
angka = 101; // assignment (mengisi niali variable)
console.log(angka);

// [var] dijadikan satu baris
var ikan = "Cupang";
console.log(ikan);

// [var] Hoisting
x = 50;
var x;
console.log(x); // Tidak error

// Menggunakan keyword let
let angka;
```

- ### Aturan Penamaan Variable

Nama variabel di dalam JavaScript disebut *identifier*. *Identifier* adalah
sebutan untuk nama dari sesuatu di dalam sebuah bahasa pemrograman (tidak hanya JavaScript). Dan berikaut ada beberapa aturan dalam menulis nama variable

1. Bisa terdiri dari huruf, angka, garis bawah “ _ ” (*underscore*), dan tanda dollar “ $ “ (*dollar sign*). Selain itu, dianggap sebagai karakter ilegal (tidak boleh digunakan).
2. Karakter pertama dari *identifier* tidak boleh berupa angka. Angka hanya bisa digunakan
sebagai karakter kedua dan seterusnya.
3. Bersifat *case sensitive*, dimana huruf besar dan kecil dianggap berbeda.
4. Harus selain dari reserved keyword, yakni kata khusus yang berfungsi sebagai perintah
di dalam pemrograman JavaScript, seperti var , while , function , dll.

### [*Reserved Keyword* Bisa Cek Disini](https://www.w3schools.com/js/js_reserved.asp)

- ### Membuat variable tanpa *keyword* var

Cara ini bisa, namun **tidak disarankan** karena bisa menimbulkan *bug* nantinya.

```javascript
angka = 12345;
console.log(angka); // 12345

nama = "Aceng";
console.log(nama); // Aceng
```
