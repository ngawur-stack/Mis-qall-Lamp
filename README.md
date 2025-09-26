<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title></title>
  <style>
    /* Hamburger Menu */
.hamburger {
  display: none;
  flex-direction: column;
  cursor: pointer;
  gap: 5px;
}
.hamburger span {
  width: 25px;
  height: 3px;
  background: #f6c606;
  border-radius: 3px;
  transition: all 0.3s ease;
}

/* Responsive - Mobile */
@media (max-width: 768px) {
  nav {
    display: none;
    flex-direction: column;
    width: 100%;
    background: #181313;
    padding: 1rem;
    position: absolute;
    top: 100%;
    left: 0;
  }
  nav.active {
    display: flex;
  }
  .hamburger {
    display: flex;
  }
  .hero h2 {
    font-size: 2rem;
  }
  .hero p {
    font-size: 1rem;
  }
  .gallery {
    flex-direction: column;
    align-items: center;
  }
  .gallery-item {
    max-width: 100%;
  }
}
    /* Reset & base */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: 'Poppins', 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #413805 0%, #5b4c0f 100%);
      color: #4b3b2b;
      line-height: 1.8;
    }
    a {
      color: #f6ce70;
      text-decoration: none;
      transition: all 0.3s ease;
    }
    a:hover {
      color: #f2d183;
      transform: translateY(-2px);
    }
    
    /* Header & Navigation */
    header {
  background: linear-gradient(45deg, #181313, #2b2305);
  backdrop-filter: blur(10px);
  padding: 1rem 2rem;
  color: #856d03;
  display: flex;
  justify-content: space-between;
  align-items: center;  /* ini yang bikin sejajar secara vertikal */
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  box-shadow: 0 4px 20px rgba(0,0,0,0.1);
}

.logo-title {
  display: flex;         /* atur horizontal */
  align-items: center;   /* sejajarkan vertikal */
  gap: 12px;             /* jarak antara logo dan teks */
}

.logo {
  height: 80px; /* sesuaikan ukuran logo */
  width: auto;
}

header h1 {
  font-family: 'Playfair Display', 'Georgia', serif;
  font-weight: 700;
  font-size: 2rem;
  letter-spacing: 3px;
  background: linear-gradient(45deg, #fab403, #c39b0b);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
    nav {
      display: flex;
      gap: 2rem;
    }
    nav a {
      font-weight: 600;
      font-size: 1.1rem;
      position: relative;
      padding: 0.5rem 0;
    }
    nav a::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 3px;
      background: #f6c606;
      transition: width 0.3s ease;
    }
    nav a:hover::after {
      width: 100%;
    }
        
    /* Hero Section */
    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: linear-gradient(135deg, 
        rgba(252, 220, 94, 0.9) 0%, 
        rgba(19, 15, 1, 0.9) 100%),
        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="50" cy="50" r="2" fill="%23ffffff" opacity="0.1"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
      color: #f9f6ec;
      text-align: center;
      padding: 6rem 2rem 4rem;
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="dots" width="20" height="20" patternUnits="userSpaceOnUse"><circle cx="10" cy="10" r="1" fill="%23ffffff" opacity="0.3"/></pattern></defs><rect width="100" height="100" fill="url(%23dots)"/></svg>');
      animation: float 20s ease-in-out infinite;
    }
    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
    }
    .hero-content {
      max-width: 800px;
      z-index: 2;
    }
    .hero h2 {
      font-size: 3.5rem;
      margin-bottom: 1.5rem;
      font-family: 'Playfair Display', 'Georgia', serif;
      text-shadow: 2px 2px 4px rgba(75, 59, 43, 0.3);
      animation: fadeInUp 1s ease-out;
    }
    .hero p {
      font-size: 1.3rem;
      margin-bottom: 2.5rem;
      font-weight: 500;
      animation: fadeInUp 1s ease-out 0.2s both;
    }
    .btn-primary {
      background: linear-gradient(135deg, #f6d68c, #d4af37);
      color: #fff8dc;
      padding: 1rem 3rem;
      border: none;
      border-radius: 50px;
      font-size: 1.2rem;
      font-weight: 700;
      cursor: pointer;
      box-shadow: 0 8px 25px rgba(246, 210, 120, 0.4);
      transition: all 0.3s ease;
      animation: fadeInUp 1s ease-out 0.4s both;
    }
    .btn-primary:hover {
      transform: translateY(-5px);
      box-shadow: 0 12px 35px rgba(184, 134, 11, 0.6);
    }
    
    /* Main Content */
    main {
      max-width: 1200px;
      margin: 0 auto;
      padding: 4rem 2rem;
    }
    
    /* Section Styling */
    .section-header {
      text-align: center;
      margin-bottom: 3rem;
    }
    .section-header h3 {
      font-family: 'Playfair Display', 'Georgia', serif;
      font-size: 2.8rem;
      margin-bottom: 1rem;
      background: linear-gradient(135deg, #f9f8f7, #c8c2be);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .section-header p {
      font-size: 1.2rem;
      color: #ead4c4;
      max-width: 600px;
      margin: 0 auto;
    }
    
    /* Features Section */
    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      margin: 3rem 0;
    }
    .feature-card {
      background: rgb(219, 199, 96);
      padding: 2.5rem;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(253, 245, 4, 0.1);
      text-align: center;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      border: 1px solid rgba(245, 226, 176, 0.1);
    }
    .feature-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(0,0,0,0.15);
    }
    .feature-icon {
      font-size: 3rem;
      margin-bottom: 1.5rem;
      color: #f5ec98;
    }
    .feature-card h4 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
      color: #25231a;
    }
    .feature-card p {
      color: #25231a;
      line-height: 1.6;
    }
    <!-- Jenis Produk Section -->
