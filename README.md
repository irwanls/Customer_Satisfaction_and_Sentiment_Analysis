# Airline Customer Satisfaction & Service Performance
**Customer Satisfaction & Sentiment Analysis**

## Project Overview

Proyek ini bertujuan untuk menganalisis tingkat kepuasan pelanggan dan mengevaluasi kualitas layanan maskapai penerbangan menggunakan pendekatan **Data Preprocessing, Customer Satisfaction Score (CSAT), dan Net Promoter Score (NPS)**.

Analisis dilakukan untuk mengidentifikasi atribut layanan yang memiliki tingkat kepuasan terendah, membandingkan pengalaman pelanggan berdasarkan kelas penerbangan, serta memahami area pelayanan yang membutuhkan perbaikan.

Melalui analisis berbasis data, proyek ini menghasilkan insight mengenai performa layanan maskapai dan rekomendasi yang dapat mendukung pengambilan keputusan dalam meningkatkan kualitas pelayanan serta pengalaman pelanggan.

## Dataset

Dataset yang digunakan adalah `Customer Satisfaction and Sentiment Analysis.csv`, yang terdiri dari **100.000 baris dan 25 kolom**.

Dataset mencakup beberapa informasi utama:

- **Customer Profile:** Gender, usia, dan tipe pelanggan.
- **Flight Information:** Jenis perjalanan, kelas penerbangan, dan jarak penerbangan.
- **Service Ratings:** Penilaian pelanggan terhadap layanan Wi-Fi, online booking, check-in, kenyamanan kursi, makanan dan minuman, layanan bagasi, serta atribut pelayanan lainnya.
- **Flight Delays:** Informasi keterlambatan keberangkatan dan kedatangan.
- **Customer Satisfaction:** Kategori kepuasan pelanggan berdasarkan pengalaman penerbangan.

## Project Workflow

### 1. Data Understanding & Preprocessing

Melakukan pemeriksaan dan persiapan data sebelum analisis, meliputi:

- Pemeriksaan struktur dan tipe data.
- Identifikasi missing values.
- Pengecekan data duplikat.
- Pemeriksaan konsistensi variabel kategorikal.
- Identifikasi outlier pada variabel numerik.
- Penanganan missing values menggunakan metode imputasi mean.

Berdasarkan hasil pemeriksaan, ditemukan **300 missing values** pada kolom `Arrival Delay in Minutes` yang ditangani menggunakan imputasi nilai rata-rata.

Tidak ditemukan baris duplikat maupun inkonsistensi kategori. Sementara itu, outlier pada beberapa variabel numerik dipertahankan karena dinilai masih wajar.

### 2. Customer Satisfaction Analysis

Mengukur tingkat kepuasan pelanggan menggunakan metrik **Customer Satisfaction Score (CSAT)** berdasarkan proporsi penilaian layanan dengan rating 4 atau 5.

Analisis meliputi:

- Pengukuran CSAT layanan secara keseluruhan.
- Identifikasi atribut layanan dengan CSAT terendah.
- Perbandingan tingkat kepuasan antaratribut pelayanan.
- Evaluasi kualitas layanan berdasarkan kelas penerbangan.

### 3. Net Promoter Score (NPS) Analysis

Menganalisis persebaran penilaian pelanggan menggunakan metrik NPS sebagaimana dihitung dalam proyek untuk mengidentifikasi atribut layanan yang memperoleh evaluasi negatif.

Analisis difokuskan pada:

- Perbandingan NPS berdasarkan atribut pelayanan.
- Identifikasi layanan dengan NPS negatif.
- Perbandingan NPS antar kelas penerbangan.
- Identifikasi area ketidakpuasan yang terjadi pada beberapa segmen pelanggan.

### 4. Flight Class & Service Performance Analysis

Membandingkan performa pelayanan berdasarkan tiga kelas penerbangan:

- Business Class.
- Economy Class (Eco).
- Economy Plus (Eco Plus).

Analisis menggunakan visualisasi heatmap CSAT dan NPS untuk mengidentifikasi perbedaan pengalaman pelanggan pada setiap atribut layanan.

### 5. Data Visualization

Menyajikan hasil analisis melalui dashboard dan visualisasi, meliputi:

- Distribusi penumpang berdasarkan kelas penerbangan.
- Customer Satisfaction Score.
- Net Promoter Score.
- Peringkat layanan dengan tingkat kepuasan terendah.
- Heatmap CSAT berdasarkan kelas penerbangan.
- Heatmap NPS berdasarkan kelas penerbangan.

## Key Findings

Berdasarkan hasil analisis, diperoleh beberapa temuan utama:

