# Clock

/*
=====================================================================
Program Jam Digital IoT dengan ESP8266 + LCD I2C
=====================================================================

Program ini menggunakan modul ESP8266 untuk mengambil data waktu 
(real-time) dari server NTP (Network Time Protocol) melalui internet. 
Data waktu kemudian ditampilkan pada LCD I2C (16x2) dalam format jam, 
hari, dan tanggal.

Konfigurasi Perangkat:
- ESP8266 terhubung ke WiFi (SSID & password diatur di variabel).
- LCD I2C (alamat 0x27, ukuran 16x2) untuk menampilkan waktu dan tanggal.

Fitur Utama:
1. **Koneksi WiFi**
   - ESP8266 terhubung ke jaringan WiFi dengan SSID & password yang 
     ditentukan di variabel `ssid` dan `password`.

2. **Sinkronisasi Waktu dengan NTP**
   - Menggunakan server `pool.ntp.org`.
   - Mengatur offset waktu sesuai zona GMT+7 (WIB) → `25200` detik.

3. **Tampilan LCD**
   - Baris pertama: jam dalam format `HH:MM:SS`, ditambah simbol "<< >>".
   - Baris kedua: nama hari + tanggal lengkap (`Hari-YYYY-MM-DD`).

4. **Debug Serial**
   - Menampilkan waktu, hari, bulan, tahun, serta epoch time di Serial Monitor 
     untuk kebutuhan debugging.

Tujuan:
- Membuat jam digital berbasis IoT yang selalu sinkron dengan waktu server.
- Menampilkan informasi waktu real-time di LCD I2C secara akurat.
- Memberikan dasar sistem monitoring atau logger yang membutuhkan waktu presisi.

=====================================================================
*/
