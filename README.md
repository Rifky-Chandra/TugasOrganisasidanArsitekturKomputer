# TugasOrganisasidanArsitekturKomputer

## 1. Jelaskan struktur antar hubungan dan beri contohnya.
  Struktur antar hubungan atau yang biasa kita sebut sebagai sistem bus adalah jalur komunikasi yang digunakan bersama oleh berbagai komponen dalam komputer melalui satu set kabel tunggal untuk menghubungkan berbagai subsistem. Sistem bus berfungsi sebagai penghubung utama yang memastikan setiap bagian komputer dapat berkomunikasi dan bekerja secara terkoordinasi dalam menjalankan tugasnya. Transfer data antar komponen komputer sangat mendominasi kerja suatu komputer, karena hampir setiap operasi bergantung pada bagaimana data dipindahkan dari satu komponen ke komponen lainnya. Data atau program yang tersimpan dalam memori dapat diakses dan dieksekusi oleh CPU melalui perantara bus, sehingga memungkinkan pemrosesan instruksi dengan efisiensi tinggi. Begitu pula, hasil eksekusi dapat dikirim ke perangkat output, seperti monitor, melalui sistem bus, memungkinkan pengguna untuk melihat hasil operasi komputer secara langsung dan interaktif.
Contoh:
- Bus ISA (Industry Standard Architecture), yang pada dasarnya adalah bus PC/AT yang beroperasi pada 8,33 MHz. Keuntungannya menggunakan bus ini adalah tetap mempertahankan kompatibiitas dengan mesin-mesin dan kartu-kartu yang ada. Pendekatan ini juga didasarkan pada sebuah bus yang telah dilisensikan secara bebas oleh IBM kepada banyak perusahaan dalam rangka untuk menjamin bahwa sebanyak mungkin pihak ketiga dapat memproduksi kartu-kartu untuk PC pertama, sesuatu yang kembali menghantui IBM. Setiap PC yang berbasiskan Intel masih menggunakan bus jenis ini, meskipun biasanya juga disertai dengan satu atau lebih bus lain.

