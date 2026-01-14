<img width="1518" height="907" alt="image" src="https://github.com/user-attachments/assets/c1fa4e96-3715-4e38-921a-ee210001faeb" /># Wireshark-Dasar-Dasarnya
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

Lihat GIF<img width="1292" height="880" alt="image" src="https://github.com/user-attachments/assets/7f06e137-efa0-45ac-ba9d-eed937189ee3" />

 

Lihat Detail File
Mengetahui detail file sangat membantu. Terutama saat bekerja dengan beberapa file pcap , terkadang Anda perlu mengetahui dan mengingat detail file (hash file, waktu pengambilan, komentar file pengambilan, antarmuka, dan statistik) untuk mengidentifikasi file, mengklasifikasikan, dan memprioritaskannya. Anda dapat melihat detailnya dengan mengikuti " Statistik --> Properti File Pengambilan" atau dengan mengklik " ikon pcap yang terletak di kiri bawah" .

Lihat GIF**** <img width="1323" height="910" alt="image" src="https://github.com/user-attachments/assets/90179112-96de-41a7-ab74-c1822624dcb5" />

Jawablah pertanyaan-pertanyaan di bawah ini.

Gunakan file "Exercise.pcapng" untuk menjawab pertanyaan.
Bacalah "komentar file tangkapan" . Apa itu flag?  TryHackMe_Wireshark_Demo
buka file exercise pcapng di wireshark- lihat icon di tampilan wire shark pojok kiri bawah -open the capture property - detail- file comment - dan cari flag nya - hasil akan tampil

Berapakah jumlah total paket? 58620
lihat halaman wireshark paling bawah pojok kanan  

Berapakah nilai hash SHA256 dari file tangkapan tersebut?
f446de335565fb0b0ee5e5a3266703c778b2f3dfad7efeaeccb2da5641a6d6eb
buka file exercise pcapng - lihat pojok kanan bawah capture property - detail - cari hash sha256- hasil akan muncul 

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
cari pencarian dan lihat di nomer paket 38- lihat http - muncul hasil - eXtensible Markup Language

Kapan tanggal kedatangan paket tersebut? (Format jawaban: Bulan/Tanggal/Tahun) 05/13/2004
klik  pencarian no 38 - lihat di http - cari date - muncul hasil 

Berapakah nilai TTL? 47
masih di pket nomer 38- cari bagian internet protocol - lihat TTL nya - muncul hasil


Berapakah ukuran payload TCP? 424
masih di paket no 38 - cari Transmissions control protocol - cari payload - hasil  

Berapakah nilai e-tag-nya? 9a01a-4696-7e354b00
(Contoh: 82ecb-6321-9e904585)
masih di paket no 38 - cari Hypertext Transfer protocol - cari Etag - hasil - 9a01a-4696-7e354b00

Navigasi Paket
Nomor Paket
Wireshark menghitung jumlah paket yang diselidiki dan menetapkan nomor unik untuk setiap paket. Hal ini membantu proses analisis untuk data tangkapan yang besar dan memudahkan untuk kembali ke titik tertentu dari suatu peristiwa.

<img width="995" height="811" alt="image" src="https://github.com/user-attachments/assets/e4cd74eb-24fe-4964-af7b-476f3663c1d8" />

Buka Paket
Nomor paket tidak hanya membantu menghitung jumlah total paket atau mempermudah pencarian/penyelidikan paket tertentu. Fitur ini tidak hanya menavigasi antar paket ke atas dan ke bawah; tetapi juga menyediakan pelacakan paket dalam bingkai dan menemukan paket berikutnya di bagian percakapan tertentu. Anda dapat menggunakan menu dan bilah alat "Go" untuk melihat paket tertentu.

<img width="1518" height="907" alt="image" src="https://github.com/user-attachments/assets/ec2f7471-0bb7-46b0-8d71-9550dcd86d0a" />

Temukan Paket
Selain nomor paket, Wireshark dapat menemukan paket berdasarkan isi paket. Anda dapat menggunakan menu "Edit --> Temukan Paket" untuk melakukan pencarian di dalam paket untuk peristiwa tertentu yang diminati. Ini membantu analis dan administrator untuk menemukan pola intrusi atau jejak kegagalan tertentu.

