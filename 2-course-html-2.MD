# HTML Part 2

![HTML](./assets/html.png)

# 1. Paragraph, Break & Comment

```html
<p>Ini paragraf 1.</p>
<p>Ini paragraf 2.</p>
```

```html
<hr />
ini baris 1 <br />
ini baris 2
```

```html
<!-- ini komentar -->
```

note:

- `<p>` digunakan untuk membuat paragraph
- `<hr>` digunakan untuk membuat garis bawah / garis pembagi
- `<br>` digunakan untuk membuat baris baru (enter)
- `<!--/* */--->` digunakan untuk membuat komentar, komentar tidak di hiraukan oleh browser. Biasanya digunakan untuk dokumentasi.

# 2.Heading

```html
<h1>Ini Heading 1</h1>
<h2>Ini Heading 2</h2>
<h3>Ini Heading 3</h3>
<h4>Ini Heading 4</h4>
<h5>Ini Heading 5</h5>
<h6>Ini Heading 6</h6>
```

note:

- Heading digunakan untuk membuat judul
- Tag header `<h1>` memiliki ukuran huruf paling besar, sedangkan `<h6>` terkecil.

# 3. HTML Text Formatting

```html
<b> Ini bold </b> <br />
<strong> Ini strong </strong> <br />
<i> Ini italic </i> <br />
<em> Ini emphasized </em> <br />
<mark> Ini marked </mark> <br />
<small> Ini small </small> <br />
<del> Ini deleted </del> <br />
<ins> Ini inserted </ins> <br />
<sub> Ini subscript </sub> <br />
<sup> Ini superscript </sup> <br />
```

# 4. Unordered Lists

```html
<h1>Sebutkan Nama Ikan:</h1>
<ul>
  <li>Ikan Lele</li>
  <li>Ikan Pa'us</li>
  <li>Ikan Teri</li>
  <li>Ikan Kon..</li>
  <li>Eh</li>
  <li>Ikan Tongkol</li>
</ul>
```

atau :

```html
<h1>Daftar belanja:</h1>
<ul type="disc">
  <li>Beras</li>
  <li>Minyak goreng</li>
</ul>
<ul type="circle">
  <li>Gula</li>
  <li>Santan</li>
</ul>
<ul type="square">
  <li>Merica</li>
  <li>Ikan</li>
</ul>
```

# 5.Ordered List

```html
<h1>Ranking Kelas X TKJ E:</h1>
<ol>
  <li>Novita</li>
  <li>Yoga</li>
  <li>Arvin</li>
  <li>Alifia</li>
  <li>Bella</li>
</ol>
```

note:

- `<ol>` mempunyai attribute type 5 macam
- `a` Ordered List dengan Lowercase Letter
- `A` Ordered List degnan Uppercase Letter
- `i` Ordered List dengan Roman Numeral
- `I` Ordered List dengan Roman
- `1` Ordered List dengan Numeral

# 6. Description List

```html
<h1>Glosarium:</h1>
<dl>
  <dt>React</dt>
  <dd>Framework Javascript</dd>
  <dt>Flutter</dt>
  <dd>Mobile Framework dengan Bahasa Dart</dd>
  <dt>Express</dt>
  <dd>Node Js Framework</dd>
</dl>
```

# 7. Table

- normal table

```html
<table>
  <tr>
    <th>Nama</th>
    <th>Code Name</th>
    <th>Alamat</th>
  </tr>
  <tr>
    <td>Panji Gumelar</td>
    <td>Panji si Petir</td>
    <td>Outside Universe</td>
  </tr>
  <tr>
    <td>Arsyad Sukma</td>
    <td>Black is Dark</td>
    <td>Inside your Shadow</td>
  </tr>
</table>
```

- styled table

```html
<head>
  <title>Tabel Kamu</title>
  <style>
    table,
    th,
    td {
      border: 1px solid black;
      border-collapse: collapse;
    }
  </style>
</head>
```

```html
<body>
  <table>
    <tr>
      <th>Nama</th>
      <th>Code Name</th>
      <th>Alamat</th>
    </tr>
    <tr>
      <td>Panji Gumelar</td>
      <td>Panji si Petir</td>
      <td>Outside Universe</td>
    </tr>
  </table>
</body>
```

atau bisa dengan menfaatkan attribute-nya seperti :

```html
<table border="1"></table>
```

- Column Span

```html
<table>
  <tr>
    <th>- Asal -</th>
    <th>- Domisili -</th>
  </tr>
  <tr>
    <td colspan="2">
      <center>
        Jakarta
      </center>
    </td>
  </tr>
</table>
```

note: Merge Column

- Ros Span

```html
<table>
  <tr>
    <th rowspan="2">Jakarta</th>
    <td>- A -</td>
    <td>- B -</td>
  </tr>
  <tr>
    <td>- C -</td>
    <td>- D -</td>
  </tr>
</table>
```

note : Merge Row

# 8. Link

- Absolute Link

```html
<a href="https://www.google.com"> Google </a>
```

Alamat absolut adalah penulisan alamat file dengan menyertakan nama website, ditulis secara lengkap.

- Alternative Link

```html
<a href="satu.html" target="_blank"> Halaman Satu </a>
```

Namun jika kita ingin membuat link di dalam situs yang sama, maka tidak perlu menyebutkan alamat lengkap tersebut. Tetapi cukup mencantumkan alamat file yang dituju relatif kepada file saat ini. Jenis alamat ini disebut alamat relatif.

note : Secara default, setiap link yang kita tulis akan terbuka pada jendela yang sama (menimpa halaman web saat ini). Tetapi apabila kita ingin halaman tersebut terbuka pada tab baru, gunakan atribut `target=”\_blank”`.

- ID Link

```html
<a href="#aku">Klik untuk cari siapa aku!</a>

<h1 id="kamu">Kamu Siapa</h1>
<h1 id="itu">Aku Siapa</h1>
<h1 id="siapa">Aku Itu Kamu</h1>
<h1 id="aku">Aku Adalah Superman</h1>
```

note: Link yang akan mencari id dari suatu elemen di halaman itu sendiri

# 9. Images

```html
<img src="cat.png" alt="Ini kucing" />
<img src="tiger.svg" alt="Ini macan" width="200" height="200" />
<img
  src="url_from_web.jpeg"
  alt="Ini gambar dari web"
  width="200"
  height="200"
/>
```

# 10. Figure and Captions

```html
<figure>
  <img src="lion.png" />
  <figcaption>
    Ini singa
  </figcaption>
</figure>
```