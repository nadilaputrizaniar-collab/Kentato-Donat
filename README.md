
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Donat Kentato - Kelompok 9</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts (Quicksand untuk kesan friendly & modern) -->
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Konfigurasi Tailwind Kustom -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Quicksand', 'sans-serif'],
                    },
                    colors: {
                        'kentato-orange': '#FF9F43',
                        'kentato-light': '#FFEAA7',
                        'kentato-pastel': '#FFF0E6',
                        'kentato-pink': '#FFD3E0',
                        'kentato-brown': '#6D4C41'
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Quicksand', sans-serif;
            background-color: #FFF8F0;
        }
        .blob {
            position: absolute;
            filter: blur(40px);
            z-index: -1;
            opacity: 0.5;
        }
        .glass-card {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.5);
        }
        .nav-scrolled {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }
        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="text-gray-800 antialiased relative overflow-x-hidden">

    <!-- Background Elements -->
    <div class="blob bg-orange-300 w-64 h-64 rounded-full top-0 left-0 mix-blend-multiply animate-blob"></div>
    <div class="blob bg-pink-300 w-64 h-64 rounded-full top-0 right-0 mix-blend-multiply animate-blob animation-delay-2000"></div>

    <!-- Navbar -->
    <nav id="navbar" class="fixed w-full z-50 transition-all duration-300 py-4 px-6">
        <div class="max-w-6xl mx-auto flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-kentato-orange flex items-center gap-2">
                <i class="fas fa-donut-small fa-spin-pulse" style="--fa-animation-duration: 3s;"></i>
                Donat Kentato
            </a>
            
            <div class="flex items-center gap-4">
                <a href="#menu" class="hidden md:block font-semibold text-gray-600 hover:text-kentato-orange transition">Menu</a>
                <a href="#about" class="hidden md:block font-semibold text-gray-600 hover:text-kentato-orange transition">Tentang</a>
                <a href="#order" class="hidden md:block font-semibold text-gray-600 hover:text-kentato-orange transition">Pesan</a>
                
                <!-- Cart Icon -->
                <button onclick="scrollToOrder()" class="relative bg-white p-2 rounded-full shadow-md text-kentato-orange hover:bg-kentato-orange hover:text-white transition group">
                    <i class="fas fa-shopping-basket text-xl"></i>
                    <span id="cart-count" class="absolute -top-1 -right-1 bg-red-500 text-white text-xs font-bold w-5 h-5 flex items-center justify-center rounded-full animate-bounce">0</span>
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="pt-32 pb-20 px-6">
        <div class="max-w-6xl mx-auto text-center">
            <span class="inline-block py-1 px-3 rounded-full bg-orange-100 text-orange-600 text-sm font-bold mb-4 border border-orange-200 shadow-sm">
                12 H • Kelompok 9
            </span>
            <h1 class="text-5xl md:text-6xl font-bold text-gray-800 mb-4 leading-tight">
                Empuk, Manis, <br><span class="text-kentato-orange">Bikin Happy!</span>
            </h1>
            <p class="text-lg md:text-xl text-gray-600 mb-2">
                Oleh: <span class="font-semibold text-pink-500">Ghizzelya, Fasya, dan Nadila</span>
            </p>
            <p class="text-gray-500 mb-8 max-w-2xl mx-auto">
                Cemilan hits harga pelajar! Cuma <span class="font-bold text-kentato-orange text-xl">Rp 5.000</span> per buah. Cocok buat nemenin nugas atau nongkrong cantik.
            </p>
            
            <div class="flex flex-col sm:flex-row justify-center gap-4">
                <a href="#menu" class="px-8 py-3 bg-kentato-orange text-white font-bold rounded-full shadow-lg hover:shadow-orange-300/50 hover:scale-105 transition transform flex items-center justify-center gap-2">
                    <i class="fas fa-utensils"></i> Lihat Menu
                </a>
                <a href="#order" class="px-8 py-3 bg-white text-kentato-orange border-2 border-kentato-orange font-bold rounded-full shadow-md hover:bg-orange-50 transition transform flex items-center justify-center gap-2">
                    <i class="fas fa-shopping-cart"></i> Pesan Sekarang
                </a>
            </div>
        </div>
    </header>

    <!-- Why Choose Us -->
    <section id="why" class="py-12 bg-white/50 backdrop-blur-sm">
        <div class="max-w-6xl mx-auto px-6">
            <h2 class="text-3xl font-bold text-center text-gray-800 mb-10">Kenapa Harus <span class="text-kentato-orange">Kentato?</span></h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Reason 1 -->
                <div class="bg-white p-6 rounded-2xl shadow-lg border-b-4 border-kentato-orange text-center hover:-translate-y-2 transition duration-300">
                    <div class="w-16 h-16 bg-orange-100 rounded-full flex items-center justify-center mx-auto mb-4 text-kentato-orange text-2xl">
                        <i class="fas fa-heart"></i>
                    </div>
                    <h3 class="font-bold text-xl mb-2">Cocok Semua Situasi</h3>
                    <p class="text-gray-600 text-sm">Ngemil saat istirahat, bareng teman, atau buat oleh-oleh orang tersayang.</p>
                </div>
                <!-- Reason 2 -->
                <div class="bg-white p-6 rounded-2xl shadow-lg border-b-4 border-pink-400 text-center hover:-translate-y-2 transition duration-300">
                    <div class="w-16 h-16 bg-pink-100 rounded-full flex items-center justify-center mx-auto mb-4 text-pink-500 text-2xl">
                        <i class="fas fa-cloud"></i>
                    </div>
                    <h3 class="font-bold text-xl mb-2">Empuk & Manis Pas</h3>
                    <p class="text-gray-600 text-sm">Tekstur fluffy yang gak bikin eneg. Manisnya pas banget di lidah.</p>
                </div>
                <!-- Reason 3 -->
                <div class="bg-white p-6 rounded-2xl shadow-lg border-b-4 border-kentato-orange text-center hover:-translate-y-2 transition duration-300">
                    <div class="w-16 h-16 bg-orange-100 rounded-full flex items-center justify-center mx-auto mb-4 text-kentato-orange text-2xl">
                        <i class="fas fa-tag"></i>
                    </div>
                    <h3 class="font-bold text-xl mb-2">Ramah di Kantong</h3>
                    <p class="text-gray-600 text-sm">Harga pelajar banget! Cuma goceng (5k) udah bisa bikin mood naik.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="py-16 px-6">
        <div class="max-w-6xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold text-gray-800">Pilihan Varian <span class="text-kentato-orange">Favoritmu</span></h2>
                <p class="text-gray-600 mt-2">Pilih yang paling kamu suka, semuanya cuma Rp 5.000!</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Product 1: Gula Halus -->
                <div class="group bg-white rounded-3xl overflow-hidden shadow-xl hover:shadow-2xl transition duration-300 transform hover:scale-105 border border-gray-100">
                    <div class="h-48 bg-gray-200 overflow-hidden relative">
                        <!-- Placeholder Image -->
                        <img src="https://dekopin.or.id/wp-content/uploads/2024/11/032875800_1604118231-shutterstock_1729999204.webp" alt="Donat Gula Halus" class="w-full h-full object-cover group-hover:rotate-6 transition duration-500">
                        <div class="absolute top-3 right-3 bg-white/90 backdrop-blur px-3 py-1 rounded-full text-xs font-bold text-gray-700 shadow-sm">
                            Best Seller
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="font-bold text-xl text-gray-800 mb-1">Donat Gula Halus</h3>
                        <p class="text-gray-500 text-sm mb-4 h-10">Donat klasik dengan taburan gula halus, lembut dan manisnya pas.</p>
                        <div class="flex items-center justify-between mt-4">
                            <span class="text-xl font-bold text-kentato-orange">Rp 5.000</span>
                            <button onclick="addToCart('Donat Gula Halus', 5000)" class="bg-gray-800 text-white px-4 py-2 rounded-full text-sm font-semibold hover:bg-kentato-orange transition flex items-center gap-2">
                                <i class="fas fa-plus"></i> Tambah
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 2: Coklat -->
                <div class="group bg-white rounded-3xl overflow-hidden shadow-xl hover:shadow-2xl transition duration-300 transform hover:scale-105 border border-gray-100">
                    <div class="h-48 bg-gray-200 overflow-hidden relative">
                        <img src="https://media.istockphoto.com/id/182420116/id/foto/donat-berlapis-cokelat.jpg?s=612x612&w=0&k=20&c=-mcWr0atVmmMPR58gIng7m1T-wHgXIOCgDAvmRvbf-Q=" alt="Donat Coklat" class="w-full h-full object-cover group-hover:rotate-6 transition duration-500">
                    </div>
                    <div class="p-6">
                        <h3 class="font-bold text-xl text-gray-800 mb-1">Donat Topping Coklat</h3>
                        <p class="text-gray-500 text-sm mb-4 h-10">Donat fluffy dengan lelehan coklat premium di atasnya.</p>
                        <div class="flex items-center justify-between mt-4">
                            <span class="text-xl font-bold text-kentato-orange">Rp 5.000</span>
                            <button onclick="addToCart('Donat Topping Coklat', 5000)" class="bg-gray-800 text-white px-4 py-2 rounded-full text-sm font-semibold hover:bg-kentato-orange transition flex items-center gap-2">
                                <i class="fas fa-plus"></i> Tambah
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 3: Strawberry -->
                <div class="group bg-white rounded-3xl overflow-hidden shadow-xl hover:shadow-2xl transition duration-300 transform hover:scale-105 border border-gray-100">
                    <div class="h-48 bg-gray-200 overflow-hidden relative">
                        <img src="https://hypeabis.id/assets/content/20230716061419000000Bomboloni.jpg" alt="Donat Strawberry" class="w-full h-full object-cover group-hover:rotate-6 transition duration-500">
                        <div class="absolute top-3 right-3 bg-pink-100 px-3 py-1 rounded-full text-xs font-bold text-pink-600 shadow-sm">
                            New!
                        </div>
                    </div>
                    <div class="p-6">
                        <h3 class="font-bold text-xl text-gray-800 mb-1">Donat Topping Strawbery</h3>
                        <p class="text-gray-500 text-sm mb-4 h-10">Donat dengan lelehan selai strawberry yang segar dan manis.</p>
                        <div class="flex items-center justify-between mt-4">
                            <span class="text-xl font-bold text-kentato-orange">Rp 5.000</span>
                            <button onclick="addToCart('Donat Topping Strawbery', 5000)" class="bg-gray-800 text-white px-4 py-2 rounded-full text-sm font-semibold hover:bg-kentato-orange transition flex items-center gap-2">
                                <i class="fas fa-plus"></i> Tambah
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Tentang Kami -->
    <section id="about" class="py-12 bg-kentato-pastel">
        <div class="max-w-4xl mx-auto px-6 text-center">
            <h2 class="text-2xl font-bold mb-4 text-kentato-orange">Tentang Kami</h2>
            <p class="text-gray-700 leading-relaxed">
                Kami dari <span class="font-bold">Kelompok 9 (12 H)</span> berkomitmen menghadirkan jajanan berkualitas yang higienis, enak, dan tentunya pas di kantong pelajar. "Donat Kentato" dibuat dengan bahan pilihan dan penuh cinta.
            </p>
        </div>
    </section>

    <!-- Order & Checkout Section -->
    <section id="order" class="py-16 px-6 relative">
        <div class="max-w-5xl mx-auto">
            <div class="bg-white rounded-3xl shadow-2xl overflow-hidden flex flex-col md:flex-row">
                
                <!-- Left: Order Form -->
                <div class="md:w-3/5 p-8 md:p-12">
                    <h2 class="text-3xl font-bold text-gray-800 mb-6 flex items-center gap-2">
                        <i class="fas fa-clipboard-list text-kentato-orange"></i> Formulir Pemesanan
                    </h2>
                    
                    <!-- Cart Summary in Form -->
                    <div id="cart-items-container" class="bg-orange-50 rounded-xl p-4 mb-6 min-h-[100px] border border-orange-100">
                        <p class="text-gray-400 text-center italic text-sm mt-4">Belum ada donat di keranjang. Yuk pilih varian di atas!</p>
                    </div>

                    <div class="flex justify-between items-center mb-6 border-t pt-4">
                        <span class="font-bold text-gray-600">Total Harga:</span>
                        <span id="total-price" class="font-bold text-2xl text-kentato-orange">Rp 0</span>
                    </div>

                    <form id="orderForm" onsubmit="event.preventDefault(); sendToWhatsapp();">
                        <div class="mb-4">
                            <label class="block text-gray-700 text-sm font-bold mb-2">Nama Lengkap</label>
                            <input type="text" id="name" placeholder="Contoh: Ghizzelya" class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:outline-none focus:border-kentato-orange focus:ring-1 focus:ring-kentato-orange bg-gray-50" required>
                        </div>
                        <div class="mb-6">
                            <label class="block text-gray-700 text-sm font-bold mb-2">Kelas</label>
                            <input type="text" id="class" placeholder="Contoh: 12 H" class="w-full px-4 py-3 rounded-xl border border-gray-300 focus:outline-none focus:border-kentato-orange focus:ring-1 focus:ring-kentato-orange bg-gray-50" required>
                        </div>

                        <button type="submit" class="w-full bg-green-500 text-white font-bold py-4 rounded-xl shadow-lg hover:bg-green-600 hover:shadow-green-200/50 transition transform hover:-translate-y-1 flex items-center justify-center gap-2 text-lg">
                            <i class="fab fa-whatsapp text-2xl"></i> Pesan via WhatsApp
                        </button>
                    </form>
                </div>

                <!-- Right: Payment Info -->
                <div class="md:w-2/5 bg-gradient-to-br from-kentato-orange to-orange-400 p-8 md:p-12 text-white flex flex-col justify-center">
                    <h3 class="text-2xl font-bold mb-6 text-center">Pembayaran</h3>
                    
                    <!-- Payment Methods -->
                    <div class="bg-white/20 backdrop-blur-md rounded-xl p-6 mb-4 text-center border border-white/30">
                        <p class="font-bold mb-2 text-sm uppercase tracking-wide">Scan QRIS / DANA</p>
                        
                        <!-- QR Code generated from the DANA link -->
                        <div class="bg-white p-2 rounded-lg inline-block shadow-lg mb-2">
                             <!-- Using QR Server API to generate QR from the DANA deep link -->
                            <img src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=https://link.dana.id/minta?full_url=https://qr.dana.id/v1/281012012025100250261187" alt="QR Code Dana" class="w-32 h-32 md:w-40 md:h-40">
                        </div>
                        <p class="text-xs mt-2 opacity-90 break-words w-full">Scan untuk bayar otomatis</p>
                    </div>

                    <div class="space-y-4">
                         <div class="flex items-center gap-3 bg-white/10 p-3 rounded-lg">
                            <i class="fas fa-wallet text-xl"></i>
                            <div>
                                <p class="text-xs opacity-75">Nomor DANA/OVO</p>
                                <p class="font-mono font-bold">0889-7512-9776</p>
                            </div>
                        </div>
                        
                        <div class="flex items-center gap-3 bg-white/10 p-3 rounded-lg">
                            <i class="fab fa-whatsapp text-xl"></i>
                            <div>
                                <p class="text-xs opacity-75">Admin (Konfirmasi)</p>
                                <p class="font-mono font-bold">0857-7368-8582</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8 px-6 text-center">
        <p class="mb-2 font-bold text-xl text-kentato-orange">Donat Kentato</p>
        <p class="text-sm text-gray-400">Dibuat dengan <i class="fas fa-heart text-red-500"></i> oleh Kelompok 9 (12 H)</p>
        <p class="text-xs text-gray-500 mt-4">&copy; 2024 Donat Kentato. All rights reserved.</p>
    </footer>

    <!-- JavaScript Logic -->
    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', function() {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('nav-scrolled');
            } else {
                navbar.classList.remove('nav-scrolled');
            }
        });

        // Cart Logic
        let cart = [];

        function addToCart(itemName, price) {
            // Check if item exists
            const existingItem = cart.find(item => item.name === itemName);
            if (existingItem) {
                existingItem.qty += 1;
            } else {
                cart.push({ name: itemName, price: price, qty: 1 });
            }
            
            updateCartUI();
            
            // Visual feedback
            const cartBtn = document.querySelector('button[onclick="scrollToOrder()"]');
            cartBtn.classList.add('scale-110', 'bg-kentato-orange', 'text-white');
            setTimeout(() => {
                cartBtn.classList.remove('scale-110');
            }, 200);
        }

        function removeFromCart(index) {
            if (cart[index].qty > 1) {
                cart[index].qty -= 1;
            } else {
                cart.splice(index, 1);
            }
            updateCartUI();
        }

        function updateCartUI() {
            const container = document.getElementById('cart-items-container');
            const totalEl = document.getElementById('total-price');
            const countEl = document.getElementById('cart-count');

            // Update Badge
            const totalQty = cart.reduce((sum, item) => sum + item.qty, 0);
            countEl.innerText = totalQty;
            countEl.classList.remove('hidden');
            if(totalQty === 0) countEl.classList.add('hidden');

            // Update List
            container.innerHTML = '';
            let total = 0;

            if (cart.length === 0) {
                container.innerHTML = '<p class="text-gray-400 text-center italic text-sm mt-4">Belum ada donat di keranjang. Yuk pilih varian di atas!</p>';
            } else {
                cart.forEach((item, index) => {
                    const itemTotal = item.price * item.qty;
                    total += itemTotal;
                    
                    const el = document.createElement('div');
                    el.className = 'flex justify-between items-center mb-2 bg-white p-2 rounded-lg shadow-sm';
                    el.innerHTML = `
                        <div>
                            <p class="font-bold text-sm text-gray-700">${item.name}</p>
                            <p class="text-xs text-gray-500">${item.qty} x Rp ${item.price.toLocaleString('id-ID')}</p>
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="font-bold text-kentato-orange text-sm">Rp ${itemTotal.toLocaleString('id-ID')}</span>
                            <button onclick="removeFromCart(${index})" class="text-red-400 hover:text-red-600 ml-2">
                                <i class="fas fa-minus-circle"></i>
                            </button>
                        </div>
                    `;
                    container.appendChild(el);
                });
            }

            totalEl.innerText = 'Rp ' + total.toLocaleString('id-ID');
        }

        function scrollToOrder() {
            document.getElementById('order').scrollIntoView({ behavior: 'smooth' });
        }

        function sendToWhatsapp() {
            const name = document.getElementById('name').value;
            const className = document.getElementById('class').value;

            if (cart.length === 0) {
                alert("Keranjang masih kosong! Silakan pilih donat terlebih dahulu.");
                return;
            }

            if (!name || !className) {
                alert("Mohon lengkapi Nama dan Kelas.");
                return;
            }

            let orderText = "";
            let totalPrice = 0;

            cart.forEach(item => {
                orderText += `• ${item.name} (${item.qty}x)%0A`;
                totalPrice += (item.price * item.qty);
            });

            // Construct WhatsApp Message
            const phone = "6285773688582"; // 0857-7368-8582 formatted
            const message = `Halo Kak, saya mau pesan Donat Kentato! 🍩%0A%0A` +
                            `*Nama:* ${name}%0A` +
                            `*Kelas:* ${className}%0A%0A` +
                            `*Pesanan:*%0A${orderText}%0A` +
                            `*Total Harga:* Rp ${totalPrice.toLocaleString('id-ID')}%0A%0A` +
                            `Apakah stok masih tersedia? Terima kasih!`;

            window.open(`https://wa.me/${phone}?text=${message}`, '_blank');
        }
    </script>
</body>
</html>