<section id="products">
  <div class="section-header">
    <h3>Jenis Produk MIS-QALL LAMP</h3>
    <p>Pilih varian yang sesuai dengan kebutuhan dan preferensi Anda</p>
  </div>
  <div class="features">
    <div class="feature-card">
      <div class="feature-icon">💡</div>
      <h4>MIS-QALL LAMP Classic</h4>
      <p>Varian standar dengan fitur meditasi dan aromaterapi, desain kaligrafi elegan.</p>
      <img src="https://via.placeholder.com/300x200?text=Classic" alt="MIS-QALL LAMP Classic" style="margin-top:1rem; border-radius: 15px; width: 100%; height: auto;" />
    </div>
    <div class="feature-card">
      <div class="feature-icon">🌿</div>
      <h4>MIS-QALL LAMP Eco</h4>
      <p>Varian ramah lingkungan dengan bahan limbah bonggol jagung dan motif batik Pekalongan.</p>
      <img src="https://via.placeholder.com/300x200?text=Eco" alt="MIS-QALL LAMP Eco" style="margin-top:1rem; border-radius: 15px; width: 100%; height: auto;" />
    </div>
    <div class="feature-card">
      <div class="feature-icon">🎶</div>
      <h4>MIS-QALL LAMP Premium</h4>
      <p>Varian lengkap dengan fitur musik religi, pencahayaan premium, dan desain eksklusif.</p>
      <img src="https://via.placeholder.com/300x200?text=Premium" alt="MIS-QALL LAMP Premium" style="margin-top:1rem; border-radius: 15px; width: 100%; height: auto;" />
    </div>
  </div>
</section>
    /* Benefits Section */
    .benefits {
      background: linear-gradient(135deg, rgba(184, 134, 11, 0.1) 0%, rgba(111, 78, 55, 0.1) 100%);
      padding: 4rem 2rem;
      border-radius: 30px;
      margin: 4rem 0;
    }
    .benefits-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }
    .benefit-item {
      background: rgb(240, 239, 237);
      padding: 2rem;
      border-radius: 15px;
      box-shadow: 0 5px 20px rgba(102, 101, 78, 0.08);
      display: flex;
      align-items: center;
      gap: 1.5rem;
    }
    .benefit-number {
      font-size: 3rem;
      font-weight: 700;
      color: #b29a39;
      min-width: 60px;
    }
    .benefit-content h4 {
      font-size: 1.3rem;
      margin-bottom: 0.5rem;
      color: #c3b050;
    }
    
    /* Varian Section */
    .Varian {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
      margin: 3rem 0;
    }
    .Varian-card {
      background: rgb(219, 199, 96);
      padding: 2.5rem;
      border-radius: 20px;
      box-shadow: 0 10px 30px rgba(253, 245, 4, 0.1);
      text-align: center;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      border: 1px solid rgba(245, 226, 176, 0.1);
    }
    .Varian-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(0,0,0,0.15);
    }
    .Varian-icon {
      font-size: 3rem;
      margin-bottom: 1.5rem;
      color: #f5ec98;
    }
    .Varian-card h4 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
      color: #25231a;
    }
    .Varian-card p {
      color: #25231a;
      line-height: 1.6;
    }

    /* Gallery Section */
