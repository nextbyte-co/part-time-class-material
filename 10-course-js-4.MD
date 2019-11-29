## Struktur Logika dan Perulangan

- ### IF Stattement

IF digunakan untuk membuat sebuah kondisi dimana sebuah program dapat memenuhi kondisi itu atau tidak, jika kondisi terpenuhi (true) maka progaram akan berjalan.

```javascript
if (kondisi) {
  // kode
}
```

diawalai dengan IF kemudian kondisi yang diinginkan, lalu eksekusi programnya ditempatkan di dalam kurung kurawal

```javascript
let perut = "lapar";

if (perut === "lapar") {
  console.log("Waktunya makan!!"); // Waktunya makan!!
}

// contoh lain
let nilai = 8;

if (nilai > 7) {
  console.log("Kamu Lulus"); // Kamu Lulus
}
```

jika kondisi tidak terpenuhi maka kode yang ada di dalam kurung kurawal tidak akan dieksekusi, dan akan dilewati begitu saja.

```javascript
let perut = "kenyang";

if (perut === "lapar") {
  console.log("Waktunya makan!!");
}
```

- ### IF ELSE Statemant

Jika IF hanya menangani kondisi yang bernilai **true**, maka IF ELSE Statement dapat menangani kondisi **true** maupun **false**.

```javascript
if (condition) {
  // kode jika true
} else {
  // kode jika false
}
```

Hampir sama dengan IF, namun ditambahkan _else_ disertai dengan kurung kurawal yang menampung kode program.

```javascript
let perut = "kenyang";

if (perut === "lapar") {
  console.log("Waktunya makan!!"); // Tidak akan dieksekusi
} else {
  console.log("Sudah kenyang!!"); // Sudah kenyang!!
}

// contoh lain
let nilai = 5;

if (nilai > 7) {
  console.log("Kamu Lulus"); // Tidak akan dieksekusi
} else {
  console.log("Kamu tidak lulus"); // Kamu tidak lulus
}
```

- ### IF ELSE IF Statement

Terkadang ada kasus-kasus yang alur loginya lebih rumit, tidak hanya membutuhkan satu kondisi, namun dua atau lebih kondisi.

```javascript
if (condition) {
  // kode kondisi 1
} else if (condition2) {
  // kode kondisi 2
} else {
  // kode kondisi 3
}
```

Terdapat dua pengecekan kondisi, jika masing-masing kondisi pertama terpanuhi (true) maka kode program akan dijalankan.

```javascript
let perut = "kenyang";

if (perut === "lapar") {
  console.log("Waktunya makan!!");
} else if (perut === "kenyang") {
  console.log("Sudah kenyang!!");
} else {
  console.log("Gak kenyag gak lapar, tapi haus");
}

// contoh lain
let nilai = 5;

if (nilai >= 9) {
  console.log("Sempurna");
} else if (nilai === 7 || nilai === 8) {
  console.log("Bagus");
} else {
  console.log("Belajar lebih giat lagi");
}
```

- ### Switch Statement

Switch Stetement struktur logikanya hampir mirip dengan IF ELSE Statement, namun lebih efisien karena kondisi yang dicek lebih banyak.

```javascript
switch (variable) {
  case condition1:
    statement1;
    break;
  case condition2:
    statement2;
    break;
  case condition3:
    statement3;
    break;
  case condition4:
    statement4;
    break;
  default:
    statement5;
}
```

Kite perlu menetukan variable setelah _keyword_ **switch** dan pemeriksaan kondisi dilakukan disetian **case**

```javascript
let jajan = "cilok";

switch (jajan) {
  case "ketoprak":
    console.log("Ketupat, tahu, toge, bihun, kerupuk, bumbu kacang");
    break;
  case "siomay":
    console.log("kentang, kol, tahu, siomay, pare, bumbu kacang");
    break;
  case "cilok":
    console.log("aci dicolok, saos, kecap");
    break;
  case "bakso":
    conole.log("bakso kuah kaldu, sledri, mie, bihun, sambal, saos");
    break;
  default:
    console.log("Gak ada tukang dagang, gak bisa jajang euy");
}
```

dalam Switch Statement, bisa juga bebrapa **case** berturut-turut.

```javascript
let nilai = 6;

switch (nilai) {
  case 1:
  case 2:
  case 3:
  case 4:
  case 5:
    console.log("Itu nilai jelek amat ya");
    break;
  case 6:
  case 7:
  case 8:
    console.log("Mending dapet nilai segini");
    break;
  case 9:
  case 10:
    console.log("Gud.. Lanjutkan sist");
    break;
  default:
    console.log("Masukan nilai 1 sampe 10");
}
```

- ### FOR Loop

Loop atau disebut juga Perulangan, adalah fitur untuk mengulang beberapa baris perintah. Dengan melakukan perulangan sangat mudah untuk menjalankan perintah secara terus-menerus.

Dalam Javascript ada 3 jenis perulangan, yaitu **for**, **while**, **do while**. Berikut contoh syntax for loop.

```javascript
for (start; kondisi; increment) {
  statement;
}
```

1. Start : Diisi dengan kondisi awal perulangan, biasanya menggunakan variable berisi angka. Misalnya : var i = 0;
2. Kondisi : Diisi dengan kondisi, biasanya dengan operasi perbandingan. Misalnya : i < 10
3. Increment : Diisi dengan instruksi menaikan variable i. Contoh : i++

