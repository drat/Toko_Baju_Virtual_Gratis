# Toko Baju Virtual - Virtual Try-On in the Wild

## Saatnya Kita Coba Baju Terbaik!
![Toko-Baju-Virtual-Gratis-a-Hugging-Face-Space-by-Deddy](https://github.com/user-attachments/assets/9367013d-11f3-47b0-ada6-ce1091e5cc25)

[![Open in Spaces](https://huggingface.co/datasets/huggingface/badges/resolve/main/open-in-hf-spaces-xl.svg)](https://deddy-toko-baju-virtual-gratis.hf.space)
[![Open in Spaces](https://huggingface.co/datasets/huggingface/badges/resolve/main/open-in-hf-spaces-xl-dark.svg)](https://deddy-toko-baju-virtual-gratis.hf.space)


Aplikasi ini adalah implementasi dari teknologi **Virtual Try-On** berbasis gambar yang memungkinkan pengguna mencoba pakaian secara virtual hanya dengan mengunggah gambar diri mereka dan pakaian yang ingin dicoba. Aplikasi ini menggunakan pendekatan berbasis model difusi yang telah ditingkatkan untuk menjaga keaslian detail pakaian dan menghasilkan gambar try-on yang realistis.

### IDM-VTON: Image-based Virtual Try-On dengan Model Difusi

Makalah ini membahas tentang **Image-based Virtual Try-On**, yaitu teknik yang menampilkan gambar seseorang yang mengenakan pakaian tertentu, berdasarkan pasangan gambar yang menunjukkan orang tersebut dan pakaian yang ingin dicoba. Karya-karya sebelumnya mengadaptasi model difusi inpainting berbasis contoh yang sudah ada untuk try-on virtual guna meningkatkan kealamian visual yang dihasilkan dibandingkan metode lain (misalnya, berbasis GAN), namun mereka gagal menjaga identitas pakaian. Untuk mengatasi keterbatasan ini, kami mengusulkan model difusi baru yang meningkatkan kesetiaan pakaian dan menghasilkan gambar try-on virtual yang autentik.

![teaser2](https://github.com/user-attachments/assets/c734e450-d8a9-486d-a184-33543ba6b996)

Metode kami, yang disebut **IDM-VTON**, menggunakan dua modul berbeda untuk mengkodekan semantik gambar pakaian; pada UNet dasar dari model difusi:
1. Semantik tingkat tinggi yang diekstraksi dari visual encoder diintegrasikan ke dalam lapisan cross-attention.
2. Fitur tingkat rendah yang diekstraksi dari UNet paralel diintegrasikan ke dalam lapisan self-attention.

Selain itu, kami menyediakan prompt tekstual yang terperinci untuk gambar pakaian dan orang guna meningkatkan keaslian visual yang dihasilkan. Terakhir, kami menyajikan metode kustomisasi menggunakan pasangan gambar orang-pakaian, yang secara signifikan meningkatkan kesetiaan dan keaslian. Hasil eksperimen kami menunjukkan bahwa metode kami mengungguli pendekatan sebelumnya (baik yang berbasis difusi maupun GAN) dalam menjaga detail pakaian dan menghasilkan gambar try-on virtual yang autentik, baik secara kualitatif maupun kuantitatif. Selain itu, metode kustomisasi yang diusulkan menunjukkan efektivitasnya dalam skenario dunia nyata.

## Fitur Utama
- **Virtual Try-On:** Coba pakaian secara virtual dengan mengunggah gambar diri Anda dan pakaian.
- **Teknologi Difusi:** Menggunakan model difusi untuk menghasilkan visual yang realistis dan autentik.
- **Preservasi Detail Pakaian:** Memastikan bahwa detail dan identitas pakaian tetap terjaga dalam gambar yang dihasilkan.
- **Kustomisasi Otentik:** Menyediakan fitur kustomisasi untuk menyesuaikan hasil try-on dengan preferensi pengguna.

## Instalasi

Untuk menjalankan aplikasi ini, Anda perlu menginstal dependensi berikut. Anda dapat melakukannya dengan menjalankan:

```bash
pip install -r requirements.txt
```

## Cara Penggunaan

1. Jalankan aplikasi menggunakan perintah berikut:

   ```bash
   python app.py
   ```

2. Buka antarmuka web di browser Anda.
3. Unggah gambar Anda di bagian "Person Image".
4. Unggah gambar pakaian yang ingin dicoba di bagian "Garment Image".
5. Klik tombol "Try On" untuk melihat hasilnya.

## Referensi dan Sumber

- [Halaman Proyek](https://idm-vton.github.io/)
- [GitHub Repository](https://github.com/yisol/IDM-VTON?tab=readme-ov-file)
- Jurnal Ilmiah: ["Improving Diffusion Models for Authentic Virtual Try-on in the Wild"](https://arxiv.org/abs/2403.05139)

## Lisensi

Proyek ini dilisensikan di bawah lisensi MIT. Lihat file [LICENSE](LICENSE) untuk informasi lebih lanjut.

### Penjelasan:
- **Deskripsi Proyek:** Memberikan gambaran umum tentang aplikasi dan teknologi yang digunakan.
- **Fitur Utama:** Menyoroti fitur-fitur yang menonjol dari aplikasi.
- **Instalasi:** Instruksi singkat tentang cara menginstal dependensi.
- **Cara Penggunaan:** Langkah-langkah dasar untuk menjalankan aplikasi dan mencobanya.
- **Referensi dan Sumber:** Menyediakan link ke halaman proyek, repositori GitHub, dan jurnal ilmiah terkait.
- **Lisensi:** Bagian ini mengacu pada lisensi proyek (disesuaikan dengan lisensi yang Anda gunakan).

Terima kasih.
-**Deddy Ratnanto**-
