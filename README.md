🎮 Steam Deal Explorer
Sebuah dashboard visualisasi data interaktif untuk menemukan penawaran (deal) game terbaik di Steam, dibuat sebagai bagian dari Proyek A4.

🚀 Demo Interaktif
Visualisasi ini di-hosting menggunakan GitHub Pages. Anda bisa mengakses versi livenya di sini:

https://<NAMA-PENGGUNA-ANDA>.github.io/<NAMA-REPO-ANDA>/steam_deal_explorer.html

(PENTING: Ganti <NAMA-PENGGUNA-ANDA> dan <NAMA-REPO-ANDA> dengan nama pengguna dan nama repositori GitHub Anda)

📖 Tentang Proyek Ini
Seringkali sulit untuk menemukan game yang bagus sekaligus murah di Steam. Diskon besar (misalnya -80%) belum tentu berarti gamenya bagus (bisa jadi ulasannya 'Mixed' atau 'Mostly Negative'). Sebaliknya, game berkualitas tinggi (ulasSAn 'Overwhelmingly Positive') mungkin jarang diskon.

Steam Deal Explorer adalah alat bantu untuk mengatasi masalah ini. Dashboard interaktif ini memungkinkan pengguna untuk memfilter ribuan game Steam berdasarkan:

- Harga

- Persentase Diskon

- Kualitas Ulasan (Recent Reviews)

- Judul Game

Tujuannya adalah untuk membantu pengguna menemukan game berkualitas tinggi yang sesuai dengan budget dan diskon yang mereka inginkan.

📸 Tampilan
(Sangat disarankan Anda mengambil screenshot dari dashboard Anda dan menambahkannya di sini. Ini membuat README Anda terlihat jauh lebih profesional.)

✨ Fitur Utama
Filter Interaktif: Cari berdasarkan judul, atur slider untuk rentang harga dan persentase diskon.

Filter Kualitas: Pilih satu atau beberapa kategori ulasan (misalnya, hanya tampilkan game 'Overwhelmingly Positive' dan 'Very Positive').

Scatter Plot (Harga Asli vs. Harga Diskon): Visualisasi yang kuat untuk melihat seberapa besar penghematan Anda. Semakin jauh titik dari garis diagonal, semakin bagus penawarannya.

Histogram Distribusi Diskon: Melihat seberapa umum diskon (misalnya -50%, -75%) pada game yang Anda filter.

Bar Chart (Diskon vs. Ulasan): Menjawab pertanyaan, "Apakah game dengan ulasan bagus mendapat diskon lebih kecil?"

Daftar 'Top Savings': Daftar game yang sudah terfilter, diurutkan berdasarkan jumlah uang (dalam dolar) yang paling banyak Anda hemat.

💻 Teknologi yang Digunakan
HTML5

CSS3 (Styling kustom yang terinspirasi dari tema Steam)

JavaScript (Vanilla): Untuk logika filtering dan menghubungkan kontrol.

Plotly.js: Library JavaScript yang digunakan untuk membuat semua chart interaktif.

📊 Sumber Data
Dataset utama: steam_store_data_2024.csv

Data di-pre-processing dan di-embed langsung ke dalam file .html untuk mempermudah hosting dan performa.

🏃 Menjalankan Secara Lokal
Karena semua library (Plotly.js) dan data sudah tertanam di dalam file steam_deal_explorer.html, Anda tidak perlu menjalankan web server lokal.

Clone atau unduh repositori ini.

Buka file steam_deal_explorer.html di browser favorit Anda.