Ada dua poin penting dalam menemukan paket. Pertama, mengetahui tipe input. Fungsi ini menerima empat tipe input (Filter tampilan, Hex, String, dan Regex). Pencarian string dan regex adalah tipe pencarian yang paling umum digunakan. Pencarian tidak peka huruf besar/kecil, tetapi Anda dapat mengatur kepekaan huruf besar/kecil dalam pencarian Anda dengan mengklik tombol radio.

Poin kedua adalah memilih kolom pencarian. Anda dapat melakukan pencarian di tiga panel (daftar paket, detail paket, dan byte paket), dan penting untuk mengetahui informasi yang tersedia di setiap panel untuk menemukan kejadian yang diminati. Misalnya, jika Anda mencoba mencari informasi yang tersedia di panel detail paket dan melakukan pencarian di panel daftar paket, Wireshark tidak akan menemukannya meskipun informasi tersebut ada.
<img width="1518" height="907" alt="image" src="https://github.com/user-attachments/assets/9d0960ef-40bb-4d45-91b9-b33f4e388557" />
Paket Tanda
Menandai paket adalah fungsi bermanfaat lainnya bagi analis. Anda dapat menemukan/menunjuk ke paket tertentu untuk penyelidikan lebih lanjut dengan menandainya. Ini membantu analis menunjukkan peristiwa yang menarik atau mengekspor paket tertentu dari hasil tangkapan. Anda dapat menggunakan menu "Edit" atau "klik kanan" untuk menandai/menghapus tanda pada paket.

Paket yang ditandai akan ditampilkan dalam warna hitam terlepas dari warna asli yang mewakili jenis koneksi. Perhatikan bahwa informasi paket yang ditandai diperbarui setiap sesi file, sehingga paket yang ditandai akan hilang setelah menutup file tangkapan.
<img width="1518" height="907" alt="image" src="https://github.com/user-attachments/assets/dfd0d4b2-a519-4c61-884f-bbf99a6a4f61" />

Komentar Paket
Mirip dengan penandaan paket, pemberian komentar adalah fitur bermanfaat lainnya bagi analis. Anda dapat menambahkan komentar untuk paket tertentu yang akan membantu penyelidikan lebih lanjut atau mengingatkan dan menunjukkan poin penting/mencurigakan bagi analis lapisan lainnya. Tidak seperti penandaan paket, komentar dapat tetap berada di dalam file tangkapan hingga operator menghapusnya.
<img width="1518" height="907" alt="image" src="https://github.com/user-attachments/assets/f8a83ba7-8d7d-4173-9a96-a29477acc530" />

Ekspor Paket
File tangkapan dapat berisi ribuan paket dalam satu file. Seperti yang disebutkan sebelumnya, Wireshark bukanlah IDS , jadi terkadang, perlu untuk memisahkan paket tertentu dari file dan menggali lebih dalam untuk menyelesaikan suatu insiden. Fungsi ini membantu analis untuk hanya membagikan paket yang mencurigakan (cakupan yang telah ditentukan). Dengan demikian, informasi yang berlebihan tidak disertakan dalam proses analisis. Anda dapat menggunakan menu "File" untuk mengekspor paket.
<img width="1518" height="907" alt="image" src="https://github.com/user-attachments/assets/bfb1d862-42c8-42ea-9e60-a615d64bcb2c" />

Ekspor Objek (Berkas)
Wireshark dapat mengekstrak file yang ditransfer melalui jaringan. Bagi seorang analis keamanan, sangat penting untuk menemukan file yang dibagikan dan menyimpannya untuk penyelidikan lebih lanjut. Ekspor objek hanya tersedia untuk aliran protokol tertentu (DICOM, HTTP , IMF, SMB , dan TFTP).
<img width="1520" height="913" alt="image" src="https://github.com/user-attachments/assets/6eb6a4cb-9811-4ab1-87f9-967c659a51c3" />

Format Tampilan Waktu
Wireshark mencantumkan paket-paket sebagaimana yang ditangkap, jadi menyelidiki alur default tidak selalu merupakan pilihan terbaik. Secara default, Wireshark menampilkan waktu dalam "Detik Sejak Awal Penangkapan", penggunaan umum adalah menggunakan Format Tampilan Waktu UTC untuk tampilan yang lebih baik. Anda dapat menggunakan menu "Tampilan --> Format Tampilan Waktu" untuk mengubah format tampilan waktu.

<img width="1520" height="913" alt="image" src="https://github.com/user-attachments/assets/390f7d78-5482-4c79-9df0-2a5dcf7b41f4" />
<img width="1214" height="359" alt="image" src="https://github.com/user-attachments/assets/6e8a1889-dc65-44ff-acde-14aff35974cd" />

