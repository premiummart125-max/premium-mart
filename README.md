# premium-mart
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Premium Mart</title>
  <meta name="description" content="Premium Mart - Fresh groceries, produce, and household items in Negombo.">
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    body { font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji"; }
    .line-clamp-2 { display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; overflow: hidden; }
    .backdrop { backdrop-filter: blur(6px); }
  </style>
</head>
<body class="bg-black text-white">
  <!-- Top Bar / Announcement -->
  <div class="bg-red-700 text-white text-sm">
    <div class="max-w-6xl mx-auto px-4 py-2 flex items-center justify-between">
      <p>🚚 Free delivery within 3km on orders over Rs. 3,000</p>
      <a class="underline hover:no-underline" href="#offers">See today’s offers →</a>
    </div>
  </div>

  <!-- Header -->
  <header class="bg-black sticky top-0 z-40 shadow-md">
    <div class="max-w-6xl mx-auto px-4 py-4 flex items-center gap-4">
      <a href="#" class="flex items-center gap-3"> 
        <img src="48 X 48 LIGHT BOARD-01.jpg" alt="Premium Mart Logo" class="h-12 w-12 rounded-xl shadow-md">
        <div>
          <div class="text-xl font-semibold leading-5 text-red-500">Premium Mart</div>
          <div class="text-xs text-gray-400 leading-4">Fresh • Friendly • Fast</div>
        </div>
      </a>
      <div class="flex-1"></div>
      <button id="cartBtn" class="relative px-4 py-2 rounded-xl bg-red-600 text-white hover:bg-red-500">
        🛒 <span class="ml-2">Cart</span>
        <span id="cartCount" class="absolute -top-2 -right-2 text-xs bg-black text-white rounded-full w-6 h-6 grid place-content-center">0</span>
      </button>
    </div>
  </header>

  <!-- Hero / Offers -->
  <section id="offers" class="max-w-6xl mx-auto px-4 mt-6">
    <div class="rounded-3xl bg-gradient-to-r from-black to-red-700 p-6 md:p-10 text-white shadow-xl">
      <h1 class="text-3xl md:text-4xl font-bold leading-tight">Welcome to Premium Mart</h1>
      <p class="mt-2 text-gray-200">ඔබට අවශ්ය හැමදේම — vegetables, fruits, dairy, snacks, and home essentials — එකම තැනකින්.</p>
      <div class="mt-5 flex gap-3">
        <a href="#products" class="px-5 py-3 rounded-2xl bg-red-600 text-white font-semibold shadow hover:shadow-md">Shop Now</a>
        <a href="#checkout" class="px-5 py-3 rounded-2xl border border-red-400 text-white font-semibold hover:bg-red-600/20">Checkout</a>
      </div>
    </div>
  </section>

  <!-- Products -->
  <section id="products" class="max-w-6xl mx-auto px-4 mt-6 mb-24">
    <div class="flex items-baseline justify-between">
      <h2 class="text-xl md:text-2xl font-semibold text-red-500">Popular Products</h2>
    </div>
    <div id="productGrid" class="grid sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 mt-4"></div>
  </section>

  <!-- Checkout Form -->
  <section id="checkout" class="bg-black border-t border-red-700">
    <div class="max-w-3xl mx-auto px-4 py-12">
      <h2 class="text-2xl font-semibold mb-4 text-red-500">Checkout</h2>
      <form id="checkoutForm" class="space-y-4">
        <div>
          <label class="block text-sm font-medium">Full Name</label>
          <input id="custName" type="text" required class="w-full px-4 py-2 rounded-xl border border-gray-700 bg-gray-900 text-white focus:ring-2 focus:ring-red-500">
        </div>
        <div>
          <label class="block text-sm font-medium">Phone Number</label>
          <input id="custPhone" type="tel" required class="w-full px-4 py-2 rounded-xl border border-gray-700 bg-gray-900 text-white focus:ring-2 focus:ring-red-500">
        </div>
        <div>
          <label class="block text-sm font-medium">Delivery Address</label>
          <textarea id="custAddress" required class="w-full px-4 py-2 rounded-xl border border-gray-700 bg-gray-900 text-white focus:ring-2 focus:ring-red-500"></textarea>
        </div>
        <div>
          <label class="block text-sm font-medium">Payment Method</label>
          <select id="custPayment" required class="w-full px-4 py-2 rounded-xl border border-gray-700 bg-gray-900 text-white focus:ring-2 focus:ring-red-500">
            <option value="Cash on Delivery">Cash on Delivery</option>
            <option value="Card on Delivery">Card on Delivery</option>
          </select>
        </div>
        <div class="flex gap-3">
          <button type="submit" class="flex-1 px-5 py-3 rounded-2xl bg-red-600 text-white font-semibold hover:bg-red-500">Place Order</button>
          <button type="button" id="whatsappOrder" class="flex-1 px-5 py-3 rounded-2xl border border-green-500 text-green-400 font-semibold hover:bg-green-600/20">WhatsApp</button>
          <button type="button" id="emailOrder" class="flex-1 px-5 py-3 rounded-2xl border border-blue-500 text-blue-400 font-semibold hover:bg-blue-600/20">Email</button>
        </div>
      </form>
      <div id="orderMessage" class="mt-4 text-green-400 font-semibold hidden">✅ Thank you! Your order has been placed.</div>
    </div>
  </section>

  <!-- Contact / Info -->
  <section id="contact" class="bg-black border-t border-red-700">
    <div class="max-w-6xl mx-auto px-4 py-12 grid md:grid-cols-3 gap-8">
      <div>
        <h3 class="text-lg font-semibold text-red-500">Visit Us</h3>
        <p class="text-gray-400 mt-2">10/2 Thalahena, Negombo</p>
        <p class="text-gray-400">Open daily 8:30 AM – 9:00 PM</p>
      </div>
      <div>
        <h3 class="text-lg font-semibold text-red-500">Contact</h3>
        <p class="text-gray-400 mt-2">Phone: 071 903 0125</p>
        <p class="text-gray-400">Email: me</p>
      </div>
    </div>
  </section>

  <footer class="bg-red-700 text-white">
    <div class="max-w-6xl mx-auto px-4 py-8 flex flex-col md:flex-row gap-4 md:items-center md:justify-between">
      <p>© <span id="year"></span> Premium Mart. All rights reserved.</p>
    </div>
  </footer>

  <script>
    const PRODUCTS = [
      { id: 1, name: 'Rathu Kakulu Rice (5kg)', price: 1550, category: 'produce', img: 'https://images.unsplash.com/photo-1606788075761-2c5aebc77e77?q=80&w=800&auto=format&fit=crop' },
      { id: 2, name: 'Onions (1kg)', price: 360, category: 'produce', img: 'https://images.unsplash.com/photo-1508747703725-719777637510?q=80&w=800&auto=format&fit=crop' },
      { id: 3, name: 'Potatoes (1kg)', price: 280, category: 'produce', img: 'https://images.unsplash.com/photo-1592928303228-87ebd98ef68b?q=80&w=800&auto=format&fit=crop' },
      { id: 4, name: 'Fresh Milk (1L)', price: 490, category: 'dairy', img: 'https://images.unsplash.com/photo-1550583724-b2692b85b150?q=80&w=800&auto=format&fit=crop' },
      { id: 5, name: 'Bread Loaf', price: 230, category: 'bakery', img: 'https://images.unsplash.com/photo-1608198093002-ad4e005484ec?q=80&w=800&auto=format&fit=crop' }
    ];

    const productGrid = document.getElementById('productGrid');
    const cartBtn = document.getElementById('cartBtn');
    const cartCount = document.getElementById('cartCount');
    let cart = [];

    function renderProducts() {
      productGrid.innerHTML = '';
      PRODUCTS.forEach(p => {
        const div = document.createElement('div');
        div.className = 'bg-gray-900 rounded-2xl shadow hover:shadow-lg overflow-hidden border border-gray-700';
        div.innerHTML = `
          <img src="${p.img}" alt="${p.name}" class="h-40 w-full object-cover">
          <div class="p-4">
            <h3 class="font-medium">${p.name}</h3>
            <p class="text-sm text-gray-400">Rs. ${p.price}</p>
            <button class="mt-2 px-3 py-2 bg-red-600 text-white rounded-xl text-sm hover:bg-red-500" onclick="addToCart(${p.id})">Add to Cart</button>
          </div>`;
        productGrid.appendChild(div);
      });
    }

    function addToCart(id) {
      const item = PRODUCTS.find(p => p.id === id);
      cart.push(item);
      cartCount.innerText = cart.length;
    }

    function buildOrderMessage() {
      let message = `*Premium Mart Order*%0A`;
      message += `Name: ${document.getElementById('custName').value}%0A`;
      message += `Phone: ${document.getElementById('custPhone').value}%0A`;
      message += `Address: ${document.getElementById('custAddress').value}%0A`;
      message += `Payment: ${document.getElementById('custPayment').value}%0A%0A`;
      message += `*Items:*%0A`;
      cart.forEach((item,i)=>{ message += `${i+1}. ${item.name} - Rs.${item.price}%0A`; });
      return message;
    }

    document.getElementById('checkoutForm').addEventListener('submit', e => {
      e.preventDefault();
      document.getElementById('orderMessage').classList.remove('hidden');
      cart = [];
      cartCount.innerText = 0;
      e.target.reset();
    });

    document.getElementById('whatsappOrder').addEventListener('click', () => {
      const msg = buildOrderMessage();
      window.open(`https://wa.me/94719030125?text=${msg}`, '_blank');
    });

    document.getElementById('emailOrder').addEventListener('click', () => {
      const msg = buildOrderMessage().replace(/%0A/g, '\n');
      window.location.href = `mailto:me?subject=Premium Mart Order&body=${msg}`;
    });

    renderProducts();
    document.getElementById('year').innerText = new Date().getFullYear();
  </script>
</body>
</html>
