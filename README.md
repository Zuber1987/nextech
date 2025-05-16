<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Enriching Innovation | Tech Gadgets</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet" />
  <style>
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background-color: #0a0a0a;
      color: #ffffff;
    }
    header {
      background: #0d0d0d;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #222;
    }
    header h1 {
      margin: 0;
      font-size: 24px;
    }
    nav a {
      margin-left: 20px;
      color: #ffffff;
      text-decoration: none;
      font-weight: 500;
    }
    .hero {
      background: url('hero-image.png') no-repeat center center/cover;
      height: 80vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }
    .hero h2 {
      font-size: 48px;
      background: linear-gradient(90deg, #00ffe0, #007cf0);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      padding: 40px;
    }
    .product-card {
      background: #1a1a1a;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 255, 255, 0.1);
      transition: transform 0.3s;
      position: relative;
    }
    .product-card:hover {
      transform: scale(1.05);
    }
    .product-card img {
      width: 100%;
      border-radius: 8px;
    }
    .product-card h3 {
      margin-top: 15px;
      font-size: 20px;
    }
    .product-card p {
      font-size: 14px;
      color: #ccc;
    }
    .product-card button {
      margin-top: 10px;
      background: #00ffe0;
      border: none;
      padding: 10px 16px;
      border-radius: 6px;
      color: #000;
      font-weight: bold;
      cursor: pointer;
      transition: background 0.3s;
    }
    .product-card button:hover {
      background: #00cccc;
    }
    #cart {
      padding: 40px;
      background-color: #111;
    }
    #cart h2 {
      margin-bottom: 20px;
    }
    #cart-items {
      list-style: none;
      padding: 0;
    }
    #cart-items li {
      padding: 8px 0;
      border-bottom: 1px solid #333;
    }
    #contact {
      background: #111;
      padding: 40px;
      color: #ccc;
    }
    #contact h2 {
      margin-bottom: 20px;
    }
    footer {
      text-align: center;
      padding: 20px;
      background: #0d0d0d;
      border-top: 1px solid #222;
    }
  </style>
</head>
<body>
  <header>
    <h1>Tech Gadgets</h1>
    <nav>
      <a href="#">Home</a>
      <a href="#products">Products</a>
      <a href="#cart">Cart</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>
  <section class="hero">
    <h2>Enriching Innovation</h2>
  </section>
  <section id="products" class="products">
    <div class="product-card">
      <img src="headphones.jpg" alt="Wireless Headphones" />
      <h3>Wireless Headphones</h3>
      <p>High-fidelity sound with noise cancellation and long battery life.</p>
      <button onclick="addToCart('Wireless Headphones')">Add to Cart</button>
    </div>
    <div class="product-card">
      <img src="smartwatch.jpg" alt="Smartwatch" />
      <h3>Smartwatch</h3>
      <p>Stay connected and track your health with futuristic design.</p>
      <button onclick="addToCart('Smartwatch')">Add to Cart</button>
    </div>
    <div class="product-card">
      <img src="earbuds.jpg" alt="True Wireless Earbuds" />
      <h3>True Wireless Earbuds</h3>
      <p>Compact, powerful, and seamless connectivity for on-the-go audio.</p>
      <button onclick="addToCart('True Wireless Earbuds')">Add to Cart</button>
    </div>
    <div class="product-card">
      <img src="laptop.jpg" alt="Slim Laptop" />
      <h3>Slim Laptop</h3>
      <p>Performance meets portability with an ultra-sleek design.</p>
      <button onclick="addToCart('Slim Laptop')">Add to Cart</button>
    </div>
  </section>
  <section id="cart">
    <h2>Your Cart</h2>
    <ul id="cart-items"></ul>
  </section>
  <section id="contact">
    <h2>Contact Us</h2>
    <p>Email: support@techgadgets.com</p>
    <p>Phone: +1 (800) 123-4567</p>
    <p>Address: 123 Innovation Drive, Tech City, TX</p>
  </section>
  <footer>
    <p>&copy; 2025 Tech Gadgets. All rights reserved.</p>
  </footer>

  <script>
    const cartItems = [];
    function addToCart(product) {
      cartItems.push(product);
      renderCart();
    }
    function renderCart() {
      const list = document.getElementById('cart-items');
      list.innerHTML = '';
      cartItems.forEach((item, index) => {
        const li = document.createElement('li');
        li.textContent = `${index + 1}. ${item}`;
        list.appendChild(li);
      });
    }
  </script>
</body>
</html>
