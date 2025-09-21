[README.md](https://github.com/user-attachments/files/22452757/README.md)
# Analisis Prioritas Bug Valorant untuk Panduan Patch Berikutnya #

## Project Overview
Tujuan proyek ini adalah untuk menganalisis laporan bug pemain Valorant untuk menghasilkan "insight" yang dapat membantu developer memilih perbaikan mana yang harus diprioritaskan dalam patch berikutnya. Proyek ini menggunakan Large Language Model (LLM) IBM Granite untuk mengkategorikan setiap laporan bug berdasarkan dampaknya, mulai dari bug kecil hingga bug yang merusak game.

Hasil klasifikasi ini kemudian divisualisasikan untuk memberikan gambaran luas tentang situasi yang paling sering dihadapi pemain. Tujuannya adalah untuk memberikan rekomendasi berbasis data tentang di mana developer harus menempatkan sumber daya perbaikan mereka untuk meningkatkan kepuasan pemain secara maksimal.

## Raw Dataset Link
Analisis ini menggunakan dataset Valorant Metacritic Reviews, yang merupakan kumpulan ulasan teks pemain.
Tautan: (https://www.kaggle.com/datasets/andrewmvd/valorant-metacritic-reviews)

## Insight & Findings
Analisis laporan "bug" pemain Valorant menunjukkan distribusi masalah yang menarik yang didasarkan pada tingkat dampaknya. Hasil utama penelitian ini adalah:

Bug yang paling sering dilaporkan oleh pemain adalah annoying dan player-disadvantage bug, bukan bug yang merusak total permainan (Game-Breaking).

Ini menunjukkan bahwa sebagian besar frustrasi pemain berasal dari masalah yang mengganggu pengalaman bermain secara konsisten, seperti masalah UI, dan kejadian yang terasa tidak adil selama pertarungan, seperti registrasi hit atau kegagalan keterampilan.

### Visualisasi Distribusi Bug
Grafik di bawah ini memvisualisasikan frekuensi setiap kategori dampak *bug* yang dilaporkan, dengan jelas menunjukkan dominasi `Annoying Bug` dan `Player-Disadvantage Bug` dalam data yang dianalisis.

Distribusi Laporan Bug Berdasarkan Tingkat Dampak : https://drive.google.com/file/d/17nmdb3lF3PekA7DRqo98ZKJZqaBjZ5v3/view?usp=sharing

## AI Support Explanation
Dalam proyek ini, dukungan AI digunakan dalam dua tahap analisis yang kompleks:

 1. Klasifikasi Bug Berbasis Dampak: Kami menggunakan model IBM Granite ("ibm-granite/granite-3.3-8b-instruct") dengan perintah yang dirancang khusus untuk memungkinkan AI berfungsi sebagai reviewer game profesional.  Metode ini memungkinkan AI untuk: mengklasifikasikan tingkat keparahannya secara akurat (misalnya, bug Player-Disadvantage atau bug Game-Breaking); dan menganalisis dan merangkum masalah utama dari setiap laporan dalam format "The Breakdown".

 2. Analisis Data Otomatis (Percobaan): Kami mencoba menganalisis data menggunakan LangChain Pandas Agent.  Proses ini menunjukkan kemampuan agen kecerdasan buatan untuk memahami perintah, menulis kode, dan bahkan melakukan "debugging" secara mandiri ketika terjadi kesalahan.  Namun, data yang telah berhasil diklasifikasikan pada tahap pertama merupakan sumber analisis dan visualisasi akhir proyek ini.
