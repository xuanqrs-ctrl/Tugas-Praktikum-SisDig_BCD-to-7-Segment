# Tugas Praktikum Sistem Digital: BCD to 7 Segment

## Deskripsi
Rangkaian ini mensimulasikan sistem digital yang mengonversi input data biner 4-bit berformat BCD menjadi sinyal pengendali visual pada *7-Segment Display*. Menggunakan **IC CD4511** (Decoder BCD-to-7-Segment), sistem mendeteksi input desimal dari angka `0` hingga `9`. Jika input melebihi batas BCD (yaitu biner `1010` hingga `1111`), IC secara otomatis akan mematikan seluruh segmen (*blanking*), karena kombinasi tersebut tidak valid dalam sistem pengodean BCD standar. 

## Anggota Kelompok
1. Iwa Kumara Alden (H1H025037)
2. Mohammad Naufal Asshidqi (H1H025041)
3. Edwin Alfian Barin (H1H025070)

## Dasar Teori

### 1. Binary Coded Decimal (BCD)
BCD merupakan sistem pengodean biner di mana setiap satu digit desimal (0-9) diwakili secara independen oleh 4 bit biner. Oleh karena itu, rentang nilai yang sah hanyalah biner `0000` (desimal 0) hingga `1001` (desimal 9). 

### 2. Decoder IC CD4511
IC CD4511 adalah decoder CMOS latch/decoder/driver BCD-ke-7-segmen. IC ini dirancang khusus untuk menggerakkan display tipe **Common Cathode** (Katoda Umum). Tiga pin kontrol penting pada IC ini meliputi:
* **Lamp Test :** Aktif LOW. Harus dihubungkan ke VCC (HIGH) untuk operasi normal. Jika diberi LOW, semua segmen display dipaksa menyala untuk pengujian LED.
* **Blanking Input :** Aktif LOW. Harus dihubungkan ke VCC (HIGH) untuk operasi normal. Jika diberi LOW, display akan mati total (*blank*).
* **Latch Enable :** Aktif HIGH. Dihubungkan ke GND (LOW) agar data input langsung diteruskan ke output tanpa dikunci (*latch*).

### 3. 7-Segment Display (Common Cathode)
Pada display tipe *Common Cathode*, seluruh kaki katoda (negatif) dari struktur LED internal dihubungkan menjadi satu pin tunggal (COM) menuju Ground (GND). Agar segmen tertentu (a-g) dapat menyala, pin anoda segmen tersebut harus menerima logika **HIGH** (+5V) dari output IC CD4511.


## Komponen Yang Digunakan
* **1x DIP Switch (4-bit)**: Sebagai input BCD 4-bit.
* **1x IC CD4511**: BCD to 7-Segment Decoder.
* **1x 7-Segment Display**: Tipe Common Cathode untuk output tampilan angka.
* **4x Resistor 1 kΩ**: Sebagai pull-down untuk input DIP Switch.
* **1x Power Supply 5V**: Sumber tegangan rangkaian.
* **Kabel Jumper**: Koneksi antar komponen (Merah untuk VCC, Hitam untuk GND).

## Tautan Rangkaian Tinkercad
* https://www.tinkercad.com/things/66ZQhb7BxoC-bcd-to-7-segment?sharecode=9ZvrhMPsqTDm4qhhmhiIXLoa0HyLt2dvvup24VMkChc
