# NODE JAVASCRIP

=> adalah sebuah runtime untuk JavaScript. yang membedakan antara node dan javascrip adalah node.js bisa hidup di luar browser

Node.js memiliki sifat open-source, cross-platform. Cross ini yang membuat node bisa hidup di manapun.

## Node JS Architecture

- Single Thread =>
  memiliki eksekusi cuman 1 tapi bisa menjalankan beberapa tugas dalam waktu yang bersamaan.

Javascript menggunakan call stack untuk melakukan manajemen single thread yang sifatnya lifo. Ketika terdapat perintah baru maka akan ditambahkan (push) dan akan di keluarkan ketika perintahnya sudah selasai (pop). Jadi lifo itu perintah yang baru masuk yang pertama kali di eksekusi atau perintah yang paling atas terlebih yang dieksekusi.

- Even loop event loop akan memeriksa terus menerus, ketika antrian kosong di call stack maka akan menambah antrian baru dari event queue sampai semua perintah selesai di eksekusi.

- Server side scripting
  javascrip bisa menampilkan hasil eksekusi menggunakan browser. Tetapi dengan menggunakan NodeJS kita dapat menjalankan javascript di server side menggunakan terminal command line menggunakan perintah “node”.

sebelum masuk node ada beberapa materi yang perlu di review :

- Arrow function expression
- Asynchronous
- JSON

## Build In Module Node JS

- CONSOLE =>
  Console merupakan module bawaan dari javascript yang ada di node JS untuk digunakan sebagai debug atau menampilkan code secara interface

- PROCESS =>
  Process adalah modules yang digunakan untuk menampilkan dan mengontrol prosess Node JS yang sedang dijalankan.

- OS =>
  OS module merupakan module yang digunakan untuk menyediakan informasi terkait sistem operasi komputer yang digunakan user.

- Util =>
  Module Util merupakan alat bantu / utilities untuk mendukung kebutuhan internal API di Node JS

- FS =>
  Atau file system merupakan module yang dapat membantu berinteraksi dengan file yang ada diluar code. FS paling sering digunakan untuk membaca file dengan ekstensi .txt, .csv, dan .json

- Timers => Timers merupakan modules yang digunakan untuk melakukan scheduling atau mengatur waktu pemanggilan fungsi yang dapat diatur di waktu tertentu

Membuat Web Server

Di Node JS kita harus membuat web server sendiri.

- Untuk menggunakan modul HTTP, gunakan require()
- Gunakan method createServer() untuk membuat server HTTP
- Callback function berada didalam http.createServer(),memiliki parameter reques dan respons yang akan dijalankan ketika seseorang mencoba mengakses komputer pada port 8080.

Menambahkan HTTP Header

- bisa menambahkan header dengan method res.writeHead()
- Argumen pertama dari method res.writeHead() adalah status code, 200
- Argumen kedua adalah objek yang berisi header respons.

Respons yang dikembalikan dari HTTP web server bisa dalam berbagai format.Contohnya, Kita bisa mengembalikan response dalam format JSON dan HTML, namun kita juga dapat mengembalikan format teks lain seperti XML dan CSV.Selain itu web server dapat mengembalikan data non-teks seperti PDF, file zip, audio, dan video.Format ini harus ditambahkan kedalam HTTP Header.

# Web server

web server terdiri dari dua komponen pentinng

- Hardware

  sisi perangkat keras, server web adalah komputer yang menyimpan perangkat lunak server web dan file komponen situs web.
  Server web terhubung ke Internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung ke web.

- Software

  Di sisi perangkat lunak, server web mencakup beberapa bagian yang mengontrol bagaimana pengguna web mengakses file yang dihosting.

Dan ada juga Server HTTP adalah perangkat lunak yang memahami URL (alamat web) dan HTTP (protokol yang digunakan browser Anda untuk melihat halaman web). Server HTTP dapat diakses melalui nama domain situs web yang disimpannya, dan mengirimkan konten situs web yang dihosting ini ke perangkat pengguna akhir.

### Static Web Server

hanya bisa mengirimkan file file yang bersifatnya static. servernya hanya bisa mengirim saja tidak bisa menerima file inputan apapun.

### Dynamic Web Server

terdapat extra software didalamnya. didalam extra software bisanya tedapat application server dan database

## Server Side Programming

Server web menunggu pesan permintaan klien, memprosesnya saat tiba, dan membalas browser web dengan pesan respons HTTP.

- situs statis adalah situs yang mengembalikan konten hard-coded yang sama dari server setiap kali sumber daya tertentu diminta

- Situs web dinamis adalah situs di mana beberapa konten respons dihasilkan secara dinamis, hanya bila diperlukan. dan bisa memasukan data kedalam databes.

## REST

adalah sebuah gaya arsitektur yang isinya menyiapkan standar di sistem komputer untuk berkomukiaksi antara backhand dan forehand.

### Komunikasi antara Klien dan Server

dengan menggunkan Making Requests.
Ada 4 kata kerja HTTP dasar.

- GET => mengambil data berdasrkan ID
- POST => buat data baru
- PUT => perbarui data tertentu (berdasarkan id)
- DELETE => menghapus data tertentu dengan id

### Header dan Terima Parameter

Di header permintaan, klien mengirimkan jenis konten yang ingin diterimanya dari server.
bisa sebuah img, vidio atau data data yang lain.

### Paths

ketika mau mengakses kita perlu sebuah paths. Paths tidak mempunyai aturan yang baku, tapi dia memiliki sebuah konvensen yang diharapkan di ikuti apalagi ketika compiketet.

## Sending Responses

### Content Types

misalnya klien meminta permintaan dengan GET ini:

GET /articles/23 HTTP/1.1
Accept: text/html, application/xhtml

kemungkin server mengirim kembali konten dengan header respons:
HTTP/1.1 200 (OK)
Content-Type: text/html

### Response Codes

ada beberapa kode status yang diharapkan yang harus dikembalikan server setelah berhasil:

GET — return 200 (OK)

POST — return 201 (CREATED)

PUT — return 200 (OK)

DELETE — return 204 (NO CONTENT)

# Express JS

adalah kerangka aplikasi web back end untuk Node.js. sebagai perangkat lunak gratis yang dirancang untuk membangun aplikasi web dan API. I

- Api itu berada diantara frontend dan backend atau penghubung antara frontend dan backend.

- Database = menyimpan semua data.

- server = menyiapkan atau mengelola sebuah data yang diminta oleh client

Mengetest API bisa dari postman, insomnia, thunder client, browser (get).

## Installation and Preparation

1.  menginstall express js dengan menggunkan
    npm install express --save

2 install module nodemon (agar dapat restart application otomatis selama proses development)

## Routes

Routes adalah sebuah end point yang diapat kita akses menggunakan URL di website. Didalam routes kita perlu menentukan method API, alamat dan response apa saja yang akan dikeluarkan

## method

Kita dapat menggunakan method yang dalam REST API seperti POST, PUT, PATCH dan DELETE

## Response

Di dalam route kita dapat mengirim response menggunakan parameter dari route express.js yaitu “res.Send()” untuk mengirim plain text ketika kita mengakses route tersebut.

## Status Code

Dalam pengaplikasian back end application, kita sangat perlu memberikan status code sebagai informasi apakah route yang kita akses berjalan sebagaimana mestinya dan tidak terjadi error.

## Middleware

Middleware function adalah sebuah fungsi yang memiliki akses ke object request (req), object response (res), dan sebuah fungsi next didalam request-response cycle.
Fungsi next biasanya di berikan nama variable next.
