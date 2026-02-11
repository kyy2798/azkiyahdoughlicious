<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Doughlicious - Pastry Bakery Multibahasa</title>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <!-- Header & Navigation -->
    <header>
      <div class="container header-content">
        <div class="logo">
          <i class="fas fa-birthday-cake"></i>
          <h1 id="site-title">Doughlicious</h1>
        </div>

        <ul class="nav-links">
          <li><a href="#home" id="nav-home">Beranda</a></li>
          <li><a href="#products" id="nav-products">Produk</a></li>
          <li><a href="#reviews" id="nav-reviews">Ulasan</a></li>
          <li><a href="#order" id="nav-order">Pesan</a></li>
        </ul>

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
              Doughlicious telah menyajikan pastry lezat sejak 2010. Kami
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
      <div class="cart-total">
        <span id="total-text">Total:</span>
        <span id="cart-total-price">Rp 0</span>
      </div>
      <button class="checkout-btn" id="checkout-btn">
        Lanjut ke Pembayaran
      </button>
    </div>

    <!-- Overlay untuk cart modal -->
    <div class="overlay" id="overlay"></div>

    <script src="script.js"></script>
  </body>
</html>

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
}

body {
  background-color: var(--cream);
  color: var(--dark-brown);
  line-height: 1.6;
  transition: all 0.3s ease;
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Header & Navigation */
header {
  background-color: var(--primary-brown);
  padding: 15px 0;
  position: sticky;
  top: 0;
  z-index: 1000;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
}

.logo i {
  font-size: 2.2rem;
  color: var(--cream);
  margin-right: 10px;
}

.logo h1 {
  color: var(--white);
  font-size: 1.8rem;
  font-weight: 700;
}

.nav-links {
  display: flex;
  list-style: none;
}

.nav-links li {
  margin-left: 25px;
}

.nav-links a {
  color: var(--white);
  text-decoration: none;
  font-weight: 500;
  font-size: 1.1rem;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: var(--cream);
}

.language-selector {
  display: flex;
  align-items: center;
  background-color: var(--light-brown);
  border-radius: 20px;
  padding: 5px;
}

.lang-btn {
  background: none;
  border: none;
  color: var(--white);
  padding: 8px 15px;
  border-radius: 15px;
  cursor: pointer;
  font-weight: 500;
  transition: all 0.3s;
}

.lang-btn.active {
  background-color: var(--primary-brown);
}

.cart-icon {
  position: relative;
  margin-left: 20px;
  cursor: pointer;
}

.cart-icon i {
  font-size: 1.8rem;
  color: var(--white);
}

.cart-count {
  position: absolute;
  top: -8px;
  right: -8px;
  background-color: var(--cream);
  color: var(--primary-brown);
  border-radius: 50%;
  width: 22px;
  height: 22px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.9rem;
  font-weight: bold;
}

/* Hero Section */
.hero {
  background:
    linear-gradient(rgba(139, 69, 19, 0.85), rgba(139, 69, 19, 0.9)),
    url("https://images.unsplash.com/photo-1509440159596-0249088772ff?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1472&q=80");
  background-size: cover;
  background-position: center;
  color: var(--white);
  padding: 100px 0;
  text-align: center;
}

.hero h2 {
  font-size: 3.2rem;
  margin-bottom: 20px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.hero p {
  font-size: 1.3rem;
  max-width: 700px;
  margin: 0 auto 30px;
  color: var(--cream);
}

.cta-button {
  display: inline-block;
  background-color: var(--cream);
  color: var(--primary-brown);
  padding: 15px 35px;
  border-radius: 30px;
  text-decoration: none;
  font-weight: bold;
  font-size: 1.2rem;
  transition: all 0.3s;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

.cta-button:hover {
  background-color: var(--white);
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
}

/* Products Section */
.section-title {
  text-align: center;
  margin: 60px 0 40px;
  color: var(--dark-brown);
  font-size: 2.5rem;
  position: relative;
}

.section-title:after {
  content: "";
  position: absolute;
  width: 100px;
  height: 4px;
  background-color: var(--primary-brown);
  bottom: -15px;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 2px;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 30px;
  margin-bottom: 60px;
}

.product-card {
  background-color: var(--white);
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
  transition:
    transform 0.3s,
    box-shadow 0.3s;
}

.product-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
}

.product-img {
  height: 200px;
  overflow: hidden;
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
}

.product-name {
  font-size: 1.4rem;
  margin-bottom: 10px;
  color: var(--dark-brown);
}

.product-price {
  color: var(--primary-brown);
  font-size: 1.3rem;
  font-weight: bold;
  margin-bottom: 15px;
}

.add-to-cart {
  background-color: var(--primary-brown);
  color: var(--white);
  border: none;
  padding: 10px 20px;
  border-radius: 25px;
  cursor: pointer;
  font-weight: 500;
  width: 100%;
  transition: background-color 0.3s;
}

.add-to-cart:hover {
  background-color: var(--light-brown);
}

/* Reviews Section */
.reviews-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 30px;
  margin-bottom: 60px;
}

.review-card {
  background-color: var(--white);
  padding: 25px;
  border-radius: 15px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
}

.review-header {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}

.review-avatar {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  overflow: hidden;
  margin-right: 15px;
  border: 3px solid var(--cream);
}

.review-avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.review-name {
  font-size: 1.2rem;
  color: var(--dark-brown);
  font-weight: 600;
}

.review-rating {
  color: #ffc107;
  margin-top: 5px;
}

.review-text {
  color: var(--gray);
  font-style: italic;
  line-height: 1.7;
}

/* Cart Modal */
.cart-modal {
  position: fixed;
  top: 0;
  right: -400px;
  width: 380px;
  height: 100%;
  background-color: var(--white);
  box-shadow: -5px 0 25px rgba(0, 0, 0, 0.15);
  z-index: 1001;
  transition: right 0.4s ease;
  padding: 25px;
  overflow-y: auto;
}

.cart-modal.open {
  right: 0;
}

.cart-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 25px;
  padding-bottom: 15px;
  border-bottom: 2px solid var(--cream);
}

