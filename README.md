# webgissmp
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wireframe SPK PPDB Zonasi GIS (EDAS) - SMP Negeri 1 Pantai Labu</title>
    <!-- Tailwind CSS untuk tata letak responsif -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Gaya Wireframe Hitam-Putih Polos (Grayscale, Garis Tepi Hitam Tipis, Tanpa Warna Mencolok) */
        * {
            font-family: 'Inter', sans-serif;
            box-sizing: border-box;
        }
        body {
            background-color: #ffffff;
            color: #111111;
        }
        .wf-box {
            background-color: #ffffff;
            border: 1.5px solid #222222;
            border-radius: 4px;
        }
        .wf-card {
            background-color: #ffffff;
            border: 1px solid #333333;
            border-radius: 4px;
        }
        .wf-header {
            background-color: #f4f4f4;
            border-bottom: 1.5px solid #222222;
        }
        .wf-btn {
            background-color: #ffffff;
            color: #111111;
            border: 1.5px solid #111111;
            border-radius: 4px;
            padding: 6px 14px;
            font-weight: 500;
            cursor: pointer;
            transition: background-color 0.15s;
        }
        .wf-btn:hover {
            background-color: #e5e5e5;
        }
        .wf-btn-dark {
            background-color: #222222;
            color: #ffffff;
            border: 1.5px solid #111111;
            border-radius: 4px;
            padding: 6px 14px;
            font-weight: 500;
            cursor: pointer;
        }
        .wf-btn-dark:hover {
            background-color: #444444;
        }
        .wf-input {
            background-color: #ffffff;
            border: 1px solid #333333;
            border-radius: 4px;
            padding: 6px 10px;
            width: 100%;
            color: #111111;
        }
        .wf-input:focus {
            outline: 2px solid #111111;
        }
        .wf-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.875rem;
        }
        .wf-table th, .wf-table td {
            border: 1px solid #333333;
            padding: 8px 10px;
            text-align: left;
        }
        .wf-table th {
            background-color: #efefef;
            font-weight: 600;
        }
        .nav-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 10px 12px;
            border: 1px solid transparent;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.9rem;
            color: #222222;
        }
        .nav-item:hover {
            background-color: #f2f2f2;
            border-color: #cccccc;
        }
        .nav-item.active {
            background-color: #e6e6e6;
            border: 1.5px solid #111111;
            font-weight: 600;
        }
        /* Mode Cetak Laporan */
        @media print {
            .no-print {
                display: none !important;
            }
            body, #app-shell, #main-content {
                margin: 0 !important;
                padding: 0 !important;
                border: none !important;
                width: 100% !important;
            }
            .wf-box, .wf-card {
                border: 1px solid #000000 !important;
            }
        }
    </style>