- Bus PCI (Peripheral Component Interconnect, bus yang tidak tergantung prosesor dan berfungsi sebagai bus mezzanine atau bus peripheral. Standar PCI adalah 64 saluran data pada kecepatan 33 MHz, laju transfer data 263 MB per detik atau 2,112 Gbps. Keunggulan PCI tidak hanya pada kecepatannya saja, tetapi murah dengan keping yang sedikit.

- Bus USB (Universal Standard Bus), semua perangkat peripheral tidak efektif apabila dipasang pada bus kecepatan tinggi PCI, sedangkan banyak peralatan yang memiliki kecepatan rendah seperti keyboard, mouse, dan printer. Sebagai solusinya, 7 vendor computer (Compaq, DEC, IBM, Intel, Microsoft, NEC, dan Northen Telecom) bersama-sama merancang bus untuk peralatan I/O berkecepatan rendah, yang dinamakan USB ini. Keuntungan yang didapatkan dan tujuan dari penerapan USB adalah sebagai berikut : 
1. Pemakai tidak harus memasang tombol atau jumper pada PCB atau peralatan.
2. Pemakai tidak harus membuka casing untuk memasang peralatan I/O baru. 
3. Hanya satu jenis kabel yang diperlukan sebagai penghubung. 
4. Dapat mensuplai daya pada peralatan-peralatan I/O. 
5. Memudahkan pemasangan peralatan-peralatan yang hanya sementara dipasang pada komputer. 
6. Tidak diperlukan reboot pada pemasangan peralatan baru dengan USB. 
7. Murah.
   
- Bus SCSI (Small Computer System Interface), perangkat peripheral eksternal yang dipopulerkan oleh macintosh pada tahun 1984. SCSI merupakan interface standar untuk drive CD-ROM, peralatan audio, hard disk, dan perangkat penyimpanan eksternal berukuran besar. SCSI menggunakan interface paralel dengan 8,16 atau 32 saluran data. Perangkat SCSI memiliki dua buah konektor, yaitu konektor input dan konektor. Seluruh perangkat berfungsi secara independen dan dapat saling bertukar data misalnya hard disk dapat mem-back up diri ke tape drive tanpa melibatkan prosesor.

- Bus P1394 / Fire Wire, semakin pesatnya kebutuhan bus I/O berkecepatan tinggi dan semakin cepatnya prosessor saat ini yang mencapai 1 Ghz, maka perlu diimbangi dengan bus berkecepatan tinggi juga. Bus SCSI dan PCI tidak dapat mencukupi kebutuhan saat ini. Sehingga dikembangkan bus performance tinggi yang dikenal dengan Fire Wire (P1393 standard IEEE). P1394 memiliki kelebihan dibandingkan dengan interface I/O lainnya, yaitu sangat cepat, murah, dan mudah untuk diimplementasikan. Pada kenyataannya, P1394 tidak hanya populer pada sistem komputer, namun juga pada peralatan elektronik seperti pada kamera digital, VCR, dan televisi. Kelebihan lain adalah penggunaan transmisi serial sehingga tidak memerlukan banyak kabel.

- FutureBus+, standar bus asinkron berkinerja tinggi yang dibuat oleh IEEE. 8 Persyaratan Dasar Rancangan Bus (dari komite Futurebus+):
1. Tidak tergantung pada arsitektur, prosesor, dan teknologi tertentu.
2. Memiliki protocol transfer asinkron dasar.
3. Mengizinkan protocol tersinkronisasi pada sumber untuk kebutuhan opsional.
4. Tidak berdasarkan pada teknologi canggih.
5. Terdiri dari protocol-protocol paralel terdistribusi penuh.
6. Menyediakan dukungan bagi sistem-sistem yang fault-tolerant dan yang memiliki reliabilitas tinggi.
7. Menawarkan dukungan langsung terhadap memori berbasis cache yang dapat digunakan bersama.
8. Memberikan definisi transportasi pesan yang kompatibel.

## 2. ⁠Bila terlalu banyak modul atau perangkat dihubungkan pada bus maka akan terjadi penurunan kinerja, sebutkan penyebabnya?
 Bila  terlalu  banyak  modul  atau  perangkat  dihubungkan  pada  bus  maka  akan terjadi penurunan kinerja, yang disebabkan oleh :  
 1. Semakin besar delay propagasi untuk mengkoordinasikan penggunaan bus.
 2. Antrian penggunaan bus semakin panjang.
 3. Dimungkinkan habisnya kapasitas transfer bus sehingga memperlambat data.
Antisipasi  dan  solusi  persoalan  di  atas  adalah  penggunaan  bus  jamak  yang  hierarkis. Modul  –  modul  dikalasifikasikan berdasarkan  kebutuhan terhadap lebar dan kecepatan bus. Bus biasanya terdiri atas bus lokal, bus sistem, dan bus ekspansi. 

## 3. ⁠Umumnya perangkat berprioritas paling rendah memiliki waktu tunggu rata-rata yang paling singkat. Dengan dasar ini biasanya CPU diberi perioritas tertinggi pada SBI. Sebutkan alasan perangkat berprioritas 16 memiliki waktu tunggu rata-rata paling rendah? Dibawah kondisi seperti apa keadaan diatas tidak berlaku?
Perangkat berpriotritas 16 memiliki waktu tunggu rata rata paling rendah  karena :  
  Dalam sistem bus, perangkat dengan prioritas lebih rendah biasanya memiliki waktu tunggu lebih lama karena akses bus diberikan terlebih dahulu kepada perangkat dengan prioritas lebih tinggi (angka prioritas lebih kecil). Bus data berfungsi menyalurkan data antara komponen komputer melalui jalur sinyal paralel (8, 16, 32 bit, atau lebih) yang bersifat dua arah (bidirectional). Hanya satu perangkat yang dapat menggunakan bus dalam satu waktu, sehingga perangkat harus memiliki tiga state (tristate) agar tidak mengganggu perangkat lain.
### aturan ini tidak berlaku jika menggunakan sistem dan metode seperti:
1. Penjadwalan Prioritas Tetap (Fixed Priority Scheduling)
2. Penjadwalan Round-Robin

Sumber Referensi:
  1. Organisasi Komputer: Struktur Bus dan Contohnya. ( https://innaimaskurniatry.blogspot.com/2017/06/struktur-hubungan-bus-dan-contohnya.html)
  2. Belajar arsitektur sistem bus~ | *Inspiration Of Computer* ( https://gamirarindu4.blogspot.com/2015/12/belajar-arsitektur-sistem-bus.html )
  3. https://123dok.com/document/zg65782q-bab-sistem-bus-organisasi-komputer.html
