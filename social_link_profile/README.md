# 🌐 Frontend Mentor — Social Links Profile  
**Solusi oleh Alid**

Selamat datang! Ini adalah solusi saya untuk challenge **Social Links Profile** dari  
[Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ).  
Challenge ini sederhana namun sangat efektif untuk melatih struktur HTML, styling dengan CSS, dan interaksi ringan menggunakan JavaScript.

---

## 🖼️ Hasil Akhir

### 💻 Tampilan Desktop
![Desktop Screenshot](./screenshot-desktop.png)

### 📱 Tampilan Mobile
![Mobile Screenshot](./screenshot-mobile.png)

---

## 🔗 Link Proyek

- 🌐 **Live Site:** https://your-live-site-url.com  
- 📁 **Solution URL:** https://your-solution-url.com  
- 👤 **Profil Frontend Mentor:** https://www.frontendmentor.io/profile/yourusername  

---

# 🧩 Tentang Challenge

Tujuan dari challenge ini adalah mereplikasi tampilan kartu profil social-link sesuai desain yang diberikan.  
Meski terlihat simpel, challenge ini menuntut:

- Konsistensi styling  
- Penggunaan spacing yang akurat  
- Responsivitas di berbagai ukuran layar  
- Efek hover yang sesuai  
- Struktur HTML yang bersih  
- Kesetiaan pada desain (pixel-perfect-ish)

Challenge ini sangat cocok untuk level **newbie — junior**, tapi tetap menantang bila ingin membuat versi yang lebih interaktif.

---

# ⚙️ Fitur yang Saya Tambahkan

Walaupun desain aslinya hanya membutuhkan HTML + CSS, saya menambahkan sentuhan modern:

### ✨ 1. **Animasi Fade-in**
Card muncul dengan transisi halus ketika halaman dimuat.

### 🌊 2. **Ripple Effect pada Tombol**
Setiap tombol memiliki efek gelombang saat diklik—memberi kesan profesional & modern.

### 🎨 3. **Hover State Lebih Halus**
Transisi warna tombol dibuat smooth, tanpa mengubah desain asli.

### 📱 4. **Responsif 100%**
Dapat dibuka dengan nyaman di HP maupun laptop.

### 🔄 5. **File dan Struktur yang Rapi**
- `index.html`
- `style.css`
- `script.js`
- `/assets/images/...`

---

# 🛠️ Teknologi yang Digunakan

### 🧱 **Front-end**
- **HTML5 (Semantic elements)**
- **CSS3**
  - Flexbox
  - Custom properties
  - Responsive units
  - CSS animation & keyframes
- **JavaScript Vanilla**
  - DOM manipulation
  - Event listener
  - Custom ripple animation

### 🎨 **Desain**
- Warna berdasarkan *style-guide* challenge  
- Font: **Inter** (400, 600, 700)  
- Mobile-first workflow  

### 🔧 Tools Pengembangan
- VS Code  
- Live Server  
- Git & GitHub  
- Frontend Mentor Assets  

---

# 🧠 Apa yang Saya Pelajari

Challenge ini ternyata memberi beberapa insight penting:

### 1️⃣ **Mengatur Layout Card**
Menggabungkan vertical centering + responsive behavior butuh kombinasi:
- `flex`
- `min-height: 100dvh`
- padding adaptif

### 2️⃣ **Membuat Komponen Reusable**
Setiap tombol dibuat dengan class `.btn` → mudah diatur & seragam.

### 3️⃣ **Animasi Interaktif dengan JS**
Saya belajar membuat ripple effect custom:

```js
const buttons = document.querySelectorAll(".btn");

buttons.forEach(btn => {
  btn.addEventListener("click", function (e) {
    const ripple = document.createElement("span");
    ripple.classList.add("ripple");

    const x = e.clientX - e.target.offsetLeft;
    const y = e.clientY - e.target.offsetTop;

    ripple.style.left = `${x}px`;
    ripple.style.top = `${y}px`;

    this.appendChild(ripple);

    setTimeout(() => ripple.remove(), 600);
  });
});
