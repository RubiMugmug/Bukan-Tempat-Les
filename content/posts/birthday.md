---
title: "Keajaiban Ulang Tahun Hololive"
date: 2023-01-03T14:03:37+01:00
tags: ["Matematika", "Level SMA", "Peluang", "Statistika", "Wibu", "Vtuber" , "Ulang Tahun"]
---

Halo kawan-kawan *wibu* dan *non-wibu*.
Saya Rubio, mahasiswa matematika dan wibu pengamat *vtuber*.
Pertama, saya mau mengucapkan selamat Tahun Baru 2023.
Semoga di tahun ini kalian bisa melihat dunia yang penuh hal-hal menarik.
Penuh dengan keluarga, teman, vtuber, dan mungkin juga matematika.

Kali ini saya menulis tentang sebuah bilangan yang menarik, dan kaitannya dengan ulang tahun vtuber Hololive.

# Dua Puluh Tiga
Saya punya fakta yang menarik tentang bilangan 23.
Jika 23 orang dipilih secara acak, ada peluang sekitar 50% setidaknya dua dari mereka memiliki tanggal ulang tahun yang saling bertepatan.

Fakta ini dikenal sebagai *Birthday Paradox*. Jika anda sudah kenal dengan fakta ini, anda boleh loncat ke bagian berikutnya. Jika belum, gambaran kasar dari buktinya ada di bagian ini.

### Perhitungan Peluang: *Sanity Check*

Untuk sebagian orang, mungkin fakta ini terdengar mengejutkan. Memang mengejutkan, makanya ia disebut paradoks.
23 orang tampaknya jauh lebih sedikit daripada 366 hari, tapi bagaimana mungkin peluang ini mencapai 50%?

Kebanyakan orang mungkin akan terkejut karena membayangkan dua soal yang berbeda ketika mendengar fakta tersebut. Saya pribadi membayangkan dua soal berikut:

**A**. Jika 23 orang dipilih secara acak, berapakah peluang "**ada pasangan orang** yang memiliki tanggal ulang tahun yang **saling bertepatan**" ? 

Ini adalah soal utama yang ingin kita jawab.

**B**. Jika 23 orang dipilih secara acak, berapakah peluang "**ada orang** yang memiliki tanggal ulang tahun yang bertepatan **dengan tanggal ulang tahunmu**" ? 

Adalah soal jebakan yang mungkin muncul di pikiran kita. Ini bukanlah soal yang *salah*, tapi bukan ini soal yang kita bicarakan. Sekarang, kedua soal tersebut akan kita kupas.

*Untuk mempermudah perhitungan, kita akan mengasumsikan peluang seseorang lahir di tanggal 29 Februari sama dengan tanggal lain, meski nyatanya tidak begitu.
Anda boleh mencoba mencari cara yang lebih akurat, namun hasil akhirnya tidak akan jauh berbeda.*

*Ini Bukan Tempat Les, tidak ada nilai ujian atau nilai PR yang perlu dikhawatirkan di sini.
Lagipula, inti dari cerita ini masih sama.*

Mari kita mulai dari soal B. Apabila kamu masuk ke ruangan yang ada 23 orang lain, peluang bahwa ada orang yang memiliki tanggal ulang tahun yang bertepatan dengan tanggal ulang tahunmu hanya 23/366, sekitar 6%. Di kasus ini, kamu membandingkan dirimu dengan 23 orang yang lain.

Kembali ke soal A. Sebelum melakukan perhitungan peluang untuk memperoleh jawaban sekitar 1/2, mari kita lihat secara sekilas berapa perbandingan yang terjadi. Saat kita membandingkan tanggal lahir, kita memilih 2 orang untuk dibandingkan. Ada berapa banyak cara untuk memilih 2 orang dari 23 orang? 

$$\binom{23}{2} = \frac{23!}{2!21!} = \frac{23 \cdot 22}{2} = 253$$

Artinya kita melakukan 253 perbandingan, ini adalah bilangan yang jauh lebih dekat dengan 365 daripada 22. Tentu jawaban akhirnya bukan 253/365, tapi sekarang setidaknya jawaban 1/2 terdengar masuk akal. 

Kita baru saja melakukan sebuah *sanity check*. Kita tidak mendapat jawaban dari soal A, melainkan sebuah perkiraan kasar yang mengkonfirmasi bahwa jawaban 1/2 masuk akal.

