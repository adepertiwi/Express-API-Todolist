# Dokumentasi Web Service & RESTful API for ToDoList Application

Dokumentasi ini menjelaskan penggunaan dan endpoint-endpoint yang tersedia pada Web Service & RESTful API for ToDoList Application. API ini menyediakan fungsi untuk mengelola daftar todo bagi pengguna yang terdaftar.

## Daftar Isi
- [Pendahuluan](#pendahuluan)
- [Registrasi](#registrasi)
- [Login](#login)
- [Endpoint Todo](#endpoint-todo)
  - [1. Mendapatkan Semua Todo](#1-mendapatkan-semua-todo)
  - [2. Mendapatkan Todo berdasarkan ID](#2-mendapatkan-todo-berdasarkan-id)
  - [3. Membuat Todo Baru](#3-membuat-todo-baru)
  - [4. Mengubah Todo](#4-mengubah-todo)
  - [5. Menghapus Todo](#5-menghapus-todo)
  - [6. Menghapus Semua Todo](#6-menghapus-semua-todo)
- [Endpoint User](#endpoint-user)

## Pendahuluan
Untuk memulai menggunakan Todo App API, ikuti langkah-langkah berikut:

    1. Clone repository: 
        git clone https://github.com/adepertiwi/Express-API-Todolist.git 
        cd Express-API-Todolist

    2. Install dependensi: 
        npm install

    3. Jalankan server: 
         npm start 
        <!-- API akan berjalan di http://localhost:3000 secara default. -->

## Registrasi
Berikut langkah langkah untuk melakukan regitrasi melalui endpoint /users.

    1. Buka aplikasi Postman atau gunakan extension Thunder Client
    2. Gunakan metode POST untuk mengakses endpoint registrasi akun
    3. Masukan  URL http://localhost:3000/users 
    4. Pilih tipe konten sebagai raw dan format JSON
    5. Sertakan informasi pengguna (seperti username, name, email dan password) dalam body permintaan. Contoh: 
        {
            "name": "Tiwi",
            "username": "Ade Pertiwi",
            "email": "tiwi@gmail.com",
            "password": "123"
        }

    6. Klik tombol "Send"
    7. Anda akan mendapatkan hasil seperti berikut:
        {
            "message": "berhasil membuat data user"
        }

Dengan mengikuti langkah-langkah di atas, Anda dapat berhasil melakukan registrasi pengguna melalui API.

## Login
Berikut langkah langkah untuk melakukan login melalui endpoint /auth/login.

    1. Buka aplikasi Postman atau gunakan extension Thunder Client
    2. Gunakan metode POST untuk mengakses endpoint login akun
    3. Masukan  URL http://localhost:3000/auth/login
    4. Pilih tipe konten sebagai raw dan format JSON
    5. Sertakan informasi pengguna (seperti email dan password) dalam body permintaan. Contoh: 
        {
            "email": "tiwi@gmail.com",
            "password": "123"
        }

    6. klik button "Send"
    7. Lalu akan muncul hasil seperti ini
        {
            "message": "login successfull",
            "userId": "......",
            "token": "......"
        }

Dengan mengikuti langkah-langkah di atas, Anda dapat berhasil melakukan login pengguna melalui API.

## Endpoint Todo

##  1. Membuat todo baru
Berikut langkah langkah untuk membuat todo baru untuk pengguna yang terotentikasi.

    1. Buka aplikasi Postman atau gunakan extension Thunder Client
    2. Gunakan metode POST untuk mengakses endpoint membuat todo baru
    3. Masukan  URL http://localhost:3000/todos
    4. Pilih tipe konten sebagai raw dan format JSON
    5. Masukan Header "Key" dengan "Authorization" dan "value" dengan "userId"
    6. Sertakan informasi todo seperti "value" dalam body permintaan. Contoh: 
        {
            "value": "Membuat todo baru"
        }

    7. klik button "Send"
    8. Lalu akan muncul hasil seperti ini
        {
            "message": "Berhasil membuat data todo"
        }

Dengan mengikuti langkah-langkah di atas, Anda dapat berhasil membuat todo baru melalui API.

##  1. Membuat todo baru
Berikut langkah langkah untuk membuat todo baru untuk pengguna yang terotentikasi.

    1. Buka aplikasi Postman atau gunakan extension Thunder Client
    2. Gunakan metode POST untuk mengakses endpoint membuat todo baru
    3. Masukan  URL http://localhost:3000/todos
    4. Pilih tipe konten sebagai raw dan format JSON
    5. Masukan Header "Key" dengan "Authorization" dan "value" dengan "userId"
    6. Sertakan informasi todo seperti "value" dalam body permintaan. Contoh: 
        {
            "value": "Membuat todo baru"
        }

    7. klik button "Send"
    8. Lalu akan muncul hasil seperti ini
        {
            "message": "Berhasil membuat data todo"
        }

Dengan mengikuti langkah-langkah di atas, Anda dapat berhasil membuat todo baru melalui API.
    