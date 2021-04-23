# Praktikum 4: CSS Layout
# Mata Kuliah Pemrograman WEB
```
Nama  : Abdul Majid
NIM   : 311810693
Kelas : TI.19.C.1
Universitas Pelita Bangsa
```
## Persiapan
Buka VSCode dan Browser lalu buat file HTML baru dengan nama lab4_box.html lalu tambahkan kode html berikut.
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
</head>
<body>
    <header>
      <h1>Box Element</h1>
    </header>
</body>
</html>
```

## 1. Membuat Box Element
Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut.
```html
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
    </section>
```
![1-Ordered-List](https://user-images.githubusercontent.com/81838946/114571355-cf352880-9ca0-11eb-9cb2-39ac056de464.PNG)

## 2. CSS Float Property
Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut.
```html
    <style>
        div {
        float:left;
        padding: 10px;
        }
        .div1 {
        background: red;
        }
        .div2 {
        background: yellow;
        }
        .div3 {
        background: green;
        }
    </style>
```
![2](https://user-images.githubusercontent.com/81838946/115150369-35032500-a092-11eb-9a1d-9b4bc428c55b.PNG)

## 3. Mengatur Clearfix Element
Clearfix digunakan untuk mengatur element setelah float element. Property clear digunakan untuk mengaturnya.

Tambahkan element div lainnya seteleah div3 seperti berikut.
```html
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
    </section>
 ```
Kemudian atur property clear pada CSS, seperti berikut.
```html
        .div4 {
            background-color: blue;
            clear: left;
            float: none;
        }
 ```
![3](https://user-images.githubusercontent.com/81838946/115150471-beb2f280-a092-11eb-8f4f-c0b84edd92c7.PNG)

 ## 4. Membuat Layout Sederhana
Buat folder baru dengan nama lab4_layout, kemudian buatlah file baru didalamnya dengan nama
home.html, dan file css dengan nama style.css.
 ```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        
    </div>
</body>
</html>
 ```
Kemudian tulis kode berikut.
```html
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        <section id="hero"></section>
        <section id="wrapper">
            <section id="main"></section>
            <aside id="sidebar"></aside>
        </section>
        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
```
![4](https://user-images.githubusercontent.com/81838946/115150724-d8086e80-a093-11eb-8c44-3da654744495.PNG)

Kemudian tambahkan kode CSS untuk membuat layoutnya.
```css
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}
body {
    line-height:1;
    font-size:100%;
    font-family:'Open Sans', sans-serif;
    color:#5a5a5a;
}
#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* header */
header {
    padding: 20px;
}
header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
```
![4-2](https://user-images.githubusercontent.com/81838946/115151155-de97e580-a095-11eb-965f-dc16503ccb79.PNG)

## 5. Membuat Navigasi
Kemudian selanjutnya mengatur navigasi.
```css
/* navigasi */
nav {
    display: block;
    background-color: #1f5faa;
}
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}
nav a.active,
nav a:hover {
    background-color: #2b83ea;
}
```
![5](https://user-images.githubusercontent.com/81838946/115151238-3c2c3200-a096-11eb-83c1-11d29b4216b8.PNG)

## 6. Membuat Hero Panel
Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.
```html
<section id="hero">
            <h1>Hello World!</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum loremelit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
            <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