#gallery {
  margin-bottom: 6rem; /* beri jarak aman sebelum CTA */
  max-width: 1200px;       /* supaya tetap center */
  margin: 0 auto 4rem;     /* jarak bawah 4rem sebelum CTA */
}

.gallery {
  display: flex;           /* jadikan 1 baris horizontal */
  justify-content: center;  /* rata tengah */
  gap: 2rem;               /* jarak antar foto */
}

.gallery-item {
  flex: 1 1 0;             /* semua item lebar sama */
  max-width: 350px;        /* opsional: batasi lebar maksimal */
  background: #f0e9c4;
  border-radius: 20px;
  overflow: hidden;
  text-align: center;
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: scale(1.05);
}

.gallery-item img {
  width: 100%;
  aspect-ratio: 16/9;      /* pastikan landscape */
  object-fit: cover;       /* potong gambar agar tetap proporsional */
  display: block;
}
    
    /* CTA Section */
    .cta-section {
      background: linear-gradient(135deg, #070500, #edc618 );
      color: white;
      padding: 6rem 2rem;
      text-align: center;
      border-radius: 30px;
      margin: 4rem 0;
      position: relative;
      overflow: hidden;
      margin-top: 6rem; /* beri jarak aman dari galeri */
}
    .cta-section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="stars" width="20" height="20" patternUnits="userSpaceOnUse"><circle cx="10" cy="10" r="1" fill="%23ffffff" opacity="0.3"/></pattern></defs><rect width="100" height="100" fill="url(%23stars)"/></svg>');
      animation: twinkle 3s ease-in-out infinite;
    }
    @keyframes twinkle {
      0%, 100% { opacity: 0.3; }
      50% { opacity: 0.8; }
    }
    .cta-content {
      position: relative;
      z-index: 2;
      max-width: 600px;
      margin: 0 auto;
    }
    .cta-content h3 {
      font-size: 2.5rem;
      margin-bottom: 1.5rem;
      font-family: 'Playfair Display', serif;
    }
    .cta-content p {
  font-size: 1.2rem;   /* ✅ perbesar ukuran teks deskripsi */
  line-height: 1.5;    /* jarak antar baris agar nyaman dibaca */
  margin-bottom: 2.5rem; /* ✅ tambah jarak bawah supaya tombol “Pesan Sekarang”
                            tidak menempel pada teks */
}
    
    /* Footer */
    footer {
      background: #9a7f12;
      color: #f9f5f0;
      padding: 4rem 2rem 2rem;
      text-align: center;
    }
    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 3rem;
      text-align: left;
    }
    .footer-section h4 {
      font-size: 1.3rem;
      margin-bottom: 1.5rem;
      color: #f1cc6e;
    }
    .social-links {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }
    .social-link {
      background: #735507;
      color: white;
      padding: 0.8rem 1.5rem;
      border-radius: 25px;
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      transition: all 0.3s ease;
    }
    .social-link:hover {
      background: #7e5d10;
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(184, 134, 11, 0.4);
    }
    .copyright {
      margin-top: 3rem;
      padding-top: 2rem;
      border-top: 1px solid rgba(184, 134, 11, 0.3);
      text-align: center;
    }
    
    /* Animations */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    /* Responsive Design */
    @media (max-width: 768px) {
      header {
        padding: 1rem;
        flex-direction: column;
        gap: 1rem;
      }
      nav {
        gap: 1rem;
      }
      .hero h2 {
        font-size: 2.5rem;
      }
      .features,
      .benefits-grid,
      .gallery {
        grid-template-columns: 1fr;
      }
      .footer-content {
        grid-template-columns: 1fr;
        text-align: center;
      }
    }
  </style>
</head>
<body>
  <header>
  <div class="logo-title">
    <img src="https://drive.google.com/uc?export=view&id=YOUR_IMAGE_ID" 
         alt="Logo MIS-QALL LAMP" class="logo" />
    <h1>MIS-QALL LAMP</h1>
  </div>

  <!-- Hamburger -->
  <div class="hamburger" id="hamburger">
    <span></span>
    <span></span>
    <span></span>
  </div>

  <!-- Navigasi -->
  <nav id="nav-menu">
    <a href="#features">Fitur</a>
    <a href="#benefits">Manfaat</a>
    <a href="#gallery">Galeri</a>
    <a href="#purchase">Beli</a>
    <a href="#contact">Kontak</a>
  </nav>
