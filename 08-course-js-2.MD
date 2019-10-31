## Tipe Data Javascript

Variable yang kita pelajari sebelumnya digunakan untuk menampung data, data sendiri dalam Javascript terdapat beberapa macam. Terdapat dua kelompok tipe data dalam Javascript, yakni **Tipe Data Primitive** dan **Tipe Data Object**.

- Perbedaan **Tipe Data Primitive** dan **Tipe Data Object**

Disebut primitif karena tipe data ini "sederhana" dan hanya terdiri dari satu nilai saja. Settidaknya ada 6 tipe data primitif dalam Javascript.

1. Number
2. String
3. Boolean
4. Null
5. Undefined
6. Symbol*

Sedangkan tipe data Object, merupakan tipe data yang boleh dibilang "Khusus" yang perilakunya berbeda dari tipe data primitive.

1. Array
2. Date
3. RegExp
4. Map dan WeakMap*
5. Set dan WeakSet*

> Tipe Data **symbol**, **map**, **weakmap**, **set**, dan **weakset** adalah tipe data baru dalam ES6.

- ### Tipe Data Number

Tipe data Number merupakan tipe data yang berisikan angka, baik angka itu bulat semisal 1, 20, 70, 200, -66, maupun akngka pecahan seperti 2.5, 0.07, 3.14.

Dalam Javascript tidak disebut tipe data *Integer* atau *Float*, semua yang bernilai angka disebut dengan tipe *Number*. Javascrip juga mendukung bilangan desimal, biner, oktal dan heksadesimal.

```javascript
var angka = 999; // desimal
let angka2 = 0b1111100111; // biner
const angka3 = 01747; // oktal
var angka4 = 0x3E7; // Heksadesimal

console.log(angka); // 999
console.log(angka2); // 999
console.log(angka3); // 999
console.log(angka4); // 999
```

- ### NaN dan Infinity

Selain "angka", ada juga dua tipe data lain yang termasuk dalam tipe data Number, yaitu **NaN (Not a Number)** dan **Infinity**. Keduanya berguna ketika ada nilai metematis yang "tidak umum".

```javascript
var foo;
foo = 7 * "a";
console.log(foo); // NaN

foo = 9 / 0;
console.log(foo); // Infinity
```

- ### Tipe Data String

Tipe data string adalah tipe data yang berupa teks yang dibungkus dengan *quotes* (' ') atau *doublequotes* (" ")

```javascript
let firstName = "Jajang";
let lastName = 'Jamudud';
var phone = "081234567890";

console.log(firstName); // Jajang
console.log(lastName); // Jamudud
console.log(phone); // 081234567890

var ayo = "Let's Go!";
let ayo2 = 'Let\'s Go!';

console.log(ayo); // Let's Go!
console.log(ayo2); // Let's Go!
```

Adapun jika ingin menggunakan tanda kutip (*doublequote*) didalam String, maka perlu yang namanya *Escape Character*, lebih lengkapnya bisa dilihatnya [Disini!](https://mathiasbynens.be/notes/javascript-escapes)

- ### Tipe Data Boolean

Tipe Data Bolean adalah tipe data yang hanya memiliki dua nilai, yakni **true** (benar) dan **false** (salah). Biasanya Boolean digunakan untuk alur logika program.

```javascript
let benar = true;
let salah = false;

console.log(benar);
console.log(salah);
```

- ### Null dan Undefined

Sebetulnya agak berlebihan jika Null dan Undefined disebut tipe data, karena keduanya menyatakan "nilai/data yang tidak ada"

```javascript
var foo = null;
console.log(foo); // null

let bar;
console.log(bar); // undefined
```

- ### Tipe Data Array

Array adalah tipe data yan dapat menampung lebih daru satu data dan dapat menggunakan tipe data yang berbeda-beda.

Daripada harus menulis seperti ini :

```javascript
let istri1 = "Syahrini";
let istri2 = "Raisa";
let istri3 = "Isyana";
let istri4 = "Mimi Peri";

console.log(istri1); // Syahrini
console.log(istri2); // Raisa
console.log(istri3); // Isyana
console.log(istri4); // Mimi Peri
```

Array membuatnya menjadi lebih simple

```javascript
let istri = ["Syahrini", "Raisa", "Isyana", "Mimi Peri"];
console.log(istri[0]); // Syahrini
console.log(istri[1]); // Raisa
console.log(istri[2]); // Isyana
console.log(istri[3]); // Mimi Peri
```

Perlu diketahui bahwa Array dimulai dari index 0. Cara mengakses elemen Array cukup mudah, yaitu dengan menggunakan kurung siku, lalu masukan index nya.

tipe data yang berbeda

```javascript
let sesuatu = [101, "Hello", false, null];
console.log(sesuatu); // Array [101, "Hello", false, null]
```

Mengetahui ada berapa data didalam sebuah Array

```javascript
let istri = ["Syahrini", "Raisa", "Isyana", "Mimi Peri"];
console.log(istri.length); // 4
```

Mengubah Elemen Array

```javascript
let istri = ["Syahrini", "Raisa", "Isyana", "Mimi Peri"];

istri[3] = "Chelsea Islan";
console.log(istri); // Array ["Syahrini", "Raisa", "Isyana", "Chelsea Islan"]
```

Array 2 Dimensi

```javascript
var koordinat = [[2,5],[3,8],[5,9]];
console.log(koordinat[0][0]); // 2
console.log(koordinat[0][1]); // 5

console.log(koordinat[1][0]); // 3
console.log(koordinat[1][1]); // 8

console.log(koordinat[2][0]); // 5
console.log(koordinat[2][1]); // 9
```