```css
/* Hero Panel */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}
#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}
#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
}
```
![6](https://user-images.githubusercontent.com/81838946/115151592-c032e980-a097-11eb-884b-855bcddbcdb8.PNG)

## 7. Mengatur Layout Main dan Sidebar
Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.
```css
/* main content */
#wrapper {
    margin: 0;
}
#main {
    float: left;
    width: 640px;
    padding: 20px;
}

/* sidebar area */
#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
}
```
## 8. Membuat Sidebar Widget
Kemudian selanjutnya menambahkan element lain dalam sidebar.
```html
            <aside id="sidebar">
                <div class="widget-box">
                    <h3 class="title">Widget Header</h3>
                    <ul>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                    </ul>
                </div>
                <div class="widget-box">
                    <h3 class="title">Widget Text</h3>
                    <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
                </div>
            </aside>
```
Kemudian tambahkan CSS.
```css
/* widget */
.widget-box {
    border:1px solid #eee;
    margin-bottom:20px;
}
.widget-box .title {
    padding:10px 16px;
    background-color:#428bca;
    color:#fff;
}
.widget-box ul {
    list-style-type:none;
}
.widget-box li {
    border-bottom:1px solid #eee;
}
.widget-box li a {
    padding:10px 16px;
    color:#333;
    display:block;
    text-decoration:none;
}
.widget-box li:hover a {
    background-color:#eee;
}
.widget-box p {
    padding:15px;
    line-height:25px;
}
```
![8](https://user-images.githubusercontent.com/81838946/115151856-ee64f900-a098-11eb-8fe3-4bf7e8801907.PNG)

## 9. Mengatur Footer
Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.
```css
/* footer */
footer {
    clear:both;
    background-color:#1d1d1d;
    padding:20px;
    color:#eee;
}
```
![9](https://user-images.githubusercontent.com/81838946/115152771-c11a4a00-a09c-11eb-9a47-9409a105a86f.PNG)

## 10. Menambahkan Elemen lainnya pada Main Content
```html
            <section id="main">
                <div class="row">
                    <div class="box">
                        <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                </div>
            </section>
```
Kemudian tambahkan CSS.
```css
/* box */
.box {
    display:block;
    float:left;
    width:33.333333%;
    box-sizing:border-box;
    -moz-box-sizing:border-box;
    -webkit-box-sizing:border-box;
    padding:0 10px;
    text-align:center;
}
.box h3 {
    margin: 15px 0;
}
.box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
}
.box img {
    border: 0;
    vertical-align: middle;
}
.image-circle {
    border-radius: 50%;
}
.row {
    margin: 0 -10px;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
}
.row:after, .row:before,
.entry:after, .entry:before {
    content:'';
    display:table;
}
.row:after,
.entry:after {
    clear:both;
}
```
![10](https://user-images.githubusercontent.com/81838946/115153031-0428ed00-a09e-11eb-9a0e-52c5aae64f75.PNG)

## 11. Menambahkan Content Artikel
Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.
```html
                <hr class="divider" />
                <article class="entry">
                    <h2>First featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
                </article>
                <hr class="divider" />
                <article class="entry">
                    <h2>First featurette heading.</h2>
                    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
                </article>
```
Kemudian tambahkan CSS.
```css
.divider {
    border:0;
    border-top:1px solid #eeeeee;
    margin:40px 0;
}

/* entry */
.entry {
    margin: 15px 0;
}
.entry h2 {
    margin-bottom: 20px;
}
.entry p {
    line-height: 25px;
}
.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}
.entry .right-img {
    float: right;
}
```
![11](https://user-images.githubusercontent.com/81838946/115153455-2cb1e680-a0a0-11eb-96e5-2eaa74024340.PNG)

## Jawab Pertanyaan dan Tugas
1. Tambahkan Layout untuk menu About => buat single layout yang berisi deskripsi, portfolio, dll.
2. Tambahkan layout untuk menu Contact => yang berisi form isian: nama, email, message, dll.

## Jawab
1. Saya menambahkan file about.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html" class="active">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        <section id="hero">
            <h1 style="text-align: center;">About Me</h1>
        </section>
        <section id="wrapper">
            <section id="main">
                <div class="row">
                    <article class="entry">
                        <h2>About Me</h2>
                        <img src="https://dummyimage.com/200x250/7b8a70/fff.png" alt="">
                        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
                    </article>
                    <hr class="divider" />
                    <div class="porto">
                        <h2>Portfolio</h2>
                        <div class="box">
                            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                        </div>
                        <div class="box">
                            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                        </div>
                        <div class="box">
                            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                        </div>
                    </div>
                    <div class="porto">
                        <div class="box">
                            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                        </div>
                        <div class="box">
                            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                        </div>
                        <div class="box">
                            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
                        </div>
                    </div>
                </div>
            </section>
            <aside id="sidebar">
                <div class="widget-box">
                    <h3 class="title">Widget Header</h3>
                    <ul>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                    </ul>
                </div>
                <div class="widget-box">
                    <h3 class="title">Widget Text</h3>
                    <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
                </div>
            </aside>
        </section>
        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```
lalu saya menambahkan css untuk class = porto pada file style.css.
```css
.row:after, .row:before,
.entry:after, .entry:before,
.porto:after, .porto:before {
    content:'';
    display:table;
}
.row:after,
.entry:after,
.porto:after {
    clear:both;
}
.porto {
    margin: 15px 0;
}

.porto img {
    border-radius: 5px;
    margin-right: 15px;
}
```
![image](https://user-images.githubusercontent.com/81838946/115889438-247df080-a47e-11eb-84db-4294edf3bce2.png)
![image](https://user-images.githubusercontent.com/81838946/115889522-38295700-a47e-11eb-840b-de525d0bae1a.png)

2. menambahkan page kontak.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header>
            <h1>Layout Sederhana</h1>
        </header>
        <nav>
            <a href="home.html">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html" class="active">Kontak</a>
        </nav>
        <section id="hero">
            <h1 style="text-align: center;">Contact Us</h1>
        </section>
        <section id="wrapper">
            <section id="main">
                <div class="row">
                    <h2>Contact Us</h2>
                    <div class="contact">                    
                        <form action="action_page.php">
                  
                            <label for="nama_dpn">Nama Depan</label>
                            <input type="text" id="nama_dpn" name="namadepan" placeholder="Nama Depan Anda..">
                  
                            <label for="nama_blkng">Nama Belakang</label>
                            <input type="text" id="nama_blkng" name="namabelakang" placeholder="Nama Belakang Anda..">
                            
                            <label for="email">Email</label>
                            <input type="text" id="email" name="email" placeholder="Email Anda..">
                  
                            <label for="pesan">Pesan</label>
                            <textarea id="pesan]" name="pesan" placeholder="Tulis sesuatu.." style="height:200px"></textarea>
                  
                            <input type="submit" value="Kirim">
                  
                        </form>
                    </div>
                </div>
            </section>
            <aside id="sidebar">
                <div class="widget-box">
                    <h3 class="title">Widget Header</h3>
                    <ul>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                        <li><a href="#">Widget Link</a></li>
                    </ul>
                </div>
                <div class="widget-box">
                    <h3 class="title">Widget Text</h3>
                    <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
                </div>
            </aside>
        </section>
        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```
lalu menambahkan css untuk form contact.
```css
/* contact*/
input[type=text], select, textarea {
    width: 100%;
    padding: 12px; 
    border: 1px solid #ccc; 
    border-radius: 4px; 
    box-sizing: border-box; 
    margin-top: 6px;
    margin-bottom: 16px; 
    resize: vertical;
  }
  
  input[type=submit] {
    background-color: #428bca;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  input[type=submit]:hover {
    background-color: #428bca;
  }
  
  .contact {
    border-radius: 5px;
    padding: 20px;
  }

```
![image](https://user-images.githubusercontent.com/81838946/115892503-69575680-a481-11eb-97fd-f4d0d961bc96.png)
![image](https://user-images.githubusercontent.com/81838946/115892545-73795500-a481-11eb-9580-4cf83464c33f.png)