Informasi Pakar
Wireshark juga mendeteksi status spesifik protokol untuk membantu analis dengan mudah menemukan kemungkinan anomali dan masalah. Perlu diingat bahwa ini hanyalah saran, dan selalu ada kemungkinan terjadinya false positive/negative. Informasi ahli dapat memberikan kelompok kategori dalam tiga tingkat keparahan yang berbeda. Detailnya ditunjukkan pada tabel di bawah ini.

Kerasnya	Warna	Informasi
Mengobrol	Biru	Informasi tentang alur kerja standar.
Catatan	Biru muda	Peristiwa penting seperti kode kesalahan aplikasi.
Memperingatkan	Kuning	Peringatan seperti kode kesalahan yang tidak biasa atau pernyataan masalah.
Kesalahan	Merah	Masalah seperti paket yang tidak terformat dengan baik.
Grup informasi yang sering ditemui tercantum dalam tabel di bawah ini. Anda dapat merujuk ke dokumentasi resmi Wireshark untuk informasi lebih lanjut tentang entri informasi ahli.

Kelompok	Informasi	Kelompok	Informasi
Checksum	Kesalahan checksum	Tidak digunakan lagi	Penggunaan protokol yang sudah usang
Komentar	Deteksi komentar paket	Cacat	Deteksi paket yang salah format
Anda dapat menggunakan "bagian kiri bawah" pada bilah status atau menu "Analisis --> Informasi Pakar" untuk melihat semua entri informasi yang tersedia melalui kotak dialog. Ini akan menampilkan nomor paket, ringkasan, protokol grup, dan total kejadian.
<img width="1463" height="530" alt="image" src="https://github.com/user-attachments/assets/e8a1b901-02e5-41bc-b80b-0b017d352132" />

Jawablah pertanyaan-pertanyaan di bawah ini.
Gunakan file "Exercise.pcapng" untuk menjawab pertanyaan. Cari string "r4w" dalam detail paket. Siapa nama artis 1? r4w8173
lihat halaman wireshark - edit - find packet - ketik di kolom pencarian r4w - lihat di bagian - Line-based text data: text/html (107 lines) -
[truncated]Sed aliquam sem ut arcu.</p><p>painted by: <a href='artists.php?artist=1'>r4w8173</a></p><p><a href='#' onClick="window.open('./comment.php?pid=1','comment','width=500,height=400')">comment on this picture</a></p></div><div cl   

Buka paket 12 dan baca komentar paketnya. Apa jawabannya?
Catatan: gunakan  perintah terminal md5sum <filename> untuk mendapatkan hash MD5.
911cd574a42865a956ccde2d04495ebf
cari go to packet - cari buka paket 12 - lihat packet comment - ada petunjuk yang di arahkan ke nomer 39765 - cari di pencarian go  to packet - ketik 39765 - cari JPEG - klik kanan - export packet byte - ketik asdf/bebas rename dan pastikan di DESKTOP saja - save - fila export object - cari find - pilih http -ketik di text filter nya -jpeg 39765 - pastikan ada file nya - kemudian buka terminal : 
ubuntu@ip-10-49-133-2:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  Templates  Videos
ubuntu@ip-10-49-133-2:~$ cd Desktop/
ubuntu@ip-10-49-133-2:~/Desktop$ sum asdf    
07914     4
ubuntu@ip-10-49-133-2:~/Desktop$ ls
Exercise.pcapng  asdf  http1.pcapng  mate-terminal.desktop  wireshark.desktop
ubuntu@ip-10-49-133-2:~/Desktop$ md5sum asdf
911cd574a42865a956ccde2d04495ebf  asdf
ubuntu@ip-10-49-133-2:~/Desktop$ 



Terdapat file ".txt" di dalam file tangkapan. Temukan file tersebut dan bacalah; siapakah nama alien tersebut? PACKETMASTER
buka halaman wireshark - file- export object - http - text filter - klik .txt - pilih save -  rename menjadi note.txt - sv ke halaman desktop- save -kilik .txt di halaman desktop dan muncul hasilnya -  PACKETMASTER

Lihat bagian informasi ahli. Berapa jumlah peringatannya? 1636
lihat di eror information level icon halaman wireshark pojok kiri bawah - cari warna kuning - 1636