</header>

  <section class="hero" aria-label="Perkenalan Produk MIS-QALL LAMP">
    <div class="hero-content">
      <h2>MIS-QALL LAMP</h2>
      <p>Inovasi Box-Lampu Relaksasi multifungsi untuk meditasi, aromaterapi, dan musik religi, berbahan limbah bonggol jagung dengan motif kaligrafi dan batik khas Pekalongan.</p>
     
    </div>
  </section>

  <main>
    <!-- Features Section -->
    <section id="features">
      <div class="section-header">
        <h3>Fitur Unggulan</h3>
        <p>Temukan keistimewaan yang membuat MIS-QALL LAMP menjadi pilihan terbaik untuk relaksasi Anda</p>
      </div>
      <div class="features">
        <div class="feature-card">
          <div class="feature-icon">🕯️</div>
          <h4>Meditasi & Relaksasi</h4>
          <p>Pencahayaan yang sempurna untuk menciptakan atmosfer meditasi yang mendalam dan menenangkan</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">🌸</div>
          <h4>Aromaterapi</h4>
          <p>Sistem aromaterapi terintegrasi untuk menyebarkan wewangian alami yang menenangkan</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">🎵</div>
          <h4>Musik Religi</h4>
          <p>Koleksi musik religi pilihan yang membantu memperkuat koneksi spiritual Anda</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">🌿</div>
          <h4>Ramah Lingkungan</h4>
          <p>Dibuat dari bahan limbah bonggol jagung yang diolah dengan teknologi ramah lingkungan</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">🎨</div>
          <h4>Seni Budaya</h4>
          <p>Motif kaligrafi dan batik khas Pekalongan yang memperkaya nilai seni dan budaya</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon">💎</div>
          <h4>Desain Elegan</h4>
          <p>Desain premium yang cocok untuk berbagai jenis ruangan dan dekorasi</p>
        </div>
      </div>
    </section>

    <!-- Benefits Section -->
    <section id="benefits" class="benefits">
      <div class="section-header">
        <h3>Manfaat Penggunaan</h3>
        <p>Rasakan perubahan positif dalam kehidupan sehari-hari dengan</p>
        <p>MIS-QALL LAMP</p>
      </div>
      <div class="benefits-grid">
        <div class="benefit-item">
          <div class="benefit-number">01</div>
          <div class="benefit-content">
            <h4>Relaksasi Mendalam</h4>
            <p>Meningkatkan kualitas meditasi dan relaksasi dengan atmosfer yang sempurna</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-number">02</div>
          <div class="benefit-content">
            <h4>Ketenangan Pikiran</h4>
            <p>Aromaterapi menciptakan suasana yang menenangkan dan mengurangi stres</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-number">03</div>
          <div class="benefit-content">
            <h4>Spiritualitas</h4>
            <p>Memperkuat koneksi spiritual melalui musik religi yang menyejukkan jiwa</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-number">04</div>
          <div class="benefit-content">
            <h4>Eco-Friendly</h4>
            <p>Mendukung gaya hidup berkelanjutan dengan produk ramah lingkungan</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-number">05</div>
          <div class="benefit-content">
            <h4>Estetika Ruang</h4>
            <p>Memperindah ruangan dengan motif budaya yang artistik dan elegan</p>
          </div>
        </div>
        <div class="benefit-item">
          <div class="benefit-number">06</div>
          <div class="benefit-content">
            <h4>Multifungsi</h4>
            <p>Cocok untuk berbagai kebutuhan: meditasi, aromaterapi, dan dekorasi</p>
          </div>
        </div>
      </div>
    </section>

<!-- Varian Section -->
    <section id="Varian" class="Varian">
      <div class="section-header">
        <h3>Varian Produk</h3>
        <p>Pilih varian yang sesuai dengan kebutuhan spiritual dan relaksasi Anda</p>
      <div class="Varian">
        <div class="Varian-card">
          <div class="Varian-icon">📖</div>
          <h4>Flow Learn</h4>
          <p>📖Kaligrafi : Al-'Alaq ayat 1</p>
          <p>🌿Aroma : Mint (segar, meningkatkan fokus)</p>
          <p>💡Cahaya : Kuning (mendukung konsentrasi & belajar)</p>
          <p>🎶Playlist : Murottal Quran untuk fokus dan semangat menuntut ilmu</p>
        </div>
        <div class="Varian-card">
          <div class="Varian-icon">🌙</div>
          <h4>Deep Dream</h4>
          <p>📖Kaligrafi : An-Naba ayat 9</p>
          <p>🌿Aroma : Kemenyan (menenangkan pikiran)</p>
          <p>💡Cahaya : Merah (membantu tidur nyenyak)</p>
          <p>🎶Playlist : Murottal Quran & shalawat pengantar tidur</p>
        </div>
        <div class="Varian-card">
          <div class="Varian-icon">🌸</div>
          <h4>Calm Bloom</h4>
          <p>📖Kaligrafi : Al-Insyirah ayat 6</p>
          <p>🌿Aroma : Lavender (meredakan stress & menenangkan hati)</p>
          <p>💡Cahaya : Biru (menyegarkan dan memberi rasa damai)</p>
          <p>🎶Playlist : Murottal Quran & shalawat penyejuk jiwa</p>
        </div>
       </div>