### Perhitungan Peluang: Komplemen dan Pola
Sekarang kita akan mencari jawaban soal A. Untuk itu, kita akan menghitung peluang dari komplemennya. Ini karena peluang dari suatu kejadian bisa diperoleh dari komplemennya, dan komplemen dari jawaban soal A lebih mudah untuk dihitung,

**C**. Jika *n* orang dipilih secara acak, berapakah peluang "**tidak ada** pasangan orang yang memiliki tanggal ulang tahun yang saling bertepatan?" 

Sekarang kita akan menjawab soal C dengan mengamati pola untuk 1,2, dan 3.

1. Apabila ada 1 orang, peluangnya 1. Sudah pasti tidak ada pasangan, karena hanya ada 1 orang, mana mungkin berpasangan. Kasihan dia kesepian 😢

2. Apabila kita tambahkan orang ke-2, peluang orang tersebut memiliki ulang tahun yang berbeda dengan orang ke-1 adalah:

    $$(366-1)/366 = 365/366$$

    Karena hanya ada 2 orang, 
    maka peluang "**tidak ada** pasangan orang yang memiliki tanggal ulang tahun yang saling bertepatan" juga 365/366

    Sehingga peluang "**ada** pasangan orang yang memiliki tanggal ulang tahun yang saling bertepata"n" adalah komplemennya,
    $$ 1 - 1/366$$

3. Apabila kita tambahkan orang ke-3, peluang orang tersebut memiliki ulang tahun yang berbeda dengan dua orang sebelumnya adalah

    $$(366-2)/366 = 364/366$$

    Sekarang kita cari peluang "**tidak ada** pasangan orang yang memiliki tanggal ulang tahun yang saling bertepatan". 
    Bisa kita peroleh dari
    "peluang orang ke-2 memiliki ulang tahun berbeda dengan orang ke-1", dan "orang ke-3 memiliki ulang tahun yang berbeda dengan dua orang sebelumnya".

    $$(365/366)(364/366)$$

    Sehingga peluang "**ada** pasangan orang yang memiliki tanggal ulang tahun yang saling bertepatan" adalah komplemennya,
    $$1 - (365/366)(364/366)$$

### Jawaban Akhir
Secara umum, jika *n* orang dipilih secara acak, peluang "**ada** pasangan orang yang memiliki tanggal ulang tahun yang saling bertepatan" adalah

$$1 - \left(\frac{366-1}{366}\right)
\left(\frac{366-2}{366}\right)
\left(\frac{366-3}{366}\right)...
\left(\frac{366-(n+1)}{366}\right)$$

