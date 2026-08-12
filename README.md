<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>StoreTopUp - Toko Top Up Game Terpercaya</title>
  <style>
    /* --- CSS RESET & VARIABLE --- */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    :root {
      --primary-color: #00d26a;
      --bg-color: #0f172a;
      --card-bg: #1e293b;
      --text-color: #f8fafc;
      --text-muted: #94a3b8;
      --border-color: #334155;
    }

    body {
      background-color: var(--bg-color);
      color: var(--text-color);
      padding-bottom: 50px;
    }

    /* --- NAVBAR --- */
    header {
      background-color: var(--card-bg);
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid var(--border-color);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .logo {
      font-size: 1.5rem;
      font-weight: bold;
      color: var(--primary-color);
    }

    nav a {
      color: var(--text-color);
      text-decoration: none;
      margin-left: 1.5rem;
      transition: color 0.2s;
    }

    nav a:hover {
      color: var(--primary-color);
    }

    /* --- CONTAINER --- */
    .container {
      max-width: 1000px;
      margin: 2rem auto;
      padding: 0 1rem;
    }

    /* --- GAME BANNER --- */
    .game-header {
      display: flex;
      align-items: center;
      gap: 1.5rem;
      background-color: var(--card-bg);
      padding: 1.5rem;
      border-radius: 12px;
      border: 1px solid var(--border-color);
      margin-bottom: 2rem;
    }

    .game-avatar {
      width: 90px;
      height: 90px;
      background-color: #3b82f6;
      border-radius: 16px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 1.2rem;
      text-align: center;
    }

    .game-info h1 {
      font-size: 1.8rem;
      margin-bottom: 0.3rem;
    }

    .game-info p {
      color: var(--text-muted);
      font-size: 0.95rem;
    }

    /* --- FORM SECTIONS --- */
    .section-card {
      background-color: var(--card-bg);
      padding: 1.5rem;
      border-radius: 12px;
      border: 1px solid var(--border-color);
      margin-bottom: 1.5rem;
    }

    .section-title {
      font-size: 1.2rem;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .section-number {
      background-color: var(--primary-color);
      color: #000;
      width: 28px;
      height: 28px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 0.9rem;
    }

    /* --- INPUT USER ID --- */
    .input-group {
      display: flex;
      gap: 1rem;
    }

    .input-group input {
      flex: 1;
      padding: 0.8rem 1rem;
      border-radius: 8px;
      border: 1px solid var(--border-color);
      background-color: var(--bg-color);
      color: var(--text-color);
      font-size: 1rem;
      outline: none;
    }

    .input-group input:focus {
      border-color: var(--primary-color);
    }

    /* --- GRID ITEMS & PAYMENTS --- */
    .grid-container {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 1rem;
    }

    .option-card {
      background-color: var(--bg-color);
      border: 2px solid var(--border-color);
      border-radius: 8px;
      padding: 1rem;
      cursor: pointer;
      text-align: center;
      transition: all 0.2s;
    }

    .option-card:hover {
      border-color: var(--primary-color);
    }

    .option-card.selected {
      border-color: var(--primary-color);
      background-color: rgba(0, 210, 106, 0.1);
    }

    .option-title {
      font-weight: bold;
      margin-bottom: 0.5rem;
    }

    .option-price {
      color: var(--primary-color);
      font-size: 0.95rem;
    }

    /* --- SUBMIT BUTTON --- */
    .btn-submit {
      width: 100%;
      padding: 1rem;
      background-color: var(--primary-color);
      color: #000;
      font-size: 1.1rem;
      font-weight: bold;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: opacity 0.2s;
    }

    .btn-submit:hover {
      opacity: 0.9;
    }

    /* RESPONSIF MOBILE */
    @media (max-width: 600px) {
      .input-group {
        flex-direction: column;
      }
      .grid-container {
        grid-template-columns: repeat(2, 1fr);
      }
    }
  </style>
</head>
<body>

  <!-- NAVBAR -->
  <header>
    <div class="logo">🎮 StoreTopUp</div>
    <nav>
      <a href="#">Beranda</a>
      <a href="#">Cek Pesanan</a>
      <a href="#">Bantuan</a>
    </nav>
  </header>

  <div class="container">
    <!-- GAME HEADER -->
    <div class="game-header">
      <div class="game-avatar">MLBB</div>
      <div class="game-info">
        <h1>Mobile Legends: Bang Bang</h1>
        <p>Proses instan 24 jam. Masukkan User ID dan Zone ID Anda.</p>
      </div>
    </div>

    <!-- FORM TOP UP -->
    <form id="topupForm">
      
      <!-- STEP 1: ID USER -->
      <div class="section-card">
        <h2 class="section-title">
          <span class="section-number">1</span> Masukkan Data Akun
        </h2>
        <div class="input-group">
          <input type="number" id="userId" placeholder="Masukkan User ID" required>
          <input type="number" id="zoneId" placeholder="(Zone ID)" required>
        </div>
      </div>

      <!-- STEP 2: NOMINAL DIAMOND -->
      <div class="section-card">
        <h2 class="section-title">
          <span class="section-number">2</span> Pilih Nominal Top Up
        </h2>
        <div class="grid-container" id="itemGrid">
          <div class="option-card" onclick="selectItem(this, '86 Diamonds', 20000)">
            <div class="option-title">💎 86 Diamonds</div>
            <div class="option-price">Rp 20.000</div>
          </div>
          <div class="option-card" onclick="selectItem(this, '172 Diamonds', 40000)">
            <div class="option-title">💎 172 Diamonds</div>
            <div class="option-price">Rp 40.000</div>
          </div>
          <div class="option-card" onclick="selectItem(this, '257 Diamonds', 60000)">
            <div class="option-title">💎 257 Diamonds</div>
            <div class="option-price">Rp 60.000</div>
          </div>
          <div class="option-card" onclick="selectItem(this, '706 Diamonds', 160000)">
            <div class="option-title">💎 706 Diamonds</div>
            <div class="option-price">Rp 160.000</div>
          </div>
          <div class="option-card" onclick="selectItem(this, 'Weekly Diamond Pass', 28000)">
            <div class="option-title">🎟️ Weekly Pass</div>
            <div class="option-price">Rp 28.000</div>
          </div>
          <div class="option-card" onclick="selectItem(this, '2195 Diamonds', 490000)">
            <div class="option-title">💎 2195 Diamonds</div>
            <div class="option-price">Rp 490.000</div>
          </div>
        </div>
      </div>

      <!-- STEP 3: METODE PEMBAYARAN -->
      <div class="section-card">
        <h2 class="section-title">
          <span class="section-number">3</span> Pilih Pembayaran
        </h2>
        <div class="grid-container" id="paymentGrid">
          <div class="option-card" onclick="selectPayment(this, 'QRIS')">
            <div class="option-title">📱 QRIS / All E-Wallet</div>
            <div class="option-price">Instan</div>
          </div>
          <div class="option-card" onclick="selectPayment(this, 'GoPay')">
            <div class="option-title">🟢 GoPay</div>
            <div class="option-price">Instan</div>
          </div>
          <div class="option-card" onclick="selectPayment(this, 'DANA')">
            <div class="option-title">🔵 DANA</div>
            <div class="option-price">Instan</div>
          </div>
          <div class="option-card" onclick="selectPayment(this, 'Transfer BCA')">
            <div class="option-title">🏦 Bank BCA</div>
            <div class="option-price">Verifikasi Otomatis</div>
          </div>
        </div>
      </div>

      <!-- STEP 4: TOMBOL BELI -->
      <button type="button" class="btn-submit" onclick="processOrder()">Beli Sekarang</button>
    </form>
  </div>

  <!-- JAVASCRIPT LOGIC -->
  <script>
    let selectedItem = null;
    let selectedPrice = 0;
    let selectedPayment = null;

    // Fungsi Memilih Item Top Up
    function selectItem(element, name, price) {
      const items = document.querySelectorAll('#itemGrid .option-card');
      items.forEach(item => item.classList.remove('selected'));
      
      element.classList.add('selected');
      selectedItem = name;
      selectedPrice = price;
    }

    // Fungsi Memilih Metode Pembayaran
    function selectPayment(element, method) {
      const payments = document.querySelectorAll('#paymentGrid .option-card');
      payments.forEach(pay => pay.classList.remove('selected'));
      
      element.classList.add('selected');
      selectedPayment = method;
    }

    // Fungsi Submit Transaksi
    function processOrder() {
      const userId = document.getElementById('userId').value;
      const zoneId = document.getElementById('zoneId').value;

      if (!userId || !zoneId) {
        alert('Harap isi User ID dan Zone ID Anda!');
        return;
      }

      if (!selectedItem) {
        alert('Harap pilih nominal Top Up!');
        return;
      }

      if (!selectedPayment) {
        alert('Harap pilih metode pembayaran!');
        return;
      }

      const confirmText = `
    === KONFIRMASI PESANAN ===
    User ID: ${userId} (${zoneId})
    Item: ${selectedItem}
    Total Harga: Rp ${selectedPrice.toLocaleString('id-ID')}
    Pembayaran: ${selectedPayment}

    Lanjutkan ke pembayaran?
      `;

      if (confirm(confirmText)) {
        alert('Pesanan berhasil dibuat! Mengalihkan ke halaman pembayaran...');
        // Di sini Anda bisa menghubungkan dengan Payment Gateway backend (Midtrans, Tripay, dll)
      }
    }
  </script>
</body>
</html># web-game
