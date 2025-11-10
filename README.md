Steam Deal Explorer

Sebuah dashboard visualisasi data interaktif untuk menemukan penawaran (deal) game terbaik di Steam, dibuat sebagai bagian dari Proyek A4.

Demo Interaktif

Visualisasi ini di-hosting menggunakan GitHub Pages. Anda bisa mengakses dan berinteraksi dengan versi livenya di sini:

https://edrilmarfadli.github.io/SteamDealExplorer/steam_deal_explorer.html

Deskripsi Proyek

Seringkali sulit untuk menemukan game yang bagus sekaligus murah di Steam. Diskon besar (misalnya -80%) belum tentu berarti gamenya bagus (bisa jadi ulasannya 'Mixed'). Sebaliknya, game berkualitas tinggi (ulasan 'Overwhelmingly Positive') mungkin jarang diskon.

Steam Deal Explorer adalah alat bantu untuk mengatasi masalah ini. Dashboard interaktif ini memungkinkan pengguna untuk memfilter ribuan game Steam berdasarkan:

- Harga

- Persentase Diskon

- Kualitas Ulasan (Recent Reviews)

- Judul Game

Tujuannya adalah untuk membantu pengguna mendefinisikan "penawaran terbaik" versi mereka sendiri dan menemukan game berkualitas tinggi yang sesuai dengan budget mereka.

Fitur Utama

Filter Interaktif: Cari berdasarkan judul, atur slider untuk rentang harga dan persentase diskon.

Filter Kualitas: Pilih satu atau beberapa kategori ulasan (misalnya, hanya tampilkan game 'Overwhelmingly Positive' dan 'Very Positive').

Scatter Plot (Harga Asli vs. Harga Diskon): Visualisasi yang kuat untuk melihat seberapa besar penghematan Anda. Semakin jauh titik dari garis diagonal, semakin bagus penawarannya.

Histogram Distribusi Diskon: Melihat seberapa umum diskon (misalnya -50%, -75%) pada game yang Anda filter.

Bar Chart (Diskon vs. Ulasan): Menjawab pertanyaan, "Apakah game dengan ulasan bagus mendapat diskon lebih kecil?"

Daftar 'Top Savings': Daftar game yang sudah terfilter, diurutkan berdasarkan jumlah uang (dalam dolar) yang paling banyak Anda hemat.

---------------------------------------- DELIVERABLES ------------------------------------------------------
1. A rationale for your design decisions:
A. Mengapa memilih visual encoding ini:
- Scatter plot dipilih karena paling efektif menunjukkan hubungan antara harga asli dan harga diskon. Games yang “diskonnya besar” langsung terlihat jauh di bawah garis diagonal (baseline).
- Histogram digunakan karena bentuknya paling tepat untuk menunjukkan sebaran diskon secara keseluruhan dan mudah dibaca.
- Bar chart dipilih karena mudah membandingkan kategori sentiment review dan melihat apakah sentiment tertentu cenderung mendapat diskon lebih besar.
B. Kenapa memilih interaction techniques ini:
- Zoom & pan dipilih karena pengguna perlu memeriksa area tertentu dari scatter yang bisa sangat padat.
- Dynamic query filters (search, slider harga, slider diskon, filter sentiment) dipilih karena sangat mendukung eksplorasi mandiri tanpa reload halaman.
- Tooltip dipilih sebagai details-on-demand supaya informasi game tetap tersedia tanpa membuat visualisasi penuh teks.
C. Kenapa memilih Plotly.js dan bukan D3.js
- Plotly menawarkan interaksi dasar seperti zoom, pan, hover, filter update, dan transisi secara otomatis.
- Plotly mempercepat implementasi sehingga fokus dapat diberikan pada logika interaksi, bukan low-level DOM manipulasi seperti D3.
- Plotly menghasilkan UI yang bersih dengan lebih sedikit kode, cocok untuk timeline tugas dua minggu
Intinya, plotly lebih mudah digunakan dan sederhana.

2. Overview of Development Process
- Pembagian Kerja

1. Edril Marfadli : Dataset & csv
2. Aqilah Fikry Albari: HTML
3. Fairuz Afif Herdanto : Analisis Data Awal & Validasi
4. Gilang Yanuar : Desain UI/UX & Styling
5. Reggy Firmansyah: Dokumentasi dan pengujian
   
- Estimasi Waktu Pengerjaan

Total waktu pengerjaan sekitar 4-5 jam.

- Bagian yang Paling Banyak Memakan Waktu
Beberapa bagian yang memakan waktu:
1. Menentukan jenis visualisasi yang paling sesuai dengan data, terutama karena dataset tidak memiliki kolom genre atau jumlah review numerik.
2. Mengonversi harga dan diskon menjadi nilai numerik serta menghitung perkiraan harga asli setiap game.
3. Mengimplementasikan sistem filter dinamis yang memengaruhi tiga grafik sekaligus (scatter, histogram, bar chart).
4. Mengatur tampilan agar mirip gaya Steam dengan tetap menjaga keterbacaan dan responsivitas.

- Komentar Terhadap Proses Pengembangan

Proses dimulai dengan eksplorasi dataset untuk memahami variabel apa saja yang memungkinkan dijadikan insight. Setelah mengetahui keterbatasan data, fokus dialihkan ke relasi harga–diskon–sentiment. Tahap berikutnya adalah membuat struktur visualisasi dan kontrol interaksinya. Implementasi dilakukan secara bertahap: mulai dari scatter plot, lalu histogram, bar chart, hingga panel daftar “Top Savings”. Setelah visualisasi berfungsi, dilakukan beberapa iterasi untuk memperbaiki tampilan, memastikan transisi antar filter berjalan mulus, dan menyesuaikan warna agar konsisten dengan tema Steam. Proses ini berjalan secara iteratif hingga dashboard mencapai bentuk final yang stabil dan mudah digunakan.

---------------------------------------- DELIVERABLES ------------------------------------------------------

Sumber Data

Dataset utama: steam_store_data_2024.csv

Data di-pre-processing dan di-embed langsung ke dalam file .html untuk mempermudah hosting dan performa.