Penyaringan Paket
Wireshark memiliki mesin filter yang canggih yang membantu analis mempersempit lalu lintas dan fokus pada peristiwa yang diminati. Wireshark memiliki dua jenis pendekatan pemfilteran: filter tangkap dan filter tampilan. Filter tangkap digunakan untuk  "menangkap" hanya paket yang valid untuk filter yang digunakan. Filter tampilan digunakan untuk  "melihat" paket yang valid untuk filter yang digunakan. Kita akan membahas perbedaan dan penggunaan lanjutan dari filter-filter ini di sesi berikutnya. Sekarang mari kita fokus pada penggunaan dasar filter tampilan, yang akan membantu analis terlebih dahulu.

Filter adalah kueri spesifik yang dirancang untuk protokol yang tersedia dalam referensi protokol resmi Wireshark. Meskipun filter hanya merupakan opsi untuk menyelidiki peristiwa yang diminati, ada dua cara berbeda untuk memfilter lalu lintas dan menghilangkan noise dari file tangkapan. Cara pertama menggunakan kueri, dan cara kedua menggunakan menu klik kanan. Wireshark menyediakan GUI yang canggih , dan ada aturan emas bagi analis yang tidak ingin menulis kueri untuk tugas-tugas dasar:  "Jika Anda dapat mengkliknya, Anda dapat memfilter dan menyalinnya."

Terapkan sebagai Filter
Ini adalah cara paling dasar untuk memfilter lalu lintas. Saat menyelidiki file tangkapan, Anda dapat mengklik bidang yang ingin Anda filter dan menggunakan "menu klik kanan" atau  menu "Analisis  --> Terapkan sebagai Filter"  untuk memfilter nilai tertentu. Setelah Anda menerapkan filter, Wireshark akan menghasilkan kueri filter yang diperlukan, menerapkannya, menampilkan paket sesuai pilihan Anda, dan menyembunyikan paket yang tidak dipilih dari panel daftar paket. Perhatikan bahwa jumlah total dan paket yang ditampilkan selalu ditunjukkan pada bilah status.<img width="1520" height="932" alt="image" src="https://github.com/user-attachments/assets/9cd8d797-e47c-4023-94ca-68a5d8ae49f6" />

Filter Percakapan
Saat Anda menggunakan opsi "Terapkan sebagai Filter", Anda hanya akan memfilter satu entitas dari paket tersebut. Opsi ini merupakan cara yang baik untuk menyelidiki nilai tertentu dalam paket. Namun, misalkan Anda ingin menyelidiki nomor paket tertentu dan semua paket terkait dengan berfokus pada alamat IP dan nomor port. Dalam hal ini, opsi "Filter Percakapan" membantu Anda hanya melihat paket yang terkait dan menyembunyikan paket lainnya dengan mudah. ​​Anda dapat menggunakan menu "klik kanan" atau menu " Analisis --> Filter Percakapan " untuk memfilter percakapan.
<img width="1520" height="932" alt="image" src="https://github.com/user-attachments/assets/5b10f58a-01c8-4c82-96b7-baae5baa4d4a" />

Warnai Percakapan
Opsi ini mirip dengan "Filter Percakapan" dengan satu perbedaan. Opsi ini menyoroti paket yang terhubung tanpa menerapkan filter tampilan dan mengurangi jumlah paket yang dilihat. Opsi ini bekerja dengan opsi "Aturan Pewarnaan" dan mengubah warna paket tanpa mempertimbangkan aturan warna yang diterapkan sebelumnya. Anda dapat menggunakan "menu klik kanan" atau menu "Lihat --> Warnai Percakapan" untuk mewarnai paket yang terhubung dalam satu klik. Perhatikan bahwa Anda dapat menggunakan menu "Lihat --> Warnai Percakapan --> Atur Ulang Pewarnaan" untuk membatalkan operasi ini.<img width="1520" height="932" alt="image" src="https://github.com/user-attachments/assets/0af78fc1-2c37-4efc-a12a-1d2b5e38c5e4" />
<img width="1520" height="932" alt="image" src="https://github.com/user-attachments/assets/ea26a084-37ac-45b8-88e8-a275d45de236" />

