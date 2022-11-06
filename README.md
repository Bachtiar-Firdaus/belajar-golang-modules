# **BELAJAR GO-LANG MODULES**

## **PERSYARATAN YANG WAJIB**

- Minimal kalian telah mempelajari Materi CAPTER 1 [LINK CATPER 1](https://github.com/Bachtiar-Firdaus/belajar-golang-dasar)

## **DESKRIPSI SINGKAT MATERI CAPTER 2**

> Ini adalah repositori yang berisi materi materi Go-Module dari golang

- Agenda
  - Membuat Go Modules
  - Membuat Module
  - Rilis Module
  - Menambah Depedency
  - Upgrade Module
  - Upgrade Depedency

## **PENGENALAN GO MODULES**

> Saat kita membuat aplikasi, biasanya kita akan menggunakan library atau depedency dari project lain, sebelum adanya Go Modules, management untuk depedency sangat sulit dilakukan di Go-Lang. Biasanya kita akan meng Copy semua source code library atau depedency lain ke project kita, hal ini membuat project kita menjadi bengkak karna penuh dengan library orang lain. Atau biasanya library orang lain akan kita save di GOPATH directory, namun hal ini akan sulit jika ternyata beberapa aplikasi butuh library yang sama dengan versi yang berbeda.

> Go-Modules mulai dikenalkan di Go-Lang 1.11 dan 1.12, dengan Go-Modules, Kita bisa membuat project dengan mudah dan depedency management yang sangat mudah

## **CARA MEMBUAT GO MODULES**

- Untuk membuat module baru kita bisa menggunakan perintah : go mod init nama-module
- Go-Lang akan secara otomatis membuat fule go.mod yang berisikan informasi nama module dan juga versi Go-Lang yang kita gunakan

## **CARA RILIS GO MODULES**

> Go-Lang terintegrasi dengan Git, untuk merilis module, kita hanya perlu membuat Tag di GIT

> untuk temen temen yang go-modulenya di non activkan bisa menggunakan perintah ini untuk mengaktivkan go module : go env -w GO111MODULE=on

- noted :setelah membuat sample module bisa menggunakan comand ini di terminal :
  - git tag v1.0.0
  - git push origin v1.0.0

## **CARA MENAMBAH DEPEDENCY**

- gunakan perintah :
  - go get nama-module
    > disini saya telah membuat sample module yang bisa kalian akses disini [LINK MODULE](https://github.com/Bachtiar-Firdaus/golang-example-module)

## **CARA UPGRADE MODULE**

> Untuk melakukan upgrade module, kita hanya mebuat tag baru di GIT

    - git tag v1.5.1
    - git push origin v1.5.1

## **CARA UPGRADE DEPEDENCY**

> Untuk upgrade depedency ke versi terbaru, kita bisa mengubah isi go.mod, lalu mengubah tagnya menjadi tag terbaru, untuk mendownoad versi terbaru gunakan perintah:

    - go get

> noted waning perubahan sekecil apapun wajib di masukan ke tag versi terbaru ketika akan di rilis karna dari sisi golang snsitif terhada versi tag yang di rilis

## **MAJOR UPGRADE MODULE**

> Major upgrade biasanya terjadi di karenakan ada perubahan pada isi kode program kita sehingga membuat tidak backward compatible, sebaiknya hal ini sebisa mungkin di hindari, namun jika tidak bisa dihindari, strategy terbaik adalah merubah nama module

    - git tag v2.0.0
    - git push origin v2.0.0
