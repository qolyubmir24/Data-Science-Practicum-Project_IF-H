# Deteksi Anomali Trafik Jaringan untuk Identifikasi Serangan DDoS

## Identitas Kelompok

| Keterangan | Informasi |
|---|---|
| Nomor Kelompok | 60 |
| Nama Kelompok | Semoga Wowok Keselek Asap |
| Mata Kuliah | Praktikum Data Science |

## Ringkasan Proyek

Proyek ini bertujuan menguji kemampuan model klasifikasi dalam membedakan aliran trafik jaringan normal (`BENIGN`) dan trafik serangan `DDoS` berdasarkan karakteristik aliran trafik jaringan.

Proyek menggunakan pendekatan **supervised learning** dengan tugas **klasifikasi biner**. Algoritma yang direncanakan untuk digunakan adalah **Random Forest**. Kinerja model akan dievaluasi menggunakan accuracy, precision, recall, F1-score, dan confusion matrix.

Pengerjaan mengikuti tahapan data science, mulai dari Business Understanding, Data Gathering, Exploratory Data Analysis (EDA), Cleaning, dan Preprocessing. Tahap Modelling, Evaluasi, dan Konklusi akan dilengkapi pada pengembangan notebook berikutnya.

## Anggota Kelompok dan Kontribusi

| No. | Nama Anggota | NIM | Kontribusi (rancangan pembagian tugas) |
|---|---|---|---|
| 1 | Mirwan Qolyubi | 123240116 | Mengkoordinasikan pengerjaan proyek; menyusun Business Understanding dan tujuan klasifikasi; memimpin analisis EDA serta penentuan strategi cleaning dan preprocessing; mengintegrasikan notebook; meninjau konsistensi hasil analisis dan dokumentasi proyek. |
| 2 | Naufal Alwi Rizqillah | 123240215 | Membantu penelusuran sumber dan verifikasi informasi dataset; menyiapkan serta memeriksa proses pemuatan dataset; membantu analisis distribusi kelas dan karakteristik fitur; meninjau hasil preprocessing. |
| 3 | Aulia Cahaya Ramadhany | 123240192 | Membantu eksplorasi data; menyusun visualisasi dan ringkasan statistik untuk EDA; memeriksa kelengkapan penjelasan hasil analisis; membantu penyusunan dokumentasi repository. |
| 4 | Muhammad Arjun Nabila | 123240156 | Membantu pemeriksaan kualitas data, seperti missing values, duplikasi, nilai tak hingga, dan nilai tidak valid; meninjau langkah cleaning; membantu pengujian ulang notebook dan pemeriksaan struktur repository. |

## Dataset

Dataset yang digunakan adalah file `Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv` yang diperoleh melalui Kaggle.

- **Nama dataset:** Friday-WorkingHours-Afternoon-DDos
- **Pengunggah Kaggle:** `ishasingh03`
- **Sumber unduhan:** [Kaggle - Friday-WorkingHours-Afternoon-DDos](https://www.kaggle.com/datasets/ishasingh03/friday-workinghours-afternoon-ddos)
- **Nama file:** `Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv`
- **Format:** CSV
- **Target:** `Label`
- **Kelas target:** `BENIGN` dan `DDoS`
- **Lisensi yang dicantumkan pada halaman dataset:** Apache License 2.0

File yang digunakan memiliki 225.745 baris dan 85 kolom, yang terdiri dari 84 kolom fitur dan satu kolom target (`Label`). Dataset berisi karakteristik aliran trafik jaringan, seperti durasi aliran, jumlah dan ukuran paket, laju trafik, interval kedatangan paket, TCP flags, serta periode aktif dan tidak aktif.

Berdasarkan nama file dan karakteristik dataset, data yang digunakan berkaitan dengan CICIDS2017. Dokumentasi CICIDS2017 dapat dilihat pada [Canadian Institute for Cybersecurity](https://www.unb.ca/cic/datasets/ids-2017.html). Dokumentasi fitur aliran dapat dilihat pada [CICFlowMeter](https://github.com/ahlashkari/CICFlowMeter/blob/master/ReadMe.txt).

## Struktur Repository

Letakkan notebook dan file CSV pada direktori yang sama karena kode pemuatan dataset menggunakan nama file relatif.

```text
Deteksi-Anomali-DDoS/
├── README.md
├── Semoga Wowok Keselek Asap.ipynb
└── Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv
```

Apabila nama notebook atau file CSV di repository berbeda, sesuaikan nama file pada struktur di atas dan path pada kode notebook.

## Cara Menjalankan Proyek

### Persyaratan

- Python 3.9 atau versi lebih baru.
- Jupyter Notebook/JupyterLab atau Visual Studio Code dengan ekstensi Jupyter.
- File dataset CSV yang telah disediakan pada repository.

### Instalasi Library

Jalankan perintah berikut pada terminal:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Menjalankan Notebook

1. Unduh atau clone repository ke komputer.
2. Pastikan file notebook dan file CSV berada pada direktori yang sama.
3. Buka folder repository menggunakan Visual Studio Code atau jalankan Jupyter Notebook.
4. Buka file `Semoga Wowok Keselek Asap.ipynb`.
5. Pilih kernel Python yang memiliki library pada bagian Persyaratan.
6. Jalankan seluruh sel notebook secara berurutan menggunakan **Run All**.

Notebook akan memuat dataset, melakukan Business Understanding dan Data Gathering, mengeksplorasi karakteristik data, membersihkan data, melakukan seleksi fitur, serta menyiapkan data latih dan data uji.

## Catatan

- Pastikan nama file CSV sesuai dengan path yang digunakan pada notebook.
- Hasil EDA dan preprocessing bergantung pada file dataset yang digunakan.
- Proyek ini merupakan eksperimen klasifikasi berbasis dataset dan tidak mencakup deployment atau deteksi trafik secara real-time.
- Setiap anggota kelompok bertanggung jawab memahami proses, kode, alasan pengambilan keputusan, dan hasil yang disajikan dalam notebook.
