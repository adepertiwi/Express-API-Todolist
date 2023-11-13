# Dokumentasi Web Service & RESTful API for ToDoList Application

Dokumentasi ini menjelaskan penggunaan dan endpoint-endpoint yang tersedia pada Web Service & RESTful API for ToDoList Application. API ini menyediakan fungsi untuk mengelola daftar todo bagi pengguna yang terdaftar.

## Daftar Isi

- [Pendahuluan](#pendahuluan)
- [Registrasi](#registrasi)
- [Login](#login)
- [Membuat Todo Baru](#membuat-todo-baru)
- [Melihat Todo Berdasarkan ID](#melihat-todo-berdasarkan-id)
- [Mengubah Todo](#mengubah-todo)
- [Menghapus Todo](#menghapus-todo)

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

## Membuat Todo Baru

Berikut langkah langkah untuk membuat todo baru untuk pengguna yang terotentikasi (Endpoint: POST /todos).

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

## Melihat Todo berdasarkan ID

Berikut langkah langkah untuk melihat todo spesifik berdasarkan ID (Endpoint: GET /todos/:id).

    1. Buka aplikasi Postman atau gunakan extension Thunder Client
    2. Gunakan metode GET untuk mengakses endpoint melihat todo spesifik berdasarkan ID
    3. Masukan  URL http://localhost:3000/todos/:id
    4. Pilih tipe konten sebagai raw dan format JSON
    5. Masukan Header "Key" dengan "Authorization" dan "value" dengan "userId"
    6. klik button "Send"
    7. Lalu akan muncul hasil seperti ini
        {
            "message": "Berhasil mendapatkan detail todo",
            "data": {
                "_id": "......",
                "value": "Membuat todo baru",
                "userID": {
                    "_id": "......",
                    "name": "Tiwi"
                },
                "__v": 0
            }
        }

Dengan mengikuti langkah-langkah di atas, Anda dapat berhasil melihat todo spesifik berdasarkan ID melalui API.

## Mengubah Todo

Berikut langkah langkah untuk perbarui todo spesifik berdasarkan ID (Endpoint: PUT /todos/:id).

    1. Buka aplikasi Postman atau gunakan extension Thunder Client
    2. Gunakan metode PUT untuk mengakses endpoint perbarui todo spesifik berdasarkan ID
    3. Masukan URL http://localhost:3000/todos/todo_id
    4. Pilih tipe konten sebagai raw dan format JSON
    5. Masukan Header "Key" dengan "Authorization" dan "value" dengan "userId"
    6. Sertakan informasi todo seperti "value" dalam body permintaan. Contoh:
        {
            "value": "Todo update"
        }

    7. klik button "Send"
    8. Lalu akan muncul hasil seperti ini
        {
            "message": "Berhasil mengubah data todo",
            "data": {
                "_id": "......",
                "value": "Todo update",
                 "userID": "......",
                "__v": 0
             }
        }

Dengan mengikuti langkah-langkah di atas, Anda dapat berhasil perbarui todo spesifik berdasarkan ID melalui API.

## Menghapus Todo

Berikut langkah langkah untuk menghapus todo spesifik berdasarkan ID(Endpoint: DELETE /todos/:id).

    1. Buka aplikasi Postman atau gunakan extension Thunder Client
    2. Gunakan metode DELETE untuk mengakses endpoint menghapus todo spesifik berdasarkan ID
    3. Masukan URL http://localhost:3000/todos/todo_id
    4. Pilih tipe konten sebagai raw dan format JSON
    5. Masukan Header "Key" dengan "Authorization" dan "value" dengan "userId"
    6. klik button "Send"
    7. Lalu akan muncul hasil seperti ini
        {
            "message": "Berhasil menghapus data todo",
            "data": {
                "_id": "......",
                "value": "Todo update",
                "userID": "......",
                "__v": 0
            }
        }

Dengan mengikuti langkah-langkah di atas, Anda dapat berhasil menghapus todo spesifik berdasarkan ID melalui API.