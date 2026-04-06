[index.html](https://github.com/user-attachments/files/26510984/index.html)
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>PMI ADUAN - Pengaduan Pekerja Migran</title>

  <script src="https://cdn.tailwindcss.com"></script>

  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    * { font-family: 'Poppins', sans-serif; }
  </style>
</head>

<body class="bg-gray-100 text-gray-800">

<!-- MENU -->
<button onclick="toggleMenu()"
  class="fixed top-4 left-4 z-50 bg-blue-800 text-white px-4 py-2 rounded shadow">
  ☰ Menu
</button>

<!-- SIDEBAR -->
<div id="sidebar"
  class="w-64 h-screen bg-blue-900 text-white p-5 fixed transform -translate-x-full transition duration-300 z-40">

  <h1 class="text-2xl font-bold mb-6">PMI ADUAN</h1>

  <nav class="flex flex-col space-y-3">
    <a href="#beranda" onclick="toggleMenu()" class="hover:bg-blue-700 p-2 rounded">Beranda</a>
    <a href="#pengaduan" onclick="toggleMenu()" class="hover:bg-blue-700 p-2 rounded">Pengaduan</a>
    <a href="#status" onclick="toggleMenu()" class="hover:bg-blue-700 p-2 rounded">Cek Status</a>
    <a href="#map" onclick="toggleMenu()" class="hover:bg-blue-700 p-2 rounded">Lokasi</a>
    <a href="#kontak" onclick="toggleMenu()" class="hover:bg-blue-700 p-2 rounded">Kontak</a>
  </nav>
</div>

<!-- HERO -->
<section id="beranda" class="bg-blue-800 text-white py-20 text-center">
  <h2 class="text-4xl font-bold mb-4">Layanan Pengaduan Pekerja Migran Indonesia</h2>
  <p class="text-lg">Laporkan masalah Anda secara cepat, aman, dan transparan</p>
</section>

<!-- INFO -->
<section class="max-w-5xl mx-auto px-4 py-10 text-center" data-aos="fade-up">
  <h3 class="text-2xl font-bold mb-4">Tentang Layanan PMI</h3>
  <p>
    Website ini digunakan untuk membantu pekerja migran Indonesia dalam menyampaikan
    pengaduan terkait masalah kerja di luar negeri seperti gaji tidak dibayar,
    kekerasan, atau pelanggaran kontrak.
  </p>
</section>

<!-- FORM PENGADUAN -->
<section id="pengaduan" class="max-w-4xl mx-auto px-4 py-10" data-aos="fade-up">
  <h3 class="text-2xl font-bold mb-6 text-center text-red-600">
    Form Pengaduan PMI
  </h3>

  <form id="formPengaduan" class="bg-white p-6 rounded shadow space-y-4">

    <input type="text" placeholder="Nama Lengkap" class="w-full border p-2 rounded" required>

    <input type="text" placeholder="NIK" class="w-full border p-2 rounded" required>

    <input type="text" placeholder="Negara Penempatan" class="w-full border p-2 rounded" required>

    <input type="text" placeholder="Nama Agen / PPTKIS" class="w-full border p-2 rounded">

    <input type="email" id="email" placeholder="Email (Gmail)" class="w-full border p-2 rounded" required>

    <select class="w-full border p-2 rounded" required>
      <option>Jenis Masalah</option>
      <option>Gaji Tidak Dibayar</option>
      <option>Kekerasan</option>
      <option>Pelanggaran Kontrak</option>
      <option>Overwork / Jam Kerja Berlebih</option>
    </select>

    <textarea rows="4" placeholder="Uraian Pengaduan"
      class="w-full border p-2 rounded" required></textarea>

    <input type="file" id="bukti"
      accept=".pdf,.jpg,.png"
      class="w-full border p-2 rounded" required>

    <button class="bg-red-600 hover:bg-red-700 text-white px-4 py-2 rounded w-full">
      Kirim Pengaduan
    </button>
  </form>
</section>

<!-- CEK STATUS -->
<section id="status" class="max-w-3xl mx-auto px-4 py-10" data-aos="fade-up">
  <h3 class="text-2xl font-bold text-center mb-4">Cek Status Pengaduan</h3>
  <div class="bg-white p-4 rounded shadow">
    <input id="cekTiket" class="w-full border p-2 rounded mb-3"
      placeholder="Masukkan Nomor Tiket">
    <button onclick="cekStatus()"
      class="bg-blue-700 text-white px-4 py-2 rounded w-full">
      Cek Status
    </button>
    <p id="hasilStatus" class="text-center mt-3 font-medium"></p>
  </div>
</section>

<!-- MAP -->
<section id="map" class="bg-gray-200 py-10" data-aos="fade-up">
  <div class="max-w-6xl mx-auto px-4">

    <h3 class="text-2xl font-bold text-center mb-2">
      Lokasi Layanan PMI
    </h3>

    <p class="text-center text-gray-600 mb-6">
      Dinas Tenaga Kerja dan Mobilitas Penduduk Aceh
    </p>

    <div class="bg-white p-4 rounded-xl shadow-lg">
      <iframe 
        src="https://maps.google.com/maps?q=Dinas%20Tenaga%20Kerja%20dan%20Mobilitas%20Penduduk%20Aceh&output=embed"
        width="100%" 
        height="400" 
        style="border:0;" 
        loading="lazy"
        class="rounded-lg">
      </iframe>
    </div>

    <div class="text-center mt-6">
      <a href="https://www.google.com/maps?q=Dinas+Tenaga+Kerja+dan+Mobilitas+Penduduk+Aceh" target="_blank"
        class="bg-blue-700 text-white px-6 py-2 rounded-lg shadow">
        📍 Buka di Google Maps
      </a>
    </div>

  </div>
</section>

<!-- FOOTER -->
<footer id="kontak" class="bg-blue-900 text-white py-6 text-center">
  &copy; <span id="tahun"></span> PMI ADUAN - Sistem Pengaduan Migran
</footer>

<!-- WHATSAPP -->
<a href="https://wa.me/6282273038353?text=Halo%20saya%20ingin%20melaporkan%20masalah%20pekerja%20migran"
 class="fixed bottom-6 right-6 bg-green-500 hover:bg-green-600 text-white px-4 py-3 rounded-full shadow-lg z-50">
  💬 Chat Admin
</a>

<!-- SCRIPT -->
<script>
function toggleMenu() {
  document.getElementById("sidebar")
    .classList.toggle("-translate-x-full");
}

function generateTicket() {
  return "PMI-" + Math.floor(100000 + Math.random() * 900000);
}

document.getElementById("formPengaduan").addEventListener("submit", function(e) {
  e.preventDefault();

  const email = document.getElementById("email").value;
  const file = document.getElementById("bukti").files[0];

  if (!email.endsWith("@gmail.com")) {
    alert("Gunakan email Gmail!");
    return;
  }

  if (file.size > 5000000) {
    alert("File maksimal 5MB!");
    return;
  }

  const tiket = generateTicket();
  alert("Pengaduan berhasil!\nNomor Tiket: " + tiket);

  this.reset();
});

function cekStatus() {
  document.getElementById("hasilStatus").innerText =
    "Status: Laporan sedang diproses oleh petugas.";
}

document.getElementById("tahun").innerText =
  new Date().getFullYear();
</script>

<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
<script>AOS.init();</script>

</body>
</html>
