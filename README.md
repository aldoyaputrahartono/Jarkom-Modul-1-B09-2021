# Jarkom-Modul-1-B09-2021

Repositori Praktikum Jarkom Modul 1

|NRP           |Nama                   |
|:------------:|:---------------------:|
|05111940000084|Aldo Yaputra Hartono   |
|05111940000092|Maximilian H M Lingga  |
|05111840000023|Izzulhaq Fawwaz Syauqiy|

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

Kelanjutan dari Soal 2, buka bagian Authorization. Pada Credentials didapatkan username dan password.

Username : `kuncimenujulautan`

Password : `tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN`

![image](https://user-images.githubusercontent.com/31863229/134381764-703c1dd6-6e75-4de2-95a0-d1f1b0fec31f.png)

Login ke `basic.ichimarumaru.tech` dan kerjakan soalnya.

![image](https://user-images.githubusercontent.com/31863229/134382261-1c8ddc7a-b072-4e05-b343-6ad7d7127d30.png)

Jawaban : `g G o B b O br BR`

## Soal 4
Temukan paket mysql yang mengandung perintah query select!

Display Filter : `mysql.query matches "SELECT"`

![image](https://user-images.githubusercontent.com/31863229/134556112-e40efcf7-85e7-412b-97c0-7524454679be.png)

## Soal 5
Login ke `portal.ichimarumaru.tech` kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file `.pcap`!

Display Filter : `mysql.query.contains "INSERT"`

![image](https://user-images.githubusercontent.com/57482751/134452546-4db74ce8-3fc6-4f6b-a20b-1e1960a1ff4f.png)

Username : `akakanomi`

Password : `pemisah4lautan`

Login ke `portal.ichimarumaru.tech` dan kerjakan soalnya.

![image](https://user-images.githubusercontent.com/57482751/134452526-6f1a1ff3-2ef2-4794-b366-5ec8c423765e.png)

Jawaban : `o O g B b G br BR`

## Soal 6
Cari username dan password ketika melakukan login ke FTP Server!

Display Filter : `ftp.request.command == "USER" or ftp.request.command == "PASS"`

![image](https://user-images.githubusercontent.com/57482751/134452566-af569f50-406a-4f4b-aad6-602c5ddd2455.png)

Username : `secretuser`

Password : `aku.pengen.pw.aja`

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

Display Filter : `ftp.request.command contains "RETR"`

![image](https://user-images.githubusercontent.com/31863229/134556251-9dea72ea-1ee3-4503-b15c-64cbaf195eaf.png)

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

Capture Filter : `src port 80`

![image](https://user-images.githubusercontent.com/31863229/134389942-02a6d3c2-cbe8-4e02-ba92-ef890c7645d0.png)

## Soal 12
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

Capture Filter : `port 21`

![image](https://user-images.githubusercontent.com/31863229/134390043-f3b4c6ea-a2a0-4a98-a7dd-2fb2619bafdd.png)

## Soal 13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

Capture Filter : `dst port 443`

![image](https://user-images.githubusercontent.com/31863229/134390089-96b4c808-dcc3-467e-a169-43c2a791053d.png)

## Soal 14
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!

Capture Filter : `dst host kemenag.go.id`

![image](https://user-images.githubusercontent.com/31863229/134390163-7ead92ea-8bed-4560-ac40-be3bb67d918f.png)

## Soal 15
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

Ambil ip masing-masing dengan `ipconfig` pada command prompt. Karena saya memakai wifi, maka didapatkan ip `192.168.64.62`.

![image](https://user-images.githubusercontent.com/31863229/134390196-9b709358-4dc1-48ea-a244-f030ec14a099.png)

Capture Filter : `ip src 192.168.64.62`

![image](https://user-images.githubusercontent.com/31863229/134390235-1c944e27-0624-44fb-9e6b-c768c948d8dc.png)

## Kendala
1. Pada soal 4, filter `contains` bersifat case-sensitive sehingga harus menggunakan filter `matches` untuk mendapatkan query `select` dan `SELECT`.
2. Pada soal 8, pengambilan file seharusnya menggunakan `RETR`. Akan tetapi tidak ada packet yang ditangkap sehingga kami mengira terdapat typo pada soal karena saat menggunakan `STOR` tertangkap 3 paket.

## Pembagian Tugas
|Nama                   |Soal   |
|:---------------------:|:-----:|
|Maximilian H M Lingga  |1 - 5  |
|Izzulhaq Fawwaz Syauqiy|6 - 10 |
|Aldo Yaputra Hartono   |11 - 15|
