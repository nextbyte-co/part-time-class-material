# Object Oriented Programming (OOP)

# 1. Pengertian OOP

Gampangnya OOP itu pemrograman yang berbasis object. Misalkan object `tamengBesi` bisa memiliki property: bentukTameng, beratTameng, dan lebarTameng. Object `tamengBesi` juga bisa memiliki method: diUpgrade(), diLelehkan() dan diLemparkan().

Contoh lain seperti object `motor` yang bisa saja memiliki property: merk, warna, dan jenis. Dimana methodnya bisa seperti: dihidupkan(), dimatikan() dan lain-lain.

# 2. Pengertian Class dan Object

Dalam teori OOP, Class adalah cetak biru untuk membuat objek. Class mirip dengan cetak biru sebuah rumah dan Object adalah hasil dari cetak biru tersebut.

![class object](./assets/class-object.png)

Jika rumah adalah class, maka rumahAbdi merupakan object dari class rumah. Jika binatang adalah class, maka unta merupakan object dari class binatang. Jika Pedang adalah class, maka pedangBesi adalah object dari class gelas.

# 3. Membuat Class dan Object

Membuat class di javascript tinggal menuliskan keyword `class` :

```javascript
class Mobil {
  // isi dari class
}
```

note:

- Disini sudah terbuat sebuah class `Mobil` namun masih belum memiliki isi
- Nama Class biasanya di awali dengan huruf besar, meskipun bisa juga menggunakan huruf kecil

Membuat class yang memiliki 2 kosa kata, biasanya menggunakan format `Camel Case` :

```javascript
class MobilBaru {
  // isi dari class
}
```

note : Dengan ditulis seperti ini kita akan gampang membedakan mana variable (diawali huruf kecil), class (diawali huruf besar)

Contoh :

```javascript
class Mobil {
  // isi dari class
}

var mobilPanji = new Mobil();
var mobilArsyad = new Mobil();
```

Kode program diatas artinya saya membuat 2 buah object dari class Mobil. Object pertama disimpan kedalam variabel `mobilPanji`, dan object kedua ke dalam variabel `mobilArsyad`.

# 4. Class Sebagai `“Object Induk”`

Class berperan sebagai wadah yang menyediakan semua hal yang dibutuhkan oleh object. Sebagai contoh, perhatikan kode program berikut:

```javascript
var mobilPanji = { merk: "Daihatsu Xenia", tipe: "MPV", harga: 150000000 };
var mobilArsyad = { merk: "Toyota Camry", tipe: "Sedan", harga: 350000000 };
```

Disini saya membuat 2 buah object: mobilPanji dan mobilArsyad. Keduanya memiliki 3 property yang sama: merk, tipe, dan harga, dengan isi data yang berlainan.

Sekarang, tambahkan method:

```javascript
var mobilPanji = {
  merk: "Daihatsu Xenia",
  tipe: "MPV",
  harga: 150000000,
  hidupkan: function() {
    return "Mesin di hidupkan";
  },
  pergi: function(km) {
    return `Mobil melaju Cepat dengan kecepatan ${km}`;
  }
};
var mobilArsyad = {
  merk: "Toyota Camry",
  tipe: "Sedan",
  harga: 350000000,
  hidupkan: function() {
    return "Mesin di hidupkan";
  },
  pergi: function(km) {
    return `Mobil melaju Cepat dengan kecepatan ${km}`;
  }
};
```

Kali ini setiap object memiliki 2 method tambahan: `hidupkan()` dan `pergi()`.

Dapat dilihat bahwa kedua object ini sebenarnya masuk ke golongan `mobil`. Tapi ini akan tidak efektif jika object yang akan dibuat sangat banyak.

# 5. Class Property

Untuk membuat property di dalam class, kita harus menggunakan method khusus bernama `constructor()`.

format standard :

```javascript
class ClassName {
  constructor(paramaterA, paramaterB) {
    this.attributeA = paramaterA;
    this.attributeB = paramaterB;
  }
```

atau bisa seperti ini :

```javascript
class Sword {
  constructor(swordName, attackPoint, durabilityPoint) {
    this.name = swordName;
    this.attack = attackPoint;
    this.durability = durabilityPoint;
  }
}
```

note: This adalah object khusus sebagai pengganti object yang nantinya di buat dari class Mobil.

Jika kita ingin membuat object dari class `Sword` tersebut,

```javascript
var pedangPanji = new Sword("Excalibur", 312, 100);
var pedangArsyad = new Sword("Flamberg", 298, 100);
```

Ini artinya 2 object dari class `Sword` telah terbuat, dan property-nya sama dengan yang telah kita inputkan.

```javascript
console.log(`Nama pedang dari Panji adalah ${pedangPanji.name}`);
```

# 6. Class Method

Sebuah class bisa membuat `method` lebih dari 1.

format dasar membuat method :

```javascript
class ClassName {
  constructor() {}

  methodA() => {
      // do something in here
  }

  // method with parameter
  methodB(parameterA) => {
      // do something in here with parameterA
  }
}
```

contoh :

```javascript
class Sword {
  constructor() {}

  serang() {
    console.log("Holy Slash !");
  }

  bertahan() {
    console.log("Pernapasan Air Bentuk ke 3 - Baladah Cisagiri");
  }

  // method with parameter
  skill(skillName) {
    console.log(`Hisatsu, ${skillName}. Horyaaa !`);
  }
}
```

# Example, Property and Method :

Sebagai contoh kali ini membuat class `sword` terlebih dahulu

```javascript
class Sword {
  constructor(swordName, attackPoint, durabilityPoint) {
    this.name = swordName;
    this.attack = attackPoint;
    this.durability = durabilityPoint;
  }

  serang() {
    return "Holy Slash !";
  }

  defend() {
    return "Pernapasan Air Bentuk ke 3 - Baladah Cisagiri";
  }

  skill(skillName) {
    return `Hisatsu, ${skillName}. Horyaaa !`;
  }

  getName() {
    return this.name;
  }

  getAttakPower() {
    return this.attack;
  }

  getDurabilityLeft() {
    return this.durability;
  }
}
```

Cara membuat object dari class yang telah dibuat :

```javascript
var mySword = new Sword("Charlemagne's Joyeuse", 612, 100);
var yourSword = new Sword("Shamshir-e-Zomorrodnegar", 436, 100);
```

Menggunakan method yang telah kita buat :

```javascript
// Mengambil nama dari method
console.log(`Nama dari pedang-ku : ${mySword.getName()}`);

// Mengambil nama dari properti
console.log(`Nama dari pedang-ku : ${mySword.name}`);

// Memanggil method dengan parameter
console.log(mySword.skill("Balada Onigiri"));
```
