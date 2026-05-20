# Tugas Praktikum Sistem Digital: BCD to 7 Segment

## Deskripsi
Rangkaian ini mensimulasikan sistem digital yang mengonversi input data biner 4-bit berformat BCD menjadi sinyal pengendali visual pada *7-Segment Display*. Menggunakan **IC CD4511** (Decoder BCD-to-7-Segment), sistem mendeteksi input desimal dari angka `0` hingga `9`. Jika input melebihi batas BCD (yaitu biner `1010` hingga `1111`), IC secara otomatis akan mematikan seluruh segmen (*blanking*), karena kombinasi tersebut tidak valid dalam sistem pengodean BCD standar. 

## Anggota Kelompok
1. Iwa Kumara Alden (H1H025037)
2. Mohammad Naufal Asshidqi (H1H025041)
3. Edwin Alfian Barin (H1H025070)

## Komponen Yang Digunakan
* **1x DIP Switch (4-bit)**: Sebagai input BCD 4-bit.
* **1x IC CD4511**: BCD to 7-Segment Decoder.
* **1x 7-Segment Display**: Tipe Common Cathode untuk output tampilan angka.
* **4x Resistor 1 kΩ**: Sebagai pull-down untuk input DIP Switch.
* **1x Power Supply 5V**: Sumber tegangan rangkaian.
* **Kabel Jumper**: Koneksi antar komponen (Merah untuk VCC, Hitam untuk GND).

## Tautan Rangkaian Tinkercad
* https://www.tinkercad.com/things/66ZQhb7BxoC-bcd-to-7-segment?sharecode=9ZvrhMPsqTDm4qhhmhiIXLoa0HyLt2dvvup24VMkChc
