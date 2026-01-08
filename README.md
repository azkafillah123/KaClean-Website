<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kaclean - Jasa Kebersihan Profesional & Terpercaya</title>
    <meta name="description" content="Kaclean menyediakan layanan asisten rumah tangga dan jasa kebersihan on-demand terbaik di Tasikmalaya. Pesan mudah, rumah bersih!">
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        .gradient-bg { background: linear-gradient(135deg, #0ea5e9 0%, #2563eb 100%); }
    </style>
</head>
<body class="bg-gray-50 font-sans">

    <nav class="bg-white shadow-md sticky top-0 z-50">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-blue-600 tracking-tight">KAClean<span class="text-gray-800">.</span></a>
            <div class="hidden md:flex space-x-8 text-gray-600 font-medium">
                <a href="#layanan" class="hover:text-blue-600">Layanan</a>
                <a href="#cara-kerja" class="hover:text-blue-600">Cara Kerja</a>
                <a href="#testimoni" class="hover:text-blue-600">Testimoni</a>
            </div>
            <button onclick="openModal()" class="bg-blue-600 text-white px-6 py-2 rounded-full font-semibold hover:bg-blue-700 transition">Pesan Sekarang</button>
        </div>
    </nav>

    <section class="gradient-bg text-white py-20 px-6">
        <div class="container mx-auto text-center">
            <h1 class="text-4xl md:text-6xl font-extrabold mb-6">Rumah Bersih Tanpa Ribet,<br>Mulai dari Satu Klik.</h1>
            <p class="text-lg md:text-xl mb-10 opacity-90">Layanan kebersihan on-demand dengan mitra terlatih dan terverifikasi.</p>
            <div class="flex justify-center space-x-4">
                <button onclick="openModal()" class="bg-white text-blue-600 px-8 py-3 rounded-lg font-bold shadow-lg hover:bg-gray-100">Cari Asisten</button>
                <a href="https://wa.me/your-number" class="border-2 border-white px-8 py-3 rounded-lg font-bold hover:bg-white hover:text-blue-600 transition">Konsultasi WA</a>
            </div>
        </div>
    </section>

    <section id="layanan" class="py-20 container mx-auto px-6">
        <h2 class="text-3xl font-bold text-center mb-12">Layanan Kami</h2>
        <div class="grid md:grid-cols-3 gap-8">
            <div class="bg-white p-8 rounded-2xl shadow-sm hover:shadow-xl transition border border-gray-100">
                <div class="text-blue-600 text-4xl mb-4"><i class="fas fa-broom"></i></div>
                <h3 class="text-xl font-bold mb-2">General Cleaning</h3>
                <p class="text-gray-600 mb-4">Pembersihan menyeluruh untuk ruang tamu, kamar tidur, dan dapur.</p>
                <p class="font-bold text-blue-600">Mulai Rp 50.000/jam</p>
            </div>
            <div class="bg-white p-8 rounded-2xl shadow-sm hover:shadow-xl transition border border-gray-100">
                <div class="text-blue-600 text-4xl mb-4"><i class="fas fa-snowflake"></i></div>
                <h3 class="text-xl font-bold mb-2">Cuci AC</h3>
                <p class="text-gray-600 mb-4">Perawatan dan cuci AC agar udara rumah tetap sehat dan dingin.</p>
                <p class="font-bold text-blue-600">Mulai Rp 75.000/unit</p>
            </div>
            <div class="bg-white p-8 rounded-2xl shadow-sm hover:shadow-xl transition border border-gray-100">
                <div class="text-blue-600 text-4xl mb-4"><i class="fas fa-hand-holding-heart"></i></div>
                <h3 class="text-xl font-bold mb-2">Asisten Harian</h3>
                <p class="text-gray-600 mb-4">Bantuan setrika, mencuci, dan merapikan rumah sesuai kebutuhan.</p>
                <p class="font-bold text-blue-600">Custom Price</p>
            </div>
        </div>
    </section>

    <div id="bookingModal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-[60] flex items-center justify-center p-4">
        <div class="bg-white rounded-2xl max-w-lg w-full p-8 relative overflow-y-auto max-h-[90vh]">
            <button onclick="closeModal()" class="absolute top-4 right-4 text-gray-400 hover:text-gray-600"><i class="fas fa-times"></i></button>
            <h2 class="text-2xl font-bold mb-6 text-gray-800">Formulir Pemesanan</h2>
            <form id="orderForm" class="space-y-4">
                <div>
                    <label class="block text-sm font-medium text-gray-700">Nama Lengkap</label>
                    <input type="text" class="w-full mt-1 p-3 border rounded-lg focus:ring-blue-500 focus:border-blue-500" placeholder="Contoh: Budi Santoso" required>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-700">Jenis Layanan</label>
                    <select class="w-full mt-1 p-3 border rounded-lg">
                        <option>General Cleaning</option>
                        <option>Cuci AC</option>
                        <option>Asisten Harian</option>
                    </select>
                </div>
                <div class="grid grid-cols-2 gap-4">
                    <div>
                        <label class="block text-sm font-medium text-gray-700">Tanggal</label>
                        <input type="date" class="w-full mt-1 p-3 border rounded-lg" required>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-gray-700">Jam</label>
                        <input type="time" class="w-full mt-1 p-3 border rounded-lg" required>
                    </div>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-700">Alamat Lengkap</label>
                    <textarea class="w-full mt-1 p-3 border rounded-lg" rows="3" placeholder="Jl. Raya Tasik No. 123..." required></textarea>
                </div>
                <button type="submit" class="w-full bg-blue-600 text-white py-3 rounded-lg font-bold hover:bg-blue-700 transition">Konfirmasi Pesanan</button>
            </form>
        </div>
    </div>

    <footer class="bg-gray-900 text-gray-400 py-12 px-6">
        <div class="container mx-auto text-center">
            <p class="mb-4">&copy; 2026 Kaclean Indonesia. All rights reserved.</p>
            <div class="flex justify-center space-x-6">
                <a href="#" class="hover:text-white">Instagram</a>
                <a href="#" class="hover:text-white">Facebook</a>
                <a href="#" class="hover:text-white">LinkedIn</a>
            </div>
        </div>
    </footer>

    <script>
        function openModal() { document.getElementById('bookingModal').classList.remove('hidden'); }
        function closeModal() { document.getElementById('bookingModal').classList.add('hidden'); }
        
        document.getElementById('orderForm').onsubmit = function(e) {
            e.preventDefault();
            alert('Pesanan Anda sedang diproses! Mitra terdekat akan menghubungi Anda.');
            closeModal();
        }
    </script>
</body>
</html>