</section>

    <!-- Gallery Section -->
    <section id="gallery">
      <div class="section-header">
        <h3>Galeri Produk</h3>
        <p>Lihat keindahan dan keunikan MIS-QALL LAMP dari berbagai sudut pandang</p>
      </div>
      <div class="gallery">
        <div class="gallery-item">
          <img src="Drive" alt="Tampilan depan MIS-QALL LAMP dengan motif kaligrafi yang elegan" />
          <div class="gallery-overlay">
            <h4>Tampilan Depan</h4>
            <p>Motif kaligrafi yang memukau dengan pencahayaan soft</p>
          </div>
        </div>
        <div class="gallery-item">
          <img src="Drive" alt="Detail batik khas Pekalongan pada body lampu" />
          <div class="gallery-overlay">
            <h4>Detail Batik</h4>
            <p>Kearifan lokal Pekalongan dalam setiap detail</p>
          </div>
        </div>
        <div class="gallery-item">
          <img src="Drive" alt="MIS-QALL LAMP dalam suasana meditasi dengan cahaya hangat" />
          <div class="gallery-overlay">
            <h4>Suasana Meditasi</h4>
            <p>Cahaya yang sempurna untuk relaksasi mendalam</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section id="purchase" class="cta-section">
      <div class="cta-content">
        <h3>Siap Mengalami Transformasi?</h3>
        <p>Pesan Mis-qall Lamp sekarang dan rasakan kedamaian yang sesungguhnya dalam hidup Anda</p>
        <a href="https://www.shopee.com/" target="_blank" class="btn-primary">Pesan Sekarang</a>
      </div>
    </section>
  </main>

  <!-- Footer -->
  <footer id="contact">
    <div class="footer-content">
      <div class="footer-section">
        <h4>Tentang Kami</h4>
        <p>MIS-QALL LAMP hadir untuk memberikan pengalaman relaksasi terbaik dengan menggabungkan teknologi modern dan kearifan lokal.</p>
      </div>
      <div class="footer-section">
        <h4>Kontak</h4>
        <p>Email: <a href="mailto:@misqall.id@gmail.com">@misqall.id</a></p>
        <p>Telepon: +62 815-7592-5550</p>
      </div>
      <div class="footer-section">
        <h4>Follow Kami</h4>
        <div class="social-links">
          <a href="https://instagram.com/misqall.id" target="_blank" rel="noopener noreferrer" class="social-link">
            📷 Instagram
          </a>
          <a href="https://wa.me/+6281575925550" target="_blank" rel="noopener noreferrer" class="social-link">
            📱 WhatsApp
          </a>
        </div>
      </div>
    </div>
    <div class="copyright">
      <p>&copy; 2025 MIS-QALL LAMP. Semua hak cipta dilindungi.</p>
    </div>
  </footer>

  <script>
    // Smooth scrolling for navigation
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
          target.scrollIntoView({
            behavior: 'smooth',
            block: 'start'
          });
        }
      });
    });

    // Animation on scroll
    const observerOptions = {
      threshold: 0.1,
      rootMargin: '0px 0px -50px 0px'
    };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.animation = 'fadeInUp 1s ease-out forwards';
          observer.unobserve(entry.target);
        }
      });
    }, observerOptions);

    // Observe elements for animation
    document.querySelectorAll('.feature-card, .benefit-item, .gallery-item').forEach(el => {
      el.style.opacity = '0';
      observer.observe(el);
    });
    // Toggle hamburger menu
const hamburger = document.getElementById("hamburger");
const navMenu = document.getElementById("nav-menu");

hamburger.addEventListener("click", () => {
  navMenu.classList.toggle("active");
});
  </script>
</body>
</html>
