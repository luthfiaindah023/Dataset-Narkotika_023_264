# Dataset-Narkotika_023_264

# 🏛️ Dataset Putusan Pengadilan: Narkotika dan Psikotropika - Pengadilan Negeri Jakarta Utara (2024)
Dataset ini mengumpulkan 50 putusan dari Pengadilan Negeri Jakarta Utara pada tahun 2024 dalam kategori Narkotika dan Psikotropika. Data ini berasal dari Direktori Putusan Mahkamah Agung RI, yang merupakan sumber resmi untuk akses publik putusan pengadilan di Indonesia. Dataset ini dirancang untuk mendukung analisis hukum, pemrosesan bahasa alami, dan studi terkait hukum pidana khusus.

🌐 Tentang Dataset
Dataset ini berfokus pada kasus PIDANA KHUSUS - Narkotika dan Psikotropika, dengan fitur-fitur berikut:

No Putusan: Nomor unik setiap putusan pengadilan.
Lembaga Peradilan: Nama lembaga yang memutuskan perkara; di sini adalah Pengadilan Negeri Jakarta Utara.
Barang Bukti: Jenis dan rincian barang bukti yang disita dalam setiap kasus.
Amar Putusan: Ringkasan keputusan atau hukuman yang dijatuhkan, seperti penjara, rehabilitasi, atau denda.
Catatan: Dataset ini hanya contoh untuk tujuan edukasi dan penelitian.

🔍 Sekilas Data
No Putusan	Lembaga Peradilan	Barang Bukti	Amar Putusan
1245/Pid.Sus/2024/PN	Pengadilan Negeri Jakarta Utara	12 gram sabu, alat hisap	Penjara 7 tahun, denda Rp2.000.000
1267/Pid.Sus/2024/PN	Pengadilan Negeri Jakarta Utara	20 butir ekstasi	Rehabilitasi, pengawasan ketat
Data ini mendukung eksplorasi lebih lanjut terkait pola putusan, tingkat hukuman, dan pengaruh barang bukti terhadap keputusan pengadilan.

🛠️ Panduan Pengolahan Data
Persiapan Data: Dataset disiapkan dalam format Excel dan memerlukan beberapa tahap preprocessing.
Preprocessing Teks: Pengolahan teks termasuk normalisasi dan penghilangan karakter khusus, serta lemmatization untuk analisis lebih lanjut.
Indexing: Data diindeks menggunakan teknik TF-IDF agar siap untuk pencarian dan analisis kata kunci dalam dokumen hukum.
Contoh Kode untuk Preprocessing dan Indexing:

python
Copy code
import pandas as pd
from sklearn.feature_extraction.text import TfidfVectorizer

# Membaca dataset
df = pd.read_excel('dataset.xlsx')
df['processed_text'] = preprocess_text(df['putusan_text'])

# Penerapan TF-IDF untuk indexing
tfidf_vectorizer = TfidfVectorizer()
tfidf_matrix = tfidf_vectorizer.fit_transform(df['processed_text'])
📈 Aplikasi dan Potensi Penggunaan
Dataset ini memiliki berbagai potensi aplikasi, antara lain:

Analisis Pola Putusan: Memahami keputusan hakim berdasarkan jenis barang bukti atau faktor lainnya.
Pengembangan Model NLP Hukum: Melatih model pemrosesan bahasa alami untuk mengenali pola putusan dan prediksi hasil kasus.
Pembelajaran Hukum Pidana: Bahan latihan untuk mahasiswa dan peneliti hukum pidana di bidang pendidikan.
📂 Struktur Proyek
bash
Copy code
📂 dataset
├── dataset.xlsx              # Data utama dalam format Excel
├── preprocessing_indexing.py # Skrip Python untuk preprocessing dan indexing
└── README.md                 # Dokumentasi dataset
⚖️ Lisensi
Dataset ini disediakan hanya untuk tujuan edukasi dan penelitian. Penggunaan komersial atau publikasi data ini harus mendapat izin dari Direktori Putusan Mahkamah Agung RI.
