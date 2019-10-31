# CSS Part 2 - Lanjutan (Position, Pseudo & Media Query)

![CSS](./assets/css-position.jpg)

# CSS Position

Dengan CSS Position kita dapat mengubah posisi elemen. CSS Position memiliki 4 nilai yang biasa digunakan :

1. Static: Nilai default property position, Static tidak terpengaruh oleh nilai kiri, kanan, atas atau bawah.
2. Relative: Memindahkan elemen sesuai dengan posisi saat ini, tanpa mempengaruhi elemen lain.
3. Absolute: Ketika posisi diatur ke absolute, suatu elemen dapat bergerak sesuai dengan diposisikan pertama.
4. Fixed: Posisi yang tidak akan berpindah-pindah meskipun jendela browser di gerakan.

Dan juga dengan 4 Property Koordinat :

1. Left
2. Right
3. Top
4. Bottom

```css
/* Position relative example */
#relative-example {
  position: relative;
  border-color: red;
  left: 20px;
  top: 10px;
}

/* Position absolute example */
#relative-div {
  background: gold;
  height: 200px;
  padding: 10px;
  position: relative; /* This turns the #relative-div into a point of reference for the #absolute-div */
}

#absolute-div {
  background: limegreen;
  color: white;
  padding: 10px;
  position: absolute; /* This makes the #absolute-div freely movable */
  bottom: 10px; /* 10px from the bottom */
  left: 20px; /* 20px from the left */
}

/* Position fixed example*/
#fixed-example {
  position: fixed;
  left: 100px;
  top: 150px;
}
```

# CSS Pseudo Class dan Pseudo Element

Pseudo Class Selector adalah selector CSS yang digunakan untuk mengakses bagian tertentu dalam HTML yang tidak ‘terlihat’ (tidak tertulis di dalam HTML) atau bagian dari HTML yang tidak bisa diakses dengan selector sederhana lain. Jika pseudo-class selector lebih berfokus kepada kondisi khusus dari HTML, maka pseudo-element selector akan menyeleksi ‘potongan’ tag atau mengakses sebuah elemen yang sebelumnya tidak ada.

## All CSS Pseudo Classes

| Selector             | Example               | Example description                                                                                      |
| -------------------- | --------------------- | -------------------------------------------------------------------------------------------------------- |
| :active              | a:active              | Selects the active link                                                                                  |
| :checked             | input:checked         | Selects every checked `<input>` element                                                                  |
| :disabled            | input:disabled        | Selects every disabled `<input>` element                                                                 |
| :empty               | p:empty               | Selects every `<p>` element that has no children                                                         |
| :enabled             | input:enabled         | Selects every enabled `<input>` element                                                                  |
| :first-child         | p:first-child         | Selects every `<p>` elements that is the first child of its parent                                       |
| :first-of-type       | p:first-of-type       | Selects every `<p>` element that is the first `<p>` element of its parent                                |
| :focus               | input:focus           | Selects the `<input>` element that has focus                                                             |
| :hover               | a:hover               | Selects links on mouse over                                                                              |
| :in-range            | input:in-range        | Selects `<input>` elements with a value within a specified range                                         |
| :invalid             | input:invalid         | Selects all `<input>` elements with an invalid value                                                     |
| :lang(language)      | p:lang(it)            | Selects every `<p>` element with a lang attribute value starting with "it"                               |
| :last-child          | p:last-child          | Selects every `<p>` elements that is the last child of its parent                                        |
| :last-of-type        | p:last-of-type        | Selects every `<p>` element that is the last `<p>` element of its parent                                 |
| :link                | a:link                | Selects all unvisited links                                                                              |
| :not(selector)       | :not(p)               | Selects every element that is not a `<p>` element                                                        |
| :nth-child(n)        | p:nth-child(2)        | Selects every `<p>` element that is the second child of its parent                                       |
| :nth-last-child(n)   | p:nth-last-child(2)   | Selects every `<p>` element that is the second child of its parent, counting from the last child         |
| :nth-last-of-type(n) | p:nth-last-of-type(2) | Selects every `<p>` element that is the second `<p>` element of its parent, counting from the last child |
| :nth-of-type(n)      | p:nth-of-type(2)      | Selects every `<p>` element that is the second `<p>` element of its parent                               |
| :only-of-type        | p:only-of-type        | Selects every `<p>` element that is the only `<p>` element of its parent                                 |
| :only-child          | p:only-child          | Selects every `<p>` element that is the only child of its parent                                         |
| :optional            | input:optional        | Selects `<input>` elements with no "required" attribute                                                  |
| :out-of-range        | input:out-of-range    | Selects `<input>` elements with a value outside a specified range                                        |
| :read-only           | input:read-only       | Selects `<input>` elements with a "readonly" attribute specified                                         |
| :read-write          | input:read-write      | Selects `<input>` elements with no "readonly" attribute                                                  |
| :required            | input:required        | Selects `<input>` elements with a "required" attribute specified                                         |
| :root                | root                  | Selects the document's root element                                                                      |
| :target              | #news:target          | Selects the current active #news element (clicked on a URL containing that anchor name)                  |
| :valid               | input:valid           | Selects all `<input>` elements with a valid value                                                        |
| :visited             | a:visited             | Selects all visited links                                                                                |

## All CSS Pseudo Elements

| Selector       | Example         | Example Description                                          |
| -------------- | :-------------- | ------------------------------------------------------------ |
| ::after        | p::after        | Insert content after every `<p>` element                     |
| ::before       | p::before       | Insert content before every `<p>` element                    |
| ::first-letter | p::first-letter | Selects the first letter of every `<p>` element              |
| ::first-line   | p::first-line   | Selects the first line of every `<p>` element                |
| ::selection    | p::selection    | Selects the portion of an element that is selected by a user |

## Contoh :

```css
/* :hover example */
.class-name {
  color: blue;
}

.class-name:hover {
  color: red;
}

/* :focus example */
.form-input {
  border: 2px solid grey;
  padding: 5px;
}
.form-input:focus {
  background: lightyellow;
  border-color: blue;
  outline: none;
}
```

# CSS Responsive menggunakan Media Query

![Responsive](./assets/responsive.gif)

Media Query berguna ketika Anda ingin memodifikasi situs atau aplikasi Anda tergantung pada tipe perangkat pada umumnya (seperti kertas print vs layar misalnya) atau karakteristik dan parameter tertentu (seperti resolusi layar atau lebar viewport browser).

Contoh penggunaan :

```css
@media screen and (min-width: 600px) {
  body {
    background-color: blue;
  }
}
@media screen and (max-width: 600px) {
  body {
    background-color: red;
  }
}
@media screen and (min-width: 900px) {
  body {
    background-color: greenyellow;
  }
}
```

Warna backgroud akan berubah-ubah mengikuti Media Query, dengan media query membuat website menjadi lebih responsive.
