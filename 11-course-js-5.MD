## Function

Dalam membuat program yang berskala besar, tentu lebih baik jika progran dipecah dalam beberapa sub program yang lebih kecil. Sub program tersebut kita bisa membungkusnya dalam sebuah **Function**.

Function sangat unik dalam Javascript, karna dapat disimpan kedalam variable. Karna uniknya itu lah Function dalam Javascript juga disebut sebagai *first-class-citizen*.

- ### Pengertian Function

Function atau fungsi, adalah sebuah kumpulan program yang bertujuan untuk menyelesaikan tugas tertentu yang mana merupakan program inti. Function sangatlah diperlukan dalam membuat suatu program baik yang sederhana maupun yang kompleks supaya alur program menjadi teratur dan mudah untuk dikelola.

berikut cara penuilisan function

```javascript
function namaFungsi(param1, param2) {
   statement;
   statement;
   return value;
}
```

Diawali dengan keyword *function* kemudian nama function-nya, dan bla perlu kita bisa memasaukna parameter. Didalam is function dapat diisi dengan program kita, lalu keyword *return* digunakan untuk mengeluarkan output dari function yang kita buat.

```javascript
function koding() {
   console.log("Jangan Lupa,");
   console.log("praktekan");
   console.log("apa yang kamu");
   console.log("sudah pelajari");
}
```

jika dijalankan, maka tidak akan muncul apa-apa, karena function harus dipanggil terlebih dahulu. Maka setelah function dipanggil, apa yang ada dalam function tersebut akan mengeluarkan outputnya.

```javascript
// memanggil function salam
koding();

// function dapat dipanggil berkali-kali
koding();
koding();
koding();
```

- ### returtn statement

perintah *return* akan mengembalikan suatu nilai ketika function dipanggil.

```javascript
function koding() {
   return "Belajar Javascript";
}

// Dimasukan dalam variable
let learn = koding();
console.log(learn);

// Me-return variable
function helo() {
   const sapa = "Halo kawan!";

   return sapa;
}

console.log(helo());
```

`console.log()` vs `return` statement

```javascript
function koding(){
   return "Belajar JS";
   console.log("Halo semuanya!"); // tidak akan muncul
}

console.log(koding());
```

`console.log()` pada funcion `koding()` tidak akan pernah dieksekusi, karena jika `return` sudah di tulis, maka program yang ada dibawahnya tidak akan dijalankan dan fungsi tersebut dianggap sudah selesai.

- ### Parameter

*Parameter* adalah tempat dimana kita bisa menaruh sebuah nilai yang nantinya nilai tersebut akan diproses oleh *function*.

```javascript
// contoh sederhana
function halo(siapa) {
   return "Selamat sinag " + salam + "!";
}

let salam = halo("Capuy");
console.log(salam); // Selamat siang Capuy!

// parameter bisa apapun tipe datanya
function belanja(kecap, micin) {
   let total = kecap + micin;
   return "Rp " + total;
}

let beli = belanja(7500, 2500);
console.log(beli); // Rp 10000

// bisa digunakan sebanyak mungkin
function menu(makan, minum) {
   return "Makan siang dengan " + makan + "dan munum " + minum;
}

console.log(menu("Bakso", "Kopi")); // Makan siang dengan Bakso dan munum Kopi
console.log(menu("Pempek", "Teh")); // Makan siang dengan Pempek dan munum Teh
console.log(menu("Rendang", "Susu")); // Makan siang dengan Rendang dan munum Susu
console.log(menu("Siamay", "Jamu")); // Makan siang dengan Siamay dan munum Jamu
```

- ### Function Declaration & Function Expression

Kedua function tersebut memiliki fungsi yang sama, hanya berbeda dalam cara penulisanya saja. Kamu bebas mau menggunakan yang mana, namun biasanya function expression akan banyak digunakan dalam membuat object.

```javascript
// Function declaration
function add(num1, num2) {
	return num1 + num2;
}

// Function expression
const add = function (num1, num2) {
	return num1 + num2;
}
```

- ### Arrow Function

Arrow function merupakan fitur dari ES6, yang memiliki cara tersendiri dalam menulis sebuah function menjadi lebih singkat dan menggunakan *symbol* panah () => sebagai ciri khas nya.

```javascript
// function biasa
const sisiwa = function(nama) { return nama };

// arrow function
const mahasiswa = nama => nama;

console.log(siswa("Uca"));
console.log(mahasiswa("Adung"));
```