Siapkan sebagai Filter 
Mirip dengan "Terapkan sebagai Filter", opsi ini membantu analis membuat filter tampilan menggunakan menu "klik kanan". Namun, tidak seperti yang sebelumnya, model ini tidak menerapkan filter setelah pilihan dibuat. Model ini menambahkan kueri yang diperlukan ke panel dan menunggu perintah eksekusi (enter) atau opsi pemfilteran lain yang dipilih dengan menggunakan  ".. dan/atau.."  dari menu "klik kanan". Siapkan sebagai Filter <img width="1586" height="932" alt="image" src="https://github.com/user-attachments/assets/5510bbc9-63cd-4aee-a589-bb37861dcc16" />

Terapkan sebagai Kolom
Secara default, panel daftar paket menyediakan informasi dasar tentang setiap paket. Anda dapat menggunakan "menu klik kanan" atau menu " Analisis --> Terapkan sebagai Kolom " untuk menambahkan kolom ke panel daftar paket. Setelah Anda mengklik suatu nilai dan menerapkannya sebagai kolom, nilai tersebut akan terlihat di panel daftar paket. Fungsi ini membantu analis memeriksa tampilan nilai/bidang tertentu di seluruh paket yang tersedia dalam file tangkapan. Anda dapat mengaktifkan/menonaktifkan kolom yang ditampilkan di panel daftar paket dengan mengklik bagian atas panel daftar paket. <img width="1520" height="932" alt="image" src="https://github.com/user-attachments/assets/9c659dab-79fa-4f95-afca-195408c3e8b5" />

Ikuti Streaming
Wireshark menampilkan semuanya dalam ukuran porsi paket. Namun, dimungkinkan untuk merekonstruksi aliran data dan melihat lalu lintas mentah seperti yang disajikan pada tingkat aplikasi. Dengan mengikuti protokol, aliran data membantu analis merekonstruksi data tingkat aplikasi dan memahami peristiwa yang diminati. Dimungkinkan juga untuk melihat data protokol yang tidak terenkripsi seperti nama pengguna, kata sandi, dan data lain yang ditransfer.

Anda dapat menggunakan "menu klik kanan" atau menu "Analisis  --> Ikuti Aliran TCP / UDP / HTTP "  untuk mengikuti aliran lalu lintas. Aliran ditampilkan dalam kotak dialog terpisah; paket yang berasal dari server disorot dengan warna biru, dan paket yang berasal dari klien disorot dengan warna merah.<img width="1515" height="932" alt="image" src="https://github.com/user-attachments/assets/6a8d4252-e131-466f-8ceb-6f55ce0aeafc" />

Setelah Anda mengikuti aliran data, Wireshark secara otomatis membuat dan menerapkan filter yang diperlukan untuk melihat aliran data tertentu. Ingat, setelah filter diterapkan, jumlah paket yang dilihat akan berubah. Anda perlu menggunakan tombol " X "  yang terletak di sisi kanan atas bilah filter tampilan untuk menghapus filter tampilan dan melihat semua paket yang tersedia dalam file tangkapan. 

Jawablah pertanyaan-pertanyaan di bawah ini.

Gunakan file " Exercise.pcapng " untuk menjawab pertanyaan.
Buka paket nomor 4. Klik kanan pada "Hypertext Transfer Protocol" dan terapkan sebagai filter.
Sekarang, lihat panel filter. Apa kueri filternya? http
pergi ke paket no 4 - klik kanan di http-  apply as filter - selected - hasil nya muncul - di kolom warna hijau http

Berapakah jumlah paket yang ditampilkan? 1089
lihat di bagian pojok kanan paling bawah halaman wireshark Displayed 

Buka paket nomor 33790, ikuti aliran HTTP, dan perhatikan responsnya dengan saksama.
Berdasarkan respons server web, berapa total jumlah artisnya? 3
pergi ke goto packet - ketik 33790 - klik kanan - follow - tcp stream - cari kolom find - ketik artist=3 ( cari sampai benar max kitik di kolom find ketik artist=1-10 misal , dan sampai benar habis/ tdk tersisa )

Siapa nama artis kedua? Blad3
cari kolom find - ketik artist=2  Blad3

Kesimpulan
Selamat!  Anda baru saja menyelesaikan ruangan "Wireshark: Dasar-Dasar".  Di ruangan ini, kita telah membahas Wireshark, apa itu, bagaimana cara kerjanya, dan bagaimana menggunakannya untuk menyelidiki tangkapan lalu lintas.

Ingin mempelajari lebih lanjut? Kami mengundang Anda untuk menyelesaikan  ruang Wireshark: Packet Operations untuk meningkatkan keterampilan Wireshark Anda dengan menyelidiki paket secara mendalam.  