Akhirnya kita bisa menjawab soal pertama, dengan bantuan 
[Google Sheets](https://docs.google.com/spreadsheets/d/1apSr23kcOJOJDaKbLLxPSbCcfzEmbLnrPhqHBDsTg0o/edit?usp=sharing).
Jika 23 orang dipilih secara acak, peluang ada orang yang memiliki tanggal ulang tahun yang saling bertepatan sekitar 0,506. Tidak jauh dari 1/2.

# Bukalah Gerbang Keajaiban
Perusahaan vtuber Hololive memiliki 55 anggota perempuan aktif.
Apabila rumus yang kita peroleh kita berikan input *n* = 55, kita peroleh peluang "ada pasangan vtuber Hololive perempuan aktif yang memiliki tanggal ulang tahun yang bertepatan" sekitar 0,986. Artinya komplemennya memiliki peluang sekitar 1-0.986 = 0.014 = 1,4%

Namun, tidak ada pasangan vtuber Hololive perempuan aktif yang memiliki tanggal ulang tahun yang bertepatan. Kejadian dengan peluang 0,014 ini saya sebut "Keajaiban Ulang Tahun Hololive".

## Rahasia Umum
Kesimpulannya adalah hal yang mungkin kebanyakan penonton vtuber sudah tahu.
Ulang tahun vtuber tidak selalu sama dengan tanggal ulang tahun *talent* atau pemerannya.
Ada beberapa vtuber yang menggeser tanggal ulang tahun virtual mereka, dan ada juga yang tidak.

(Menurut saya tidak masalah tanggalnya "asli" atau tidak, yang penting konten ulang tahunnya asik. 👍)

Ada beberapa alasan mereka melakukan ini:

1. **Tanggal dipilih untuk kenyamanan pemeran.**

    Ulang tahun adalah hari kerja bagi vtuber, mereka akan sibuk membuat konten ulang tahun mereka sendiri. Beberapa talent mungkin akan menggeser ulang tahun virtual mereka, supaya ada waktu untuk merayakan ulang tahun pribadi.

2. **Tanggal dipilih untuk menjaga privasi pemeran.**

    Ulang tahun termasuk data pribadi, dan beberapa vtuber akan menggeser untuk menambah lapisan perlindungan privasi mereka.

3. ***Lore Gimmick*, tanggal dipilih sesuai tema dari karakter vtuber.**

    Contohnya si hiu Gawr Gura lahir di tanggal tayang perdana film Jaws (20 Juni), atau si Zombie Kureiji Ollie lahir di Hari Zombie Sedunia (13 Oktober)

4. **Tanggal dipilih untuk menghindari tanggal yang saling bertepatan.**

    Tanggal ulang tahun yang saling bertepatan akan menyebabkan audiens terpecah menjadi 2, karena ada konflik jadwal antara dua perayaan penting di hari yang sama.
    
Angka peluang 0,014 yang kita peroleh dapat menjadi bukti statistik untuk alasan 4.
Dalam statistik, kita perlu merumuskan hipotesis nol dan hipotesis alternatif.

Hipotesis nol: "Alasan 4 tidak mempengaruhi vtuber Hololive dalam menentukan tanggal lahir."
    
Hipotesis alternatif: "Alasan 4 mempengaruhi vtuber Hololive dalam menentukan tanggal lahir."

Peluang 0,014 yang kita punya adalah peluang dari kejadian yang kita amati terjadi, dengan mengasumsikan Hipotesis nol. Ini disebut p-value. p-value bernilai 0,014 cukup kecil untuk menolak hipotesis nol. Dapat disimpulkan bahwa alasan 4 memiliki pengaruh yang signifikan secara statistik.

Statistik tidak selalu bisa memberikan kesimpulan yang pasti, jadi kecuali ada testimoni dari vtuber Hololive, kita tidak akan tahu pasti (dan kita tidak perlu tahu).

### Observasi Tambahan

Secara umum, keajaiban ini juga bisa dilihat di kelompok vtuber lain, meski tidak signifikan secara statistik.
1. Nijisanji (ex) ID dengan 18 orang tidak memiliki pasangan orang yang tanggal ulang tahunnya bertepatan, peluang ini terjadi sekitar 65,4%.
2. Nijisanji EN dengan 35 orang tidak memiliki pasangan orang yang tanggal ulang tahunnya bertepatan, peluang ini terjadi sekitar 18,7%.

Perlu diingat juga bahwa dalam sejarah Hololive ada tiga pasangan anggota Hololive yang tanggal ulang tahunnya saling bertepatan.
1. Astel Leda dengan Tsunomaki Watame (6 Juni)
2. Ayunda Risu dengan Aragami Oga (15 Januari)
3. Artia dengan Hakui Koyori (15 Maret)

Saya pikir bukti ini tidak cukup untuk menyangkal alasan 4.
Astel dan Oga adalah vtuber laki-laki dari cabang Holostars, yang mungkin struktur manajemen dan target pasarnya berbeda. Tanggal debut Astel, Watame, Risu dan Oga juga sangat berdekatan: 7 Desember 2019, 29 Desember 2019, 10 April 2020, dan 1 Mei 2020. Sementara Artia adalah mantan anggota Hololive CN, yang berhenti aktif jauh sebelum debut Koyori.

Bagaimana menurut kalian? Apakah alasan 4 efeknya nyata, atau "Keajaiban Ulang Tahun Hololive" hanyalah kebetulan?

# Penutup
Artikel pertama blog ini akhirnya selesai juga.
Selama satu tahun ke depan saya akan fokus meningkatkan konsistensi dan kualitas isi blog ini.
Apabila ada waktu, mungkin saya akan mencoba format lain seperti video atau infografis sebagai pelengkap.

Bagaimana pendapat kalian tentang artikel ini dan blog ini secara umum? Kotak untuk kritik, saran dan pendapat selalu terbuka lebar.
Untuk menyampaikannya, kalian bisa interaksi lewat media sosial berikut.
1. [Facebook](https://www.facebook.com/mugmugcomics). 
2. [Twitter](https://twitter.com/MugmugComics).