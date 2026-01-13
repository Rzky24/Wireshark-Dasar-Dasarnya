# Wireshark-Dasar-Dasarnya
Wireshark adalah alat analisis paket jaringan sumber terbuka dan lintas platform yang mampu mengendus dan menyelidiki lalu lintas langsung serta memeriksa tangkapan paket ( PCAP ). Alat ini umum digunakan sebagai salah satu alat analisis paket terbaik. Di ruangan ini, kita akan mempelajari dasar-dasar Wireshark dan menggunakannya untuk melakukan analisis paket fundamental.

Tujuan pembelajaran
Navigasi dan konfigurasikan Wireshark
Periksa paket dan temukan informasi dari berbagai lapisan TCP /IP.
Terapkan filter tampilan

Pengaturan Lingkungan
Tekan tombol Mulai Mesin di bawah untuk memulai mesin virtual.


Nyalakan Mesin
Mesin akan memulai dalam tampilan Layar Terpisah. Jika tidak terlihat, gunakan tombol biru " Tampilkan Tampilan Terpisah" di bagian atas halaman.

Terdapat dua file tangkapan layar yang diberikan di VM . Anda dapat menggunakan http1.pcapngfile tersebut untuk mensimulasikan tindakan yang ditunjukkan pada tangkapan layar. Harap dicatat bahwa Anda perlu menggunakan Exercise.pcapngfile tersebut untuk menjawab pertanyaan.
File mana yang digunakan untuk mensimulasikan tangkapan layar?
http1.pcapng
File mana yang digunakan untuk menjawab pertanyaan-pertanyaan tersebut?
Exercise.pcapng
Me

Gambaran Umum Alat
Kasus Penggunaan
Wireshark adalah salah satu alat analisis lalu lintas paling ampuh yang tersedia saat ini. Ada banyak kegunaan untuk alat ini:

Mendeteksi dan mengatasi masalah jaringan, seperti titik kegagalan beban jaringan dan kemacetan.
Mendeteksi anomali keamanan, seperti host nakal, penggunaan port yang tidak normal, dan lalu lintas yang mencurigakan.
Meneliti dan mempelajari detail protokol, seperti kode respons dan data muatan.
Catatan: Wireshark bukanlah Sistem Deteksi Intrusi ( IDS ). Wireshark hanya memungkinkan analis untuk menemukan dan menyelidiki paket secara mendalam. Wireshark juga tidak memodifikasi paket; ia hanya membacanya. Oleh karena itu, mendeteksi anomali atau masalah jaringan sangat bergantung pada pengetahuan dan keterampilan investigasi analis.

GUI dan Data
GUI Wireshark dibuka dengan satu halaman terpadu, yang membantu pengguna menyelidiki lalu lintas dengan berbagai cara. Sekilas, lima bagian menonjol.
Bilah alat	Toolbar utama berisi beberapa menu dan pintasan untuk penyadapan dan pemrosesan paket, termasuk penyaringan, pengurutan, peringkasan, ekspor, dan penggabungan. 
Tampilkan Bilah Filter	Bagian kueri dan penyaringan utama.
Berkas Terbaru	Daftar berkas yang baru saja diselidiki. Anda dapat memanggil kembali berkas yang terdaftar dengan mengklik dua kali. 
Filter dan Antarmuka Pengambilan Gambar	Filter tangkapan dan titik pengintaian yang tersedia (antarmuka jaringan). Antarmuka jaringan adalah titik penghubung antara komputer dan jaringan. Koneksi perangkat lunak (misalnya, lo, eth0, dan ens33) memungkinkan perangkat keras jaringan.
Bilah Status	Status alat, profil, dan informasi paket numerik.

Gambar di bawah ini menunjukkan jendela utama Wireshark. Bagian-bagian yang dijelaskan dalam tabel ditandai dengan sorotan.

