# 1. Introduction

## 1.1 Purpose

Tujuan dari dokumen *Software Requirements Specification* (SRS) ini adalah untuk memberikan deskripsi yang lengkap dan terperinci mengenai perangkat lunak untuk sistem **ATLAS (Decentralized P2P Train Telemetry & Braking Alert System)**.

Dokumen ini secara spesifik mendefinisikan seluruh persyaratan fungsional dan non-fungsional, antarmuka eksternal, serta batasan operasional dari ATLAS. ATLAS dirancang sebagai sistem keselamatan transportasi nirkabel jarak jauh yang memantau dan bertukar data telemetri kereta api secara *real-time* (meliputi koordinat posisi satelit, kecepatan, arah pergerakan, dan status pengereman) serta memicu peringatan dini (visual dan audio) kepada masinis ketika parameter jarak aman tabrakan terlewati. Sistem ini beroperasi penuh secara terdesentralisasi (*peer-to-peer*) menggunakan teknologi komunikasi LoRa dan koreksi posisi presisi tinggi GPS RTK, sehingga memungkinkan kereta mendeteksi ancaman di area *blind spot* tanpa memerlukan ketergantungan pada infrastruktur server pusat atau jaringan seluler.

Dokumen SRS ini ditujukan untuk digunakan oleh berbagai pihak, meliputi:
1. **Tim Pengembang dan Arsitek Sistem (Hardware & Software):** Sebagai panduan teknis utama dan acuan referensi dalam merancang arsitektur *node* perangkat keras, mengimplementasikan algoritma pemrosesan telemetri, serta membangun integrasi ke sistem *automatic braking*.
2. **Tim Penguji (Quality Assurance & Testers):** Sebagai landasan (*baseline*) untuk menyusun rencana pengujian (*test plans*), skenario validasi, dan verifikasi untuk memastikan sistem selalu memberikan respon peringatan yang akurat dalam berbagai kondisi lapangan.
3. **Pemangku Kepentingan (Stakeholders) dan Petugas Keselamatan Perkeretaapian:** Untuk mengevaluasi keselarasan desain sistem dengan tujuan operasional dan memastikan bahwa implementasi ATLAS telah memenuhi kaidah serta standar keselamatan perkeretaapian yang berlaku.