.cart-title {
  font-size: 1.8rem;
  color: var(--dark-brown);
}

.close-cart {
  background: none;
  border: none;
  font-size: 1.8rem;
  color: var(--dark-brown);
  cursor: pointer;
}

.cart-items {
  margin-bottom: 25px;
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
}

.cart-item-price {
  color: var(--primary-brown);
  font-weight: bold;
}

.cart-item-quantity {
  display: flex;
  align-items: center;
}

.quantity-btn {
  background-color: var(--cream);
  border: none;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  font-weight: bold;
  color: var(--dark-brown);
}

.cart-quantity {
  margin: 0 10px;
  font-weight: bold;
}

.remove-item {
  background: none;
  border: none;
  color: #ff6b6b;
  cursor: pointer;
  margin-left: 10px;
  font-size: 1.1rem;
}

.cart-total {
  display: flex;
  justify-content: space-between;
  font-size: 1.4rem;
  font-weight: bold;
  color: var(--dark-brown);
  padding-top: 20px;
  border-top: 2px solid var(--cream);
  margin-bottom: 25px;
}

.checkout-btn {
  background-color: var(--primary-brown);
  color: var(--white);
  border: none;
  width: 100%;
  padding: 15px;
  border-radius: 30px;
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s;
}

.checkout-btn:hover {
  background-color: var(--light-brown);
}

/* Order Form */
.order-form-container {
  background-color: var(--white);
  padding: 40px;
  border-radius: 20px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  margin-bottom: 60px;
}

.form-title {
  color: var(--dark-brown);
  margin-bottom: 30px;
  font-size: 2rem;
  text-align: center;
}

.form-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 25px;
  margin-bottom: 30px;
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
  padding: 14px;
  border: 2px solid #ddd;
  border-radius: 10px;
  font-size: 1rem;
  color: var(--gray);
  transition: border-color 0.3s;
}

.form-group input:focus,
.form-group select:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--primary-brown);
}

