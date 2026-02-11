<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Doughlicious - Pastry Bakery Multibahasa</title>
    <!-- Menggunakan Font Awesome untuk Ikon -->
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
    
    <style>
      /* --- RESET & VARIABEL --- */
      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      }

      :root {
        --primary-brown: #8b4513;
        --light-brown: #a0522d;
        --cream: #f5f5dc;
        --white: #ffffff;
        --dark-brown: #5d2906;
        --gray: #444;
        --light-gray: #f8f8f8;
        --shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        --transition: all 0.3s ease;
      }

      html {
        scroll-behavior: smooth;
        /* Agar scroll锚点 tidak tertutup header sticky */
        scroll-padding-top: 80px; 
      }

      body {
        background-color: var(--cream);
        color: var(--dark-brown);
        line-height: 1.6;
      }

      .container {
        width: 100%;
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 20px;
      }

      /* --- HEADER & NAVIGASI --- */
      header {
        background-color: var(--primary-brown);
        padding: 15px 0;
        position: sticky;
        top: 0;
        z-index: 1000;
        box-shadow: var(--shadow);
      }

      .header-content {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 15px;
      }

      .logo {
        display: flex;
        align-items: center;
        text-decoration: none;
      }

      .logo i {
        font-size: 2rem;
        color: var(--cream);
        margin-right: 10px;
      }

      .logo h1 {
        color: var(--white);
        font-size: 1.5rem;
        font-weight: 700;
        white-space: nowrap;
      }

      .nav-links {
        display: flex;
        list-style: none;
        gap: 20px;
      }

      .nav-links a {
        color: var(--white);
        text-decoration: none;
        font-weight: 500;
        font-size: 1rem;
        transition: var(--transition);
      }

      .nav-links a:hover {
        color: var(--cream);
      }

      .header-actions {
        display: flex;
        align-items: center;
        gap: 15px;
      }

      .language-selector {
        display: flex;
        background-color: var(--light-brown);
        border-radius: 20px;
        padding: 3px;
      }

      .lang-btn {
        background: none;
        border: none;
        color: var(--white);
        padding: 6px 12px;
        border-radius: 15px;
        cursor: pointer;
        font-weight: 500;
        font-size: 0.85rem;
        transition: var(--transition);
      }

      .lang-btn.active {
        background-color: var(--primary-brown);
        box-shadow: 0 2px 4px rgba(0,0,0,0.2);
      }

      .cart-icon {
        position: relative;
        cursor: pointer;
        color: var(--white);
        font-size: 1.5rem;
      }

      .cart-count {
        position: absolute;
        top: -8px;
        right: -8px;
        background-color: var(--white);
        color: var(--primary-brown);
        border-radius: 50%;
        width: 20px;
        height: 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 0.75rem;
        font-weight: bold;
      }

      /* --- HERO SECTION --- */
      .hero {
        background: linear-gradient(rgba(139, 69, 19, 0.85), rgba(139, 69, 19, 0.9)),
          url("https://images.unsplash.com/photo-1509440159596-0249088772ff?ixlib=rb-4.0.3&auto=format&fit=crop&w=1472&q=80");
        background-size: cover;
        background-position: center;
        color: var(--white);
        padding: 100px 0;
        text-align: center;
      }

      .hero h2 {
        font-size: 3rem;
        margin-bottom: 20px;
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
      }

      .hero p {
        font-size: 1.2rem;
        max-width: 700px;
        margin: 0 auto 30px;
        color: var(--cream);
      }

      .cta-button {
        display: inline-block;
        background-color: var(--cream);
        color: var(--primary-brown);
        padding: 12px 30px;
        border-radius: 30px;
        text-decoration: none;
        font-weight: bold;
        font-size: 1.1rem;
        transition: var(--transition);
      }

      .cta-button:hover {
        background-color: var(--white);
        transform: translateY(-3px);
        box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
      }

      /* --- PRODUCTS SECTION --- */
      .section-title {
        text-align: center;
        margin: 60px 0 40px;
        color: var(--dark-brown);
        font-size: 2.2rem;
        position: relative;
      }

      .section-title::after {
        content: "";
        position: absolute;
        width: 80px;
        height: 3px;
        background-color: var(--primary-brown);
        bottom: -10px;
        left: 50%;
        transform: translateX(-50%);
        border-radius: 2px;
      }

      .products-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
        gap: 30px;
        margin-bottom: 60px;
      }

      .product-card {
        background-color: var(--white);
        border-radius: 15px;
        overflow: hidden;
        box-shadow: var(--shadow);
        transition: var(--transition);
        display: flex;
        flex-direction: column;
      }

      .product-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 10px 25px rgba(0, 0, 0, 0.15);
      }

      .product-img {
        height: 200px;
        overflow: hidden;
        background-color: #eee;
      }

      .product-img img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: transform 0.5s;
      }

      .product-card:hover .product-img img {
        transform: scale(1.05);
      }

      .product-info {
        padding: 20px;
        flex-grow: 1;
        display: flex;
        flex-direction: column;
      }

      .product-name {
        font-size: 1.2rem;
        margin-bottom: 8px;
        color: var(--dark-brown);
      }

      .product-price {
        color: var(--primary-brown);
        font-size: 1.1rem;
        font-weight: bold;
        margin-bottom: 15px;
      }

      .add-to-cart {
        margin-top: auto;
        background-color: var(--primary-brown);
        color: var(--white);
        border: none;
        padding: 10px;
        border-radius: 8px;
        cursor: pointer;
        font-weight: 500;
        transition: background-color 0.3s;
      }

      .add-to-cart:hover {
        background-color: var(--light-brown);
      }

      /* --- REVIEWS SECTION --- */
      .reviews-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 30px;
        margin-bottom: 60px;
      }

      .review-card {
        background-color: var(--white);
        padding: 25px;
        border-radius: 15px;
        box-shadow: var(--shadow);
      }

      .review-header {
        display: flex;
        align-items: center;
        margin-bottom: 15px;
      }

      .review-avatar {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        overflow: hidden;
        margin-right: 15px;
        border: 2px solid var(--cream);
      }

      .review-avatar img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }

      .review-name {
        font-size: 1.1rem;
        color: var(--dark-brown);
        font-weight: 600;
      }

      .review-rating {
        color: #ffc107;
        font-size: 0.9rem;
      }

      .review-text {
        color: var(--gray);
        font-style: italic;
        line-height: 1.6;
        font-size: 0.95rem;
      }

      /* --- ORDER FORM --- */
      .order-form-container {
        background-color: var(--white);
        padding: 40px;
        border-radius: 20px;
        box-shadow: var(--shadow);
        margin-bottom: 60px;
      }

      .form-title {
        color: var(--dark-brown);
        margin-bottom: 30px;
        font-size: 1.8rem;
        text-align: center;
      }

      .form-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        margin-bottom: 20px;
      }

      .form-group {
        margin-bottom: 20px;
      }

      .form-group label {
        display: block;
        margin-bottom: 8px;
        color: var(--dark-brown);
        font-weight: 500;
      }

      .form-group input,
      .form-group select,
      .form-group textarea {
        width: 100%;
        padding: 12px;
        border: 2px solid #ddd;
        border-radius: 8px;
        font-size: 1rem;
        color: var(--gray);
        transition: border-color 0.3s;
        background-color: var(--light-gray);
      }

      .form-group input:focus,
      .form-group select:focus,
      .form-group textarea:focus {
        outline: none;
        border-color: var(--primary-brown);
        background-color: var(--white);
      }

      .submit-order {
        background-color: var(--primary-brown);
        color: var(--white);
        border: none;
        padding: 15px 40px;
        border-radius: 30px;
        font-size: 1.1rem;
        font-weight: bold;
        cursor: pointer;
        display: block;
        margin: 20px auto 0;
        transition: background-color 0.3s;
      }

      .submit-order:hover {
        background-color: var(--light-brown);
      }

      /* --- FOOTER --- */
      footer {
        background-color: var(--dark-brown);
        color: var(--cream);
        padding: 50px 0 20px;
      }

      .footer-content {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 40px;
        margin-bottom: 30px;
      }

      .footer-column h3 {
        font-size: 1.3rem;
        margin-bottom: 20px;
        color: var(--white);
      }

      .footer-column p {
        margin-bottom: 10px;
        font-size: 0.95rem;
      }

      .social-icons {
        display: flex;
        margin-top: 20px;
        gap: 15px;
      }

      .social-icons a {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 35px;
        height: 35px;
        background-color: var(--light-brown);
        border-radius: 50%;
        color: var(--white);
        text-decoration: none;
        transition: var(--transition);
      }

      .social-icons a:hover {
        background-color: var(--cream);
        color: var(--primary-brown);
      }

      .copyright {
        text-align: center;
        padding-top: 20px;
        border-top: 1px solid rgba(255, 255, 255, 0.1);
        color: rgba(255, 255, 255, 0.6);
        font-size: 0.9rem;
      }

      /* --- CART MODAL --- */
      .cart-modal {
        position: fixed;
        top: 0;
        right: -400px;
        width: 380px;
        max-width: 100%;
        height: 100%;
        background-color: var(--white);
        box-shadow: -5px 0 25px rgba(0, 0, 0, 0.2);
        z-index: 1001;
        transition: right 0.4s ease;
        padding: 25px;
        overflow-y: auto;
        display: flex;
        flex-direction: column;
      }

      .cart-modal.open {
        right: 0;
      }

      .cart-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
        padding-bottom: 15px;
        border-bottom: 2px solid var(--cream);
      }

      .cart-title {
        font-size: 1.5rem;
        color: var(--dark-brown);
      }

      .close-cart {
        background: none;
        border: none;
        font-size: 1.5rem;
        color: var(--dark-brown);
        cursor: pointer;
      }

      .cart-items {
        flex-grow: 1;
        overflow-y: auto;
      }

      .cart-item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 15px 0;
        border-bottom: 1px solid #eee;
      }

      .cart-item-info h4 {
        color: var(--dark-brown);
        margin-bottom: 5px;
        font-size: 1rem;
      }

      .cart-item-price {
        color: var(--primary-brown);
        font-weight: bold;
        font-size: 0.9rem;
      }

      .cart-item-quantity {
        display: flex;
        align-items: center;
      }

      .quantity-btn {
        background-color: var(--cream);
        border: none;
        width: 28px;
        height: 28px;
        border-radius: 50%;
        cursor: pointer;
        font-weight: bold;
        color: var(--dark-brown);
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .cart-quantity {
        margin: 0 10px;
        font-weight: bold;
        font-size: 0.9rem;
      }

      .remove-item {
        background: none;
        border: none;
        color: #ff6b6b;
        cursor: pointer;
        margin-left: 10px;
      }

      .cart-footer {
        margin-top: 20px;
        border-top: 2px solid var(--cream);
        padding-top: 20px;
      }

      .cart-total {
        display: flex;
        justify-content: space-between;
        font-size: 1.3rem;
        font-weight: bold;
        color: var(--dark-brown);
        margin-bottom: 20px;
      }

      .checkout-btn {
        background-color: var(--primary-brown);
        color: var(--white);
        border: none;
        width: 100%;
        padding: 15px;
        border-radius: 10px;
        font-size: 1.1rem;
        font-weight: bold;
        cursor: pointer;
        transition: background-color 0.3s;
      }

      .checkout-btn:hover {
        background-color: var(--light-brown);
      }

      .overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 1000;
        opacity: 0;
        visibility: hidden;
        transition: var(--transition);
      }

      .overlay.active {
        opacity: 1;
        visibility: visible;
      }

      /* --- TOAST NOTIFICATION (Pengganti Alert) --- */
      .toast-container {
        position: fixed;
        bottom: 30px;
        right: 30px;
        z-index: 2000;
        display: flex;
        flex-direction: column;
        gap: 10px;
      }

      .toast {
        background-color: var(--dark-brown);
        color: var(--white);
        padding: 12px 24px;
        border-radius: 8px;
        box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        display: flex;
        align-items: center;
        gap: 10px;
        transform: translateX(120%);
        transition: transform 0.4s cubic-bezier(0.68, -0.55, 0.27, 1.55);
        min-width: 250px;
      }

      .toast.show {
        transform: translateX(0);
      }

      .toast i {
        color: #4cd137;
      }

      /* --- RESPONSIVE --- */
      @media (max-width: 768px) {
        .header-content {
          justify-content: center;
        }
        
        .nav-links {
          order: 3;
          width: 100%;
          justify-content: center;
          margin-top: 15px;
        }

        .hero h2 {
          font-size: 2rem;
        }

        .cart-modal {
          width: 100%;
        }
      }
    </style>
  </head>
  <body>
    <!-- Header & Navigation -->
    <header>
      <div class="container header-content">
        <a href="#" class="logo">
          <i class="fas fa-birthday-cake"></i>
          <h1 id="site-title">Doughlicious</h1>
        </a>

        <ul class="nav-links">
          <li><a href="#home" id="nav-home">Beranda</a></li>
          <li><a href="#products" id="nav-products">Produk</a></li>
          <li><a href="#reviews" id="nav-reviews">Ulasan</a></li>
          <li><a href="#order" id="nav-order">Pesan</a></li>
        </ul>

        <div class="header-actions">
          <div class="language-selector">
            <button class="lang-btn active" data-lang="id">ID</button>
            <button class="lang-btn" data-lang="en">EN</button>
            <button class="lang-btn" data-lang="it">IT</button>
          </div>

          <div class="cart-icon" id="cart-icon">
            <i class="fas fa-shopping-cart"></i>
            <span class="cart-count" id="cart-count">0</span>
          </div>
        </div>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
      <div class="container">
        <h2 id="hero-title">Pastry Lezat, Dibuat dengan Cinta</h2>
        <p id="hero-text">
          Temukan kelezatan pastry buatan tangan kami yang dipanggang segar
          setiap hari. Dari croissant klasik hingga kue kreatif, kami menyajikan
          kualitas terbaik.
        </p>
        <a href="#products" class="cta-button" id="hero-button"
          >Lihat Produk Kami</a
        >
      </div>
    </section>

    <!-- Products Section -->
    <section class="container" id="products">
      <h2 class="section-title" id="products-title">Produk Unggulan</h2>
      <div class="products-grid" id="products-container">
        <!-- Produk akan di-generate dengan JavaScript -->
      </div>
    </section>

    <!-- Reviews Section -->
    <section class="container" id="reviews">
      <h2 class="section-title" id="reviews-title">Ulasan Pelanggan</h2>
      <div class="reviews-container" id="reviews-container">
        <!-- Ulasan akan di-generate dengan JavaScript -->
      </div>
    </section>

    <!-- Order Form -->
    <section class="container" id="order">
      <div class="order-form-container">
        <h2 class="form-title" id="order-title">Formulir Pemesanan</h2>
        <form id="order-form">
          <div class="form-grid">
            <div class="form-group">
              <label for="name" id="name-label">Nama Lengkap</label>
              <input type="text" id="name" required />
            </div>
            <div class="form-group">
              <label for="email" id="email-label">Email</label>
              <input type="email" id="email" required />
            </div>
            <div class="form-group">
              <label for="phone" id="phone-label">Nomor Telepon</label>
              <input type="tel" id="phone" required />
            </div>
            <div class="form-group">
              <label for="delivery" id="delivery-label"
                >Metode Pengiriman</label
              >
              <select id="delivery" required>
                <option value="" id="delivery-default">
                  Pilih metode pengiriman
                </option>
                <option value="pickup" id="delivery-pickup">
                  Ambil di toko
                </option>
                <option value="delivery" id="delivery-delivery">
                  Antar ke alamat
                </option>
              </select>
            </div>
          </div>
          <div class="form-group">
            <label for="address" id="address-label"
              >Alamat Lengkap (jika diantar)</label
            >
            <textarea id="address" rows="3"></textarea>
          </div>
          <div class="form-group">
            <label for="notes" id="notes-label"
              >Catatan Tambahan (opsional)</label
            >
            <textarea
              id="notes"
              rows="3"
              placeholder="Contoh: Tanpa kacang, tambah coklat, dll."
            ></textarea>
          </div>
          <button type="submit" class="submit-order" id="submit-order">
            Pesan Sekarang
          </button>
        </form>
      </div>
    </section>

    <!-- Footer -->
    <footer>
      <div class="container">
        <div class="footer-content">
          <div class="footer-column">
            <h3 id="footer-about">Tentang Kami</h3>
            <p id="footer-about-text">
              Doughlicious telah menyajikan pastry lezat sejak 2025. Kami
              berkomitmen menggunakan bahan terbaik dan resep tradisional.
            </p>
            <div class="social-icons">
              <a href="#"><i class="fab fa-instagram"></i></a>
              <a href="#"><i class="fab fa-facebook"></i></a>
              <a href="#"><i class="fab fa-twitter"></i></a>
            </div>
          </div>
          <div class="footer-column">
            <h3 id="footer-contact">Kontak</h3>
            <p>
              <i class="fas fa-map-marker-alt"></i> Jl. Pastry No. 123, Kota
              Pastry
            </p>
            <p><i class="fas fa-phone"></i> +62 123 4567 890</p>
            <p><i class="fas fa-envelope"></i> info@doughlicious.com</p>
          </div>
          <div class="footer-column">
            <h3 id="footer-hours">Jam Buka</h3>
            <p id="hours-mon">Senin - Jumat: 7:00 - 20:00</p>
            <p id="hours-sat">Sabtu: 7:00 - 22:00</p>
            <p id="hours-sun">Minggu: 8:00 - 18:00</p>
          </div>
        </div>
        <div class="copyright">
          <p>
            &copy; <span id="current-year">2023</span> Doughlicious.
            <span id="footer-rights">Semua hak dilindungi.</span>
          </p>
        </div>
      </div>
    </footer>

    <!-- Cart Modal -->
    <div class="cart-modal" id="cart-modal">
      <div class="cart-header">
        <h2 class="cart-title" id="cart-title">Keranjang Belanja</h2>
        <button class="close-cart" id="close-cart">&times;</button>
      </div>
      <div class="cart-items" id="cart-items">
        <!-- Item keranjang akan di-generate dengan JavaScript -->
      </div>
      <div class="cart-footer">
        <div class="cart-total">
          <span id="total-text">Total:</span>
          <span id="cart-total-price">Rp 0</span>
        </div>
        <button class="checkout-btn" id="checkout-btn">
          Lanjut ke Pembayaran
        </button>
      </div>
    </div>

    <!-- Overlay untuk cart modal -->
    <div class="overlay" id="overlay"></div>

    <!-- Toast Notification Container -->
    <div class="toast-container" id="toast-container"></div>

    <script>
      // --- DATA APLIKASI ---
      
      // Daftar Produk
      const products = [
        {
          id: 1,
          name: {
            id: "Croissant Almond",
            en: "Almond Croissant",
            it: "Croissant alle Mandorle",
          },
          price: 25000,
          img src="croissant almond.jpg" alt="croissant almond"/>,
        },
        {
          id: 2,
          name: {
            id: "Pain au Chocolat",
            en: "Pain au Chocolat",
            it: "Pain au Chocolat",
          },
          price: 22000,
          image:
            "https://images.unsplash.com/photo-1608198093002-ad4e005f1bca?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 3,
          name: { id: "Danish Keju", en: "Cheese Danish", it: "Danish al Formaggio" },
          price: 28000,
          image:
            "https://images.unsplash.com/photo-1509365465985-25d11c17e812?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 4,
          name: {
            id: "Éclair Coklat",
            en: "Chocolate Éclair",
            it: "Éclair al Cioccolato",
          },
          price: 32000,
          image:
            "https://images.unsplash.com/photo-1551024601-564964e3a2d8?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 5,
          name: {
            id: "Macaron Campuran",
            en: "Assorted Macarons",
            it: "Macaron Assortiti",
          },
          price: 45000,
          image:
            "https://www.primarasa.co.id/images/images/kulit%20macaron.jpg",
        },
        {
          id: 6,
          name: {
            id: "Tart Stroberi",
            en: "Strawberry Tart",
            it: "Crostata di Fragole",
          },
          price: 38000,
          image:
            "https://images.unsplash.com/photo-1565958011703-44f9829ba187?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 7,
          name: {
            id: "Bolu Coklat Belgia",
            en: "Belgian Chocolate Cake",
            it: "Torta al Cioccolato Belga",
          },
          price: 150000,
          image:
            "https://images.unsplash.com/photo-1578985545062-69928b1d9587?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 8,
          name: {
            id: "Tiramisu Klasik",
            en: "Classic Tiramisu",
            it: "Tiramisù Classico",
          },
          price: 42000,
          image:
            "https://images.unsplash.com/photo-1571877227200-a0d98ea607e9?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 9,
          name: {
            id: "Kue Keju New York",
            en: "New York Cheesecake",
            it: "Cheesecake New York",
          },
          price: 65000,
          image:
            "https://images.unsplash.com/photo-1533134242443-d4fd215305ad?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 10,
          name: {
            id: "Pavlova Berry",
            en: "Berry Pavlova",
            it: "Pavlova ai Frutti di Bosco",
          },
          price: 48000,
          image: "https://images.unsplash.com/photo-1488477181946-6428a029177b?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 11,
          name: {
            id: "Canelé Bordeaux",
            en: "Canelé de Bordeaux",
            it: "Canelé di Bordeaux",
          },
          price: 18000,
          image: "https://images.unsplash.com/photo-1626198226928-95178bf7ec36?auto=format&fit=crop&w=800&q=80",
        },
        {
          id: 12,
          name: {
            id: "Financier Madu",
            en: "Honey Financier",
            it: "Financier al Miele",
          },
          price: 15000,
          image:
            "https://images.unsplash.com/photo-1612203985729-70726954388c?auto=format&fit=crop&w=800&q=80",
        },
      ];

      // Daftar Ulasan
      const reviews = [
        {
          name: { id: "Sari Wijaya", en: "Sari Wijaya", it: "Sari Wijaya" },
          rating: 5,
          text: {
            id: "Croissant almondnya luar biasa! Renyah di luar, lembut di dalam. Toko favorit saya untuk sarapan.",
            en: "The almond croissant is amazing! Crispy on the outside, soft on the inside. My favorite bakery for breakfast.",
            it: "Il croissant alle mandorle è fantastico! Croccante fuori, morbido dentro. Il mio panificio preferito per la colazione.",
          },
          avatar: "https://randomuser.me/api/portraits/women/32.jpg",
        },
        {
          name: { id: "Budi Santoso", en: "Budi Santoso", it: "Budi Santoso" },
          rating: 4,
          text: {
            id: "Pain au chocolat terbaik di kota! Selalu segar dan coklatnya melimpah. Harga sangat worth it.",
            en: "Best pain au chocolat in town! Always fresh with generous chocolate. Very worth the price.",
            it: "Il miglior pain au chocolat in città! Sempre fresco con tanto cioccolato. Ne vale davvero il prezzo.",
          },
          avatar: "https://randomuser.me/api/portraits/men/54.jpg",
        },
        {
          name: { id: "Maria Rossi", en: "Maria Rossi", it: "Maria Rossi" },
          rating: 5,
          text: {
            id: "Saya dari Italia dan saya harus mengatakan bahwa pastri di sini sangat autentik! Danish keju mengingatkan saya pada rumah.",
            en: "I'm from Italy and I have to say the pastries here are very authentic! The cheese danish reminds me of home.",
            it: "Vengo dall'Italia e devo dire che i dolci qui sono molto autentici! Il danish al formaggio mi ricorda casa.",
          },
          avatar: "https://randomuser.me/api/portraits/women/65.jpg",
        },
      ];

      // Data Terjemahan (Translations)
      const translations = {
        id: {
          "site-title": "Doughlicious",
          "nav-home": "Beranda",
          "nav-products": "Produk",
          "nav-reviews": "Ulasan",
          "nav-order": "Pesan",
          "hero-title": "Pastry Lezat, Dibuat dengan Cinta",
          "hero-text":
            "Temukan kelezatan pastry buatan tangan kami yang dipanggang segar setiap hari. Dari croissant klasik hingga kue kreatif, kami menyajikan kualitas terbaik.",
          "hero-button": "Lihat Produk Kami",
          "products-title": "Produk Unggulan",
          "add-to-cart": "Tambah ke Keranjang",
          "reviews-title": "Ulasan Pelanggan",
          "order-title": "Formulir Pemesanan",
          "name-label": "Nama Lengkap",
          "email-label": "Email",
          "phone-label": "Nomor Telepon",
          "delivery-label": "Metode Pengiriman",
          "delivery-default": "Pilih metode pengiriman",
          "delivery-pickup": "Ambil di toko",
          "delivery-delivery": "Antar ke alamat",
          "address-label": "Alamat Lengkap (jika diantar)",
          "notes-label": "Catatan Tambahan (opsional)",
          "submit-order": "Pesan Sekarang",
          "cart-title": "Keranjang Belanja",
          "total-text": "Total:",
          "checkout-btn": "Lanjut ke Pembayaran",
          "remove-item": "Hapus",
          "footer-about": "Tentang Kami",
          "footer-about-text":
            "Doughlicious telah menyajikan pastry lezat sejak 2025. Kami berkomitmen menggunakan bahan terbaik dan resep tradisional.",
          "footer-contact": "Kontak",
          "footer-hours": "Jam Buka",
          "hours-mon": "Senin - Jumat: 7:00 - 20:00",
          "hours-sat": "Sabtu: 7:00 - 22:00",
          "hours-sun": "Minggu: 8:00 - 18:00",
          "footer-rights": "Semua hak dilindungi.",
          "order-success":
            "Pesanan berhasil! Kami akan menghubungi Anda untuk konfirmasi.",
          "cart-empty": "Keranjang Anda kosong.",
          "cart-item-added": "Ditambahkan ke keranjang!",
        },
        en: {
          "site-title": "Doughlicious",
          "nav-home": "Home",
          "nav-products": "Products",
          "nav-reviews": "Reviews",
          "nav-order": "Order",
          "hero-title": "Delicious Pastries, Made with Love",
          "hero-text":
            "Discover the deliciousness of our handmade pastries baked fresh daily. From classic croissants to creative cakes, we serve the best quality.",
          "hero-button": "View Our Products",
          "products-title": "Featured Products",
          "add-to-cart": "Add to Cart",
          "reviews-title": "Customer Reviews",
          "order-title": "Order Form",
          "name-label": "Full Name",
          "email-label": "Email",
          "phone-label": "Phone Number",
          "delivery-label": "Delivery Method",
          "delivery-default": "Select delivery method",
          "delivery-pickup": "Pickup in store",
          "delivery-delivery": "Delivery to address",
          "address-label": "Full Address (if delivered)",
          "notes-label": "Additional Notes (optional)",
          "submit-order": "Order Now",
          "cart-title": "Shopping Cart",
          "total-text": "Total:",
          "checkout-btn": "Proceed to Checkout",
          "remove-item": "Remove",
          "footer-about": "About Us",
          "footer-about-text":
            "Doughlicious has been serving delicious pastries since 2025. We are committed to using the best ingredients and traditional recipes.",
          "footer-contact": "Contact",
          "footer-hours": "Opening Hours",
          "hours-mon": "Monday - Friday: 7:00 - 20:00",
          "hours-sat": "Saturday: 7:00 - 22:00",
          "hours-sun": "Sunday: 8:00 - 18:00",
          "footer-rights": "All rights reserved.",
          "order-success": "Order successful! We will contact you for confirmation.",
          "cart-empty": "Your cart is empty.",
          "cart-item-added": "Added to cart!",
        },
        it: {
          "site-title": "Doughlicious",
          "nav-home": "Home",
          "nav-products": "Prodotti",
          "nav-reviews": "Recensioni",
          "nav-order": "Ordina",
          "hero-title": "Pasticceria Deliziosa, Fatta con Amore",
          "hero-text":
            "Scopri la delizia delle nostre pasticcerie fatte a mano, cotte fresche ogni giorno. Dai croissant classici alle torte creative, serviamo la migliore qualità.",
          "hero-button": "Vedi i Nostri Prodotti",
          "products-title": "Prodotti in Evidenza",
          "add-to-cart": "Aggiungi al Carrello",
          "reviews-title": "Recensioni dei Clienti",
          "order-title": "Modulo d'Ordine",
          "name-label": "Nome Completo",
          "email-label": "Email",
          "phone-label": "Numero di Telefono",
          "delivery-label": "Metodo di Consegna",
          "delivery-default": "Seleziona metodo di consegna",
          "delivery-pickup": "Ritiro in negozio",
          "delivery-delivery": "Consegna a domicilio",
          "address-label": "Indirizzo Completo (se consegnato)",
          "notes-label": "Note Aggiuntive (opzionale)",
          "submit-order": "Ordina Ora",
          "cart-title": "Carrello della Spesa",
          "total-text": "Totale:",
          "checkout-btn": "Procedi al Pagamento",
          "remove-item": "Rimuovi",
          "footer-about": "Chi Siamo",
          "footer-about-text":
            "Doughlicious serve deliziose pasticcerie dal 2025. Ci impegniamo a utilizzare i migliori ingredienti e ricette tradizionali.",
          "footer-contact": "Contatti",
          "footer-hours": "Orari di Apertura",
          "hours-mon": "Lunedì - Venerdì: 7:00 - 20:00",
          "hours-sat": "Sabato: 7:00 - 22:00",
          "hours-sun": "Domenica: 8:00 - 18:00",
          "footer-rights": "Tutti i diritti riservati.",
          "order-success":
            "Ordine effettuato con successo! Ti contatteremo per la conferma.",
          "cart-empty": "Il tuo carrello è vuoto.",
          "cart-item-added": "Aggiunto al carrello!",
        },
      };

      // --- STATE APLIKASI ---
      let currentLanguage = "id";
      let cart = [];
      let cartTotal = 0;

      // --- FUNGSI UTILITAS ---

      // Toast Notification System (Pengganti Alert)
      function showToast(message) {
        const container = document.getElementById("toast-container");
        const toast = document.createElement("div");
        toast.className = "toast";
        toast.innerHTML = `<i class="fas fa-check-circle"></i> <span>${message}</span>`;
        
        container.appendChild(toast);
        
        // Trigger animasi masuk
        setTimeout(() => toast.classList.add("show"), 100);

        // Hapus toast setelah 3 detik
        setTimeout(() => {
          toast.classList.remove("show");
          setTimeout(() => toast.remove(), 400);
        }, 3000);
      }

      // Format Harga berdasarkan bahasa
      function formatPrice(price) {
        if (currentLanguage === "en") {
          return `$${(price / 14000).toFixed(2)}`;
        } else if (currentLanguage === "it") {
          return `€${(price / 16000).toFixed(2)}`;
        } else {
          return `Rp ${price.toLocaleString("id-ID")}`;
        }
      }

      // --- FUNGSI RENDER & LOGIKA ---

      // Render Produk ke DOM
      function renderProducts() {
        const container = document.getElementById("products-container");
        if (!container) return;
        container.innerHTML = "";

        products.forEach((product) => {
          const card = document.createElement("div");
          card.className = "product-card";
          card.innerHTML = `
            <div class="product-img">
              <img src="${product.image}" alt="${product.name[currentLanguage]}" loading="lazy">
            </div>
            <div class="product-info">
              <h3 class="product-name">${product.name[currentLanguage]}</h3>
              <p class="product-price">${formatPrice(product.price)}</p>
              <button class="add-to-cart" data-id="${product.id}">
                ${translations[currentLanguage]["add-to-cart"]}
              </button>
            </div>
          `;
          container.appendChild(card);
        });

        // Event Listener tombol tambah keranjang
        document.querySelectorAll(".add-to-cart").forEach((btn) => {
          btn.addEventListener("click", (e) => {
            addToCart(parseInt(e.target.dataset.id));
          });
        });
      }

      // Render Ulasan
      function renderReviews() {
        const container = document.getElementById("reviews-container");
        if (!container) return;
        container.innerHTML = "";

        reviews.forEach((review) => {
          const card = document.createElement("div");
          card.className = "review-card";
          
          // Generate bintang rating
          let starsHtml = "";
          for (let i = 1; i <= 5; i++) {
            if (i <= review.rating) {
              starsHtml += '<i class="fas fa-star"></i>';
            } else {
              starsHtml += '<i class="far fa-star"></i>';
            }
          }

          card.innerHTML = `
            <div class="review-header">
              <div class="review-avatar">
                <img src="${review.avatar}" alt="${review.name[currentLanguage]}">
              </div>
              <div>
                <h4 class="review-name">${review.name[currentLanguage]}</h4>
                <div class="review-rating">${starsHtml}</div>
              </div>
            </div>
            <p class="review-text">"${review.text[currentLanguage]}"</p>
          `;
          container.appendChild(card);
        });
      }

      // Update Teks Bahasa pada Elemen Statis
      function updateTranslations() {
        const t = translations[currentLanguage];
        
        // Update elemen berdasarkan ID
        document.querySelectorAll("[id]").forEach((el) => {
          if (t[el.id]) {
            // Cek apakah ini input dengan placeholder
            if (el.tagName === "TEXTAREA" && !el.value && el.id === "notes") {
               el.placeholder = t[el.id === "notes" ? "notes-label" : el.id]; // Fallback simple
               // Update placeholder spesifik
               if(currentLanguage === 'id') el.placeholder = "Contoh: Tanpa kacang, tambah coklat, dll.";
               if(currentLanguage === 'en') el.placeholder = "Example: No nuts, extra chocolate, etc.";
               if(currentLanguage === 'it') el.placeholder = "Esempio: Senza noci, cioccolato extra, ecc.";
            } else if (el.tagName !== "INPUT" && el.tagName !== "TEXTAREA" && !el.querySelector("input, select, textarea")) {
               // Jangan ganti textContent jika elemen tersebut punya anak interaktif (bukan teks murni)
               el.textContent = t[el.id];
            }
          }
        });
        
        // Perbarui placeholder khusus secara manual
        const notesEl = document.getElementById("notes");
        if(notesEl) {
            if(currentLanguage === 'id') notesEl.placeholder = "Contoh: Tanpa kacang, tambah coklat, dll.";
            else if(currentLanguage === 'en') notesEl.placeholder = "Example: No nuts, extra chocolate, etc.";
            else if(currentLanguage === 'it') notesEl.placeholder = "Esempio: Senza noci, cioccolato extra, ecc.";
        }
      }

      // Update Tampilan Keranjang
      function updateCartUI() {
        // Update badge count
        const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
        const cartCountEl = document.getElementById("cart-count");
        if (cartCountEl) cartCountEl.textContent = totalItems;

        // Render Item Keranjang
        const cartItemsContainer = document.getElementById("cart-items");
        if (!cartItemsContainer) return;

        if (cart.length === 0) {
          cartItemsContainer.innerHTML = `<p style="text-align:center; color:#888; padding: 20px;">${translations[currentLanguage]["cart-empty"]}</p>`;
        } else {
          cartItemsContainer.innerHTML = "";
          cart.forEach((item) => {
            const product = products.find((p) => p.id === item.id);
            if (!product) return;

            const itemEl = document.createElement("div");
            itemEl.className = "cart-item";
            itemEl.innerHTML = `
              <div class="cart-item-info">
                <h4>${product.name[currentLanguage]}</h4>
                <p class="cart-item-price">${formatPrice(product.price)}</p>
              </div>
              <div class="cart-item-quantity">
                <button class="quantity-btn decrease" data-id="${product.id}">-</button>
                <span class="cart-quantity">${item.quantity}</span>
                <button class="quantity-btn increase" data-id="${product.id}">+</button>
                <button class="remove-item" data-id="${product.id}" aria-label="${translations[currentLanguage]['remove-item']}">
                  <i class="fas fa-trash"></i>
                </button>
              </div>
            `;
            cartItemsContainer.appendChild(itemEl);
          });

          // Event Listeners dinamis untuk tombol di dalam cart
          cartItemsContainer.querySelectorAll(".quantity-btn.decrease").forEach(btn => {
            btn.onclick = () => updateQuantity(parseInt(btn.dataset.id), -1);
          });
          cartItemsContainer.querySelectorAll(".quantity-btn.increase").forEach(btn => {
            btn.onclick = () => updateQuantity(parseInt(btn.dataset.id), 1);
          });
          cartItemsContainer.querySelectorAll(".remove-item").forEach(btn => {
            btn.onclick = () => removeFromCart(parseInt(btn.dataset.id));
          });
        }

        // Update Total Harga
        cartTotal = cart.reduce((sum, item) => {
          const product = products.find((p) => p.id === item.id);
          return sum + (product.price * item.quantity);
        }, 0);
        
        const totalEl = document.getElementById("cart-total-price");
        if (totalEl) totalEl.textContent = formatPrice(cartTotal);
      }

      // --- LOGIKA KERANJANG (CART LOGIC) ---

      function addToCart(productId) {
        const existingItem = cart.find((item) => item.id === productId);
        if (existingItem) {
          existingItem.quantity += 1;
        } else {
          cart.push({ id: productId, quantity: 1 });
        }
        updateCartUI();
        showToast(translations[currentLanguage]["cart-item-added"]);
      }

      function updateQuantity(productId, change) {
        const item = cart.find((item) => item.id === productId);
        if (item) {
          item.quantity += change;
          if (item.quantity <= 0) {
            removeFromCart(productId);
          } else {
            updateCartUI();
          }
        }
      }

      function removeFromCart(productId) {
        cart = cart.filter((item) => item.id !== productId);
        updateCartUI();
      }

      // Toggle Modal Keranjang
      function toggleCart() {
        const modal = document.getElementById("cart-modal");
        const overlay = document.getElementById("overlay");
        modal.classList.toggle("open");
        overlay.classList.toggle("active");
      }

      // --- INISIALISASI ---

      function initApp() {
        // Set tahun copyright
        document.getElementById("current-year").textContent = new Date().getFullYear();

        // Render awal
        renderProducts();
        renderReviews();
        updateTranslations();
        updateCartUI();

        // Ganti Bahasa
        document.querySelectorAll(".lang-btn").forEach((btn) => {
          btn.addEventListener("click", (e) => {
            // Update UI tombol aktif
            document.querySelectorAll(".lang-btn").forEach((b) => b.classList.remove("active"));
            e.target.classList.add("active");

            // Set bahasa baru
            currentLanguage = e.target.dataset.lang;
            
            // Re-render komponen
            renderProducts();
            renderReviews();
            updateTranslations();
            updateCartUI();
          });
        });

        // Event Listeners UI Utama
        document.getElementById("cart-icon").addEventListener("click", toggleCart);
        document.getElementById("close-cart").addEventListener("click", toggleCart);
        document.getElementById("overlay").addEventListener("click", toggleCart);
        
        document.getElementById("checkout-btn").addEventListener("click", () => {
          if (cart.length === 0) {
            showToast(translations[currentLanguage]["cart-empty"]);
            return;
          }
          showToast(`${translations[currentLanguage]["checkout-btn"]} - ${formatPrice(cartTotal)}`);
        });

        // Submit Form
        document.getElementById("order-form").addEventListener("submit", (e) => {
          e.preventDefault();
          // Simulasi pengiriman data
          showToast(translations[currentLanguage]["order-success"]);
          e.target.reset();
          cart = [];
          updateCartUI();
          toggleCart(); // Tutup cart jika terbuka
        });
      }

      // Jalankan saat DOM siap
      document.addEventListener("DOMContentLoaded", initApp);

    </script>
  </body>
</html>
