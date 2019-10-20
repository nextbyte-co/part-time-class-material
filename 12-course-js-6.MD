## Javascript Object

- ### Pengertian Object

Javascript merupakan pemograman berbasis object. Object mirip dengan array, yaitu sebuah tipe data yang dapat menampung tipe data lain. Object bisa diisi dengan string, number, boolean, array, bahkan object juga.

```javascript
const objectName = {
   property1: "value1",
   property1: "value1",
   property1: "value1",

   method1: function() {
      return "isi method1"
   },

   method2: function() {
      return "isi method2"
   }
}
```

*property* adalah sebutan untuk variable yang ada didalam object, sedangkan *value* adalah isi dari property. Sedangkan *method* adalah function yang ditempatkan didala object.

- ### Object Property

Seperti yang sudah dsebutkan diatas bahwa *property* adalah sebutan untuk variable yang ada didalam object.

```javascript
const footballClub = {
   name: "FC Barcelona",
   manager: "Ernesto Valverde",
   captain: "Lionel Messi",
   stadium: "Camp Nou"
}
```

cara memanggil property sangat mudah.

```javascript
// cara yang umum digunakan
console.log(footbalClub.name); // FC Barcelona
console.log(footbalClub.manager); // Ernesto Valverde
console.log(footbalClub.captain); // Lionel Messi
console.log(footbalClub.stadium); // Camp Nou

// cara lainya
console.log(footbalClub["name"]); // FC Barcelona
console.log(footbalClub["manager"]); // Ernesto Valverde
console.log(footbalClub["captain"]); // Lionel Messi
console.log(footbalClub["stadium"]); // Camp Nou
```

menambah object property

```javascript
let footbalClub = {};

footbalClub.name = "Persib Bandung";
footbalClub.coach = "Robert Rene Albert";
footbalClub.captain = "Supardi Natsir";
footbalClub.stadium = "GBLA";
footbalClub.supporter = "Bobotoh";
footbalClub.born = 1933;

console.log();
```

mengubah nilai object property

```javascript
let timnas = {
   captain: "Firman Utina",
   coach: "Afred Riedl",
   stadium: "GBK",
}

console.log(timnas.captain); // Firman Utina

timnas.captain = "Boaz Salosa";

console.log(timnas.captain); // Boaz Salosa
```

- ### Object Method

Seperti yang disebutkan sebelumnya, object method adalah function yang ditempatkan didalam object. Cara menulis nya sama dengan function biasa yaitu menggunakan *function expression*

``` javascript
let motor = {
   nama: "Interceptor 650",
   merk: "Royal Enfield",
   tipe: "Cruiser",
   harga: 170000000,
   nyalakan: function() {
      return "Mesin dinyalakan";
   },

   sanmori: tempat => {
      return "Kuy sanmori ke " + tempat;
   }
}

console.log(motor.nama); // Interceptor 650
console.log(motor.merk); // Royal Enfield
console.log(motor.tipe); // Cruiser
console.log(motor.haga); // 170000000

console.log(motor.nyalakan()); // Mesin dinyalakan
console.log(motor.sanmori("Bintaro")); // Kuy sanmori ke Bintaro
```

mengubah nilai object method

```javascript
let motor = {
   nama: "Interceptor 650",
   merk: "Royal Enfield",
   nyalakan: function() {
      return "Mesin dinyalakan";
   },

   sanmori: tempat => {
      return "Kuy sanmori ke " + tempat;
   }
}

motor.nyalakan = "methodnya diubah";

console.log(mobil.pergi("JJS")); // Error
```

- ### Nested Object

Nested object adalah sebutan untuk object yang ada didalam object. Jadi nested object bisa kita tempatkan didalam sebuah property.

```javascript
let karyawan = {
   nama: "Ateng Bengep",
   jabatan: "Programmer",
   tugas: {
      pagi: "Meeting",
      siang: "Kerjain Project",
      sore: "Laporan"
   },
   umur: 25
};

console.log(karyawan.tugas.pagi); // Meeting
console.log(karyawan.tugas.sore); // Laporan
```

- ### Object Reference

Object reference merupakan suatu perilaku dari sebuah object ketika ditempatkan pada variable baru.

```javascript
let karyawan = {
   nama: "Ateng Bagoy",
   posisi: "Programmer"
}

let = karyawanBaru = karyawan;

consle.log(karyawan.nama); // Ateng Bagoy
consle.log(karyawanBaru.nama); // Ateng Bagoy

karyawan.nama = "Caweng Sutaweng";

consle.log(karyawan.nama); // Caweng Sutaweng
consle.log(karyawanBaru.nama); // Caweng Sutaweng

karyawanBaru.posisi = "Designer";

console.log(karyawan.posisi); // Designer
console.log(karyawanBaru.posisi); // Designer

console.log(karyawan === karyawanBaru); // true
```