.submit-order {
  background-color: var(--primary-brown);
  color: var(--white);
  border: none;
  padding: 16px 40px;
  border-radius: 30px;
  font-size: 1.2rem;
  font-weight: bold;
  cursor: pointer;
  display: block;
  margin: 0 auto;
  transition: background-color 0.3s;
}

.submit-order:hover {
  background-color: var(--light-brown);
}

/* Footer */
footer {
  background-color: var(--dark-brown);
  color: var(--cream);
  padding: 50px 0 30px;
  margin-top: 50px;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 40px;
  margin-bottom: 40px;
}

.footer-column h3 {
  font-size: 1.5rem;
  margin-bottom: 20px;
  color: var(--white);
}

.footer-column p,
.footer-column a {
  color: var(--cream);
  margin-bottom: 10px;
  display: block;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-column a:hover {
  color: var(--white);
}

.social-icons {
  display: flex;
  margin-top: 20px;
}

.social-icons a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background-color: var(--light-brown);
  border-radius: 50%;
  margin-right: 15px;
  font-size: 1.2rem;
}

.copyright {
  text-align: center;
  padding-top: 30px;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  color: rgba(255, 255, 255, 0.7);
  font-size: 0.9rem;
}

/* Overlay untuk cart modal */
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
  transition: all 0.3s;
}

.overlay.active {
  opacity: 1;
  visibility: visible;
}

/* Responsive Design */
@media (max-width: 992px) {
  .header-content {
    flex-direction: column;
  }

  .nav-links {
    margin-top: 20px;
  }

  .language-selector,
  .cart-icon {
    margin-top: 15px;
  }

  .hero h2 {
    font-size: 2.5rem;
  }
}

@media (max-width: 768px) {
  .nav-links {
    flex-direction: column;
    align-items: center;
  }

  .nav-links li {
    margin: 10px 0;
  }

  .cart-modal {
    width: 100%;
    right: -100%;
  }

  .hero {
    padding: 70px 0;
  }

  .hero h2 {
    font-size: 2rem;
  }

  .section-title {
    font-size: 2rem;
  }
}

// Data produk dengan 12 menu (6 sebelumnya + 6 baru)
const products = [
  {
    id: 1,
    name: {
      id: "Croissant Almond",
      en: "Almond Croissant",
      it: "Croissant alle Mandorle",
    },
    price: 25000,
    image:
      "https://i.pinimg.com/originals/ef/f2/3e/eff23e936f25796aa4a732786473fc8b.jpg",
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
      "https://th.bing.com/th/id/OIP.Fc5B1CObarCPZqBRE6PMZQHaJQ?o=7rm=3&rs=1&pid=ImgDetMain&o=7&rm=3",
  },
  {
    id: 3,
    name: { id: "Danish Keju", en: "Cheese Danish", it: "Danish al Formaggio" },
    price: 28000,
    image:
      "https://tse4.mm.bing.net/th/id/OIP.DmSMZbEWWTJuBUvDJCAD0QHaHa?rs=1&pid=ImgDetMain&o=7&rm=3",
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
      "https://thescranline.com/wp-content/uploads/2023/01/CHOCOLATE-ECLAIRS-WEB-04.jpg",
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
      "https://thescranline.com/wp-content/uploads/2023/01/CHOCOLATE-ECLAIRS-WEB-04.jpg",
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
      "https://images.unsplash.com/photo-1565958011703-44f9829ba187?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1465&q=80",
  },
  // Menu tambahan 1-6
  {
    id: 7,
    name: {
      id: "Bolu Coklat Belgia",
      en: "Belgian Chocolate Cake",
      it: "Torta al Cioccolato Belga",
    },
    price: 150000,
    image:
      "https://images.unsplash.com/photo-1578985545062-69928b1d9587?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1389&q=80",
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
      "https://tse1.mm.bing.net/th/id/OIP.e2gI-cGefgkJ0D_MQIcbZQHaE7?rs=1&pid=ImgDetMain&o=7&rm=3",
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
      "https://mujermexico.com/wp-content/uploads/2023/07/cheesecake-origen.jpg",
  },
  {
    id: 10,
    name: {
      id: "Pavlova Berry",
      en: "Berry Pavlova",
      it: "Pavlova ai Frutti di Bosco",
    },
    price: 48000,
    image: "https://athomedishes.com/assets/images/1740391778375-nm2jhrf4.webp",
  },
  {
    id: 11,
    name: {
      id: "Canelé Bordeaux",
      en: "Canelé de Bordeaux",
      it: "Canelé di Bordeaux",
    },
    price: 18000,
    image: "https://i.ytimg.com/vi/tHe7rxHgflk/maxresdefault.jpg",
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
      "https://therecipemaster.com/wp-content/uploads/2025/01/financier-recipe.webp",
  },
];

