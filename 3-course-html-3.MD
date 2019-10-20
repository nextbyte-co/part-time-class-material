# HTML Part 3

![HTML](./assets/html.png)

# 1. SVG (Scalable Vector Graphic)

```html
<svg width="200" height="200">
  <circle cx="100" cy="100" r="80" stroke="red" stroke-width="5" fill="blue" />
</svg>
<svg width="400" height="200">
  <rect
    x="25"
    y="25"
    width="300"
    height="100"
    style="fill: rgb(100, 0, 100);
stroke-width: 5;
stroke: black;"
  ></rect>
</svg>
```

# 2. Form

```html
<form action="" method="post">
  ---- INSERT FORM ELEMENT ----
</form>
```

- Input Form

```html
<p><input type="text" /></p>
<p><input type="password" required /></p>
<p><input type="checkbox" /></p>
<p><input type="radio" /></p>
<p><input type="number" min="1" max="10" /></p>
<p><textarea rows="8" cols="64">Ketik di sini</textarea></p>

<p><input type="submit" value="OK" /></p>
```

- Button

```html
<button type="button">OK</button>
<button type="button" onclick="doSomething();">Apply</button>
```

- Select Option

```html
<p>Apa hewan kesukaanmu ?</p>
<select>
  <option>Kucing</option>
  <option>Kudanil</option>
  <option>Digimon</option>
</select>
```

- Option Group

```html
<p>Minuman Favoritmu ?</p>
<select>
  <optgroup label="jus-buah">
    <option>Jambu</option>
    <option>Wortel</option>
    <option>Kiwi</option>
  </optgroup>

  <optgroup label="kopi">
    <option>Americano</option>
    <option>Africano</option>
    <option>Indonesiano</option>
  </optgroup>
</select>
```

- Labels

```html
<label for="user">Username:</label>
<input type="text" name="user" />

<label for="pass">Password:</label>
<input type="password" name="pass" />
```

- Fieldset and Legends

```html
<fieldset>
  <legend>Data Diri</legend>
  <p>
    <label for="nama">Nama:</label>
    <input type="text" name="nama" />
  </p>

  <p>
    <label for="usia">Usia:</label>
    <input type="number" name="usia" />
  </p>
</fieldset>
```

# 3. Division Tag

```html
<body>
  <div>Ini Division 1</div>
  <div>Ini Division 2</div>
  <div>Ini Division 3</div>
</body>
```

note: Tag div biasanya dibuat sebagai wadah atau pembungkus suatu element atau beberapa element. Cara kerja-nya sama dengan tag `<p>` yang block element.

# 4. Span Tag

```html
<body>
  <p>Ini adalah pokemon <span>API<span></p>
</body>
```

note: Cara kerjanya sama dengan tag `<div>` namun dia inline element

# 5. Articles and Sections

```html
<article>
  <section class="header">
    <h1>Header Artikel</h1>
    <p>Selamat datang!</p>
  </section>
  <section class="main">
    <p>Ini konten utama.</p>
  </section>
  <section class="footer">
    <p>Bye!</p>
  </section>
</article>
```

# 6. Main, Headers and Footers

```html
<article>
  <header>
    <h1>Header Artikel</h1>
    <p>Selamat datang!</p>
  </header>
  <main>
    <p>Ini konten utama.</p>
  </main>
  <footer>
    <p>Bye!</p>
  </footer>
</article>
```

# 7. Asides

```html
<article>
  <header>
    <h1>Header Artikel</h1>
    <p>Selamat datang!</p>
  </header>
  <section class="main">
    <p>Ini konten utama.</p>
    <aside>
      <h2>Ini Snippet!</h2>
      <p>Ini teks Snippet</p>
    </aside>
  </section>
  <footer>
    <p>Bye!</p>
  </footer>
</article>
```

# 8. Navigation

```html
<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Blog</a></li>
    <li><a href="#">News</a></li>
  </ul>
</nav>
```

---

# Tugas HTML

1. Buat repository baru di github : `web-profile`
2. Buat profile tentang dirimu dengan HTML, CV juga boleh
3. Push ke github