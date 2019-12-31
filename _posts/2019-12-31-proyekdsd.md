---
layout: post
title: proyek dsd ++++
---

Pada tanggal 30 Desember 2019, gua dan kelompok DSD yang terdiri Suhe, Cici, dan Hanz mempresentasikan proyek akhir kami yang merupakan lampu lalu lintas. Fitur yang dimiliki lampu lalu lintas ini adalah:

1. _Countdown_ dari 9 ke 0
2. Lampu kuning dari 3 ke 0
3. _Shift_ lampu merah ke lampu hijau

![rangkaian](/images/rangkaian.jpg "Rangkaian DSD")

Rangkaian _clock_ menggunakan _astable multivibrator_ dengan kombinasi resistor 680K dan 100K juga kapasitor 1uF dan 10nF. _Duty cycle_ yang didapat di atas 52.8%.

Ceritanya aing gabut, jadi pengen nambahin fitur lanjutan supaya lampu lalu lintasnya lebih realistis. Heheheh.

Fitur yang ingin gua tambahkan di sini adalah:

1. _Countdown_ yang berbeda per lampu,
2. Lampu kuning yang juga menyala ketika lampu hijau akan menyala dan sebaliknya,
3. _Clock_ 1Hz (bener-bener 1Hz kondisi ideal pake _dpulse_ bawaan Proteus),
4. Untuk perempatan jalan :)
5. text saat lampu merah karena nggak terbatas biaya yang bisa dipakai HAHAHAHA 

## 1. Countdown yang berbeda per lampu (31 Desember 2019)

kali ini gua pengen bikin rangkaian digital pertama untuk lampu merah/hijau. Di sini, gua membuat rangkaian _countdown_ 50 detik (49 ke 0, lupa eh bikin dari 50 jadi beda :( ) menggunakan D flip-flop dan counter 74192 (karena saya malas membuat counter JK flipflop hehehe). Ini skematik sementara untuk rangkaian counter down 50 detik.

![rangkaian lampu hijau/merah](/images/oklol.jpg "kalo gua nulis ini kalian baca ga ya? harus hover mouse dulu woi")

Rangkaian ini dibuat menggunakan 4 D flipflop (menggunakan Karnaugh Map 4x4) dengan BCD, sehingga 10-15 merupakan _don't care_. Oh ya, adanya _logic probe_ di kiri bawah itu buat ngecek pulse yang keluar tuh bener dari 0100 ke 0000 atau tidak ya, gengs. Di sini juga gua menggunakan _7 Segment Display_ dengan _Common Anode_.