// Data ulasan
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

// Data terjemahan lengkap
const translations = {
  id: {
    // Navigation
    "site-title": "Doughlicious",
    "nav-home": "Beranda",
    "nav-products": "Produk",
    "nav-reviews": "Ulasan",
    "nav-order": "Pesan",

    // Hero
    "hero-title": "Pastry Lezat, Dibuat dengan Cinta",
    "hero-text":
      "Temukan kelezatan pastry buatan tangan kami yang dipanggang segar setiap hari. Dari croissant klasik hingga kue kreatif, kami menyajikan kualitas terbaik.",
    "hero-button": "Lihat Produk Kami",

    // Products
    "products-title": "Produk Unggulan",
    "add-to-cart": "Tambah ke Keranjang",

    // Reviews
    "reviews-title": "Ulasan Pelanggan",

    // Order Form
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

    // Cart
    "cart-title": "Keranjang Belanja",
    "total-text": "Total:",
    "checkout-btn": "Lanjut ke Pembayaran",
    "remove-item": "Hapus",

    // Footer
    "footer-about": "Tentang Kami",
    "footer-about-text":
      "Doughlicious telah menyajikan pastry lezat sejak 2025. Kami berkomitmen menggunakan bahan terbaik dan resep tradisional.",
    "footer-contact": "Kontak",
    "footer-hours": "Jam Buka",
    "hours-mon": "Senin - Jumat: 7:00 - 20:00",
    "hours-sat": "Sabtu: 7:00 - 22:00",
    "hours-sun": "Minggu: 8:00 - 18:00",
    "footer-rights": "Semua hak dilindungi.",

    // Messages
    "order-success":
      "Pesanan berhasil! Kami akan menghubungi Anda untuk konfirmasi.",
    "cart-empty": "Keranjang Anda kosong.",
    "cart-item-added": "Ditambahkan ke keranjang!",
  },
  en: {
    // Navigation
    "site-title": "Doughlicious",
    "nav-home": "Home",
    "nav-products": "Products",
    "nav-reviews": "Reviews",
    "nav-order": "Order",

    // Hero
    "hero-title": "Delicious Pastries, Made with Love",
    "hero-text":
      "Discover the deliciousness of our handmade pastries baked fresh daily. From classic croissants to creative cakes, we serve the best quality.",
    "hero-button": "View Our Products",

    // Products
    "products-title": "Featured Products",
    "add-to-cart": "Add to Cart",

    // Reviews
    "reviews-title": "Customer Reviews",

    // Order Form
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

    // Cart
    "cart-title": "Shopping Cart",
    "total-text": "Total:",
    "checkout-btn": "Proceed to Checkout",
    "remove-item": "Remove",

    // Footer
    "footer-about": "About Us",
    "footer-about-text":
      "Doughlicious has been serving delicious pastries since 2025. We are committed to using the best ingredients and traditional recipes.",
    "footer-contact": "Contact",
    "footer-hours": "Opening Hours",
    "hours-mon": "Monday - Friday: 7:00 - 20:00",
    "hours-sat": "Saturday: 7:00 - 22:00",
    "hours-sun": "Sunday: 8:00 - 18:00",
    "footer-rights": "All rights reserved.",

    // Messages
    "order-success": "Order successful! We will contact you for confirmation.",
    "cart-empty": "Your cart is empty.",
    "cart-item-added": "Added to cart!",
  },
  it: {
    // Navigation
    "site-title": "Doughlicious",
    "nav-home": "Home",
    "nav-products": "Prodotti",
    "nav-reviews": "Recensioni",
    "nav-order": "Ordina",

    // Hero
    "hero-title": "Pasticceria Deliziosa, Fatta con Amore",
    "hero-text":
      "Scopri la delizia delle nostre pasticcerie fatte a mano, cotte fresche ogni giorno. Dai croissant classici alle torte creative, serviamo la migliore qualità.",
    "hero-button": "Vedi i Nostri Prodotti",

    // Products
    "products-title": "Prodotti in Evidenza",
    "add-to-cart": "Aggiungi al Carrello",

    // Reviews
    "reviews-title": "Recensioni dei Clienti",

    // Order Form
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

    // Cart
    "cart-title": "Carrello della Spesa",
    "total-text": "Totale:",
    "checkout-btn": "Procedi al Pagamento",
    "remove-item": "Rimuovi",

    // Footer
    "footer-about": "Chi Siamo",
    "footer-about-text":
      "Doughlicious serve deliziose pasticcerie dal 2025. Ci impegniamo a utilizzare i migliori ingredienti e ricette tradizionali.",
    "footer-contact": "Contatti",
    "footer-hours": "Orari di Apertura",
    "hours-mon": "Lunedì - Venerdì: 7:00 - 20:00",
    "hours-sat": "Sabato: 7:00 - 22:00",
    "hours-sun": "Domenica: 8:00 - 18:00",
    "footer-rights": "Tutti i diritti riservati.",

    // Messages
    "order-success":
      "Ordine effettuato con successo! Ti contatteremo per la conferma.",
    "cart-empty": "Il tuo carrello è vuoto.",
    "cart-item-added": "Aggiunto al carrello!",
  },
};