Sekarang buka Wireshark dan ikuti panduan langkah demi langkahnya. 
<img width="1558" height="735" alt="image" src="https://github.com/user-attachments/assets/7ee3005a-9f48-4df3-b002-317542a3dbb0" />
Memuat File PCAP
Gambar di atas menunjukkan antarmuka Wireshark yang kosong. Satu-satunya informasi yang tersedia adalah http1.pcapfile yang baru saja diproses. Mari kita muat file tersebut dan lihat presentasi paket Wireshark secara detail. Perhatikan bahwa Anda juga dapat menggunakan menu "File" , menyeret dan meletakkan file, atau mengklik dua kali pada file untuk memuat file pcap 
<img width="1200" height="460" alt="image" src="https://github.com/user-attachments/assets/0c3329ea-75aa-44b4-8746-72bab9537501" />
Sekarang, kita dapat melihat nama file yang telah diproses, jumlah paket secara detail, dan detail paket. Detail paket ditampilkan dalam tiga panel berbeda, yang memungkinkan kita untuk menemukannya dalam berbagai format.
Panel Daftar Paket	Ringkasan setiap paket (alamat sumber dan tujuan, protokol, dan informasi paket). Anda dapat mengklik daftar untuk memilih paket yang ingin Anda selidiki lebih lanjut. Setelah Anda memilih paket, detailnya akan muncul di panel lainnya.
Panel Detail Paket	Penjelasan rinci protokol dari paket yang dipilih.
Panel Byte Paket	Representasi heksadesimal dan ASCII yang telah didekode dari paket yang dipilih. Ini menyoroti bidang paket tergantung pada bagian yang diklik di panel detail.
Paket Mewarnai
Selain informasi paket yang cepat, Wireshark juga mewarnai paket berdasarkan kondisi dan protokol yang berbeda untuk mendeteksi anomali dan protokol dalam tangkapan dengan cepat (ini menjelaskan mengapa hampir semuanya berwarna hijau dalam tangkapan layar yang diberikan). Sekilas informasi paket ini dapat membantu melacak dengan tepat apa yang Anda cari selama analisis. Anda dapat membuat aturan warna khusus untuk mendeteksi peristiwa yang menarik dengan menggunakan filter tampilan, dan kita akan membahasnya di ruangan berikutnya. Sekarang mari kita fokus pada pengaturan default dan memahami cara melihat dan menggunakan detail data yang disajikan.

Wireshark memiliki dua jenis metode pewarnaan paket: aturan sementara yang hanya tersedia selama sesi program dan aturan permanen yang disimpan dalam file preferensi (profil) dan tersedia untuk sesi program berikutnya. Anda dapat menggunakan "menu klik kanan" atau  menu "Lihat --> Aturan Pewarnaan"  untuk membuat aturan pewarnaan permanen.  Menu "Warnai Daftar Paket"  mengaktifkan/menonaktifkan aturan pewarnaan. Pewarnaan paket sementara dilakukan dengan "menu klik kanan" atau  menu "Lihat --> Filter Percakapan"  , yang dibahas dalam TUGAS-5.

Warna permanen standar ditampilkan di bawah ini.
<img width="1590" height="710" alt="image" src="https://github.com/user-attachments/assets/bc2d7d40-b85f-434d-8a0b-c7c61e3c96b3" />
Mengendus Lalu Lintas
Anda dapat menggunakan tombol "hiu" biru untuk memulai penyadapan jaringan (menangkap lalu lintas), tombol merah akan menghentikan penyadapan, dan tombol hijau akan memulai kembali proses penyadapan. Bilah status juga akan menampilkan antarmuka penyadapan yang digunakan dan jumlah paket yang dikumpulkan.
<img width="1809" height="813" alt="image" src="https://github.com/user-attachments/assets/0c7bb626-36a0-41d8-8336-efc4c39b25e4" />
Menggabungkan File PCAP
Wireshark dapat menggabungkan dua file pcap menjadi satu file tunggal. Anda dapat menggunakan jalur menu "File --> Merge" untuk menggabungkan file pcap yang sudah ada dengan file yang telah diproses. Saat Anda memilih file kedua, Wireshark akan menampilkan jumlah total paket dalam file yang dipilih. Setelah Anda mengklik "open", Wireshark akan menggabungkan file pcap yang ada dengan file yang dipilih dan membuat file pcap baru . Perhatikan bahwa Anda perlu menyimpan file pcap yang telah "digabungkan" sebelum mengerjakannya.

Lihat GIF
 

Lihat Detail File
Mengetahui detail file sangat membantu. Terutama saat bekerja dengan beberapa file pcap , terkadang Anda perlu mengetahui dan mengingat detail file (hash file, waktu pengambilan, komentar file pengambilan, antarmuka, dan statistik) untuk mengidentifikasi file, mengklasifikasikan, dan memprioritaskannya. Anda dapat melihat detailnya dengan mengikuti " Statistik --> Properti File Pengambilan" atau dengan mengklik " ikon pcap yang terletak di kiri bawah" .

Lihat GIF****
Jawablah pertanyaan-pertanyaan di bawah ini.
Gunakan file "Exercise.pcapng" untuk menjawab pertanyaan.
Bacalah "komentar file tangkapan" . Apa itu flag? TryHackMe_Wireshark_Demo
Berapakah jumlah total paket?
58620
Berapakah nilai hash SHA256 dari file tangkapan tersebut?
f446de335565fb0b0ee5e5a3266703c778b2f3dfad7efeaeccb2da5641a6d6eb

Analisis Paket
Analisis Paket
Analisis paket juga dikenal sebagai analisis protokol, yang menyelidiki detail paket dengan mendekode protokol dan field yang tersedia. Wireshark mendukung daftar panjang protokol untuk analisis, dan Anda juga dapat menulis skrip analisis Anda sendiri. Anda dapat menemukan detail lebih lanjut tentang analisis di sini .

