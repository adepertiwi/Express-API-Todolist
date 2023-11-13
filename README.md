# Dokumentasi Web Service & RESTful API for ToDoList Application

Dokumentasi ini menjelaskan penggunaan dan endpoint-endpoint yang tersedia pada Web Service & RESTful API for ToDoList Application. API ini menyediakan fungsi untuk mengelola daftar todo bagi pengguna yang terdaftar.

## Daftar Isi

- [Pendahuluan](#pendahuluan)
- [Authentication](#authentication)
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

#
    1. Clone repository: 
        git clone https://github.com/adepertiwi/Express-API-Todolist.git 
        cd Express-API-Todolist

    2. Install dependensi: 
        npm install

    3. Jalankan server: 
         npm start 
        <!-- API akan berjalan di http://localhost:3000 secara default. -->

## Authentication
Untuk mengakses endpoint Todo, Anda perlu menyertakan JWT (JSON Web Token) yang valid pada header permintaan. Dapatkan JWT dengan melakukan login melalui endpoint /auth/login.

    1. Buka aplikasi Postman atau bisa menggunakan extension Thunder Client
    2. Gunakan Metode POST untuk endpoint registrasi akun 
    3. Sertakan informasi pengguna (seperti username, name dan password) dalam body permintaan.
        contoh: 
        {
            "username": "Ade Pertiwi",
            "name": "tiwi",
            "password": "123"
        }

    4. klik button "Send"
    5. Lalu akan muncul hasil seperti ini
        {
            "message": "berhasil membuat data user"
        }


