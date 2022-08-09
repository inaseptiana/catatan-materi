# Sequelize

Sequelize adalah ORM (Object Relational Mapping) Node JS yang berbasis promise. Sequelize mendukung sebagian besar relational Database seperti MySQL, PostgresQL, MariaDB, SQLite dan Miscrosoft SQL Server.

~ ORM adalah suatu metode pemrograman yang digunakan untuk mengkonversi data dari lingkungan bahasa pemrograman berorientasi objek (OOP) dengan lingkungan database relational.

### Generate Model

adalah membuat table.

### Generate Seed

Seed adalah data awal yang bisa kita gunakan untuk mengisi data di database untuk keperluan awal project menggunakan sequelize.
Setelah berhasil kita dapat mengisi data seed. terdapat 2 data yang perlu di isi yaitu “up” untuk mengisi data di db, dan “down” untuk drop atau menghapus semua data seed di db

### Membuat CRUD Dengan Express dan Sequelize

Setelah Model tersedia, maka model tersebut bisa kita gunakan untuk membuat CRUD.

Beberapa endpoint RESTFul :

1 Get All Todos

untuk membuat sebuah routing yang menjalankan perintah mengambil semua data todo.

2 Get Todo Detail By Id

untuk membuat sebuah routing yang menjalankan perintah mengambil data berdasarkan ID yang di input.

3 Create New Todo

untuk membuat sebuah routing yang menjalankan perintah membuat todo yang baru.

4 Update Todo By Id

untuk mengupdate data yang sudah ada atau memperbarui data yang ada sesuai ID yang di minta.

5 Delete Todo By id

untuk mendelete data sesuai ID yang diminta atau menghapus data sesui ID.

# Mongo DB

MongoDB adalah salah satu database open source NoSQL yang cukup populer digunakan. Dan sering dipakai untuk aplikasi berbasis Cloud, Big Data maupun Grid COmputing. Jika SQL menyimpan data menggunakan relasi tabel, MongoDB menggunakan dokumen dengan format JSON.

## NoSQL adalah Not Only SQL

Artinya kita bisa mengolah database dengan fleksibel dan tidak membutuhkan Query. Akhirnya kita memiliki skalabilitas yang tinggi.

## Kelebihan Mongodb

- Sistem tidak membutuhkan Tabel
- Tidak perlu menggunakan Tabel yang terstruktur
- By Default sudah menggunakan JSON(JavaScript Object Notation), sehingga memudahkan integrasi dengan JavaScript
- Performa lebih cepat dengan kemampuan menampung banyak data yang bervariasi

## kekurnagan Mongodb

- Tidak mendukung transaksi
- Masalah konsistensi data
- Menggunakan banyak memory
- Hanya bisa menampung maksimal 16MB disetiap document

## komponen dari Database MongoDB

- Database adalah wadah untuk menyimpan berbagai macam Collection
- Collection adalah tempat kumpulan dari berbagai macam document, sehingga collection sering disamakan dengan tabel pada SQL
- Document adalah unit terkecil yang berada pada MongoDB

## Operasi CRUD MongoDB

- Show dbs untuk mellihat daftar database .
- db.createCollections(“artis”) untuk menambahkan Collection baru
- db.artis.insert({
  nama: "Peterpan",
  genre: "pop"
  })
  untuk menambahkan data di dalam collection.
- db.artis.find() untuk melihat data.
- db.artis.update({
  'nama':'Peterpan'
  },{
  $set:{'nama':'Noah'}
  })
  untuk mengupdate data nama atau mengubah nama
- db.artis.remove({
  'nama': ‘Noah’
  })
  untuk menghapus data nama

Dalam mendesain MongoDB kita ada 2 pendekatan yaitu Embedding dan Referencing

## Relasi dalam MongoDB

### One-to-One Relationships

Hubungan one-to-one mewakili dari hubungan 2 objek yang berbeda.

### One-to-Many Relationships

Bayangkan kita sedang menggunakan aplikasi music streaming kita, Satu lagu akan diputar oleh banyak user. Lebih detailnya 1 lagu bisa diputar oleh ratusan atau ribuan user.

### Many-to-Many Relationships

Sekarang bayangkan kita sebagai seorang user bisa memiliki playlist, sebuah playlist bisa didengarkan oleh banyak user dan seorang user bisa memiliki lebih dari 1 playlist untuk didengarkan. Lalu dalam playlist kita juga berisi dari banyak lagu.
