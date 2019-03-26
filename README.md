# How to MongoDB-Atlas & Compass

## Jump-to!
1. [Register](#register)
2. [Installation](#installation)
    1. [MongoDB & Compass](#mongodb--compass)
        1. [Download & Install](#download--install)
        2. [Install Compass by Bundle](#compass)
        3. [Add Environment](#add-environment)
3. [Importing Data](#import)
    1. [Via Shell](#via-shell)
        1. [Dapatkan Address host](#get-the-address)
        2. [Import Data](#do-import)
4. [Akses Atlas](#access)
    1. [Via Compass](#via-compass)
        1. [Copy Connection String](#copy-connection-string)
        2. [Login](#login)
        3. [Hasil Import](#import-result)
        4. [Contoh Filter Query](#contoh-query)

## Pre-Requisite
1. Register here at [mongodb](https://cloud.mongodb.com/user#/atlas/register/accountProfile)

## Register
Setelah terdaftar, maka tambahkan whitelist `IP Address` yang anda perlukan seperti alamat Internet Rumah anda atau `0.0.0.0/0` agar bisa diakses dimana saja(meskipun tidak aman) dan buatlah User. Ketika anda berhasil memasukkannya, akan muncul seperti gambar dibawah ini.
![whitelist](https://github.com/abaar/mongodb/blob/master/resource/screenshot/whitelist.PNG)

## Installation
### MongoDB & Compass
#### Download & Install
Pertama-tama donwload dan install sesuai `OS` anda website resmi [MongoDB](https://www.mongodb.com/download-center/community)
#### Compass 
Pada `V.4.0` anda akan diberikan untuk install `MongoDB Compass` , centanglah karena kita juga akan menggunakan `Compass` untuk mengakses data.

![Compass option](https://github.com/abaar/mongodb/blob/master/resource/screenshot/install%20compass.PNG)

#### Add Environment
Kemudian tambahkan `The-Path-U-Installed-MongoDB/bin` kedalam environment agar bisa menjalankan fitur `MongoDB` di shell. 


## Import
### Via Shell
#### Get the address
Langkah pertama yang diperlukan adalah dapatkan address server anda, berikut contoh alamatnya:
```
panca-base-shard-00-01-stevm.gcp.mongodb.net:27017
```
Seperti gambar dibawah ini 

![addr](https://github.com/abaar/mongodb/blob/master/resource/screenshot/cluster-addr.PNG)

#### Do import
Kemudian jalankan syntax berikut (ubahlah [] sesuai kebutuhan anda):
```
mongoimport --host [alamat] --db [namadatabase] --type json --file [alamat file yang akan di import] --jsonArray --authenticationDatabase admin --ssl --username [username yang tadi dibuat] --password [passwordnya] 
```
Seperti gambar dibawah ini

![import](https://github.com/abaar/mongodb/blob/master/resource/screenshot/import.PNG)


## Access
### Via Compass
Jalankan `COMPASS`
#### Copy Connection String
Setelah anda menjalankan maka anda cukup `copy` alamat yang ada pada dashboard `cluster` anda seperti gambar dibawah ini karena Compass akan mengecek `clipboard` anda dan memasukkan data secara otomatis.

![copy addr to compas](https://github.com/abaar/mongodb/blob/master/resource/screenshot/whichcompass.PNG)

![copied addr compass](https://github.com/abaar/mongodb/blob/master/resource/screenshot/copy-detected.PNG)

#### Login
Lalu yang hanya anda perlukan adalah memasukkan `PASSWORD` user. Setelah itu anda bisa login kedalam Atlas memalui Compass
#### Import Result!
Anda telah masuk dan berikut contoh screenshot data yang telah di `IMPORT`

![result of import](https://github.com/abaar/mongodb/blob/master/resource/screenshot/compass.PNG)

#### Contoh Query!
Berikut adalah contoh Query filter yang bisa dilakukan pada Compass
![example of query](https://github.com/abaar/mongodb/blob/master/resource/screenshot/example%20of%20queries.PNG)