Catatan: Bagian ini membahas bagaimana Wireshark menggunakan lapisan OSI untuk memecah paket dan bagaimana menggunakan lapisan-lapisan ini untuk analisis. Diharapkan Anda sudah memiliki pengetahuan dasar tentang model OSI dan cara kerjanya. 

Detail Paket
Anda dapat mengklik paket di panel daftar paket untuk membuka detailnya (klik dua kali akan membuka detail di jendela baru). Paket terdiri dari 5 hingga 7 lapisan berdasarkan model OSI. Kita akan membahas semuanya dalam paket HTTP dari contoh tangkapan. Gambar di bawah menunjukkan tampilan paket nomor 27.
<img width="1953" height="1058" alt="image" src="https://github.com/user-attachments/assets/acbdd1d2-73f3-48dc-ba08-3b5243a606b6" />

Setiap kali Anda mengklik detail, bagian yang sesuai akan disorot di panel byte paket.
<img width="1950" height="412" alt="image" src="https://github.com/user-attachments/assets/7671024f-4327-45df-b291-4a86e9e1f54c" />

Mari kita lihat lebih dekat panel detailnya.
<img width="898" height="161" alt="image" src="https://github.com/user-attachments/assets/315079f2-19b8-4f35-86c0-92caef0fe148" />
Kita dapat melihat tujuh lapisan berbeda pada paket tersebut: frame/packet, source [MAC], source [IP], protocol, protocol errors, application protocol, dan application data. Di bawah ini kita akan membahas lapisan-lapisan tersebut secara lebih detail.

Frame (Lapisan 1): Ini akan menunjukkan frame/paket apa yang sedang Anda lihat dan detail spesifik untuk lapisan Fisik dari model OSI.

Lihat gambar <img width="827" height="418" alt="image" src="https://github.com/user-attachments/assets/c8ff38ef-4c9d-4034-8df8-8bb7d924f7c9" />

 

Sumber [MAC] (Lapisan 2): Ini akan menunjukkan kepada Anda Alamat MAC sumber dan tujuan; dari lapisan Tautan Data model OSI.

Lihat gambar <img width="1134" height="112" alt="image" src="https://github.com/user-attachments/assets/00bcb041-b189-4ada-b445-ace111a51e08" />

 

Sumber [IP] (Lapisan 3): Ini akan menunjukkan alamat IPv4 sumber dan tujuan; dari lapisan Jaringan pada model OSI.

Lihat gambar <img width="829" height="331" alt="image" src="https://github.com/user-attachments/assets/297b2633-d6b3-49fe-8796-0d56262836c8" />

 

Protokol (Lapisan 4): Ini akan menunjukkan detail protokol yang digunakan ( UDP / TCP ) dan port sumber serta tujuan; dari lapisan Transport pada model OSI.

Lihat gambar <img width="1054" height="532" alt="image" src="https://github.com/user-attachments/assets/5d738b30-11dc-420b-a9d1-463fcbd2a45e" />

 

Kesalahan Protokol: Kelanjutan dari lapisan ke-4 ini menunjukkan segmen-segmen spesifik dari TCP yang perlu disusun kembali.

Lihat gambar <img width="1259" height="135" alt="image" src="https://github.com/user-attachments/assets/f6b2fa6a-b70c-45f8-9cd6-75c8fb84eeb4" />

 

Protokol Aplikasi (Lapisan 5): Ini akan menampilkan detail spesifik untuk protokol yang digunakan, seperti HTTP , FTP , dan SMB . Dari lapisan Aplikasi model OSI.

Lihat gambar <img width="1261" height="352" alt="image" src="https://github.com/user-attachments/assets/2ebef0c7-af02-46e2-b544-fd95e2b21da0" />

 

Data Aplikasi:  Ekstensi lapisan ke-5 ini dapat menampilkan data spesifik aplikasi.

Lihat gambar <img width="1159" height="102" alt="image" src="https://github.com/user-attachments/assets/bd34fa9a-9778-4ff9-8522-19fe51028759" />

Jawablah pertanyaan-pertanyaan di bawah ini.
Gunakan file "Exercise.pcapng" untuk menjawab pertanyaan. Lihat paket nomor 38. Bahasa markup apa yang digunakan dalam protokol HTTP?

eXtensible Markup Language


Kapan tanggal kedatangan paket tersebut? (Format jawaban: Bulan/Tanggal/Tahun)

05/13/2004


Berapakah nilai TTL?

47


Berapakah ukuran payload TCP?

424

Berapakah nilai e-tag-nya?
(Contoh: 82ecb-6321-9e904585)

9a01a-4696-7e354b00










