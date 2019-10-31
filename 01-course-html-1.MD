# HTML Part 1

![HTML](./assets/html.png)

HTML (Hypertext Markup Language) merupakan bahasa dasar pembuatan web. Disebut dasar karena dalam membuat web, jika hanya menggunakan HTML tampilan web terasa hambar. Terdapat banyak bahasa pemrograman web yang ditujukan untuk memanipulasi kode HTML, seperti JavaScript dan PHP. Akan tetapi sebelum anda belajar JavaScript maupun PHP, memahami HTML merupakan hal yang paling awal.

# Struktur Dasar HTML

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Judul Website</title>
  </head>
  <body>
    <p>Isi Dari Website</p>
  </body>
</html>
```

Setiap halaman HTML setidaknya memiliki struktur dasar yang terdiri dari : Tag DTD atau DOCTYPE, tag html, tag head, dan tag body. Inilah yang merupakan struktur paling dasar dari HTML, walaupun HTML tidak hanya berisi struktur tersebut.

- Tag `<html>`

  Ini adalah tag pembuka dari keseluruhan halaman web. Semua kode HTML harus berada di dalam tag ini. Tag html dimulai dengan `<html>` dan diakhiri dengan `</html>`

- Tag `<head>`

  Elemen pada tag `<head>` umumnya akan berisi berbagai definisi halaman, seperti kode CSS, JavaScript, dan kode-kode lainnya yang tidak tampil di browser.

- Tag `<body>`

  Tag `<body>` akan berisi semua elemen yang akan tampil dalam halaman web, seperti paragraf, tabel, link, gambar, dll. Tag body ini ditutup dengan `</body>`. Sebagian besar waktu kita dalam merancang web akan dihabiskan di dalam tag `<body>` ini.

# Tag dan Atribut pada HTML

Sebagai sebuah bahasa markup, HTML membutuhkan cara untuk memberitahu web browser untuk apa fungsi sebuah text. Apakah text itu ditulis sebagai sebuah paragraf, list, atau sebagai link. Dalam HTML, tanda ini dikenal dengan istilah tag.

Berikut adalah format dasar penulisan tag HTML:

```html
<tag_pembuka>objek yang dikenai perintah tag</tag_penutup>
```

Contoh :

```html
<p>Ini adalah sebuah paragraf</p>
```

1. `<p>` adalah tag pembuka, dalam contoh ini p adalah tag untuk paragraf.
2. `</p>` adalah tag penutup paragraf. Perbedaannya dengan tag pembuka terletak dari tanda forward slash (/)

List lengkap tag HTML: [tag html](https://www.w3schools.com/tags/default.asp)

# Element pada HTML

Element adalah isi dari tag yang berada diantara tag pembuka dan tag penutup, termasuk tag itu sendiri dan atribut yang dimilikinya (jika ada). Sebagai contoh perhatikan kode HTML berikut:

```html
<p>Ini adalah sebuah <em>paragraf</em></p>
```

Dari contoh diatas,`<p>` Ini adalah sebuah `<em>`paragraf`</em>` `</p>` merupakan elemen p.

# Atribut dalam HTML

Atribut adalah informasi tambahan yang diberikan kepada tag. Informasi ini bisa berupa instruksi untuk warna dari text, besar huruf dari text, dll. Setiap atribut memiliki pasangan nama dan nilai (value) yang ditulis dengan name=”value”. Value diapit tanda kutip, boleh menggunakan tanda kutip satu (‘) atau dua (“).

Contoh kode HTML:

```html
<a href="https://nextbyte.co">ini adalah sebuah link</a>
```

- Atribut yang sering digunakan :

1. `id` = Atribut yang menyediakan pengidentifikasi unik di seluruh dokumen untuk elemen, hanya boleh 1 nama Id di 1 dokumen HTML yang artinya tidak boleh sama.
2. `class` = Atribut yang menyediakan cara untuk mengklasifikasikan elemen yang sama. Contohnya seperti didalam suatu dokumen ada beberapa element yang mempunyai `class="notation"` dimana `class="notation"` mempunyai style `<h1>`, yang berarti element-element yang mempunyai `class="notation"` akan mempunyai style text `<h1>`
3. `style` = Atribut yang digunakan untuk styling seperti warna, jenis font, background, dll langsung di element tersebut.
4. `title` = Atribut yang digunakan untuk melampirkan penjelasan subteksual ke suatu elemen. Di sebagian besar browser, atribut ini ditampilkan sebagai apa yang sering disebut dengan tooltip.

List lengkap Atribut HTML : [HTML Attribute Reference](https://www.w3schools.com/tags/ref_attributes.asp)