1. **Overall Customer Satisfaction:** CSAT layanan secara keseluruhan mencapai **48,59%**, menunjukkan bahwa kurang dari separuh penilaian atribut layanan berada pada kategori puas (rating 4 atau 5).

2. **Lowest Customer Satisfaction:** Lima atribut layanan dengan CSAT terendah adalah:
   - Inflight Wi-Fi Service: **30,99%**
   - Ease of Online Booking: **33,59%**
   - Gate Location: **36,82%**
   - Food and Drink: **45,02%**
   - Check-in Service: **47,81%**

3. **Digital Service Performance:** Inflight Wi-Fi Service memperoleh NPS sebesar **−12,36**, sedangkan Ease of Online Booking memperoleh **−8,22**. Hasil ini mengindikasikan bahwa pengalaman layanan digital merupakan salah satu area utama yang membutuhkan evaluasi.

4. **Flight Class Distribution:** Sebanyak 47,81% penumpang menggunakan Business Class, sekitar 45% menggunakan Economy Class, dan 7,2% menggunakan Economy Plus.

5. **Service Performance by Flight Class:** Business Class umumnya memperoleh tingkat kepuasan lebih tinggi. Pada atribut Seat Comfort, Business Class mencapai CSAT **68,63%**, dibandingkan Economy Class sebesar 44,42% dan Economy Plus sebesar 45,75%.

6. **Service Performance Differences:** Business Class tidak selalu memperoleh penilaian tertinggi. Pada atribut Departure/Arrival Time Convenience, Economy Class memiliki CSAT sebesar **55,62%**, lebih tinggi dibandingkan Business Class sebesar 41,53%.

7. **Wi-Fi Service Dissatisfaction:** Inflight Wi-Fi memperoleh NPS negatif pada seluruh kelas penerbangan, yaitu Business (−7,24), Economy (−17,90), dan Economy Plus (−10,99). Hal ini menunjukkan bahwa kualitas layanan Wi-Fi menjadi permasalahan yang ditemukan pada semua segmen kelas penerbangan.

## Business Recommendations

Berdasarkan hasil analisis, rekomendasi yang diberikan meliputi:

- **Improve Inflight Wi-Fi Service:** Memprioritaskan evaluasi kualitas layanan Wi-Fi selama penerbangan karena memiliki CSAT terendah dan NPS negatif di seluruh kelas.
- **Optimize Online Booking Experience:** Mengevaluasi kemudahan proses pemesanan tiket secara online untuk meningkatkan pengalaman pelanggan.
- **Focus on Economy Segments:** Memberikan perhatian khusus pada pengalaman pelanggan Economy dan Economy Plus, terutama pada layanan digital dan proses boarding.
- **Segment-Based Service Evaluation:** Melakukan evaluasi kualitas pelayanan berdasarkan atribut layanan dan kelas penerbangan, bukan hanya menggunakan skor kepuasan secara keseluruhan.

## Tools & Technologies

- **Python** — Pengolahan dan analisis data.
- **Pandas** — Data manipulation, pemeriksaan kualitas data, dan preprocessing.
- **Data Visualization Dashboard** — Penyajian metrik CSAT, NPS, dan perbandingan kualitas layanan.
- **CSAT & NPS Metrics** — Pengukuran dan evaluasi penilaian pelanggan terhadap atribut layanan.

## Conclusion

Proyek ini menunjukkan pentingnya analisis kepuasan pelanggan dalam mengevaluasi performa layanan maskapai penerbangan.

Hasil analisis menunjukkan bahwa **Overall Service CSAT sebesar 48,59%** masih menyisakan ruang perbaikan yang signifikan, terutama pada layanan Inflight Wi-Fi dan Ease of Online Booking yang memperoleh CSAT terendah serta NPS negatif.

Selain itu, perbandingan berdasarkan kelas penerbangan menunjukkan bahwa Business Class umumnya memberikan pengalaman layanan yang lebih baik, namun tidak selalu unggul pada seluruh atribut.

Temuan ini memperlihatkan bahwa evaluasi pelayanan perlu dilakukan secara spesifik berdasarkan jenis layanan dan segmen pelanggan agar rekomendasi perbaikan lebih tepat sasaran.

Secara keseluruhan, proyek ini dapat menjadi dasar pertimbangan dalam menentukan prioritas peningkatan kualitas layanan, khususnya pada pengalaman digital dan pelayanan pelanggan Economy serta Economy Plus.

---

**Author:** Irwan Lazuardi Saldeni

**Project:** Airline Customer Satisfaction & Service Performance — Customer Satisfaction and Sentiment Analysis

**Dataset:** Customer Satisfaction and Sentiment Analysis