</head>
<body class="min-h-screen flex flex-col">

    <!-- ==================== 1. HALAMAN LOGIN ==================== -->
    <div id="page-login" class="min-h-screen flex flex-col justify-between bg-white p-4">
        <!-- Bar Atas Wireframe Browser/Sistem -->
        <div class="wf-box px-4 py-2 flex flex-wrap justify-between items-center text-xs text-neutral-700">
            <span>WIREFRAME ANTARMUKA SISTEM (HALAMAN 1/8 : LOGIN)</span>
            <span>SMP NEGERI 1 PANTAI LABU — KAB. DELI SERDANG</span>
        </div>

        <!-- Kontainer Form Login -->
        <div class="my-auto mx-auto w-full max-w-md wf-box p-6 sm:p-8">
            <div class="flex flex-col items-center text-center mb-6 pb-4 border-b border-neutral-300">
                <!-- Placeholder Logo Sekolah Hitam Putih -->
                <div class="w-16 h-16 wf-box flex items-center justify-center mb-3 bg-neutral-100">
                    <svg class="w-9 h-9 text-neutral-800" fill="none" stroke="currentColor" stroke-width="1.5" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M12 3L2 9l10 6 10-6-10-6zM2 15l10 6 10-6M4 10.5v6.5M20 10.5v6.5" />
                    </svg>
                </div>
                <h1 class="text-lg font-bold tracking-tight uppercase">SMP NEGERI 1 PANTAI LABU</h1>
                <p class="text-xs text-neutral-600 mt-1">Sistem Pendukung Keputusan Penerimaan Siswa Baru<br>Jalur Zonasi Berbasis GIS (Metode EDAS)</p>
            </div>

            <form id="login-form" onsubmit="handleLogin(event)" class="space-y-4">
                <div>
                    <label class="block text-sm font-medium mb-1">Username</label>
                    <input type="text" id="login-username" class="wf-input" placeholder="Masukkan username (contoh: admin)" value="admin" required>
                </div>
                <div>
                    <label class="block text-sm font-medium mb-1">Password</label>
                    <input type="password" id="login-password" class="wf-input" placeholder="Masukkan password" value="123456" required>
                </div>
                <div class="flex items-center justify-between text-xs text-neutral-600">
                    <label class="flex items-center gap-1.5 cursor-pointer">
                        <input type="checkbox" checked class="accent-black"> Ingat sesi saya
                    </label>
                    <span>Hak Akses: Admin / Panitia PPDB</span>
                </div>
                <button type="submit" class="wf-btn-dark w-full py-2.5 text-sm uppercase tracking-wide">
                    MASUK KE SISTEM
                </button>
            </form>

            <!-- Tombol Cepat Wireframe -->
            <div class="mt-5 pt-4 border-t border-dashed border-neutral-400 text-center">
                <p class="text-xs text-neutral-500 mb-2">Navigasi Cepat Pratinjau Wireframe:</p>
                <button type="button" onclick="enterSystem('dashboard')" class="wf-btn w-full text-xs">
                    Langsung Buka Halaman Utama (Dashboard) →
                </button>
            </div>
        </div>

        <div class="text-center text-xs text-neutral-500 py-2">
            Jl. Besar Rantau Panjang, Desa Kelambir, Kec. Pantai Labu — Wireframe Rancangan Antarmuka
        </div>
    </div>

    <!-- ==================== KERANGKA UTAMA (HALAMAN 2 - 8) ==================== -->
    <div id="app-shell" class="hidden min-h-screen flex flex-col">
        <!-- Topbar Header -->
        <header class="wf-header px-4 py-3 flex flex-wrap items-center justify-between gap-2 no-print">
            <div class="flex items-center gap-3">
                <button onclick="toggleSidebar()" class="wf-btn md:hidden px-2.5 py-1 text-sm">☰ Menu</button>
                <div class="w-9 h-9 wf-box flex items-center justify-center bg-white">
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M3 21h18M5 21V7l7-4 7 4v14M9 21v-6h6v6" />
                    </svg>
                </div>
                <div>
                    <div class="font-bold text-sm sm:text-base leading-tight">SPK PPDB ZONASI GIS — SMP NEGERI 1 PANTAI LABU</div>
                    <div class="text-xs text-neutral-600">Metode Evaluation Based on Distance from Average Solution (EDAS)</div>
                </div>
            </div>
            <div class="flex items-center gap-3 text-xs">
                <span class="wf-card px-2.5 py-1 bg-white">Peran: <strong>Admin (Panitia PPDB)</strong></span>
                <button onclick="logoutSystem()" class="wf-btn text-xs">Keluar (Login)</button>
            </div>
        </header>

        <!-- Body Layout: Sidebar + Main Content -->
        <div class="flex-1 flex relative">
            <!-- Sidebar Navigasi -->
            <aside id="sidebar" class="w-64 border-r border-neutral-800 bg-white p-3 flex-shrink-0 hidden md:flex flex-col justify-between no-print">
                <div class="space-y-1">
                    <div class="text-[11px] font-semibold uppercase tracking-wider text-neutral-500 px-2 py-1">Menu Utama Sistem</div>
                    <div onclick="navigateTo('dashboard')" id="nav-dashboard" class="nav-item active">
                        <span>[1]</span> <span>Dashboard</span>
                    </div>
                    <div onclick="navigateTo('siswa')" id="nav-siswa" class="nav-item">
                        <span>[2]</span> <span>Data Calon Siswa</span>
                    </div>
                    <div onclick="navigateTo('kriteria')" id="nav-kriteria" class="nav-item">
                        <span>[3]</span> <span>Data Kriteria & Bobot</span>
                    </div>
                    <div onclick="navigateTo('gis')" id="nav-gis" class="nav-item">
                        <span>[4]</span> <span>Lokasi GIS Zonasi</span>
                    </div>
                    <div onclick="navigateTo('edas')" id="nav-edas" class="nav-item">
                        <span>[5]</span> <span>Perhitungan EDAS</span>
                    </div>
                    <div onclick="navigateTo('hasil')" id="nav-hasil" class="nav-item">
                        <span>[6]</span> <span>Hasil Pemeringkatan</span>
                    </div>
                    <div onclick="navigateTo('laporan')" id="nav-laporan" class="nav-item">
                        <span>[7]</span> <span>Laporan Seleksi</span>
                    </div>
                </div>

                <div class="mt-6 pt-3 border-t border-neutral-300 text-xs text-neutral-600 space-y-2">
                    <div class="wf-card p-2.5 bg-neutral-50">
                        <div class="font-semibold text-neutral-800">Titik Sekolah (Acuan):</div>
                        <div>SMPN 1 Pantai Labu</div>
                        <div class="font-mono text-[11px] mt-0.5">Lat: 3.65987, Lng: 98.81234</div>
                    </div>
                    <button onclick="logoutSystem()" class="wf-btn w-full text-xs">← Kembali ke Halaman Login</button>
                </div>
            </aside>

            <!-- Konten Utama -->
            <main id="main-content" class="flex-1 p-4 sm:p-6 bg-white overflow-x-auto">
                
                <!-- ==================== 2. HALAMAN DASHBOARD ==================== -->
                <section id="sec-dashboard" class="space-y-5">
                    <div class="flex flex-wrap justify-between items-center border-b border-neutral-800 pb-3">
                        <div>
                            <h2 class="text-lg font-bold">Halaman Dashboard</h2>
                            <p class="text-xs text-neutral-600">Ringkasan data pendaftar jalur zonasi, kriteria penilaian, dan hasil pemeringkatan EDAS.</p>
                        </div>
                        <span class="text-xs wf-card px-2 py-1">Wireframe Halaman 2/8</span>
                    </div>

                    <!-- Kartu Ringkasan -->
                    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
                        <div class="wf-box p-4">
                            <div class="text-xs uppercase text-neutral-600">Total Calon Siswa</div>
                            <div id="dash-total-siswa" class="text-2xl font-bold mt-1">5 Siswa</div>
                            <div class="text-xs text-neutral-500 mt-1">Jalur Zonasi / Domisili</div>
                        </div>
                        <div class="wf-box p-4">
                            <div class="text-xs uppercase text-neutral-600">Siswa Memenuhi Syarat</div>
                            <div id="dash-valid-siswa" class="text-2xl font-bold mt-1">5 Siswa</div>
                            <div class="text-xs text-neutral-500 mt-1">KK ≥ 1 Thn & Usia ≤ 15 Thn</div>
                        </div>
                        <div class="wf-box p-4">
                            <div class="text-xs uppercase text-neutral-600">Jumlah Kriteria EDAS</div>
                            <div class="text-2xl font-bold mt-1">4 Kriteria</div>
                            <div class="text-xs text-neutral-500 mt-1">2 Cost & 2 Benefit</div>
                        </div>
                        <div class="wf-box p-4">
                            <div class="text-xs uppercase text-neutral-600">Rata-rata Jarak Sekolah</div>
                            <div id="dash-avg-jarak" class="text-2xl font-bold mt-1">1.18 km</div>
                            <div class="text-xs text-neutral-500 mt-1">Dihitung via Koordinat GIS</div>
                        </div>
                    </div>

                    <!-- Dua Kolom: Ringkasan Kriteria & Pratinjau Peringkat -->
                    <div class="grid grid-cols-1 lg:grid-cols-12 gap-5">
                        <div class="lg:col-span-5 wf-box p-4">
                            <div class="flex justify-between items-center mb-3">
                                <h3 class="font-semibold text-sm">Ringkasan Kriteria & Bobot</h3>
                                <button onclick="navigateTo('kriteria')" class="wf-btn text-xs py-1 px-2">Kelola</button>
                            </div>
                            <table class="wf-table">
                                <thead>
                                    <tr>
                                        <th>Kode</th>
                                        <th>Nama Kriteria</th>
                                        <th>Jenis</th>
                                        <th>Bobot</th>
                                    </tr>
                                </thead>
                                <tbody id="dash-kriteria-body"></tbody>
                            </table>
                        </div>

                        <div class="lg:col-span-7 wf-box p-4">
                            <div class="flex justify-between items-center mb-3">
                                <h3 class="font-semibold text-sm">Pratinjau Urutan Prioritas (Hasil EDAS)</h3>
                                <button onclick="navigateTo('hasil')" class="wf-btn text-xs py-1 px-2">Lihat Semua</button>
                            </div>
                            <div class="overflow-x-auto">
                                <table class="wf-table">
                                    <thead>
                                        <tr>
                                            <th>Peringkat</th>
                                            <th>Nama Calon Siswa</th>
                                            <th>Jarak (C1)</th>
                                            <th>Skor Akhir (AS)</th>
                                            <th>Status</th>
                                        </tr>
                                    </thead>
                                    <tbody id="dash-ranking-body"></tbody>
                                </table>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- ==================== 3. HALAMAN DATA CALON SISWA ==================== -->
                <section id="sec-siswa" class="hidden space-y-5">
                    <div class="flex flex-wrap justify-between items-center border-b border-neutral-800 pb-3">
                        <div>
                            <h2 class="text-lg font-bold">Halaman Data Calon Siswa</h2>
                            <p class="text-xs text-neutral-600">Pengelolaan data pendaftar PPDB jalur zonasi beserta koordinat domisili dan nilai kriteria.</p>
                        </div>
                        <span class="text-xs wf-card px-2 py-1">Wireframe Halaman 3/8</span>
                    </div>

                    <!-- Toolbar Pencarian & Tambah -->
                    <div class="wf-box p-4 flex flex-wrap justify-between items-center gap-3">
                        <div class="flex items-center gap-2 w-full sm:w-auto">
                            <input type="text" id="search-siswa" onkeyup="renderSiswaTable()" class="wf-input sm:w-72 text-sm" placeholder="Cari Nama, NIK, NISN, atau Alamat...">
                        </div>
                        <button onclick="openSiswaModal()" class="wf-btn-dark text-sm">+ Tambah Calon Siswa</button>
                    </div>

                    <!-- Tabel Data Calon Siswa -->
                    <div class="wf-box p-4 overflow-x-auto">
                        <table class="wf-table">
                            <thead>
                                <tr>
                                    <th>No</th>
                                    <th>Nama Calon Siswa</th>
                                    <th>NIK</th>
                                    <th>NISN</th>
                                    <th>Alamat Domisili</th>
                                    <th>Tgl Lahir (Usia)</th>
                                    <th>Koordinat (Lat, Lng)</th>
                                    <th>Jarak (km)</th>
                                    <th>Aksi</th>
                                </tr>
                            </thead>
                            <tbody id="siswa-table-body"></tbody>
                        </table>
                    </div>
                </section>

                <!-- ==================== 4. HALAMAN DATA KRITERIA DAN BOBOT ==================== -->
                <section id="sec-kriteria" class="hidden space-y-5">
                    <div class="flex flex-wrap justify-between items-center border-b border-neutral-800 pb-3">
                        <div>
                            <h2 class="text-lg font-bold">Halaman Data Kriteria dan Bobot</h2>
                            <p class="text-xs text-neutral-600">Pengaturan kriteria seleksi jalur zonasi (Permendikdasmen No. 3 Tahun 2025) dan bobot perhitungan EDAS.</p>
                        </div>
                        <span class="text-xs wf-card px-2 py-1">Wireframe Halaman 4/8</span>
                    </div>

                    <div class="wf-box p-4 space-y-4">
                        <div class="flex flex-wrap justify-between items-center gap-2">
                            <div class="text-sm font-medium">Daftar Kriteria Penilaian (Total Bobot Harus = 1.00 / 100%)</div>
                            <div id="total-bobot-badge" class="wf-card px-3 py-1 text-xs font-semibold">Total Bobot: 1.00 (100%)</div>
                        </div>

                        <div class="overflow-x-auto">
                            <table class="wf-table">
                                <thead>
                                    <tr>
                                        <th>Kode</th>
                                        <th>Nama Kriteria</th>
                                        <th>Jenis Kriteria</th>
                                        <th>Keterangan Aturan</th>
                                        <th class="w-36">Nilai Bobot (wj)</th>
                                    </tr>
                                </thead>
                                <tbody id="kriteria-table-body"></tbody>
                            </table>
                        </div>

                        <div class="flex flex-wrap justify-between items-center pt-2 gap-2">
                            <span id="kriteria-msg" class="text-xs text-neutral-700">Ubah nilai bobot pada kolom input lalu klik Simpan untuk memperbarui perhitungan EDAS.</span>
                            <div class="flex gap-2">
                                <button onclick="resetKriteriaDefault()" class="wf-btn text-xs">Reset Default</button>
                                <button onclick="saveKriteriaBobot()" class="wf-btn-dark text-xs">Simpan Perubahan Bobot</button>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- ==================== 5. HALAMAN LOKASI GIS ==================== -->
                <section id="sec-gis" class="hidden space-y-5">
                    <div class="flex flex-wrap justify-between items-center border-b border-neutral-800 pb-3">
                        <div>
                            <h2 class="text-lg font-bold">Halaman Lokasi GIS (Pemetaan Zonasi)</h2>
                            <p class="text-xs text-neutral-600">Visualisasi skematis titik lokasi SMP Negeri 1 Pantai Labu, radius zona, dan persebaran domisili calon siswa.</p>
                        </div>
                        <span class="text-xs wf-card px-2 py-1">Wireframe Halaman 5/8</span>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-12 gap-5">
                        <!-- Area Peta Skematis Hitam Putih -->
                        <div class="lg:col-span-8 wf-box p-4 flex flex-col">
                            <div class="flex flex-wrap justify-between items-center gap-2 mb-3 text-xs">
                                <span class="font-semibold">PETA DIGITAL ZONASI — KECAMATAN PANTAI LABU</span>
                                <div class="flex items-center gap-3">
                                    <span>[■] SMPN 1 Pantai Labu</span>
                                    <span>[●] Titik Rumah Siswa</span>
                                    <span>(---) Radius Zona</span>
                                </div>
                            </div>

                            <!-- Kanvas SVG Peta Skematis Hitam-Putih -->
                            <div class="border border-neutral-800 bg-neutral-50 relative overflow-hidden">
                                <svg id="gis-map-svg" viewBox="0 0 640 420" class="w-full h-auto block">
                                    <!-- Grid Koordinat Skematis -->
                                    <g stroke="#e0e0e0" stroke-width="1">
                                        <line x1="0" y1="70" x2="640" y2="70" />
                                        <line x1="0" y1="140" x2="640" y2="140" />
                                        <line x1="0" y1="210" x2="640" y2="210" />
                                        <line x1="0" y1="280" x2="640" y2="280" />
                                        <line x1="0" y1="350" x2="640" y2="350" />
                                        <line x1="128" y1="0" x2="128" y2="420" />
                                        <line x1="256" y1="0" x2="256" y2="420" />
                                        <line x1="384" y1="0" x2="384" y2="420" />
                                        <line x1="512" y1="0" x2="512" y2="420" />
                                    </g>

                                    <!-- Garis Jalan & Sungai Skematis Pantai Labu -->
                                    <path d="M 0,60 Q 180,85 320,55 T 640,75" fill="none" stroke="#bdbdbd" stroke-width="6" />
                                    <text x="20" y="48" font-size="10" fill="#666666">Garis Pesisir / Sungai Pantai Labu</text>

                                    <path d="M 40,260 L 320,210 L 600,190" fill="none" stroke="#999999" stroke-width="3" />
                                    <path d="M 320,60 L 320,210 L 290,410" fill="none" stroke="#999999" stroke-width="2.5" />
                                    <text x="390" y="183" font-size="10" fill="#555555">Jl. Besar Rantau Panjang</text>

                                    <!-- Lingkaran Radius Zona 3 km & 1 km -->
                                    <circle cx="320" cy="210" r="175" fill="none" stroke="#444444" stroke-width="1.2" stroke-dasharray="6,4" />
                                    <text x="320" y="398" text-anchor="middle" font-size="11" fill="#333333">Batas Zona Kedua (Radius 3.0 km)</text>

                                    <circle cx="320" cy="210" r="95" fill="none" stroke="#111111" stroke-width="1.5" stroke-dasharray="4,3" />
                                    <text x="320" y="317" text-anchor="middle" font-size="11" font-weight="600" fill="#111111">Zona Utama (Radius 1.0 km)</text>

                                    <!-- Garis Penghubung Jarak Aktif -->
                                    <line id="gis-active-line" x1="320" y1="210" x2="320" y2="210" stroke="#111111" stroke-width="1.5" stroke-dasharray="2,2" />

                                    <!-- Marker Siswa Dinamis -->
                                    <g id="gis-student-markers"></g>

                                    <!-- Marker Pusat: SMP Negeri 1 Pantai Labu -->
                                    <g transform="translate(320, 210)">
                                        <rect x="-12" y="-12" width="24" height="24" fill="#111111" stroke="#ffffff" stroke-width="2" rx="3" />
                                        <text x="0" y="4" text-anchor="middle" fill="#ffffff" font-size="11" font-weight="bold">S</text>
                                        <rect x="-68" y="-34" width="136" height="18" fill="#ffffff" stroke="#111111" stroke-width="1" rx="2" />
                                        <text x="0" y="-22" text-anchor="middle" fill="#111111" font-size="10" font-weight="bold">SMPN 1 Pantai Labu</text>
                                    </g>
                                </svg>
                            </div>
                        </div>

                        <!-- Panel Detail Lokasi & Simulasi Hitung Jarak -->
                        <div class="lg:col-span-4 wf-box p-4 flex flex-col justify-between space-y-4">
                            <div class="space-y-3">
                                <h3 class="font-semibold text-sm border-b border-neutral-300 pb-2">Detail Koordinat & Hitung Jarak</h3>
                                <div>
                                    <label class="block text-xs font-medium mb-1">Pilih Calon Siswa</label>
                                    <select id="gis-select-siswa" onchange="selectSiswaOnMap(this.value)" class="wf-input text-sm"></select>
                                </div>
                                <div>
                                    <label class="block text-xs font-medium mb-1">Alamat Domisili</label>
                                    <input type="text" id="gis-alamat" class="wf-input text-xs bg-neutral-50" readonly>
                                </div>
                                <div class="grid grid-cols-2 gap-2">
                                    <div>
                                        <label class="block text-xs font-medium mb-1">Latitude</label>
                                        <input type="number" step="0.00001" id="gis-lat" class="wf-input text-xs font-mono">
                                    </div>
                                    <div>
                                        <label class="block text-xs font-medium mb-1">Longitude</label>
                                        <input type="number" step="0.00001" id="gis-lng" class="wf-input text-xs font-mono">
                                    </div>
                                </div>
                                <div class="wf-card p-3 bg-neutral-50">
                                    <div class="text-xs text-neutral-600">Jarak ke SMPN 1 Pantai Labu (Haversine):</div>
                                    <div id="gis-jarak-output" class="text-xl font-bold mt-0.5">0.45 km</div>
                                </div>
                                <button onclick="recalculateGisDistance()" class="wf-btn-dark w-full text-xs">Hitung Ulang & Update Jarak</button>
                            </div>

                            <div class="border-t border-neutral-300 pt-3">
                                <div class="text-xs font-semibold mb-2">Daftar Jarak Terdekat:</div>
                                <ul id="gis-nearest-list" class="text-xs space-y-1.5"></ul>
                            </div>
                        </div>
                    </div>
                </section>

                <!-- ==================== 6. HALAMAN PERHITUNGAN EDAS ==================== -->
                <section id="sec-edas" class="hidden space-y-5">
                    <div class="flex flex-wrap justify-between items-center border-b border-neutral-800 pb-3">
                        <div>
                            <h2 class="text-lg font-bold">Halaman Perhitungan Metode EDAS</h2>
                            <p class="text-xs text-neutral-600">Tahapan matematis Evaluation Based on Distance from Average Solution (X → AV → PDA/NDA → SP/SN → NSP/NSN → AS).</p>
                        </div>
                        <span class="text-xs wf-card px-2 py-1">Wireframe Halaman 6/8</span>
                    </div>

                    <!-- Langkah 1 & 2: Matriks Keputusan (X) dan Solusi Rata-Rata (AV) -->
                    <div class="wf-box p-4 space-y-3">
                        <h3 class="font-semibold text-sm">1. Matriks Keputusan (X) & Solusi Rata-Rata (AV)</h3>
                        <div class="overflow-x-auto">
                            <table class="wf-table" id="edas-table-matrix"></table>
                        </div>
                    </div>

                    <!-- Langkah 3: Matriks PDA dan NDA -->
                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-4">
                        <div class="wf-box p-4 space-y-2">
                            <h3 class="font-semibold text-sm">2a. Positive Distance from Average (PDA)</h3>
                            <div class="overflow-x-auto">
                                <table class="wf-table" id="edas-table-pda"></table>
                            </div>
                        </div>
                        <div class="wf-box p-4 space-y-2">
                            <h3 class="font-semibold text-sm">2b. Negative Distance from Average (NDA)</h3>
                            <div class="overflow-x-auto">
                                <table class="wf-table" id="edas-table-nda"></table>
                            </div>
                        </div>
                    </div>

                    <!-- Langkah 4, 5, 6: SP, SN, NSP, NSN, dan Skor Penilaian Akhir (AS) -->
                    <div class="wf-box p-4 space-y-3">
                        <h3 class="font-semibold text-sm">3. Jumlah Terbobot (SP/SN), Normalisasi (NSP/NSN), dan Skor Akhir (AS)</h3>
                        <div class="overflow-x-auto">
                            <table class="wf-table" id="edas-table-final"></table>
                        </div>
                    </div>
                </section>

                <!-- ==================== 7. HALAMAN HASIL PEMERINGKATAN ==================== -->
                <section id="sec-hasil" class="hidden space-y-5">
                    <div class="flex flex-wrap justify-between items-center border-b border-neutral-800 pb-3">
                        <div>
                            <h2 class="text-lg font-bold">Halaman Hasil Pemeringkatan Prioritas</h2>
                            <p class="text-xs text-neutral-600">Urutan prioritas calon siswa baru jalur zonasi berdasarkan nilai Appraisal Score (AS) tertinggi ke terendah.</p>
                        </div>
                        <span class="text-xs wf-card px-2 py-1">Wireframe Halaman 7/8</span>
                    </div>

                    <div class="wf-box p-4 flex flex-wrap justify-between items-center gap-3">
                        <div class="flex items-center gap-2 text-xs">
                            <label class="font-semibold">Simulasi Kuota Daya Tampung:</label>
                            <input type="number" id="kuota-input" value="3" min="1" max="20" onchange="renderAllViews()" class="wf-input w-20 text-center font-bold">
                            <span>Siswa Prioritas Utama</span>
                        </div>
                        <button onclick="navigateTo('laporan')" class="wf-btn-dark text-xs">Buka Pratinjau Laporan →</button>
                    </div>

                    <div class="wf-box p-4 overflow-x-auto">
                        <table class="wf-table">
                            <thead>
                                <tr>
                                    <th>Peringkat</th>
                                    <th>NISN</th>
                                    <th>Nama Calon Siswa</th>
                                    <th>Jarak (C1)</th>
                                    <th>Usia (C2)</th>
                                    <th>Urutan Daftar (C3)</th>
                                    <th>Lama KK (C4)</th>
                                    <th>Nilai AS</th>
                                    <th>Keterangan Prioritas</th>
                                </tr>
                            </thead>
                            <tbody id="hasil-table-body"></tbody>
                        </table>
                    </div>
                </section>

                <!-- ==================== 8. HALAMAN LAPORAN ==================== -->
                <section id="sec-laporan" class="hidden space-y-5">
                    <div class="flex flex-wrap justify-between items-center border-b border-neutral-800 pb-3 no-print">
                        <div>
                            <h2 class="text-lg font-bold">Halaman Laporan Hasil Seleksi</h2>
                            <p class="text-xs text-neutral-600">Format dokumen laporan resmi hasil pemeringkatan PPDB jalur zonasi siap cetak.</p>
                        </div>
                        <div class="flex items-center gap-2">
                            <span class="text-xs wf-card px-2 py-1">Wireframe Halaman 8/8</span>
                            <button onclick="window.print()" class="wf-btn-dark text-xs">Cetak / Simpan PDF</button>
                        </div>
                    </div>

                    <!-- Lembar Dokumen Laporan Hitam Putih -->
                    <div class="wf-box p-6 sm:p-8 max-w-4xl mx-auto bg-white space-y-6">
                        <!-- Kop Surat Sekolah -->
                        <div class="border-b-2 border-neutral-900 pb-4 text-center space-y-1">
                            <div class="text-xs uppercase tracking-wider">Pemerintah Kabupaten Deli Serdang — Dinas Pendidikan</div>
                            <div class="text-lg font-bold uppercase">SMP NEGERI 1 PANTAI LABU</div>
                            <div class="text-xs text-neutral-700">Jl. Besar Rantau Panjang, Desa Kelambir, Kecamatan Pantai Labu, Kab. Deli Serdang</div>
                        </div>

                        <div class="text-center space-y-1">
                            <h3 class="font-bold text-sm uppercase underline">LAPORAN HASIL PENENTUAN PRIORITAS PENERIMAAN SISWA BARU JALUR ZONASI</h3>
                            <p class="text-xs text-neutral-600">Berdasarkan Perhitungan Metode Evaluation Based on Distance from Average Solution (EDAS) & GIS</p>
                        </div>

                        <!-- Tabel Laporan -->
                        <div class="overflow-x-auto">
                            <table class="wf-table">
                                <thead>
                                    <tr>
                                        <th>Peringkat</th>
                                        <th>NIK</th>
                                        <th>NISN</th>
                                        <th>Nama Calon Siswa</th>
                                        <th>Alamat</th>
                                        <th>Jarak (km)</th>
                                        <th>Skor EDAS (AS)</th>
                                        <th>Status Rekomendasi</th>
                                    </tr>
                                </thead>
                                <tbody id="laporan-table-body"></tbody>
                            </table>
                        </div>

                        <!-- Tanda Tangan -->
                        <div class="grid grid-cols-2 gap-8 pt-6 text-xs">
                            <div>
                                <div>Mengetahui,</div>
                                <div class="font-semibold">Kepala SMP Negeri 1 Pantai Labu</div>
                                <div class="h-16"></div>
                                <div class="font-semibold underline">( ................................................ )</div>
                                <div>NIP. ........................................</div>
                            </div>
                            <div class="text-right">
                                <div>Pantai Labu, November 2026</div>
                                <div class="font-semibold">Ketua Panitia PPDB Jalur Zonasi</div>
                                <div class="h-16"></div>
                                <div class="font-semibold underline">( ................................................ )</div>
                                <div>NIP. ........................................</div>
                            </div>
                        </div>
                    </div>
                </section>

            </main>
        </div>
    </div>

    <!-- ==================== MODAL TAMBAH / EDIT CALON SISWA ==================== -->
    <div id="siswa-modal" class="hidden fixed inset-0 bg-black/40 flex items-center justify-center p-4 z-50 no-print">
        <div class="wf-box bg-white w-full max-w-lg p-5 space-y-4">
            <div class="flex justify-between items-center border-b border-neutral-300 pb-2">
                <h3 id="modal-siswa-title" class="font-bold text-sm">Tambah Data Calon Siswa</h3>
                <button onclick="closeSiswaModal()" class="text-sm font-bold px-2">✕</button>
            </div>
            <form id="siswa-form" onsubmit="saveSiswaForm(event)" class="space-y-3 text-xs">
                <input type="hidden" id="form-siswa-id">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                    <div>
                        <label class="block font-medium mb-1">Nama Lengkap</label>
                        <input type="text" id="form-nama" class="wf-input" required>
                    </div>
                    <div>
                        <label class="block font-medium mb-1">Tanggal Lahir</label>
                        <input type="date" id="form-tgl-lahir" class="wf-input" value="2012-05-14" required>
                    </div>
                    <div>
                        <label class="block font-medium mb-1">NIK (16 Digit)</label>
                        <input type="text" id="form-nik" class="wf-input" required>
                    </div>
                    <div>
                        <label class="block font-medium mb-1">NISN</label>
                        <input type="text" id="form-nisn" class="wf-input" required>
                    </div>
                </div>
                <div>
                    <label class="block font-medium mb-1">Alamat Domisili</label>
                    <input type="text" id="form-alamat" class="wf-input" required>
                </div>
                <div class="grid grid-cols-2 sm:grid-cols-4 gap-2">
                    <div>
                        <label class="block font-medium mb-1">Latitude</label>
                        <input type="number" step="0.00001" id="form-lat" class="wf-input font-mono" value="3.66210" required>
                    </div>
                    <div>
                        <label class="block font-medium mb-1">Longitude</label>
                        <input type="number" step="0.00001" id="form-lng" class="wf-input font-mono" value="98.81420" required>
                    </div>
                    <div>
                        <label class="block font-medium mb-1">Urutan Daftar (C3)</label>
                        <input type="number" min="1" id="form-waktu" class="wf-input" value="6" required>
                    </div>
                    <div>
                        <label class="block font-medium mb-1">Lama KK/Thn (C4)</label>
                        <input type="number" step="0.5" min="1" id="form-domisili" class="wf-input" value="3" required>
                    </div>
                </div>
                <div class="flex justify-end gap-2 pt-3 border-t border-neutral-300">
                    <button type="button" onclick="closeSiswaModal()" class="wf-btn">Batal</button>
                    <button type="submit" class="wf-btn-dark">Simpan Data</button>
                </div>
            </form>
        </div>
    </div>

    <!-- ==================== LOGIKA JAVASCRIPT (GIS + EDAS + CRUD) ==================== -->
    <script>
        // Koordinat Acuan SMP Negeri 1 Pantai Labu (Desa Kelambir, Pantai Labu)
        const SCHOOL_COORDS = {
            name: "SMP Negeri 1 Pantai Labu",
            lat: 3.65987,
            lng: 98.81234
        };

        // Data Kriteria sesuai Tabel 3.3 Proposal
        let criteriaList = [
            { code: 'C1', name: 'Jarak ke sekolah', type: 'cost', weight: 0.40, desc: 'Dihitung via GIS (km). Semakin dekat semakin diprioritaskan.' },
            { code: 'C2', name: 'Usia', type: 'benefit', weight: 0.25, desc: 'Usia calon siswa (tahun), maksimal 15 tahun.' },
            { code: 'C3', name: 'Waktu pendaftaran', type: 'cost', weight: 0.15, desc: 'Urutan hari/waktu mendaftar. Semakin awal semakin diprioritaskan.' },
            { code: 'C4', name: 'Lama Domisili', type: 'benefit', weight: 0.20, desc: 'Masa terbit Kartu Keluarga (tahun), minimal 1 tahun.' }
        ];

        // Data Sampel Calon Siswa (Alternatif)
        let students = [
            { id: 1, nama: 'Ahmad Fauzi', nik: '1207281405120001', nisn: '0124589011', alamat: 'Jl. Besar Rantau Panjang, Desa Kelambir', tglLahir: '2012-05-14', usia: 14.1, lat: 3.66250, lng: 98.81410, waktuDaftar: 1, lamaDomisili: 5.0 },
            { id: 2, nama: 'Siti Rahmah', nik: '1207285208110002', nisn: '0118923402', alamat: 'Dusun II Desa Pantai Labu Pekan', tglLahir: '2011-08-12', usia: 14.8, lat: 3.66620, lng: 98.81890, waktuDaftar: 2, lamaDomisili: 6.5 },
            { id: 3, nama: 'M. Rizky Pratama', nik: '1207280311120003', nisn: '0127734103', alamat: 'Desa Rugemuk, Kec. Pantai Labu', tglLahir: '2012-11-03', usia: 13.6, lat: 3.65120, lng: 98.80350, waktuDaftar: 3, lamaDomisili: 4.0 },
            { id: 4, nama: 'Nurul Aini', nik: '1207286102120004', nisn: '0123349804', alamat: 'Desa Paluh Sibaji, Pantai Labu', tglLahir: '2012-02-21', usia: 14.3, lat: 3.67150, lng: 98.82110, waktuDaftar: 4, lamaDomisili: 7.0 },
            { id: 5, nama: 'Dedi Kurniawan', nik: '1207281909120005', nisn: '0129912005', alamat: 'Desa Denai Lama, Pantai Labu', tglLahir: '2012-09-19', usia: 13.8, lat: 3.65510, lng: 98.80980, waktuDaftar: 5, lamaDomisili: 3.5 }
        ];

        let selectedGisStudentId = 1;

        // Rumus Haversine untuk menghitung jarak geografis (km) dari rumah ke SMPN 1 Pantai Labu
        function calculateDistanceKm(lat1, lon1, lat2 = SCHOOL_COORDS.lat, lon2 = SCHOOL_COORDS.lng) {
            const R = 6371; // Radius bumi dalam km
            const dLat = (lat2 - lat1) * Math.PI / 180;
            const dLon = (lon2 - lon1) * Math.PI / 180;
            const a = Math.sin(dLat / 2) * Math.sin(dLat / 2) +
                      Math.cos(lat1 * Math.PI / 180) * Math.cos(lat2 * Math.PI / 180) *
                      Math.sin(dLon / 2) * Math.sin(dLon / 2);
            const c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1 - a));
            return Number((R * c).toFixed(2));
        }

        // Hitung usia dari tanggal lahir
        function calculateAge(dobString) {
            const dob = new Date(dobString);
            const refDate = new Date('2026-07-01');
            const diffYears = (refDate - dob) / (1000 * 60 * 60 * 24 * 365.25);
            return Number(diffYears.toFixed(1));
        }

        // ==================== PERHITUNGAN METODE EDAS (SESUAI RUMUS BAB II) ====================
        function computeEDAS() {
            const m = students.length;
            if (m === 0) return { rows: [], av: {} };

            // 1. Matriks Keputusan X
            const matrix = students.map(s => {
                const jarak = calculateDistanceKm(s.lat, s.lng);
                return {
                    ...s,
                    C1: jarak,
                    C2: s.usia,
                    C3: s.waktuDaftar,
                    C4: s.lamaDomisili
                };
            });

            // 2. Solusi Rata-Rata (AVj = sum(xij) / m)
            const av = {};
            criteriaList.forEach(c => {
                const sum = matrix.reduce((acc, row) => acc + row[c.code], 0);
                av[c.code] = sum / m;
            });

            // 3. Jarak Positif (PDA) & Jarak Negatif (NDA) dari Rata-Rata
            // Benefit: PDA = max(0, (xij - AVj)/AVj), NDA = max(0, (AVj - xij)/AVj)
            // Cost:    PDA = max(0, (AVj - xij)/AVj), NDA = max(0, (xij - AVj)/AVj)
            const stepData = matrix.map(row => {
                const pda = {};
                const nda = {};
                let sp = 0;
                let sn = 0;

                criteriaList.forEach(c => {
                    const val = row[c.code];
                    const avg = av[c.code] || 1;
                    if (c.type === 'benefit') {
                        pda[c.code] = Math.max(0, (val - avg) / avg);
                        nda[c.code] = Math.max(0, (avg - val) / avg);
                    } else {
                        pda[c.code] = Math.max(0, (avg - val) / avg);
                        nda[c.code] = Math.max(0, (val - avg) / avg);
                    }
                    // 4. Jumlah Terbobot SPi dan SNi
                    sp += c.weight * pda[c.code];
                    sn += c.weight * nda[c.code];
                });

                return { ...row, pda, nda, sp, sn };
            });

            // 5. Normalisasi Nilai (NSPi dan NSNi)
            const maxSP = Math.max(...stepData.map(d => d.sp));
            const maxSN = Math.max(...stepData.map(d => d.sn));

            const finalRows = stepData.map(d => {
                const nsp = maxSP === 0 ? 1 : (d.sp / maxSP);
                const nsn = maxSN === 0 ? 1 : (1 - (d.sn / maxSN));
                // 6. Skor Penilaian Akhir ASi = 1/2 * (NSPi + NSNi)
                const as = 0.5 * (nsp + nsn);
                return { ...d, nsp, nsn, as };
            });

            // 7. Pemeringkatan (urut AS tertinggi ke terendah)
            const sorted = [...finalRows].sort((a, b) => b.as - a.as);
            sorted.forEach((item, idx) => {
                item.rank = idx + 1;
            });

            // Kembalikan urutan asli beserta peringkatnya
            const rowsWithRank = finalRows.map(item => {
                const found = sorted.find(s => s.id === item.id);
                return { ...item, rank: found.rank };
            });

            return { rows: rowsWithRank, sorted, av };
        }

        // ==================== NAVIGASI HALAMAN ====================
        function handleLogin(e) {
            e.preventDefault();
            enterSystem('dashboard');
        }

        function enterSystem(page = 'dashboard') {
            document.getElementById('page-login').classList.add('hidden');
            document.getElementById('app-shell').classList.remove('hidden');
            navigateTo(page);
            renderAllViews();
        }

        function logoutSystem() {
            document.getElementById('app-shell').classList.add('hidden');
            document.getElementById('page-login').classList.remove('hidden');
        }

        function toggleSidebar() {
            const sb = document.getElementById('sidebar');
            sb.classList.toggle('hidden');
        }

        function navigateTo(pageId) {
            const sections = ['dashboard', 'siswa', 'kriteria', 'gis', 'edas', 'hasil', 'laporan'];
            sections.forEach(sec => {
                document.getElementById(`sec-${sec}`).classList.add('hidden');
                const navEl = document.getElementById(`nav-${sec}`);
                if (navEl) navEl.classList.remove('active');
            });

            document.getElementById(`sec-${pageId}`).classList.remove('hidden');
            const activeNav = document.getElementById(`nav-${pageId}`);
            if (activeNav) activeNav.classList.add('active');

            // Tutup sidebar mobile otomatis setelah klik
            if (window.innerWidth < 768) {
                document.getElementById('sidebar').classList.add('hidden');
            }
            renderAllViews();
        }

        // ==================== RENDER SEMUA HALAMAN ====================
        function renderAllViews() {
            const edasResult = computeEDAS();
            const kuota = parseInt(document.getElementById('kuota-input')?.value || 3, 10);

            // 1. Update Dashboard
            document.getElementById('dash-total-siswa').textContent = `${students.length} Siswa`;
            document.getElementById('dash-valid-siswa').textContent = `${students.length} Siswa`;
            document.getElementById('dash-avg-jarak').textContent = `${(edasResult.av.C1 || 0).toFixed(2)} km`;

            document.getElementById('dash-kriteria-body').innerHTML = criteriaList.map(c => `
                <tr>
                    <td class="font-semibold">${c.code}</td>
                    <td>${c.name}</td>
                    <td class="uppercase text-xs">${c.type}</td>
                    <td>${c.weight.toFixed(2)}</td>
                </tr>
            `).join('');

            document.getElementById('dash-ranking-body').innerHTML = edasResult.sorted.map(s => `
                <tr>
                    <td class="font-bold">#${s.rank}</td>
                    <td>${s.nama}</td>
                    <td>${s.C1.toFixed(2)} km</td>
                    <td class="font-mono font-semibold">${s.as.toFixed(4)}</td>
                    <td><span class="wf-card px-2 py-0.5 text-xs">${s.rank <= kuota ? 'Prioritas' : 'Cadangan'}</span></td>
                </tr>
            `).join('');

            // 2. Render Tabel Data Calon Siswa
            renderSiswaTable();

            // 3. Render Tabel Kriteria & Bobot
            renderKriteriaTable();

            // 4. Render GIS Map & Dropdown
            renderGisView(edasResult.rows);

            // 5. Render Perhitungan EDAS
            renderEdasTables(edasResult);

            // 6. Render Hasil Pemeringkatan & Laporan
            renderHasilAndLaporan(edasResult.sorted, kuota);
        }

        function renderSiswaTable() {
            const keyword = (document.getElementById('search-siswa')?.value || '').toLowerCase();
            const filtered = students.filter(s =>
                s.nama.toLowerCase().includes(keyword) ||
                s.nik.includes(keyword) ||
                s.nisn.includes(keyword) ||
                s.alamat.toLowerCase().includes(keyword)
            );

            document.getElementById('siswa-table-body').innerHTML = filtered.map((s, idx) => {
                const jarak = calculateDistanceKm(s.lat, s.lng);
                return `
                    <tr>
                        <td>${idx + 1}</td>
                        <td class="font-medium">${s.nama}</td>
                        <td class="font-mono text-xs">${s.nik}</td>
                        <td class="font-mono text-xs">${s.nisn}</td>
                        <td>${s.alamat}</td>
                        <td>${s.tglLahir} (${s.usia} thn)</td>
                        <td class="font-mono text-xs">${s.lat.toFixed(5)}, ${s.lng.toFixed(5)}</td>
                        <td class="font-semibold">${jarak.toFixed(2)} km</td>
                        <td class="whitespace-nowrap space-x-1">
                            <button onclick="openSiswaModal(${s.id})" class="wf-btn text-xs py-1 px-2">Edit</button>
                            <button onclick="deleteSiswa(${s.id})" class="wf-btn text-xs py-1 px-2">Hapus</button>
                        </td>
                    </tr>
                `;
            }).join('');
        }

        function renderKriteriaTable() {
            const totalW = criteriaList.reduce((acc, c) => acc + Number(c.weight), 0);
            document.getElementById('total-bobot-badge').textContent = `Total Bobot: ${totalW.toFixed(2)} (${Math.round(totalW * 100)}%)`;

            document.getElementById('kriteria-table-body').innerHTML = criteriaList.map((c, i) => `
                <tr>
                    <td class="font-bold">${c.code}</td>
                    <td class="font-medium">${c.name}</td>
                    <td><span class="wf-card px-2 py-0.5 text-xs uppercase">${c.type}</span></td>
                    <td class="text-xs text-neutral-600">${c.desc}</td>
                    <td>
                        <input type="number" step="0.05" min="0" max="1" id="input-weight-${i}" value="${c.weight}" class="wf-input text-xs font-mono">
                    </td>
                </tr>
            `).join('');
        }

        function saveKriteriaBobot() {
            let sum = 0;
            const newWeights = criteriaList.map((_, i) => {
                const val = parseFloat(document.getElementById(`input-weight-${i}`).value) || 0;
                sum += val;
                return val;
            });

            if (Math.abs(sum - 1.0) > 0.001) {
                document.getElementById('kriteria-msg').textContent = `Peringatan: Total bobot saat ini ${sum.toFixed(2)}. Pastikan jumlah total bobot sama dengan 1.00.`;
                return;
            }

            criteriaList.forEach((c, i) => c.weight = newWeights[i]);
            document.getElementById('kriteria-msg').textContent = 'Bobot kriteria berhasil disimpan dan perhitungan EDAS telah diperbarui.';
            renderAllViews();
        }

        function resetKriteriaDefault() {
            const defaults = [0.40, 0.25, 0.15, 0.20];
            criteriaList.forEach((c, i) => c.weight = defaults[i]);
            renderAllViews();
        }

        // ==================== LOGIKA GIS SKEMATIS ====================
        function renderGisView(rows) {
            const selectEl = document.getElementById('gis-select-siswa');
            selectEl.innerHTML = rows.map(s => `<option value="${s.id}" ${s.id === selectedGisStudentId ? 'selected' : ''}>${s.nama} (${s.C1.toFixed(2)} km)</option>`).join('');

            const markersGroup = document.getElementById('gis-student-markers');
            markersGroup.innerHTML = '';

            rows.forEach((s, idx) => {
                // Konversi delta lat/lng ke koordinat piksel SVG di sekitar pusat (320, 210)
                const dx = (s.lng - SCHOOL_COORDS.lng) * 9500;
                const dy = -(s.lat - SCHOOL_COORDS.lat) * 9500;
                const cx = Math.max(30, Math.min(610, 320 + dx));
                const cy = Math.max(30, Math.min(390, 210 + dy));
                const isSelected = s.id === selectedGisStudentId;

                if (isSelected) {
                    const line = document.getElementById('gis-active-line');
                    line.setAttribute('x2', cx);
                    line.setAttribute('y2', cy);
                }

                const g = document.createElementNS('http://www.w3.org/2000/svg', 'g');
                g.setAttribute('transform', `translate(${cx}, ${cy})`);
                g.style.cursor = 'pointer';
                g.onclick = () => selectSiswaOnMap(s.id);

                g.innerHTML = `
                    <circle r="${isSelected ? 8 : 5}" fill="${isSelected ? '#111111' : '#ffffff'}" stroke="#111111" stroke-width="2" />
                    <text x="10" y="4" font-size="10" font-weight="${isSelected ? 'bold' : 'normal'}" fill="#111111">${idx + 1}. ${s.nama.split(' ')[0]}</text>
                `;
                markersGroup.appendChild(g);
            });

            // Isi detail siswa terpilih
            const activeStudent = rows.find(s => s.id === selectedGisStudentId) || rows[0];
            if (activeStudent) {
                selectedGisStudentId = activeStudent.id;
                document.getElementById('gis-alamat').value = activeStudent.alamat;
                document.getElementById('gis-lat').value = activeStudent.lat;
                document.getElementById('gis-lng').value = activeStudent.lng;
                document.getElementById('gis-jarak-output').textContent = `${activeStudent.C1.toFixed(2)} km`;
            }

            // Daftar terdekat
            const sortedByDist = [...rows].sort((a, b) => a.C1 - b.C1);
            document.getElementById('gis-nearest-list').innerHTML = sortedByDist.map((s, i) => `
                <li class="flex justify-between border-b border-neutral-200 pb-1">
                    <span>${i + 1}. ${s.nama}</span>
                    <span class="font-mono font-semibold">${s.C1.toFixed(2)} km</span>
                </li>
            `).join('');
        }

        function selectSiswaOnMap(id) {
            selectedGisStudentId = Number(id);
            renderAllViews();
        }

        function recalculateGisDistance() {
            const lat = parseFloat(document.getElementById('gis-lat').value);
            const lng = parseFloat(document.getElementById('gis-lng').value);
            const idx = students.findIndex(s => s.id === selectedGisStudentId);
            if (idx !== -1 && !isNaN(lat) && !isNaN(lng)) {
                students[idx].lat = lat;
                students[idx].lng = lng;
                renderAllViews();
            }
        }

        // ==================== RENDER TABEL PERHITUNGAN EDAS ====================
        function renderEdasTables({ rows, av }) {
            // 1. Matriks X & AV
            document.getElementById('edas-table-matrix').innerHTML = `
                <thead>
                    <tr>
                        <th>Alternatif (Calon Siswa)</th>
                        <th>C1: Jarak (Cost)</th>
                        <th>C2: Usia (Benefit)</th>
                        <th>C3: Daftar (Cost)</th>
                        <th>C4: Domisili (Benefit)</th>
                    </tr>
                </thead>
                <tbody>
                    ${rows.map(r => `
                        <tr>
                            <td class="font-medium">${r.nama}</td>
                            <td class="font-mono">${r.C1.toFixed(2)}</td>
                            <td class="font-mono">${r.C2.toFixed(1)}</td>
                            <td class="font-mono">${r.C3}</td>
                            <td class="font-mono">${r.C4.toFixed(1)}</td>
                        </tr>
                    `).join('')}
                    <tr class="bg-neutral-100 font-semibold">
                        <td>Solusi Rata-Rata (AVj)</td>
                        <td class="font-mono">${(av.C1 || 0).toFixed(4)}</td>
                        <td class="font-mono">${(av.C2 || 0).toFixed(4)}</td>
                        <td class="font-mono">${(av.C3 || 0).toFixed(4)}</td>
                        <td class="font-mono">${(av.C4 || 0).toFixed(4)}</td>
                    </tr>
                </tbody>
            `;

            // 2a. Matriks PDA
            document.getElementById('edas-table-pda').innerHTML = `
                <thead>
                    <tr>
                        <th>Alternatif</th>
                        <th>C1</th>
                        <th>C2</th>
                        <th>C3</th>
                        <th>C4</th>
                    </tr>
                </thead>
                <tbody>
                    ${rows.map(r => `
                        <tr>
                            <td>${r.nama}</td>
                            <td class="font-mono">${r.pda.C1.toFixed(4)}</td>
                            <td class="font-mono">${r.pda.C2.toFixed(4)}</td>
                            <td class="font-mono">${r.pda.C3.toFixed(4)}</td>
                            <td class="font-mono">${r.pda.C4.toFixed(4)}</td>
                        </tr>
                    `).join('')}
                </tbody>
            `;

            // 2b. Matriks NDA
            document.getElementById('edas-table-nda').innerHTML = `
                <thead>
                    <tr>
                        <th>Alternatif</th>
                        <th>C1</th>
                        <th>C2</th>
                        <th>C3</th>
                        <th>C4</th>
                    </tr>
                </thead>
                <tbody>
                    ${rows.map(r => `
                        <tr>
                            <td>${r.nama}</td>
                            <td class="font-mono">${r.nda.C1.toFixed(4)}</td>
                            <td class="font-mono">${r.nda.C2.toFixed(4)}</td>
                            <td class="font-mono">${r.nda.C3.toFixed(4)}</td>
                            <td class="font-mono">${r.nda.C4.toFixed(4)}</td>
                        </tr>
                    `).join('')}
                </tbody>
            `;

            // 3. SP, SN, NSP, NSN, AS
            document.getElementById('edas-table-final').innerHTML = `
                <thead>
                    <tr>
                        <th>Alternatif</th>
                        <th>SPi</th>
                        <th>SNi</th>
                        <th>NSPi</th>
                        <th>NSNi</th>
                        <th>Skor Penilaian (ASi)</th>
                        <th>Peringkat</th>
                    </tr>
                </thead>
                <tbody>
                    ${rows.map(r => `
                        <tr>
                            <td class="font-medium">${r.nama}</td>
                            <td class="font-mono">${r.sp.toFixed(4)}</td>
                            <td class="font-mono">${r.sn.toFixed(4)}</td>
                            <td class="font-mono">${r.nsp.toFixed(4)}</td>
                            <td class="font-mono">${r.nsn.toFixed(4)}</td>
                            <td class="font-mono font-bold">${r.as.toFixed(4)}</td>
                            <td class="font-bold">#${r.rank}</td>
                        </tr>
                    `).join('')}
                </tbody>
            `;
        }

        function renderHasilAndLaporan(sortedRows, kuota) {
            document.getElementById('hasil-table-body').innerHTML = sortedRows.map(s => `
                <tr>
                    <td class="font-bold">#${s.rank}</td>
                    <td class="font-mono text-xs">${s.nisn}</td>
                    <td class="font-medium">${s.nama}</td>
                    <td>${s.C1.toFixed(2)} km</td>
                    <td>${s.C2.toFixed(1)} thn</td>
                    <td>Ke-${s.C3}</td>
                    <td>${s.C4.toFixed(1)} thn</td>
                    <td class="font-mono font-bold">${s.as.toFixed(4)}</td>
                    <td>
                        <span class="wf-card px-2 py-0.5 text-xs ${s.rank <= kuota ? 'bg-neutral-900 text-white font-semibold' : ''}">
                            ${s.rank <= kuota ? 'DIREKOMENDASIKAN DITERIMA' : 'CADANGAN'}
                        </span>
                    </td>
                </tr>
            `).join('');

            document.getElementById('laporan-table-body').innerHTML = sortedRows.map(s => `
                <tr>
                    <td class="font-bold text-center">${s.rank}</td>
                    <td class="font-mono text-xs">${s.nik}</td>
                    <td class="font-mono text-xs">${s.nisn}</td>
                    <td>${s.nama}</td>
                    <td>${s.alamat}</td>
                    <td>${s.C1.toFixed(2)} km</td>
                    <td class="font-mono font-semibold">${s.as.toFixed(4)}</td>
                    <td class="font-semibold">${s.rank <= kuota ? 'Prioritas Utama' : 'Cadangan'}</td>
                </tr>
            `).join('');
        }

        // ==================== CRUD MODAL CALON SISWA ====================
        function openSiswaModal(id = null) {
            const modal = document.getElementById('siswa-modal');
            modal.classList.remove('hidden');

            if (id) {
                const s = students.find(item => item.id === id);
                document.getElementById('modal-siswa-title').textContent = 'Edit Data Calon Siswa';
                document.getElementById('form-siswa-id').value = s.id;
                document.getElementById('form-nama').value = s.nama;
                document.getElementById('form-tgl-lahir').value = s.tglLahir;
                document.getElementById('form-nik').value = s.nik;
                document.getElementById('form-nisn').value = s.nisn;
                document.getElementById('form-alamat').value = s.alamat;
                document.getElementById('form-lat').value = s.lat;
                document.getElementById('form-lng').value = s.lng;
                document.getElementById('form-waktu').value = s.waktuDaftar;
                document.getElementById('form-domisili').value = s.lamaDomisili;
            } else {
                document.getElementById('modal-siswa-title').textContent = 'Tambah Data Calon Siswa';
                document.getElementById('siswa-form').reset();
                document.getElementById('form-siswa-id').value = '';
                document.getElementById('form-lat').value = '3.66210';
                document.getElementById('form-lng').value = '98.81420';
                document.getElementById('form-waktu').value = students.length + 1;
                document.getElementById('form-domisili').value = '3';
            }
        }

        function closeSiswaModal() {
            document.getElementById('siswa-modal').classList.add('hidden');
        }

        function saveSiswaForm(e) {
            e.preventDefault();
            const idVal = document.getElementById('form-siswa-id').value;
            const tglLahir = document.getElementById('form-tgl-lahir').value;
            const payload = {
                nama: document.getElementById('form-nama').value.trim(),
                tglLahir,
                usia: calculateAge(tglLahir),
                nik: document.getElementById('form-nik').value.trim(),
                nisn: document.getElementById('form-nisn').value.trim(),
                alamat: document.getElementById('form-alamat').value.trim(),
                lat: parseFloat(document.getElementById('form-lat').value),
                lng: parseFloat(document.getElementById('form-lng').value),
                waktuDaftar: parseInt(document.getElementById('form-waktu').value, 10),
                lamaDomisili: parseFloat(document.getElementById('form-domisili').value)
            };

            if (idVal) {
                const idx = students.findIndex(s => s.id === Number(idVal));
                if (idx !== -1) students[idx] = { ...students[idx], ...payload };
            } else {
                const newId = students.length ? Math.max(...students.map(s => s.id)) + 1 : 1;
                students.push({ id: newId, ...payload });
            }

            closeSiswaModal();
            renderAllViews();
        }

        function deleteSiswa(id) {
            students = students.filter(s => s.id !== id);
            renderAllViews();
        }

        // Inisialisasi awal
        window.onload = function() {
            renderAllViews();
        };
    </script>
</body>
</html>
