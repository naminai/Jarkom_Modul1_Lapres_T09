# Jarkom Modul1 Lapres T09
Anggota Kelompok:  
- Donny Kurnia Ramadhani     (05311840000004)  
- Muhammad Zulfikar Fauzi    (05311840000012)

---
### A. Display Filter
__1.__ Sebutkan webserver yang digunakan pada "testing.mekanis.me"!  
Penyelesaian:  
Filter: __http contains "testing.mekanis.me"__
![image](https://user-images.githubusercontent.com/61267430/96320201-e53c9600-103b-11eb-8f04-41c53389b809.png)  
Kemudian kita follow TCP Stream, dan kita dapatkan web servernya yaitu nginx/1.14.0
![image](https://user-images.githubusercontent.com/61267430/96320270-26cd4100-103c-11eb-8cec-caeb098b20a8.png)  

__2.__ Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!  
Penyelesaian:  
Filter: __http contains "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"__  
![image](https://user-images.githubusercontent.com/61267430/96320516-c7bbfc00-103c-11eb-8972-507b5e28f84f.png)
Kita double click untuk mendapatkan detail paket tersebut, dan cari di bagian cookie untuk mendapatkan Full Request URI-nya
![image](https://user-images.githubusercontent.com/61267430/96320596-0651b680-103d-11eb-90b3-8d54efe8fbe3.png)
Full Request URI kita klik 2 kali untuk kemudian mengantarkan kita pada gambar yang kita cari, dan kita simpan
![image](https://user-images.githubusercontent.com/61267430/96320710-5af53180-103d-11eb-8c6f-26fdf0f61b3d.png)  

__3.__ Cari username dan password ketika login di "ppid.dpr.go.id"!  
Penyelesaian:  
Filter: __http.host == "ppid.dpr.go.id" && http.request.method == POST__  
![image](https://user-images.githubusercontent.com/61267430/96320869-cb03b780-103d-11eb-9cc6-40c4466de262.png)  
Kita double klik untuk mendapatkan detail paket. Lalu kita dapatkan pada bagian HTML Form URL Encoded  
Username: 10pemuda  
Password: guncangdunia
![image](https://user-images.githubusercontent.com/61267430/96321062-5aa96600-103e-11eb-98ae-491d08a50ae4.png)  

__4.__ Temukan paket dari web-web yang menggunakan basic authentication method!  
Penyelesaian:  
Filter: __http.authbasic__  
Kita dapatkan paket-paketnya.
![image](https://user-images.githubusercontent.com/61267430/96321168-a0662e80-103e-11eb-9328-206b9b1726d8.png)  

__5.__ Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!  
Penyelesaian:  
Filter: __http.host == "aku.pengen.pw" && http.request.method == GET__  
![image](https://user-images.githubusercontent.com/61267430/96321254-e6bb8d80-103e-11eb-8b1f-6cbec2c43d85.png)    
Lalu kita double click untuk mendapatkan detail paket  
![image](https://user-images.githubusercontent.com/61267430/96321386-66495c80-103f-11eb-9f5d-069c045cae24.png)  
Kita kemudian masuk, namun ternyata diperlukan kredensial untuk masuk.  
![image](https://user-images.githubusercontent.com/61267430/96321314-2d10ec80-103f-11eb-878d-3526c950b7b0.png)  
Kita dapatkan kredensialnya dengan mengikuti paket kedua  
![image](https://user-images.githubusercontent.com/61267430/96321447-a9a3cb00-103f-11eb-93a3-c611523600ed.png) 
Kita masukkan kredensialnya 
![image](https://user-images.githubusercontent.com/61267430/96321563-14550680-1040-11eb-9fd6-72f5daebeec7.png)
Kita jawab pertanyaan yang ada pada aku.pengen.pw  
![image](https://user-images.githubusercontent.com/61267430/96321640-66962780-1040-11eb-9afc-0cd94176aa14.png)

__6.__ Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).  
Penyelesaian:  
Filter: __ftp-data__  
![image](https://user-images.githubusercontent.com/61267430/96321747-bd9bfc80-1040-11eb-8450-10b93242d229.png)  
Kita Follow TCP Stream dari paket paling atas dan kita simpan. (Tidak lupa save data as raw agar bisa di-save dalam bentuk asli).  
![image](https://user-images.githubusercontent.com/61267430/96321899-3f8c2580-1041-11eb-9cca-c0819744c6f7.png)  
Lalu kita dapatkan password dari zipkey.txt (sudah terlihat pada pencarian paket ftp-data yang awal).  
![image](https://user-images.githubusercontent.com/61267430/96321955-72ceb480-1041-11eb-9d9f-13b4e1e29aa9.png)  
Kita masukkan passwordnya dan kita dapatkan isinya.  
![image](https://user-images.githubusercontent.com/61267430/96321998-9b56ae80-1041-11eb-875f-e9acdfa3a486.png)  

__7.__ Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"  
Penyelesaian:  
Filter: __ftp-data contains “Yes.pdf”__  
![image](https://user-images.githubusercontent.com/61267430/96322087-ee306600-1041-11eb-9d43-e3e894951cc1.png)  
Kemudian kita Follow TCP Stream, Save data as Raw dan kita simpan sebagai 473.zip  
![image](https://user-images.githubusercontent.com/61267430/96322127-13bd6f80-1042-11eb-91ce-d800399b4b1c.png)  
Kita buka Yes.pdf dalam 473.zip dan kita dapatkan isinya.
![image](https://user-images.githubusercontent.com/61267430/96322189-4bc4b280-1042-11eb-8a80-e32280916ec7.png)  

__8.__ Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!  
Penyelesaian:  
Filter: __ftp-data && host 198.246.117.106__  
Pada awalnya kita hanya menggunakan filter `ftp-data`, namun ternyata data ftp yang disimpan tidak hanya dalam Microsoft FTP Service melainkan terdapat pula data-data lainnya. Maka kita menggunakan ip host yang kita temukan sebagai Microsoft FTP Service.
![image](https://user-images.githubusercontent.com/61267430/96322428-3d2acb00-1043-11eb-8992-c5d7c2f6083c.png)  

__9.__ Cari username dan password ketika login FTP pada localhost!  
Penyelesaian:  
Filter: __ftp contains USER || ftp contains PASS__  
![image](https://user-images.githubusercontent.com/61267430/96322483-706d5a00-1043-11eb-9180-ab086bc8b3a9.png)

__10.__ Cari file .pdf di wireshark lalu download dan buka file tersebut!  
clue: "25 50 44 46"  
Penyelesaian:  
Filter: __http contains “.pdf”__  
![image](https://user-images.githubusercontent.com/61267430/96322552-bc200380-1043-11eb-91c4-38f06998df57.png)  
Kita temukan dan kita double click untuk mendapatkan URI dari file pdf yang kita cari.  
![image](https://user-images.githubusercontent.com/61267430/96322746-8596b880-1044-11eb-9266-fb464262ee63.png)  
Kita dapatkan dan download. Kemudian kita buka file tersebut dan kita dapatkan sesuai gambar di bawah ini.
![image](https://user-images.githubusercontent.com/61267430/96322671-305aa700-1044-11eb-9f3a-847e3b1c47bc.png)  

---
### B. Capture Filter  
__11.__ Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!  
Penyelesaian:  
Filter:  __port 21__  
![image](https://user-images.githubusercontent.com/61267430/96322957-4d43aa00-1045-11eb-96b6-4165a28b4ccd.png)

__12.__ Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!  
Penyelesaian:  
Filter:  __src port 80__  
![image](https://user-images.githubusercontent.com/61267430/96322978-62203d80-1045-11eb-957c-08dc2aeedf73.png)  

__13.__ Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!  
Penyelesaian:  
Filter: __dst port 443___  
![image](https://user-images.githubusercontent.com/61267430/96323213-584b0a00-1046-11eb-8c64-0991f34a473d.png)  

__14.__ Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!  
Penyelesaian:  
Filter: __src [ip sendiri] dalam kasus ini “src 192.168.1.4”__  
Kita dapatkan ip kita sendiri dengan menggunakan command `ipconfig`
![image](https://user-images.githubusercontent.com/61267430/96322998-80863900-1045-11eb-9a25-a6219ac29ebf.png)  
Lalu kita filter.  
![image](https://user-images.githubusercontent.com/61267430/96323062-ce02a600-1045-11eb-837b-58cb92c9050b.png)  

__15.__ Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!  
Penyelesaian:  
Filter: __dst 103.94.190.11__  
Pertama-tama kita dapatkan ip dari monta.if.its.ac.id dengan command `ping`  
![image](https://user-images.githubusercontent.com/61267430/96323110-fee2db00-1045-11eb-9d8d-1a869589e68d.png)  
Lalu kita filter.  
![image](https://user-images.githubusercontent.com/61267430/96323187-3ea9c280-1046-11eb-8a6a-6f7e6a362f2b.png)