// State aplikasi
let currentLanguage = "id";
let cart = [];
let cartTotal = 0;

// Format harga ke Rupiah
function formatPrice(price) {
  if (currentLanguage === "en") {
    return `$${(price / 14000).toFixed(2)}`;
  } else if (currentLanguage === "it") {
    return `€${(price / 16000).toFixed(2)}`;
  } else {
    return `Rp ${price.toLocaleString("id-ID")}`;
  }
}

// Render produk
function renderProducts() {
  const productsContainer = document.getElementById("products-container");
  if (!productsContainer) return;

  productsContainer.innerHTML = "";

  products.forEach((product) => {
    const productCard = document.createElement("div");
    productCard.className = "product-card";
    productCard.innerHTML = `
            <div class="product-img">
                <img src="${product.image}" alt="${product.name[currentLanguage]}">
            </div>
            <div class="product-info">
                <h3 class="product-name">${product.name[currentLanguage]}</h3>
                <p class="product-price">${formatPrice(product.price)}</p>
                <button class="add-to-cart" data-id="${product.id}">
                    ${translations[currentLanguage]["add-to-cart"]}
                </button>
            </div>
        `;
    productsContainer.appendChild(productCard);
  });

  // Tambahkan event listener untuk tombol "Tambah ke Keranjang"
  document.querySelectorAll(".add-to-cart").forEach((button) => {
    button.addEventListener("click", function () {
      const productId = parseInt(this.getAttribute("data-id"));
      addToCart(productId);
    });
  });
}

// Render ulasan
function renderReviews() {
  const reviewsContainer = document.getElementById("reviews-container");
  if (!reviewsContainer) return;

  reviewsContainer.innerHTML = "";

  reviews.forEach((review) => {
    const reviewCard = document.createElement("div");
    reviewCard.className = "review-card";

    // Buang rating bintang
    let stars = "";
    for (let i = 0; i < 5; i++) {
      if (i < review.rating) {
        stars += '<i class="fas fa-star"></i>';
      } else {
        stars += '<i class="far fa-star"></i>';
      }
    }

    reviewCard.innerHTML = `
            <div class="review-header">
                <div class="review-avatar">
                    <img src="${review.avatar}" alt="${review.name[currentLanguage]}">
                </div>
                <div>
                    <h4 class="review-name">${review.name[currentLanguage]}</h4>
                    <div class="review-rating">${stars}</div>
                </div>
            </div>
            <p class="review-text">"${review.text[currentLanguage]}"</p>
        `;
    reviewsContainer.appendChild(reviewCard);
  });
}

