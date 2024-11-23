# Panduan Installasi  

## Sistem yang Dibutuhkan  

Walaupun menggunakan model **client-server**, SIMRS Khanza dapat diinstal pada satu komputer untuk keperluan ujicoba atau jika jumlah komputer terbatas dan jaringan tidak tersedia.  
Untuk kebutuhan server dan client, berikut spesifikasi minimum:  

### Server  
1. **Sistem Operasi:** Windows, Linux, atau macOS (32-bit maupun 64-bit).  
2. **Webserver:** Apache dengan dukungan PHP.  
3. **Database Server:** MySQL, MariaDB, atau Percona.  
4. **Versi PHP:** 7.x atau sesuai dengan rekomendasi aplikasi.  

### Client  
1. **Sistem Operasi:** Windows, Linux, atau macOS (32-bit maupun 64-bit).  
2. **Java JRE:** Sesuai dengan arsitektur sistem operasi.  

---

## Alamat Unduh  

**Aplikasi dan Sumber Data:**  
👉 [Download SIMRS KhanzaHMS](https://drive.google.com/drive/folders/0ByL--Jg6bdF7RG1NSlVTT2ZPODg)  
👉 [GitHub SIMRS Khanza](https://github.com/mas-elkhanza/SIMRS-Khanza)  

---

## Instalasi Server  

1. **Pastikan Kompatibilitas Sistem:**  
   Verifikasi arsitektur sistem operasi dan software pendukung yang akan digunakan.  

2. **Instalasi Webserver dan Database:**  
   - Gunakan bundle software seperti [XAMPP](https://www.apachefriends.org/download.html), yang mencakup Apache, PHP, dan MySQL, atau instal masing-masing secara manual.  
   - Pilih versi yang sesuai dengan sistem operasi Anda.  

3. **Persiapan Database:**  
   - Unduh file database `sik.sql` dari [GitHub SIMRS Khanza](https://github.com/mas-elkhanza/SIMRS-Khanza).  
   - Buka aplikasi seperti **HeidiSQL** atau **phpMyAdmin**.  
   - Buat database baru bernama `sik`.  
   - Impor file `sik.sql` ke database `sik`. Tunggu hingga proses impor selesai.  

4. **Penempatan Folder WebApps:**  
   - Unduh folder `webapps` dari [GitHub SIMRS Khanza](https://github.com/mas-elkhanza/SIMRS-Khanza).  
   - Salin folder `webapps` ke direktori publik webserver Anda:  
     - Jika menggunakan **WAMP**, letakkan di `wamp/www`.  
     - Jika menggunakan **XAMPP**, letakkan di `xamp/htdocs`.  

5. **Pengaturan Database:**  
   - Buka file konfigurasi di **setting/database.xml** atau **setting/database.ini**.  
   - Sesuaikan pengaturan koneksi database (username, password, host).  

6. **Pengaturan WebApps:**  
   - Pastikan folder dan file webapps dapat diakses melalui browser.  
   - Periksa konfigurasi untuk memastikan aplikasi terhubung dengan database.  

---

## Instalasi Client  


1. **Install Java Runtime Environment (JRE):**  
   Pastikan menginstal JRE sesuai dengan versi Windows Anda (32-bit atau 64-bit).  

2. **Install XAMPP:**  
   Instal XAMPP untuk menjalankan database dan server lokal.  

3. **Import Database:**  
   - Buka **HeidiSQL**, pilih **New**, klik **OK**, lalu klik **Connect**.  
   - Buat database baru dengan nama `sik` melalui menu **Tools → Create Database**.  
   - Klik nama database `sik` di panel kiri.  
   - Pilih menu **Import → Load SQL File**, cari file `sik.sql`, lalu klik tombol **Execute** (tanda segitiga ke kanan).  
   - Jika terjadi kendala, buka file `sik.sql` dengan Notepad, salin seluruh isinya, tempelkan ke tab **SQL** di HeidiSQL, lalu klik **Execute**.  

4. **Tempatkan Folder WebApps:**  
   - Jika menggunakan **WAMP**, letakkan folder **webapps** di `wamp/www`.  
   - Jika menggunakan **XAMPP**, letakkan folder **webapps** di `xamp/htdocs`.  
   - Disarankan menggunakan versi XAMPP yang disertakan.  

5. **Menjalankan Software:**  
   - Klik dua kali file **Aplikasi.bat** untuk menjalankan Software Khanza HMS.  
   - Klik dua kali file **AntrianLoket.bat** untuk menjalankan Software Antrian Loket.  
   - Klik dua kali file **AntrianPoli.bat** untuk menjalankan Software Antrian Poli.  

6. **Membuat Shortcut:**  
   - Buat shortcut dari file **Aplikasi.bat**, lalu letakkan di desktop agar lebih mudah diakses.  
   - Jika aplikasi tidak berjalan, coba jalankan file **khanza.jar** dengan klik dua kali.  

7. **Pengaturan Client-Server:**  
   - Buka file **setting/database.xml** atau **setting/database.ini**.  
   - Ganti `localhost` dengan **IP Server** Anda.  
   - Pastikan pengaturan hak akses (privileges) di database server telah diatur.  

8. **Mengaktifkan Aplikasi Presensi via Fingerprint:**  
   - Gunakan hardware **Digital Persona U Are U 4500**.  
   - Konfigurasikan file **setting/database.ini** untuk device, verification, activation, dan working in background sesuai spesifikasi perangkat fingerprint.  
   - Instal file **FlexCodeSDK.exe** dan driver yang disertakan di folder **setting**.  
   - Klik **presensi.exe** untuk menjalankan aplikasi presensi.  

---

## Panduan Belajar  

Tersedia panduan belajar melalui channel YouTube:  
👉 [SIMRS Khanza Indonesia - YouTube Channel](https://www.youtube.com/@simrskhanzaindonesia)
👉 [SIMRS Khanza - YouTube Channel](https://www.youtube.com/channel/UC6318L_Z_lXVwuQe331C2iw)  (**Depricated**)
