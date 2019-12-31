---
layout: post
title: proyek dsd ++++
---

Pada tanggal 30 Desember 2019, gua dan kelompok DSD yang terdiri Suhe, Glory, dan Hanz mempresentasikan proyek akhir kami yang merupakan lampu lalu lintas. Fitur yang dimiliki lampu lalu lintas ini adalah:

1. _Countdown_ dari 9 ke 0
2. Lampu kuning dari 3 ke 0
3. _Shift_ lampu merah ke lampu hijau

![rangkaian](/images/rangkaian.jpg "Rangkaian DSD")

Rangkaian _clock_ menggunakan _astable multivibrator_ dengan kombinasi resistor 680K dan 100K juga kapasitor 1uF dan 10nF. _Duty cycle_ yang didapat di atas 52.8%

Fitur yang ingin gua tambahkan di sini adalah:

1. _Countdown_ yang berbeda per lampu
2. Lampu kuning yang juga menyala ketika lampu hijau akan menyala dan sebaliknya
3. _Clock_ 1Hz (bener-bener 1Hz kondisi ideal pake pulse bawaan Proteus)
4. Untuk perempatan jalan :)
5. text saat lampu merah karena nggak terbatas biaya yang bisa dipakai HAHAHAHA 

## 1. Countdown yang berbeda per lampu

kali ini gua pengen bikin rangkaian digital pertama untuk lampu merah/hijau. Di sini, gua membuat rangkaian _countdown_ 50 detik menggunakan D flip-flop dan counter 74192 (karena saya malas membuat counter JK flipflop hehehe). Ini skematik sementara untuk rangkaian counter down 50 detik.

![rangkaian lampu hijau/merah](/images/oklol.bmp "kalo gua nulis ini kalian baca ga ya? harus hover mouse dulu woi")

