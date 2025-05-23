# PerancanganWeb-DesainGrafis-BisDigrafis-BisDig

file:///C:/xampp/htdocs/xampp/nandacantik/Untitled-2%20copy.html

# PerancanganWeb-DesainGrafis-BisDig

Repositori ini berisi berbagai contoh implementasi komponen dan fitur web sederhana, serta penjelasan mengenai konsep dasar perancangan web dan desain grafis.

---

## Konsep Responsive Design dan Media Queries

Bagian ini menjelaskan pentingnya **Responsive Design** dalam pengembangan web modern, yang memungkinkan situs web beradaptasi dengan berbagai ukuran layar dan perangkat.

### Responsive Design
Pendekatan ini berfokus pada fleksibilitas *layout* menggunakan:
* **Grid Fleksibel:** Penggunaan unit relatif (`%`, `em`, `rem`, `vw`, `vh`) untuk ukuran elemen.
* **Gambar Fleksibel:** Gambar yang menyesuaikan ukurannya secara proporsional (misalnya, `max-width: 100%;`).
* **Media Queries:** Aturan CSS yang diterapkan berdasarkan karakteristik perangkat.

### Media Queries
*Media queries* adalah fitur CSS3 yang memungkinkan penerapan gaya berbeda berdasarkan kondisi seperti lebar *viewport*, tinggi, orientasi, atau resolusi perangkat. Sintaks dasarnya adalah `@media media_type and (feature: value) { ... }`. Ini memungkinkan desainer untuk mendefinisikan *breakpoint* di mana *layout* akan berubah untuk mengoptimalkan pengalaman pengguna.

---

## Contoh Layout Gambar Fleksibel (Responsive Image Gallery)

Contoh ini menunjukkan bagaimana *responsive design* dan *media queries* dapat digunakan untuk membuat *layout* galeri gambar yang secara otomatis menyesuaikan jumlah kolom berdasarkan lebar layar.

### Struktur Kode:
* **`index.html`**: Berisi struktur dasar halaman dan wadah untuk galeri gambar (`.gallery-container`) dengan beberapa item gambar (`.gallery-item`). File ini juga menautkan ke `styles.css`.
* **`styles.css`**: File ini berisi semua aturan CSS, termasuk penggunaan Flexbox untuk *layout* dan *media queries* untuk menyesuaikan jumlah kolom:
    * **Mobile-First:** Awalnya, setiap gambar akan menempati satu kolom penuh (`100%` lebar) di layar kecil.
    * **Tablet (`min-width: 768px`):** *Layout* berubah menjadi 2 kolom.
    * **Desktop (`min-width: 1024px`):** *Layout* berubah menjadi 3 kolom.
    * **Large Desktop (`min-width: 1440px`):** *Layout* berubah menjadi 4 kolom.
    * Penggunaan `flex: 1 1 calc(X% - gap)` dan `gap` memastikan *layout* fleksibel dengan jarak antar gambar yang konsisten.

### Cara Menggunakan:
1.  Buka file `index.html` di browser web Anda.
2.  Coba ubah ukuran jendela browser Anda (atau gunakan fitur *developer tools* untuk mensimulasikan ukuran perangkat yang berbeda) untuk melihat bagaimana *layout* gambar beradaptasi secara dinamis.
