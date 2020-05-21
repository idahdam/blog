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
5. Teks saat lampu merah karena nggak terbatas biaya yang bisa dipakai HAHAHAHA 

Sejauh ini, rangkaian terakhir (1 Desember 2019) udah sampe sini:

![rangkaian full](/images/11111.jpg "anjinggg mantep jg")

> Peringatan
>> Proteus ini nggak memperhitungkan arus SEBENARNYA yang melalui rangkaian ataupun IC. Kalau kalian tetap ingin mengaplikasikan proyek ini ke atas _breadboard_ atau _protoboard_, kalian tetep harus menggunakan multimeter, resistor, serta _datasheet_ untuk memastikan nggak ada arus yang melewati sebuah rangkaian melewati kapasitasnya. trims.

## _Countdown_ yang berbeda per lampu (31 Desember 2019)

kali ini gua pengen bikin rangkaian digital pertama untuk lampu merah/hijau. Di sini, gua membuat rangkaian _countdown_ 50 detik (49 ke 0, lupa eh bikin dari 50 jadi beda :( ) menggunakan D flip-flop dan counter 74192 (karena saya malas membuat counter JK flipflop hehehe). Ini skematik sementara untuk rangkaian counter down 50 detik.

![rangkaian lampu hijau/merah](/images/oklol.jpg "kalo gua nulis ini kalian baca ga ya? harus hover mouse dulu woi")

Rangkaian ini dibuat menggunakan 4 D flipflop (menggunakan Karnaugh Map 4x4) dengan BCD, sehingga 10-15 merupakan _don't care_. Oh ya, adanya _logic probe_ di kiri bawah itu buat ngecek pulse yang keluar tuh bener dari 0100 ke 0000 atau tidak ya, gengs. Di sini juga gua menggunakan _7 Segment Display_ dengan _Common Anode_.

Rangkaian ini gua bikin untuk perempatan jalan, dengan analogi arah kompas utara-selatan-timur-barat. bila lampu hijau berada pada utara dan selatan, lampu merah untuk timur dan barat. Awalnya, gua berpikir untuk memberikan jumlah waktu yang berbeda untuk tiap-tiap lampu, namun setelah gua lakukan, terdapat ketidaksinkronan perubahan lampu yang dapat menyebabkan kecelakaan.

## Lampu kuning menyala pada saat lampu merah/hijau menyala menuju pergantian hijau/merah & untuk perempatan jalan

Oke, lampu kuning dibuat berdasarkan 2 hal

1. Ketika satuan bergerak dari 5 ke 0, dan
2. Ketika puluhan berada pada posisi 0

Kondisi yang dipenuhi di sini adalah AND, oleh karena itu haruslah dibentuk AND dari 1 dan 2. Untuk satuan, ketika counting dari 5 ke 0, akan men- _trigger_ hasil keluaran menjadi 1 dan untuk puluhan akan men- _trigger_ ketika bernilai 0000.

## TEKS KETIKA GERAK HADOOOO _WAY TOO MUCH TO DO_ BGT DI

Santui, gua pengen bikin ini emang karena gua gabut aja. 

2 kalimat yang ingin gua gunakan ketika lampu merah dan lampu hijau adalah:
- Hati-hati (9 karakter)
- Met jalan (9 karakter)

Di sini, gua akan menggunakan satu hal yang jarang digunakan di projek sederhana seperti ini, yaitu 14 _Segment Display_. Tapi karena _its too much_, gua lanjutin lain hari aja ya. Hehehe. Sekian.



