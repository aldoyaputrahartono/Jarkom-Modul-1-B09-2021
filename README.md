# Jarkom-Modul-1-B09-2021

Repository Praktikum Jarkom Modul 1
- 05111940000084_Aldo Yaputra Hartono
-
- 05111840000023_Izzulhaq Fawwaz Syauqiy

## Soal 1
Sebutkan webserver yang digunakan pada `ichimarumaru.tech`!

Display Filter : `http contains "ichimarumaru.tech"`

![image](https://user-images.githubusercontent.com/31863229/134379580-2211a00b-fb0b-4dfc-a17e-85588d641ecc.png)

Klik kanan lalu pilih Follow > TCP Stream, dapat dilihat bahwa webserver yang digunakan adalah nginx/1.18.0 (Ubuntu).

![image](https://user-images.githubusercontent.com/31863229/134379646-4040cb0b-caf0-4572-b70c-339a8710df3e.png)

## Soal 2
Temukan paket dari web-web yang menggunakan basic authentication method!

Display Filter : `http.authbasic`

![image](https://user-images.githubusercontent.com/31863229/134379905-d2c1d381-7a83-4e24-90d8-2f187d483af5.png)

Pada Authorization terdapat tulisan `Basic`.

![image](https://user-images.githubusercontent.com/31863229/134379944-a465a932-2a9e-4824-8ccb-f9bbda3a55b6.png)

## Soal 3
Ikuti perintah di `basic.ichimarumaru.tech`! Username dan password bisa didapatkan dari file `.pcapng`!

Display Filter : `http.authbasic`

![image](https://user-images.githubusercontent.com/31863229/134379905-d2c1d381-7a83-4e24-90d8-2f187d483af5.png)

Kelanjutan dari Soal 2, buka bagian Authorization.

Pada Credentials didapatkan username (`kuncimenujulautan`) dan password (`tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN`).

![image](https://user-images.githubusercontent.com/31863229/134381764-703c1dd6-6e75-4de2-95a0-d1f1b0fec31f.png)

Login ke `basic.ichimarumaru.tech` dan kerjakan soalnya.

![image](https://user-images.githubusercontent.com/31863229/134382261-1c8ddc7a-b072-4e05-b343-6ad7d7127d30.png)

## Soal 4
Temukan paket mysql yang mengandung perintah query select!

Jawab 4

## Soal 5
Login ke `portal.ichimarumaru.tech` kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file `.pcap`!

Jawab 5

## Soal 6
Cari username dan password ketika melakukan login ke FTP Server!

Jawab 6

## Soal 7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya `Real.pdf`)

Display Filter : `ftp-data contains "Real.pdf"`

![image](https://user-images.githubusercontent.com/31863229/134383683-53652a05-3eb0-48d4-8d8a-ed30483f46a0.png)

Klik kanan lalu pilih Follow > TCP Stream, ubah tipe Raw dan Save As dengan nama `Real.zip`.

![image](https://user-images.githubusercontent.com/31863229/134383719-7f32f327-e44c-46a3-a69d-127d5b98b11d.png)

Lakukan unzip `Real.zip` dan buka `Real.pdf`.

![image](https://user-images.githubusercontent.com/31863229/134383764-9f8a252e-4266-4137-9304-30b8e58c1fd1.png)

## Soal 8
Cari paket yang menunjukan pengambilan file dari FTP tersebut!

Display Filter : `ftp.request.command contains "STOR"`

![image](https://user-images.githubusercontent.com/31863229/134385345-1be60bb7-6691-4cb1-9a97-75c659644e82.png)

## Soal 9
Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama `secret.zip`. Simpan dan buka file tersebut!

Display Filter : `ftp-data.command contains "secret.zip"`

![image](https://user-images.githubusercontent.com/31863229/134388533-79731a89-5c37-409d-9404-198e6e9dba00.png)

Klik kanan lalu pilih Follow > TCP Stream, ubah tipe Raw dan Save As dengan nama `secret.zip`.

![image](https://user-images.githubusercontent.com/31863229/134388566-98e3b4a4-6f74-4610-a5ab-afa0756f9e22.png)

Password dibutuhkan untuk mengekstrak `secret.zip`.

![image](https://user-images.githubusercontent.com/31863229/134388613-bda12dc4-db57-453c-89a0-7b21b033cd16.png)

## Soal 10
Selain itu terdapat `history.txt` yang kemungkinan berisi history bash server tersebut! Gunakan isi dari `history.txt` untuk menemukan password untuk membuka file rahasia yang ada di `secret.zip`!

Display Filter : `ftp-data.command contains "history.txt"`

![image](https://user-images.githubusercontent.com/31863229/134389002-cbe05e02-cb7a-422e-8438-af8ab5ab2c2d.png)

Klik kanan lalu pilih Follow > TCP Stream, dapat dilihat bahwa password dari file `Wanted.pdf` yang ada di dalam `secret.zip` berada pada `bukanapaapa.txt`.

![image](https://user-images.githubusercontent.com/31863229/134389046-9ae5ca36-ec36-43ff-84a1-783df5dfa497.png)

Display Filter : `ftp-data.command contains "bukanapaapa.txt"`

![image](https://user-images.githubusercontent.com/31863229/134389083-b7a33d2c-b4ea-4961-8826-777e7286bb0c.png)

Klik kanan lalu pilih Follow > TCP Stream, dapat dilihat bahwa password dari file `Wanted.pdf` adalah `d1b1langbukanapaapajugagapercaya`.

![image](https://user-images.githubusercontent.com/31863229/134389118-7fd21f13-3d5b-4caf-b747-4b7fe932333b.png)

Lakukan unzip `secret.zip` dan buka `Wanted.pdf`.

![image](https://user-images.githubusercontent.com/31863229/134389173-34042064-f067-4836-b770-1b7bd852eedf.png)

## Soal 11
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

Jawab 11

## Soal 12
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

Jawab 12

## Soal 13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

Jawab 13

## Soal 14
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!

Jawab 14

## Soal 15
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Jawab 15
