# Tugas-2-Social-Media-Analysis

### Tugas 2: Scraping Keyword "Prabowo" dari Media Sosial
# Latar Belakang Pemilihan Keyword "Prabowo" 

Untuk tugas kedua, saya memilih kata kunci Ferry Irwandi, Gibran, dan Kemenkeu karena::

1. Signifikansi dan Relevansi Publik

    Ferry Irwandi merupakan figur yang mulai dikenal publik melalui perannya dalam dunia politik/pemerintahan, sehingga relevan untuk dianalisis dalam konteks wacana publik.

    Gibran Rakabuming Raka, sebagai Wakil Presiden Indonesia, merupakan tokoh nasional yang kerap menjadi sorotan media dan perbincangan masyarakat, baik terkait kebijakan maupun aktivitas politiknya.

    Kementerian Keuangan (Kemenkeu) adalah lembaga vital negara yang kebijakannya berdampak langsung pada perekonomian nasional, sehingga selalu menjadi topik penting di media sosial maupun pemberitaan.

2. Memenuhi Kebutuhan Volume Data
    Popularitas tokoh publik dan lembaga negara ini menjamin ketersediaan data dalam jumlah besar. Diskusi mengenai Gibran sebagai wapres, kebijakan Kemenkeu, maupun keterlibatan Ferry Irwandi dalam isu tertentu memudahkan pencapaian target minimal 1.000 baris data.

3. Potensi Analisis yang Kaya
    Topik ini sarat dengan opini publik yang beragam, mulai dari apresiasi, kritik, hingga diskusi kebijakan. Dengan begitu, data yang diperoleh sangat potensial untuk dianalisis lebih lanjut, misalnya melalui analisis sentimen (positif, negatif, netral), identifikasi isu strategis, hingga pemetaan persepsi publik terhadap tokoh maupun institusi terkait.

# Cara Kerja Menggunakan `Tweet Harvest` di Google Colab
Tugas kedua dieksekusi menggunakan *tool* **Tweet Harvest** di dalam lingkungan **Google Colaboratory**. Pendekatan ini dipilih karena praktis dan tidak memerlukan instalasi di komputer pribadi. Berikut alur kerjanya sesuai *notebook* yang dibuat:

1.  **Instalasi dan Setup:**
    Langkah pertama di dalam Colab adalah menginstal `Tweet Harvest` menggunakan perintah `npx`. Ini memastikan kita selalu menggunakan versi terbaru dari *tool* tersebut.

2.  **Konfigurasi Parameter Scraping:**
    Sebelum eksekusi, semua parameter yang dibutuhkan diatur dalam variabel Python agar mudah diubah:
    * **`filename`**: Nama file output diatur menjadi `'prabowo.csv'`.
    * **`search_keyword`**: Kata kunci pencarian utama diatur menjadi `'prabowo'`.
    * **`limit`**: Batas jumlah tweet yang ingin diambil diatur menjadi `1200` untuk memastikan target 1000 data terlampaui.
    * **`auth_token`**: Token autentikasi dimasukkan di sini. Token ini berfungsi sebagai kunci akses aman untuk masuk ke akun X (Twitter) tanpa harus menggunakan *username* dan *password* secara langsung di dalam kode.

3.  **Eksekusi Perintah Scraping:**
    Perintah inti dijalankan menggunakan `os.system()`. Kode ini secara dinamis menggabungkan semua variabel yang sudah diatur sebelumnya menjadi satu perintah terminal yang lengkap. Perintah inilah yang menyuruh `Tweet Harvest` untuk mulai bekerja: membuka browser virtual, melakukan pencarian, men-*scroll* halaman, dan "memanen" data.

4.  **Hasil Akhir:**
    Setelah proses selesai, `Tweet Harvest` secara otomatis menghasilkan file `prabowo.csv` di dalam lingkungan penyimpanan Google Colab. File ini berisi ribuan baris data tweet, lengkap dengan berbagai metadata berharga seperti isi tweet, *username*, waktu posting, jumlah *likes*, jumlah *retweet*, dan lainnya, yang siap untuk diunduh dan dianalisis.