// Update terjemahan
function updateTranslations() {
  Object.keys(translations[currentLanguage]).forEach((key) => {
    const element = document.getElementById(key);
    if (element) {
      if (
        key === "submit-order" ||
        key === "checkout-btn" ||
        key === "add-to-cart" ||
        key === "hero-button" ||
        key === "remove-item"
      ) {
        element.textContent = translations[currentLanguage][key];
      } else if (key === "footer-about-text" || key === "hero-text") {
        element.textContent = translations[currentLanguage][key];
      } else {
        element.textContent = translations[currentLanguage][key];
      }
    }
  });

  // Update placeholder untuk textarea catatan
  const notesTextarea = document.getElementById("notes");
  if (notesTextarea) {
    if (currentLanguage === "id") {
      notesTextarea.placeholder = "Contoh: Tanpa kacang, tambah coklat, dll.";
    } else if (currentLanguage === "en") {
      notesTextarea.placeholder = "Example: No nuts, extra chocolate, etc.";
    } else if (currentLanguage === "it") {
      notesTextarea.placeholder = "Esempio: Senza noci, cioccolato extra, ecc.";
    }
  }
}

// Update cart count
function updateCartCount() {
  const cartCount = document.getElementById("cart-count");
  if (!cartCount) return;

  const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
  cartCount.textContent = totalItems;
}

// Update cart total
function updateCartTotal() {
  const cartTotalElement = document.getElementById("cart-total-price");
  if (!cartTotalElement) return;

  cartTotal = cart.reduce((sum, item) => {
    const product = products.find((p) => p.id === item.id);
    return sum + product.price * item.quantity;
  }, 0);

  cartTotalElement.textContent = formatPrice(cartTotal);
}

// Render cart items
function renderCartItems() {
  const cartItemsContainer = document.getElementById("cart-items");
  if (!cartItemsContainer) return;

  if (cart.length === 0) {
    cartItemsContainer.innerHTML = `<p>${translations[currentLanguage]["cart-empty"]}</p>`;
    updateCartTotal();
    return;
  }

  cartItemsContainer.innerHTML = "";

  cart.forEach((item) => {
    const product = products.find((p) => p.id === item.id);
    if (!product) return;

    const cartItem = document.createElement("div");
    cartItem.className = "cart-item";
    cartItem.innerHTML = `
            <div class="cart-item-info">
                <h4>${product.name[currentLanguage]}</h4>
                <p class="cart-item-price">${formatPrice(product.price)}</p>
            </div>
            <div class="cart-item-quantity">
                <button class="quantity-btn decrease" data-id="${product.id}">-</button>
                <span class="cart-quantity">${item.quantity}</span>
                <button class="quantity-btn increase" data-id="${product.id}">+</button>
                <button class="remove-item" data-id="${product.id}">${translations[currentLanguage]["remove-item"]}</button>
            </div>
        `;
    cartItemsContainer.appendChild(cartItem);
  });

  // Tambahkan event listeners untuk tombol di cart
  document.querySelectorAll(".quantity-btn.decrease").forEach((button) => {
    button.addEventListener("click", function () {
      const productId = parseInt(this.getAttribute("data-id"));
      updateCartItemQuantity(productId, -1);
    });
  });

  document.querySelectorAll(".quantity-btn.increase").forEach((button) => {
    button.addEventListener("click", function () {
      const productId = parseInt(this.getAttribute("data-id"));
      updateCartItemQuantity(productId, 1);
    });
  });

  document.querySelectorAll(".remove-item").forEach((button) => {
    button.addEventListener("click", function () {
      const productId = parseInt(this.getAttribute("data-id"));
      removeFromCart(productId);
    });
  });

  updateCartTotal();
}

// Tambah item ke cart
function addToCart(productId) {
  const existingItem = cart.find((item) => item.id === productId);

  if (existingItem) {
    existingItem.quantity += 1;
  } else {
    cart.push({ id: productId, quantity: 1 });
  }

  updateCartCount();
  renderCartItems();

  // Tampilkan notifikasi
  alert(translations[currentLanguage]["cart-item-added"]);
}