```javascript
// contoh sederhana
for (let i = 0; i < 10; i++) {
  console.log("Hello World!");
}

// contoh looping dari 1 - 10
for (let i = 0; i <= 10; i++) {
  console.log("Nomor " + i);
}

// contoh loping dari 10 - 1
for (let i = 10; i >= 0; i--) {
  console.log("Nomor " + i);
}

// contoh lain
for (let i = 2; i <= 20; i = i + 2) {
  console.log("Berkelipatan 2 " + i);
}
```

- Nested For Loop

Nested for loop adalah sebuah for loop yang berada didalam for loop lainya, atau bersarang.

```javascript
for (start1; kondisi1; increment1) {
  statement1;

  for (start2; kondisi2; increment3) {
    console.log("");
  }
}
```

contohnya

```javascript
// contoh sederhana
let i, j;
for (i = 1; i <= 6; i++) {
  for (j = 1; j <= 8; i++) {
    console.log("variabel i berisi " + i + ", dan variabel j berisi " + j);
  }
}
```

- ### Infinifty Loop

Infinity loop adalah perulangan yang terus-menerus dan tak pernah berhenti. Biasanya terjadi karena keteledoran kita sendiri dalam menulis program.

```javascript
// contoh
for (let i = 20; i > 10; i++) {
  console.log("Nah kan..");
}
```

- ### Break and Continue Statement

Perintah **Break** digunakan untuk menghentikan perulangan sebelum sepenuhnya selesai.

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break;
  }
  console.log("Belajar Javascript " + i);
}
```

Sedangkan perintah **Continue** adalh kebalikan dari perinyah **Break**, program akan dilanjutkan sampai selesai

```javascript
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    continue;
  }
  console.log("Belajar Javascript " + i);
}
```

- ### WHILE Loop

Perulangan kedua setelah For adalah While. Perulangan ini mirip dengan For, namum penempatan **start**, **kondisi** dan **increment** berbeda dengan For.

```javascript
start;
while (kondisi) {
  statement;
  increment;
}
```

Uniknya increment berada didalam looping itu sendiri.

```javascript
// contoh sederhana
let i = 0;
while (i <= 10) {
  console.log("Belajar JS");
  i++;
}

// perulangan terbalik
let i = 100;
while (i > 0) {
  console.log(i + " * 5 = " + i * 5);
  i = i - 5;
}

// menggunakan break
let i = 0;
while (i <= 10) {
  if (i === 5) {
    break;
  }
  console.log("Belajar Jevascript" + i);
  i++;
}
```

- ### DO WHILE Loop

Do While Loop hampir sama dengan While Loop, namun beda penempatan kondisinya

```javascript
start;
do {
  statement;
  increment;
} while (kondisi);
```

Berikut contoh penggunaanya.

```javascript
let i = 0;
do {
  console.log("Belejar Javascript");
  i++;
} while (i <= 10);
```

Do While ini memenag jarang digunakan, namun perlu untuk sekedar mengetahui.

- ### FOR OF Loop

Terdapat juga perulangan For Of dalam javascript, biasanya dilakukan dalam perulangan dengan Array.

```javascript
let barcelona = ["Messi", "Suarez", "Griezman", "Dembele", "Busquets"];

for (i of barcelona) {
  console.log(i);
}
```

# Tugas Javascript (IF dan SWITCH)

## Tugas IF ELSE

Buat 5 buah kondisi untuk mengecek usia seseorang, dengan detail kondisi seperti berikut :

1. Jika usia 0 sampai 5 tahun maka dia adalah "Balita".
2. Jika usia 6 sampai 12 tahun maka dia adalah "Anak-anak".
3. Jika usia 13 sampai 20 tahun maka dia adalah "Remaja".
4. Jika usia 21 sampai 40 tahun maka dia adalah "Dewasa".
5. Jika usia 41 sampai 60 tahun maka dia adalah "Tua".

Kemudian, jika usia tidak memenuhi kelima kondisi diatas _(else)_, maka dia sudah paruh baya atau meninggal.

## Tugas SWITCH

Buat sebuah variable dengan nama _klubEropa_, dan lakukan pengecekan dengan 7 kondisi.

1. Jika _klubEropa_ berisi _"Liverpool"_, maka cetak di `console` "Klub Inggris".
1. Jika _klubEropa_ berisi _"Barcelona"_, maka cetak di `console` "Klub Spanyol".
1. Jika _klubEropa_ berisi _"Juventus"_, maka cetak di `console` "Klub Italia".
1. Jika _klubEropa_ berisi _"PSG"_, maka cetak di `console` "Klub Prancis".
1. Jika _klubEropa_ berisi _"Borrusia Dortmun"_, maka cetak di `console` "Klub Jerman".
1. Jika _klubEropa_ berisi _"Galatasaray"_, maka cetak di `console` "Klub Turki".
1. Jika _klubEropa_ berisi _"AJAX"_, maka cetak di `console` "Klub Belanda".
1. Dan _Default_ nya adalah "Bukan Klub Eropa".

# Tugas Looping Javascript (FOR dan WHILE)

## Tugas For Loop

1. Buat perulang _Genap_ dengan kelipatan 4, dari 100 sampai 0.
2. Buat perulangan _Ganjil_ dengan kelipatan 3, dari 0 sampai 90.

## Tugas While Loop

1. Buat perulang _Genap_ dengan kelipatan 4, dari 0 sampai 100.
2. Buat perulangan _Ganjil_ dengan kelipatan 3, dari 100 sampai 0.

## Tugas For Of Loop

```javascript
let asean = [
  "Indonesia",
  "Singapura",
  "Malaysia",
  "Thailand",
  "Vietnam",
  "Brunei",
  "Kamboja",
  "Laos",
  "Myanmar",
  "Filipina",
  "Timor Leste"
];
```

Buat perulangan _For Of Loop_ dengan _Array_ diatas.
