## Operator Javascript

Operator digunakan untuk mengolah data yang sudah terdefinisi sebelumnya dalam kode program. Terdapat beberapa operator dalam Javascript.

1. Operator Aritmatika
2. Operator Increment dan Decrement
3. Operator Pebandingan
4. Operator Logika
5. Operator String
6. Operator Bitwise
7. Operator Assignment
8. Operator Spread

- ### Operator Aritmatika

Adalah operator yang melakukan perhitungan matematika, tentunya berkaitan dengan angka. Seperti penambahan, pengurangan, perkalian dan pembagian.

| Nama Operator       | Operator | Contoh | Hasil                   |
| -------------       |:--------:| -------| ----------------------- |
| plus / positif      | +        | +x     | Nilai positif dari x    |
| negatif / minus     | -        | -y     | Nilai negatif dari y    |
| penambahan          | +        | x + y  | total dari x dan y      |
| pengurangan         | -        | x - y  | selisih dari x dan y    |
| perkalian           | *        | x * y  | hasil kali dari x dan y |
| pembagian           | /        | a / b  | hasil bagi dari x dan y |
| modulus / sisa bagi | %        | a % b  | sisa pembagian x bagi y |

```javascript
let foo;

foo = +100;
console.log(foo); // 100

foo = -22;
console.log(foo); // -22

foo = 30 + 5;
console.log(foo); // 35

foo = 3.33 + 9.02;
console.log(foo); // 12.35

foo = 9 * 7;
console.log(foo); // 63

foo = 6 + 8 / 2 + 6;
console.log(foo); // 16

foo = 30 % 7;
console.log(foo); // 2
```

- ### Increment dan decrement

Operator Increment digunakan untuk menambah suatu nilai sebanyak satu angka (+1), penulisanya adalah seperti ini i++, merupakan penulisan singkat dari i = i + 1.

Operator Decrement digunakan untuk mengurang suatu nilai sebanyak satu angka (-1), penulisanya adalah seperti ini i--, merupakan penulisan singkat dari i = i - 1.

| Nama           | Contoh   | Hasil                                        |
| -------------- |:--------:| -------------------------------------------- |
| pre-increment  | ++a      | tambah nilai a dengan 1, lalu kirim nilai a  |
| post-increment | a++      | kirim nilai a, lalu tambah nilai a dengan 1  |
| pre-decrement  | --a      | kurangi nilai a dengan 1, lalu kirim nilai a |
| post-decrement | a--      | kirim nilai a, lalu kurangi nilai a dengan 1 |

```javascript
var foo;
foo = 7;
console.log(++foo); // 8
console.log(foo); // 8

foo = 7;
console.log(foo++); // 7
console.log(foo); // 8

foo = 7;
console.log(--foo); // 6
console.log(foo); // 6

foo = 7;
console.log(foo--); // 7
console.log(foo); // 6
```

- ### Operator Perbandingan

Operator Perbandinan fungsinya untuk memeriksa antara nilai yang satu dengan nilai yang lainya, apakah lebih besar, lebih kecil, sama besar atau tidak sama.

| Nama Operator                | Operator | Contoh  | Hasil                   |
| ---------------------------- |:--------:| ------- | ----------------------- |
| sama dengan                  | ==       | x == y  | Nilai positif dari x    |
| identik dengan               | ===      | x === y | Nilai negatif dari y    |
| tidak sama dengan            | !=       | x != b  | total dari x dan y      |
| tidak identik denga          | !==      | x !== y | selisih dari x dan y    |
| kurang dari                  | <        | x < y   | hasil kali dari x dan y |
| lebih dari                   | >        | a > b   | hasil bagi dari x dan y |
| kurang dari atau sama dengan | <=       | a <= b  | sisa pembagian x bagi y |
| lebih dari atau sama dengan  | >=       | a >= b  | sisa pembagian x bagi y |

```javascript
var foo;
foo = 9 < 12;
console.log(foo); // true

foo = 5 < 5;
console.log(foo); // false

foo = 5 <= 5;
console.log(foo); // true

foo = 8 != 12;
console.log(foo); // true

foo = 15 == 12;
console.log(foo); // false

foo = 15 === 15;
console.log(foo); // true

foo = 0.3 === 3e-1;
console.log(foo); // true
```

- ### Operator Logika

Operator Logika digunakan ketka membandinkan dua kondisi logika, apakah itu benar (**true**) atau salah (**false**).

| Nama Operator | Operator | Contoh  | Hasil                                             |
| ------------- |:--------:| ------- | ------------------------------------------------- |
| AND           | &&       | x && y  | true, jika a dan b sama-sama bernilai true        |
| OR            | ||       | x || y  | true, jika salah satu dari a atau b bernilai true |
| NOT           | !        | !x      | true, jika a bernilai false.                      |

```javascript
var foo;
foo = true && false;
console.log(foo); // false

foo = true || false;
console.log(foo); // true

foo = !false;96
console.log(foo); // true

foo = true || true && false;
console.log(foo); // true

foo = false && true || true;
console.log(foo); // true
```

- ### Operator String Concatonation

Ada satu operator untuk string, operator ini digunakan untuk penyambung antar string. Ada dua cara dalam melakukan penyambungan string

1. String Concatination (ES5)

```javascript
let foo, bar, baz;

foo = "Sedang " + "Belajar " + "JavaScript";
console.log(foo); // Sedang Belajar JavaScript

foo = "Belajar " + "ECMAScript " + 5;
console.log(foo); // Belajar ECMAScript 5

foo = 'Selamat ';
bar = "Belajar ";
baz = `Bro / Sist`;

let hasil = foo + bar + baz;
console.log(hasil);  // Selamat Belajar Bro / Sist
```

2. Template String (ES6)

```javascript
let foo, bar, baz;

foo = 'Selamat ';
bar = "Belajar ";
baz = `Bro / Sist`;

let hasil = `${foo} ${bar} Javascript ${baz}`
console.log(hasil);  // Selamat Belajar Javascript Bro / Sist
```

- ### Spread Operator

Spread operator merupaka fitur baru di ES6, gunanya untuk keperluan Array atau Object untuk menggabungkan Array atau Object itu sendiri. Cara menggunakan Spread Operator dengan menulis titik tiga kali (...), diikuti dengan variable yang ingin digabungkan.

```javascript
let huruf = ['a', 'b', 'c', 'd'];
console.log(huruf); // Array ['a', 'b', 'c', 'd']

let angka = [1, 2, 3, 4];
console.log(angka); // Array [1, 2, 3, 4]

let totalHuruf = [...hufur, 'e', 'f'];
console.log(totalHuruf); // Array ['a', 'b', 'c', 'd', 'e', 'f']

let totalAngka = [0, ...angka, 5, 6];
console.log(totalAngka); // Array [0, 1, 2, 3, 4, 5, 6]

let totalGabungan = [...huruf, ...angka];
console.log(totalGabungan); //// Array ['a', 'b', 'c', 'd', 1, 2, 3, 4]
```