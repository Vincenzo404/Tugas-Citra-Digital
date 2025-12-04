Langkah-Langkah Penggunaan setiap cell

Cell 1, 2, 3 (Instalasi Dependensi)
Tujuan: Menginstal semua paket Python yang diperlukan seperti modelscope, opencv-python (untuk pemrosesan gambar), dan matplotlib (untuk menampilkan gambar).

Cell 4, 5, 6 (Kloning Repositori dan Setup Bobot)
Tujuan: Mengkloning repositori DDColor dan menyiapkan folder /content/DDColor/weights yang kemungkinan digunakan untuk menyimpan file bobot (weight file) model.

Cell 7 (Mengunduh Model)
Tujuan: Mengunduh bobot model DDColor dari ModelScope dan menyimpannya secara lokal.

Cell 9 (Menginisialisasi Pipeline)
Tujuan: Membuat objek colorizer yang merupakan pipeline untuk menjalankan tugas pewarnaan gambar. Perhatikan bahwa kode ini secara eksplisit mencoba menggunakan GPU (cuda:0). Jika perangkat Anda tidak memiliki GPU atau Anda tidak mengaturnya di Colab, ModelScope akan otomatis beralih menggunakan CPU.

Cell 13 (Upload Gambar dan Pre-processing):
Tujuan:
Menjalankan fungsi files.upload() yang akan menampilkan tombol "Choose Files". Klik tombol tersebut dan pilih satu gambar hitam putih (grayscale) dari komputer Anda. dan
Setelah diunggah, kode akan membaca gambar menggunakan OpenCV (cv2.imread) dan mengkonversinya dari format BGR (bawaan OpenCV) ke RGB (format yang diharapkan oleh Matplotlib/model).

Cell 17 & 29 (Menjalankan Model dan Mengambil Output)
Tujuan: Menerapkan model colorizer pada gambar input dan menyimpan gambar berwarna yang dihasilkan ke variabel color_img.

Cell 35 (Menampilkan Gambar)
Tujuan: Menampilkan gambar input (hitam putih) dan gambar output (berwarna) secara berdampingan untuk perbandingan.

Setelah menjalankan sel ini, Anda akan melihat visualisasi gambar asli dan gambar yang telah diwarnai.
