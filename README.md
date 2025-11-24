
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pop Polish - Layanan Nail Art</title>
    <!-- Memuat Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Memuat Font Nunito (Ramah dan Modern) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800&display=swap" rel="stylesheet">
    
    <style>
        /* Menggunakan font Nunito sebagai default */
        body {
            font-family: 'Nunito', sans-serif;
        }
        /* Kustomisasi scrollbar agar lebih estetik */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #fef2f2; /* rose-50 */
        }
        ::-webkit-scrollbar-thumb {
            background: #f472b6; /* pink-400 */
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #ec4899; /* pink-500 */
        }
    </style>
</head>
<body class="bg-rose-50 text-rose-900">

    <!-- ===== Header dan Navigasi ===== -->
    <header class="bg-white/80 backdrop-blur-sm sticky top-0 z-50 shadow-sm">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <!-- Logo / Brand -->
            <a href="#" class="text-3xl font-extrabold text-pink-500">
                Pop Polish
            </a>
            
            <!-- Navigasi Desktop -->
            <nav class="hidden md:flex space-x-6 items-center">
                <a href="#beranda" class="text-rose-700 hover:text-pink-500 transition duration-300">Beranda</a>
                <a href="#tentang" class="text-rose-700 hover:text-pink-500 transition duration-300">Tentang Kami</a>
                <a href="#layanan" class="text-rose-700 hover:text-pink-500 transition duration-300">Layanan</a>
                <a href="#testimoni" class="text-rose-700 hover:text-pink-500 transition duration-300">Testimoni</a>
                <a href="#pesan" class="bg-pink-500 text-white px-4 py-2 rounded-full font-bold hover:bg-pink-600 transition duration-300 shadow-md">Pesan Sekarang</a>
            </nav>

            <!-- Ikon Keranjang -->
            <button onclick="toggleCartModal()" class="relative p-2 rounded-full hover:bg-rose-100 transition duration-300">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7 text-pink-500" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z" />
                </svg>
                <span id="cart-count" class="absolute top-0 right-0 bg-pink-600 text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center">0</span>
            </button>
        </div>
    </header>

    <main>
        <!-- ===== Bagian Beranda (Hero) ===== -->
        <section id="beranda" class="relative h-[80vh] min-h-[500px] flex items-center justify-center text-center text-white" 
                 style="background-image: url('https://source.unsplash.com/1600x900/?nail-art,manicure'); background-size: cover; background-position: center;">
            <div class="absolute inset-0 bg-black/40"></div> <!-- Overlay gelap -->
            
            <div class="relative z-10 p-4">
                <h1 class="text-5xl md:text-7xl font-extrabold mb-4" style="text-shadow: 2px 2px 8px rgba(0,0,0,0.7);">Pop Polish</h1>
                <p class="text-lg md:text-xl font-semibold bg-black/50 py-1 px-3 rounded-full inline-block">12 H | Kelompok 3</p>
                <p class="text-md md:text-lg mt-2 font-light">Naiya, Pradita, dan Mawar</p>
                
                <p class="text-2xl md:text-3xl font-bold mt-8" style="text-shadow: 1px 1px 4px rgba(0,0,0,0.5);">Nail Art Cantik, Harga Terjangkau</p>
                <p class="text-xl md:text-2xl font-bold text-pink-300">Mulai dari Rp 5.000 - Rp 10.000</p>
                
                <a href="#layanan" class="mt-8 inline-block bg-pink-500 text-white px-8 py-3 rounded-full font-bold text-lg hover:bg-pink-600 transition duration-300 shadow-lg">
                    Lihat Layanan Kami
                </a>
            </div>
        </section>

        <!-- ===== Bagian Tentang Kami ===== -->
        <section id="tentang" class="py-20 container mx-auto px-4">
            <div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-10 items-center">
                <div class="rounded-2xl shadow-xl overflow-hidden">
                    <img src="https://placehold.co/500x500/fecaca/7f1d1d?text=Tim+Pop+Polish" alt="Ilustrasi tim Pop Polish" class="w-full h-full object-cover">
                </div>
                <div class="text-center md:text-left">
                    <h2 class="text-4xl font-extrabold text-pink-500 mb-4">Tentang Kami</h2>
                    <p class="text-lg text-rose-800 mb-3">
                        Selamat datang di Pop Polish! Kami adalah Kelompok 3 (Naiya, Pradita, dan Mawar) dari kelas 12 H yang memiliki passion di dunia kecantikan kuku.
                    </p>
                    <p class="text-rose-700">
                        Misi kami adalah menyediakan layanan nail art yang cantik, berkualitas, dan super terjangkau untuk semua kalangan, terutama teman-teman pelajar. Kami percaya bahwa tampil cantik tidak harus mahal!
                    </p>
                </div>
            </div>
        </section>

        <!-- ===== Bagian Daftar Layanan ===== -->
        <section id="layanan" class="py-20 bg-rose-100">
            <div class="container mx-auto px-4">
                <h2 class="text-4xl font-extrabold text-pink-500 mb-12 text-center">Layanan & Harga</h2>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                    
                    <!-- Contoh Kartu Layanan 1 -->
                    <div class="bg-white rounded-2xl shadow-lg overflow-hidden flex flex-col transition-transform duration-300 hover:-translate-y-2">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRrsJWdqL5ZURoGy1gCYBfT8PmL6bo91JNJHA&s" alt="Nail art satu warna polos" class="w-full h-48 object-cover">
                        <div class="p-6 flex flex-col flex-grow">
                            <h3 class="text-2xl font-bold text-rose-800 mb-2">Nail Art Polos</h3>
                            <p class="text-rose-700 mb-4 flex-grow">Satu warna cantik pilihanmu. Simpel dan elegan.</p>
                            <p class="text-3xl font-extrabold text-pink-500 mb-4">Rp 5.000</p>
                            <button onclick="addToCart('Nail Art Polos', 5000)" class="w-full bg-pink-500 text-white py-2 rounded-full font-bold hover:bg-pink-600 transition duration-300">
                                + Keranjang
                            </button>
                        </div>
                    </div>

                    <!-- Contoh Kartu Layanan 2 -->
                    <div class="bg-white rounded-2xl shadow-lg overflow-hidden flex flex-col transition-transform duration-300 hover:-translate-y-2">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRvmrcCHJKh5Ue6eesqFgF2zzC1hqzBym1RIQ&s" alt="Nail art dengan glitter" class="w-full h-48 object-cover">
                        <div class="p-6 flex flex-col flex-grow">
                            <h3 class="text-2xl font-bold text-rose-800 mb-2">Nail Art Glitter</h3>
                            <p class="text-rose-700 mb-4 flex-grow">Tambahan glitter berkilau untuk tampilan lebih glamor.</p>
                            <p class="text-3xl font-extrabold text-pink-500 mb-4">Rp 7.000</p>
                            <button onclick="addToCart('Nail Art Glitter', 7000)" class="w-full bg-pink-500 text-white py-2 rounded-full font-bold hover:bg-pink-600 transition duration-300">
                                + Keranjang
                            </button>
                        </div>
                    </div>

                    <!-- Contoh Kartu Layanan 3 -->
                    <div class="bg-white rounded-2xl shadow-lg overflow-hidden flex flex-col transition-transform duration-300 hover:-translate-y-2">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQk6RZeqWjayL6m2Zo8kG6VFnx5Ky0QX8Um_w&s" alt="Nail art dengan stiker" class="w-full h-48 object-cover">
                        <div class="p-6 flex flex-col flex-grow">
                            <h3 class="text-2xl font-bold text-rose-800 mb-2">Nail Art Sticker</h3>
                            <p class="text-rose-700 mb-4 flex-grow">Pilihan stiker lucu dan imut untuk kuku yang unik.</p>
                            <p class="text-3xl font-extrabold text-pink-500 mb-4">Rp 8.000</p>
                            <button onclick="addToCart('Nail Art Sticker', 8000)" class="w-full bg-pink-500 text-white py-2 rounded-full font-bold hover:bg-pink-600 transition duration-300">
                                + Keranjang
                            </button>
                        </div>
                    </div>
                    
                    <!-- Contoh Kartu Layanan 4 -->
                    <div class="bg-white rounded-2xl shadow-lg overflow-hidden flex flex-col transition-transform duration-300 hover:-translate-y-2">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRV99PYj4s3cgtwOA5jCw4LJXgjoaFHNY4sgA&s" alt="Nail art custom desain" class="w-full h-48 object-cover">
                        <div class="p-6 flex flex-col flex-grow">
                            <h3 class="text-2xl font-bold text-rose-800 mb-2">Nail Art Custom</h3>
                            <p class="text-rose-700 mb-4 flex-grow">Desain gambar simpel sesuai keinginanmu (karakter, bunga, dll).</p>
                            <p class="text-3xl font-extrabold text-pink-500 mb-4">Rp 10.000</p>
                            <button onclick="addToCart('Nail Art Custom', 10000)" class="w-full bg-pink-500 text-white py-2 rounded-full font-bold hover:bg-pink-600 transition duration-300">
                                + Keranjang
                            </button>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- ===== Bagian Testimoni ===== -->
        <section id="testimoni" class="py-20">
            <div class="container mx-auto px-4">
                <h2 class="text-4xl font-extrabold text-pink-500 mb-12 text-center">Testimoni Pelanggan</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <!-- Testimoni 1 -->
                    <div class="bg-white p-8 rounded-2xl shadow-lg text-center">
                        <p class="text-5xl text-pink-300">✨✨✨✨✨</p>
                        <p class="text-rose-700 italic text-lg my-4">"Hasilnya rapi banget! Harganya juga pas di kantong pelajar. Suka banget pokoknya, auto langganan!"</p>
                        <p class="font-bold text-rose-900">- Amanda, Siswi SMA</p>
                    </div>
                    <!-- Testimoni 2 -->
                    <div class="bg-white p-8 rounded-2xl shadow-lg text-center">
                        <p class="text-5xl text-pink-300">✨✨✨✨✨</p>
                        <p class="text-rose-700 italic text-lg my-4">"Murah meriah tapi gak murahan. Kakaknya ramah-ramah banget lagi. Desainnya lucu-lucu!"</p>
                        <p class="font-bold text-rose-900">- Bintang, Siswi SMP</p>
                    </div>
                    <!-- Testimoni 3 -->
                    <div class="bg-white p-8 rounded-2xl shadow-lg text-center">
                        <p class="text-5xl text-pink-300">✨✨✨✨✨</p>
                        <p class="text-rose-700 italic text-lg my-4">"Aku minta desain custom dan hasilnya bagus! Temen-temenku pada nanyain bikin di mana. Recommended!"</p>
                        <p class="font-bold text-rose-900">- Citra, Mahasiswi</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- ===== Bagian Formulir Pemesanan ===== -->
        <section id="pesan" class="py-20 bg-rose-100">
            <div class="container mx-auto px-4">
                <h2 class="text-4xl font-extrabold text-pink-500 mb-8 text-center">Formulir Pemesanan</h2>
                <div class="max-w-2xl mx-auto bg-white p-8 rounded-2xl shadow-xl">
                    <form id="order-form">
                        <div class="mb-4">
                            <label for="nama" class="block text-lg font-bold text-rose-800 mb-2">Nama Lengkap</label>
                            <input type="text" id="nama" name="nama" class="w-full px-4 py-2 border border-rose-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-pink-400" placeholder="Masukkan namamu..." required>
                        </div>
                        <div class="mb-4">
                            <label for="alamat" class="block text-lg font-bold text-rose-800 mb-2">Alamat Lengkap</label>
                            <textarea id="alamat" name="alamat" rows="3" class="w-full px-4 py-2 border border-rose-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-pink-400" placeholder="Contoh: Jl. Merdeka No. 17, RT 01/RW 05, Kel. Bahagia, Kec. Sentosa" required></textarea>
                        </div>
                        <div class="mb-6">
                            <label for="nomor_hp" class="block text-lg font-bold text-rose-800 mb-2">Nomor HP (WhatsApp)</label>
                            <input type="tel" id="nomor_hp" name="nomor_hp" class="w-full px-4 py-2 border border-rose-200 rounded-lg focus:outline-none focus:ring-2 focus:ring-pink-400" placeholder="Contoh: 081234567890" required>
                        </div>

                        <!-- Info Keranjang sebelum submit -->
                        <div class="bg-rose-50 p-4 rounded-lg mb-6">
                            <h4 class="text-lg font-bold text-rose-800 mb-2">Ringkasan Pesanan Anda:</h4>
                            <div id="form-cart-summary" class="text-rose-700">
                                <p><i>Keranjang Anda masih kosong. Silakan pilih layanan terlebih dahulu.</i></p>
                            </div>
                            <div id="form-cart-total" class="text-xl font-extrabold text-pink-600 mt-2">Total: Rp 0</div>
                        </div>
                        
                        <!-- Pilihan Pembayaran -->
                        <div class="mb-6">
                            <h3 class="text-xl font-bold text-rose-800 mb-3 text-center">Pilihan Pembayaran</h3>
                            <p class="text-center text-rose-700 mb-4">Selesaikan pesanan Anda, lalu lakukan pembayaran melalui salah satu metode di bawah ini.</p>
                            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                                <!-- Tombol Bayar via QRIS (sekarang menampilkan QR Code DANA) -->
                                <button type="button" onclick="toggleQrisModal()" class="flex-1 bg-gray-800 text-white py-3 rounded-lg font-bold text-lg hover:bg-gray-900 transition duration-300">
                                    Bayar via QRIS/DANA
                                </button>
                                <!-- Tombol Bayar via DANA (menampilkan nomor HP DANA) -->
                                <button type="button" onclick="toggleDanaModal()" class="flex-1 bg-blue-500 text-white py-3 rounded-lg font-bold text-lg hover:bg-blue-600 transition duration-300">
                                    Bayar via Transfer DANA
                                </button>
                            </div>
                            <p class="text-center text-rose-600 mt-2 text-sm">Nomor DANA: 088291625569</p>
                        </div>
                        
                        <!-- Tombol Submit -->
                        <button type="submit" class="w-full bg-pink-500 text-white py-3 rounded-full font-extrabold text-xl hover:bg-pink-600 transition duration-300 shadow-lg">
                            Kirim Pesanan via WhatsApp
                        </button>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <!-- ===== Footer ===== -->
    <footer class="bg-rose-200 py-8 text-center">
        <p class="text-rose-800 font-bold">Pop Polish &copy; 2025</p>
        <p class="text-rose-700">Dibuat oleh Kelompok 3 (12 H): Naiya, Pradita, dan Mawar</p>
    </footer>

    <!-- ===== Tombol WhatsApp Mengambang ===== -->
    <a href="https://wa.me/6288297627547?text=Halo%20Pop%20Polish%2C%20saya%20mau%20bertanya%20tentang%20layanan%20nail%20art..." 
       target="_blank" 
       class="fixed bottom-6 right-6 bg-green-500 text-white p-4 rounded-full shadow-lg hover:bg-green-600 transition duration-300 z-50"
       aria-label="Chat di WhatsApp">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="currentColor" viewBox="0 0 16 16">
            <path d="M13.601 2.326A7.854 7.854 0 0 0 7.994 0C3.627 0 .068 3.558.064 7.926c0 1.399.366 2.76 1.057 3.965L0 16l4.204-1.102a7.933 7.933 0 0 0 3.79.965h.004c4.368 0 7.926-3.558 7.93-7.93A7.898 7.898 0 0 0 13.6 2.326zM7.994 14.521a6.573 6.573 0 0 1-3.356-.92l-.24-.144-2.494.654.666-2.433-.156-.251a6.56 6.56 0 0 1-1.007-3.505c0-3.626 2.957-6.584 6.591-6.584a6.56 6.56 0 0 1 4.66 1.931 6.557 6.557 0 0 1 1.928 4.66c-.004 3.639-2.961 6.592-6.592 6.592zm3.615-4.934c-.197-.099-1.17-.578-1.353-.646-.182-.065-.315-.099-.445.099-.133.197-.513.646-.627.775-.114.133-.232.148-.43.05-.197-.1-.836-.308-1.592-.985-.59-.525-.985-1.175-1.103-1.372-.114-.198-.011-.304.088-.403.087-.088.197-.232.296-.346.1-.114.133-.198.198-.33.065-.134.034-.248-.015-.347-.05-.1-.445-1.076-.612-1.47-.16-.389-.323-.335-.445-.34-.114-.007-.247-.007-.38-.007a.729.729 0 0 0-.529.247c-.182.198-.691.677-.691 1.654 0 .977.71 1.916.81 2.049.098.133 1.394 2.132 3.383 2.992.47.205.84.326 1.129.418.475.152.904.129 1.246.08.38-.058 1.171-.48 1.338-.943.164-.464.164-.86.114-.943-.049-.084-.182-.133-.38-.232z"/>
        </svg>
    </a>

    <!-- ===== Modal Keranjang Belanja ===== -->
    <div id="cart-modal" class="fixed inset-0 bg-black/50 z-50 flex items-center justify-center p-4 hidden">
        <div class="bg-white w-full max-w-lg rounded-2xl shadow-xl overflow-hidden">
            <div class="flex justify-between items-center p-6 border-b border-rose-100">
                <h3 class="text-2xl font-extrabold text-pink-500">Keranjang Anda</h3>
                <button onclick="toggleCartModal()" class="text-rose-400 hover:text-rose-600 p-1">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </button>
            </div>
            <div class="p-6 max-h-[60vh] overflow-y-auto">
                <div id="cart-items" class="space-y-4">
                    <p class="text-rose-600">Keranjang Anda kosong.</p>
                </div>
            </div>
            <div class="p-6 bg-rose-50 border-t border-rose-100">
                <div class="flex justify-between items-center mb-4">
                    <span class="text-xl font-bold text-rose-800">Total:</span>
                    <span id="cart-total" class="text-2xl font-extrabold text-pink-600">Rp 0</span>
                </div>
                <a href