// Update quantity item di cart
function updateCartItemQuantity(productId, change) {
  const item = cart.find((item) => item.id === productId);

  if (item) {
    item.quantity += change;

    if (item.quantity <= 0) {
      cart = cart.filter((item) => item.id !== productId);
    }
  }

  updateCartCount();
  renderCartItems();
}

// Hapus item dari cart
function removeFromCart(productId) {
  cart = cart.filter((item) => item.id !== productId);
  updateCartCount();
  renderCartItems();
}

// Toggle cart modal
function toggleCartModal() {
  const cartModal = document.getElementById("cart-modal");
  const overlay = document.getElementById("overlay");

  cartModal.classList.toggle("open");
  overlay.classList.toggle("active");

  // Render ulang item cart saat modal dibuka
  if (cartModal.classList.contains("open")) {
    renderCartItems();
  }
}

// Inisialisasi aplikasi
function initApp() {
  // Set tahun saat ini di footer
  const currentYearElement = document.getElementById("current-year");
  if (currentYearElement) {
    currentYearElement.textContent = new Date().getFullYear();
  }

  // Render konten awal
  renderProducts();
  renderReviews();
  updateTranslations();
  updateCartCount();

  // Event listener untuk tombol bahasa
  document.querySelectorAll(".lang-btn").forEach((button) => {
    button.addEventListener("click", function () {
      const lang = this.getAttribute("data-lang");

      // Update tombol aktif
      document.querySelectorAll(".lang-btn").forEach((btn) => {
        btn.classList.remove("active");
      });
      this.classList.add("active");

      // Update bahasa
      currentLanguage = lang;
      renderProducts();
      renderReviews();
      updateTranslations();
      renderCartItems();
    });
  });

  // Event listener untuk ikon cart
  const cartIcon = document.getElementById("cart-icon");
  if (cartIcon) {
    cartIcon.addEventListener("click", toggleCartModal);
  }

  // Event listener untuk tombol close cart
  const closeCartBtn = document.getElementById("close-cart");
  if (closeCartBtn) {
    closeCartBtn.addEventListener("click", toggleCartModal);
  }

  // Event listener untuk overlay
  const overlay = document.getElementById("overlay");
  if (overlay) {
    overlay.addEventListener("click", toggleCartModal);
  }

  // Event listener untuk tombol checkout
  const checkoutBtn = document.getElementById("checkout-btn");
  if (checkoutBtn) {
    checkoutBtn.addEventListener("click", function (e) {
      e.preventDefault();
      if (cart.length === 0) {
        alert(translations[currentLanguage]["cart-empty"]);
        return;
      }
      alert(
        `${translations[currentLanguage]["checkout-btn"]} - ${formatPrice(cartTotal)}`,
      );
    });
  }

  // Event listener untuk formulir pemesanan
  const orderForm = document.getElementById("order-form");
  if (orderForm) {
    orderForm.addEventListener("submit", function (e) {
      e.preventDefault();

      // Validasi sederhana
      const name = document.getElementById("name").value;
      const email = document.getElementById("email").value;
      const phone = document.getElementById("phone").value;
      const delivery = document.getElementById("delivery").value;

      if (!name || !email || !phone || !delivery) {
        alert("Harap isi semua field yang wajib diisi.");
        return;
      }

      // Tampilkan konfirmasi
      alert(translations[currentLanguage]["order-success"]);

      // Reset formulir
      orderForm.reset();

      // Reset keranjang
      cart = [];
      updateCartCount();
      renderCartItems();
    });
  }

  // Smooth scroll untuk navigation links
  document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
    anchor.addEventListener("click", function (e) {
      e.preventDefault();

      const targetId = this.getAttribute("href");
      if (targetId === "#") return;

      const targetElement = document.querySelector(targetId);
      if (targetElement) {
        window.scrollTo({
          top: targetElement.offsetTop - 80,
          behavior: "smooth",
        });
      }
    });
  });
}

// Jalankan aplikasi saat DOM siap
document.addEventListener("DOMContentLoaded", initApp);

rapikan codingan tersebut
