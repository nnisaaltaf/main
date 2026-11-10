# main <!DOCTYPE html>
<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portofolio - Altafunisa Aflikha Ratnawati</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
 9   <link rel="stylesheethref="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Font: Outfit -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        spiderRed: '#E62429',
                        spiderRedGlow: '#FF2E34',
                        spiderBlue: '#0055FF',
                        spiderBlueGlow: '#00D4FF',
                        spiderDark: '#0B0F19',
                        spiderCard: '#131B2E',
                    },
                    fontFamily: {
                        outfit: ['Outfit', 'sans-serif'],
                    },
                    boxShadow: {
                        'neon-red': '0 0 20px rgba(230, 36, 41, 0.6), 0 0 40px rgba(230, 36, 41, 0.2)',
                        'neon-blue': '0 0 20px rgba(0, 85, 255, 0.6), 0 0 40px rgba(0, 85, 255, 0.2)',
                        'neon-combo': '-5px 0 20px rgba(230, 36, 41, 0.5), 5px 0 20px rgba(0, 85, 255, 0.5)',
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Outfit', sans-serif;
            background-color: #060911;
            color: #E2E8F0;
            overflow-x: hidden;
        }

        /* Web Pattern Background */
        .spider-web-bg {
            background-image: 
                radial-gradient(circle at 20% 20%, rgba(230, 36, 41, 0.15) 0%, transparent 40%),
                radial-gradient(circle at 80% 80%, rgba(0, 85, 255, 0.15) 0%, transparent 40%),
                radial-gradient(circle at 50% 50%, rgba(15, 23, 42, 0.8) 0%, #060911 100%),
                repeating-radial-gradient(circle at 50% 50%, transparent 0, transparent 40px, rgba(255, 255, 255, 0.02) 41px, transparent 42px);
        }

        /* Spider Line Grid Overlay */
        .spider-grid {
            background-size: 50px 50px;
            background-image:
                linear-gradient(to right, rgba(255, 255, 255, 0.02) 1px, transparent 1px),
                linear-gradient(to bottom, rgba(255, 255, 255, 0.02) 1px, transparent 1px);
        }

        /* Pulsing Glow Animation */
        @keyframes pulse-glow {
            0%, 100% {
                box-shadow: 0 0 15px rgba(230, 36, 41, 0.5), 0 0 30px rgba(0, 85, 255, 0.3);
            }
            50% {
                box-shadow: 0 0 25px rgba(0, 85, 255, 0.6), 0 0 45px rgba(230, 36, 41, 0.4);
            }
        }

        .animate-spider-glow {
            animation: pulse-glow 4s infinite ease-in-out;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            background: #060911;
        }
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(to bottom, #E62429, #0055FF);
            border-radius: 5px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(to bottom, #FF2E34, #00D4FF);
        }
    </style>
</head>
<body class="spider-web-bg spider-grid min-h-screen selection:bg-spiderRed selection:text-white">

    <!-- NAVBAR -->
    <nav class="fixed top-0 left-0 w-full z-50 bg-opacity-80 backdrop-blur-md bg-[#060911] border-b border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Logo -->
                <div class="flex items-center space-x-3 cursor-pointer" onclick="window.scrollTo({top:0, behavior:'smooth'})">
                    <div class="w-10 h-10 rounded-full bg-gradient-to-tr from-spiderRed to-spiderBlue p-[2px] flex items-center justify-center animate-spider-glow">
                        <div class="w-full h-full bg-spiderDark rounded-full flex items-center justify-center">
                            <i class="fa-solid fa-spider text-spiderRed text-xl"></i>
                        </div>
                    </div>
                    <span class="font-extrabold text-xl tracking-wider text-white">ALTAFUNISA<span class="text-spiderRed">.</span></span>
                </div>

                <!-- Desktop Menu -->
                <div class="hidden md:block">
                    <div class="flex items-baseline space-x-6">
                        <a href="#hero" class="px-3 py-2 rounded-md text-sm font-medium hover:text-spiderRed transition-colors">Beranda</a>
                        <a href="#about" class="px-3 py-2 rounded-md text-sm font-medium hover:text-spiderBlueGlow transition-colors">Tentang Saya</a>
                        <a href="#skills" class="px-3 py-2 rounded-md text-sm font-medium hover:text-spiderRed transition-colors">Keahlian</a>
                        <a href="#projects" class="px-3 py-2 rounded-md text-sm font-medium hover:text-spiderBlueGlow transition-colors">Project</a>
                        <a href="#contact" class="px-4 py-2 rounded-full text-sm font-semibold bg-gradient-to-r from-spiderRed to-spiderBlue text-white hover:opacity-90 shadow-neon-red transition-all transform hover:-translate-y-0.5">Kontak</a>
                    </div>
                </div>

                <!-- Mobile Menu Button -->
                <div class="md:hidden">
                    <button id="mobile-menu-btn" class="text-gray-300 hover:text-white focus:outline-none p-2">
                        <i class="fa-solid fa-bars text-2xl" id="menu-icon"></i>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden bg-[#0B0F19] border-b border-slate-800 px-4 pt-2 pb-4 space-y-2">
            <a href="#hero" class="mobile-link block px-3 py-2 rounded-md text-base font-medium hover:bg-slate-800">Beranda</a>
            <a href="#about" class="mobile-link block px-3 py-2 rounded-md text-base font-medium hover:bg-slate-800">Tentang Saya</a>
            <a href="#skills" class="mobile-link block px-3 py-2 rounded-md text-base font-medium hover:bg-slate-800">Keahlian</a>
            <a href="#projects" class="mobile-link block px-3 py-2 rounded-md text-base font-medium hover:bg-slate-800">Project</a>
            <a href="#contact" class="mobile-link block px-3 py-2 rounded-md text-base font-medium bg-gradient-to-r from-spiderRed to-spiderBlue text-center font-bold">Kontak</a>
        </div>
    </nav>

    <!-- 1. HERO SECTION -->
    <section id="hero" class="min-h-screen pt-28 pb-16 flex items-center justify-center relative overflow-hidden">
        <!-- Ambient Glow Backdrops -->
        <div class="absolute top-1/4 left-10 w-72 h-72 bg-spiderRed rounded-full filter blur-[120px] opacity-20 pointer-events-none"></div>
        <div class="absolute bottom-10 right-10 w-80 h-80 bg-spiderBlue rounded-full filter blur-[140px] opacity-25 pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full z-10">
            <div class="flex flex-col md:flex-row items-center justify-between gap-12">
                
                <!-- Hero Text -->
                <div class="flex-1 text-center md:text-left space-y-6">
                    <div class="inline-flex items-center space-x-2 px-3 py-1.5 rounded-full border border-spiderRed/30 bg-spiderRed/10 text-spiderRed text-sm font-semibold">
                        <i class="fa-solid fa-bolt animate-pulse"></i>
                        <span>Selamat Datang di Portofolio Saya</span>
                    </div>

                    <h1 class="text-4xl sm:text-6xl font-extrabold tracking-tight text-white leading-tight">
                        Halo, Saya <br/>
                        <span class="text-transparent bg-clip-text bg-gradient-to-r from-spiderRed via-red-400 to-spiderBlueGlow">
                            Altafunisa Aflikha R.
                        </span>
                    </h1>

                    <p class="text-lg text-slate-300 max-w-xl leading-relaxed">
                        Halo selamat datang di website portofolio saya, website ini dibuat untuk menaruh seluruh project yang saya buat, <span class="text-spiderBlueGlow font-semibold">enjoy!</span>
                    </p>

                    <div class="flex flex-wrap justify-center md:justify-start gap-4 pt-4">
                        <a href="#projects" class="px-7 py-3.5 rounded-xl font-bold bg-spiderRed hover:bg-red-600 text-white shadow-neon-red transition-all duration-300 transform hover:-translate-y-1 flex items-center space-x-2">
                            <span>Lihat Project</span>
                            <i class="fa-solid fa-arrow-right"></i>
                        </a>
                        <a href="#contact" class="px-7 py-3.5 rounded-xl font-bold border-2 border-spiderBlue text-white hover:bg-spiderBlue/20 shadow-neon-blue transition-all duration-300 transform hover:-translate-y-1 flex items-center space-x-2">
                            <i class="fa-solid fa-paper-plane"></i>
                            <span>Hubungi Saya</span>
                        </a>
                    </div>
                </div>

                <!-- Hero Photo with Spider-Man Theme Frame -->
                <div class="flex-1 flex justify-center relative">
                    <!-- Rotating Decorative Spider Web Rings -->
                    <div class="relative w-72 h-72 sm:w-80 sm:h-80 lg:w-96 lg:h-96">
                        <div class="absolute inset-0 rounded-full border-2 border-dashed border-spiderRed opacity-40 animate-[spin_20s_linear_infinite]"></div>
                        <div class="absolute -inset-4 rounded-full border-2 border-dashed border-spiderBlue opacity-30 animate-[spin_35s_linear_infinite_reverse]"></div>

                        <!-- Main Image Container -->
                        <div class="w-full h-full rounded-3xl bg-gradient-to-tr from-spiderRed via-spiderDark to-spiderBlue p-1.5 shadow-neon-combo transition-transform duration-500 hover:scale-105">
                            <div class="w-full h-full bg-spiderDark rounded-[22px] overflow-hidden relative group">
                                <img src="https://placehold.co/600x600/0b0f19/e62429?text=Altafunisa+Aflikha" 
                                     alt="Altafunisa Aflikha Ratnawati" 
                                     class="w-full h-full object-cover object-center group-hover:scale-110 transition-transform duration-500"
                                     onerror="this.onerror=null; this.src='https://placehold.co/600x600/131b2e/00d4ff?text=Foto+Altafunisa';">
                                
                                <!-- Spider Badge Overlay -->
                                <div class="absolute bottom-4 right-4 bg-spiderDark/90 border border-spiderBlue/50 backdrop-blur-md px-3 py-1.5 rounded-lg flex items-center space-x-2">
                                    <i class="fa-solid fa-graduation-cap text-spiderBlueGlow"></i>
                                    <span class="text-xs font-semibold text-slate-200">SMK Cyber Media</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 2. ABOUT SECTION -->
    <section id="about" class="py-24 relative bg-slate-950/60 border-t border-b border-slate-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center space-y-4 mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-spiderBlueGlow">Perkenalan Diri</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Tentang <span class="text-spiderRed">Saya</span></h3>
                <div class="w-24 h-1 bg-gradient-to-r from-spiderRed to-spiderBlue mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 items-center">
                <!-- Spidey Card Visual -->
                <div class="lg:col-span-5 flex justify-center">
                    <div class="w-full max-w-md bg-spiderCard border border-slate-800 rounded-2xl p-6 relative overflow-hidden shadow-2xl hover:border-spiderRed/50 transition-all duration-300">
                        <div class="absolute -right-10 -bottom-10 w-40 h-40 bg-spiderRed/10 rounded-full filter blur-2xl"></div>
                        <i class="fa-solid fa-spider absolute top-4 right-4 text-6xl text-slate-800/40"></i>
                        
                        <div class="space-y-4 relative z-10">
                            <div class="w-14 h-14 rounded-xl bg-spiderRed/20 border border-spiderRed/40 flex items-center justify-center text-spiderRed text-2xl">
                                <i class="fa-solid fa-user-graduate"></i>
                            </div>
                            <h4 class="text-xl font-bold text-white">Siswa Aktif</h4>
                            <p class="text-sm text-slate-300 leading-relaxed">
                                Memiliki semangat belajar yang tinggi dalam bidang Manajemen Perkantoran dan Layanan Bisnis. Siap beradaptasi dengan dunia kerja digital dan profesional.
                            </p>
                            <div class="pt-2 border-t border-slate-800 flex justify-between text-xs text-slate-400">
                                <span>Institusi: SMK Cyber Media</span>
                                <span>Jurusan: MPLB</span>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Detail Text -->
                <div class="lg:col-span-7 space-y-6">
                    <h4 class="text-2xl font-bold text-white leading-snug">
                        Halo! Saya <span class="text-spiderRed">Altafunisa Aflikha Ratnawati</span>, Siswa Berbakat di Jurusan MPLB.
                    </h4>
                    <p class="text-slate-300 leading-relaxed">
                        Saat ini saya sedang menempuh pendidikan di <span class="text-white font-semibold underline decoration-spiderBlue">SMK CYBER MEDIA</span> dengan mengambil konsentrasi keahlian <span class="text-white font-semibold underline decoration-spiderRed">MPLB (Manajemen Perkantoran dan Layanan Bisnis)</span>.
                    </p>
                    <p class="text-slate-300 leading-relaxed">
                        Melalui jurusan ini, saya dibekali dengan berbagai keterampilan penting seperti pengelolaan administrasi modern, otomatisasi perkantoran, tata kelola dokumen digital, serta pelayanan bisnis yang profesional dan efisien. Saya selalu berantusias untuk mengasah kemampuan teknis maupun interpersonal demi menciptakan hasil kerja yang optimal.
                    </p>

                    <!-- Info Badges -->
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 pt-4">
                        <div class="p-4 rounded-xl bg-spiderDark border border-slate-800 flex items-center space-x-4">
                            <div class="w-10 h-10 rounded-lg bg-spiderBlue/20 text-spiderBlueGlow flex items-center justify-center text-lg">
                                <i class="fa-solid fa-school"></i>
                            </div>
                            <div>
                                <h5 class="text-xs text-slate-400">Sekolah</h5>
                                <p class="text-sm font-semibold text-white">SMK Cyber Media</p>
                            </div>
                        </div>

                        <div class="p-4 rounded-xl bg-spiderDark border border-slate-800 flex items-center space-x-4">
                            <div class="w-10 h-10 rounded-lg bg-spiderRed/20 text-spiderRed flex items-center justify-center text-lg">
                                <i class="fa-solid fa-briefcase"></i>
                            </div>
                            <div>
                                <h5 class="text-xs text-slate-400">Jurusan</h5>
                                <p class="text-sm font-semibold text-white">MPLB (Manajemen Perkantoran)</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 3. SKILLS SECTION -->
    <section id="skills" class="py-24 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center space-y-4 mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-spiderRed">Keahlian Utama</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Kemampuan & <span class="text-spiderBlueGlow">Skill</span></h3>
                <div class="w-24 h-1 bg-gradient-to-r from-spiderBlue to-spiderRed mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
                
                <!-- Skill 1: Word -->
                <div class="bg-spiderCard border border-slate-800 hover:border-spiderBlue transition-all duration-300 rounded-2xl p-6 group hover:-translate-y-2 shadow-lg">
                    <div class="w-14 h-14 rounded-xl bg-blue-600/20 text-blue-500 flex items-center justify-center text-2xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-file-word"></i>
                    </div>
                    <h4 class="text-xl font-bold text-white mb-2">Microsoft Word</h4>
                    <p class="text-sm text-slate-400 leading-relaxed mb-4">
                        Penyusunan surat resmi, pembuatan dokumen bisnis, format laporan, dan mail merge perkantoran.
                    </p>
                    <div class="w-full bg-slate-800 h-2 rounded-full overflow-hidden">
                        <div class="bg-blue-500 h-full rounded-full w-[90%]"></div>
                    </div>
                </div>

                <!-- Skill 2: Excel -->
                <div class="bg-spiderCard border border-slate-800 hover:border-emerald-500 transition-all duration-300 rounded-2xl p-6 group hover:-translate-y-2 shadow-lg">
                    <div class="w-14 h-14 rounded-xl bg-emerald-600/20 text-emerald-500 flex items-center justify-center text-2xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-file-excel"></i>
                    </div>
                    <h4 class="text-xl font-bold text-white mb-2">Microsoft Excel</h4>
                    <p class="text-sm text-slate-400 leading-relaxed mb-4">
                        Pengolahan data administrasi, penggunaan rumus (VLOOKUP, IF, SUM), dan grafik data bisnis.
                    </p>
                    <div class="w-full bg-slate-800 h-2 rounded-full overflow-hidden">
                        <div class="bg-emerald-500 h-full rounded-full w-[85%]"></div>
                    </div>
                </div>

                <!-- Skill 3: PowerPoint -->
                <div class="bg-spiderCard border border-slate-800 hover:border-orange-500 transition-all duration-300 rounded-2xl p-6 group hover:-translate-y-2 shadow-lg">
                    <div class="w-14 h-14 rounded-xl bg-orange-600/20 text-orange-500 flex items-center justify-center text-2xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-file-powerpoint"></i>
                    </div>
                    <h4 class="text-xl font-bold text-white mb-2">PowerPoint</h4>
                    <p class="text-sm text-slate-400 leading-relaxed mb-4">
                        Desain slide presentasi yang menarik, komunikatif, profesional, serta menyusun materi rapat.
                    </p>
                    <div class="w-full bg-slate-800 h-2 rounded-full overflow-hidden">
                        <div class="bg-orange-500 h-full rounded-full w-[88%]"></div>
                    </div>
                </div>

                <!-- Skill 4: Komunikasi -->
                <div class="bg-spiderCard border border-slate-800 hover:border-spiderRed transition-all duration-300 rounded-2xl p-6 group hover:-translate-y-2 shadow-lg">
                    <div class="w-14 h-14 rounded-xl bg-spiderRed/20 text-spiderRed flex items-center justify-center text-2xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa-solid fa-comments"></i>
                    </div>
                    <h4 class="text-xl font-bold text-white mb-2">Skill Komunikasi</h4>
                    <p class="text-sm text-slate-400 leading-relaxed mb-4">
                        Komunikasi verbal dan tertulis yang efektif dalam Bahasa Indonesia & Bahasa Inggris.
                    </p>
                    <div class="w-full bg-slate-800 h-2 rounded-full overflow-hidden">
                        <div class="bg-spiderRed h-full rounded-full w-[92%]"></div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 4. PROJECT SECTION -->
    <section id="projects" class="py-24 relative bg-slate-950/60 border-t border-b border-slate-900">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center space-y-4 mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-spiderBlueGlow">Karya & Tugas</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Project <span class="text-spiderRed">Saya</span></h3>
                <p class="text-slate-400 max-w-xl mx-auto text-sm">Berikut adalah beberapa project dan tugas yang pernah saya kerjakan selama menempuh pendidikan.</p>
                <div class="w-24 h-1 bg-gradient-to-r from-spiderRed to-spiderBlue mx-auto rounded-full"></div>
            </div>

            <!-- Filter Buttons -->
            <div class="flex justify-center space-x-3 mb-10 flex-wrap gap-y-2">
                <button class="project-filter-btn active px-4 py-2 rounded-full text-xs font-bold bg-spiderRed text-white shadow-neon-red" data-filter="all">Semua</button>
                <button class="project-filter-btn px-4 py-2 rounded-full text-xs font-bold bg-spiderDark border border-slate-800 text-slate-300 hover:text-white" data-filter="admin">Administrasi</button>
                <button class="project-filter-btn px-4 py-2 rounded-full text-xs font-bold bg-spiderDark border border-slate-800 text-slate-300 hover:text-white" data-filter="presentation">Presentasi</button>
            </div>

            <!-- Project Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                
                <!-- Project Item 1 -->
                <div class="project-card bg-spiderCard rounded-2xl overflow-hidden border border-slate-800 hover:border-spiderBlue/60 transition-all duration-300 shadow-xl" data-category="admin">
                    <div class="h-48 bg-slate-800 relative overflow-hidden group">
                        <img src="https://placehold.co/600x400/1e293b/00d4ff?text=Laporan+Administrasi+Excel" alt="Project Administrasi Excel" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-spiderDark via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-3 left-3 bg-spiderBlue/80 text-white text-[10px] font-extrabold uppercase px-2.5 py-1 rounded-md">Excel & Admin</span>
                    </div>
                    <div class="p-6 space-y-3">
                        <h4 class="text-lg font-bold text-white hover:text-spiderBlueGlow transition-colors">Sistem Pengolahan Data Perkantoran</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Project pembuatan rekapitulasi data laporan keuangan sederhana dan inventaris barang menggunakan rumus kompleks Microsoft Excel.
                        </p>
                        <div class="pt-4 flex items-center justify-between border-t border-slate-800 text-xs">
                            <span class="text-slate-500"><i class="fa-regular fa-folder text-spiderRed mr-1"></i> MPLB Project</span>
                            <span class="text-spiderBlueGlow font-semibold cursor-pointer hover:underline" onclick="openProjectModal('Sistem Pengolahan Data Perkantoran', 'Project ini berfokus pada efisiensi pengolahan data inventaris sarana dan prasarana perkantoran menggunakan Microsoft Excel secara terintegrasi.')">Detail <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i></span>
                        </div>
                    </div>
                </div>

                <!-- Project Item 2 -->
                <div class="project-card bg-spiderCard rounded-2xl overflow-hidden border border-slate-800 hover:border-spiderRed/60 transition-all duration-300 shadow-xl" data-category="presentation">
                    <div class="h-48 bg-slate-800 relative overflow-hidden group">
                        <img src="https://placehold.co/600x400/1e293b/e62429?text=Slide+Presentasi+Bisnis" alt="Project Presentasi PPT" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-spiderDark via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-3 left-3 bg-spiderRed/80 text-white text-[10px] font-extrabold uppercase px-2.5 py-1 rounded-md">PowerPoint</span>
                    </div>
                    <div class="p-6 space-y-3">
                        <h4 class="text-lg font-bold text-white hover:text-spiderRed transition-colors">Desain Presentasi Profile Perusahaan</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Merancang slide presentasi modern dan interaktif untuk kebutuhan company profile dan penyampaian proposal bisnis.
                        </p>
                        <div class="pt-4 flex items-center justify-between border-t border-slate-800 text-xs">
                            <span class="text-slate-500"><i class="fa-regular fa-folder text-spiderBlue mr-1"></i> Public Speaking</span>
                            <span class="text-spiderBlueGlow font-semibold cursor-pointer hover:underline" onclick="openProjectModal('Desain Presentasi Profile Perusahaan', 'Merancang slide presentasi berbasis visual modern untuk mempermudah komunikasi materi rapat dan layanan bisnis.')">Detail <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i></span>
                        </div>
                    </div>
                </div>

                <!-- Project Item 3 -->
                <div class="project-card bg-spiderCard rounded-2xl overflow-hidden border border-slate-800 hover:border-spiderBlue/60 transition-all duration-300 shadow-xl" data-category="admin">
                    <div class="h-48 bg-slate-800 relative overflow-hidden group">
                        <img src="https://placehold.co/600x400/1e293b/ffffff?text=Arsip+Dokumen+Digital" alt="Project Arsip Dokumen" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                        <div class="absolute inset-0 bg-gradient-to-t from-spiderDark via-transparent to-transparent opacity-80"></div>
                        <span class="absolute top-3 left-3 bg-blue-600/80 text-white text-[10px] font-extrabold uppercase px-2.5 py-1 rounded-md">Word & Kearsipan</span>
                    </div>
                    <div class="p-6 space-y-3">
                        <h4 class="text-lg font-bold text-white hover:text-spiderBlueGlow transition-colors">Penyusunan Surat & Kearsipan Digital</h4>
                        <p class="text-slate-400 text-sm leading-relaxed">
                            Pembuatan template korespondensi standar bisnis dan tata kelola kearsipan digital yang rapi dan terorganisir.
                        </p>
                        <div class="pt-4 flex items-center justify-between border-t border-slate-800 text-xs">
                            <span class="text-slate-500"><i class="fa-regular fa-folder text-spiderRed mr-1"></i> Layanan Bisnis</span>
                            <span class="text-spiderBlueGlow font-semibold cursor-pointer hover:underline" onclick="openProjectModal('Penyusunan Surat & Kearsipan Digital', 'Penyusunan berbagai jenis surat korespondensi bisnis resmi dan pengaturan pola kearsipan modern.')">Detail <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i></span>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 5. CONTACT ME SECTION -->
    <section id="contact" class="py-24 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center space-y-4 mb-16">
                <h2 class="text-xs font-bold uppercase tracking-widest text-spiderRed">Terhubung Dengan Saya</h2>
                <h3 class="text-3xl sm:text-4xl font-extrabold text-white">Hubungi <span class="text-spiderBlueGlow">Saya</span></h3>
                <p class="text-slate-400 max-w-xl mx-auto text-sm">Silakan ikuti media sosial saya atau hubungi kontak di bawah ini untuk kolaborasi maupun informasi lebih lanjut.</p>
                <div class="w-24 h-1 bg-gradient-to-r from-spiderBlue to-spiderRed mx-auto rounded-full"></div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                
                <!-- Instagram Card -->
                <a href="https://instagram.com/nnisaa.alt" target="_blank" class="bg-spiderCard border border-slate-800 hover:border-pink-500 p-8 rounded-2xl flex flex-col items-center text-center group hover:-translate-y-2 transition-all duration-300 shadow-xl">
                    <div class="w-16 h-16 rounded-2xl bg-gradient-to-tr from-yellow-500 via-pink-500 to-purple-600 flex items-center justify-center text-white text-3xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fa-brands fa-instagram"></i>
                    </div>
                    <h4 class="text-lg font-bold text-white mb-1">Instagram</h4>
                    <p class="text-sm text-slate-400 mb-4">@nnisaa.alt</p>
                    <span class="text-xs font-bold text-pink-400 group-hover:underline flex items-center space-x-1">
                        <span>Kunjungi Profil</span>
                        <i class="fa-solid fa-arrow-right text-[10px]"></i>
                    </span>
                </a>

                <!-- WhatsApp Card -->
                <a href="https://wa.me/6288291488621" target="_blank" class="bg-spiderCard border border-slate-800 hover:border-emerald-500 p-8 rounded-2xl flex flex-col items-center text-center group hover:-translate-y-2 transition-all duration-300 shadow-xl">
                    <div class="w-16 h-16 rounded-2xl bg-emerald-500 flex items-center justify-center text-white text-3xl mb-4 group-hover:scale-110 transition-transform shadow-lg shadow-emerald-500/30">
                        <i class="fa-brands fa-whatsapp"></i>
                    </div>
                    <h4 class="text-lg font-bold text-white mb-1">WhatsApp</h4>
                    <p class="text-sm text-slate-400 mb-4">088291488621</p>
                    <span class="text-xs font-bold text-emerald-400 group-hover:underline flex items-center space-x-1">
                        <span>Kirim Pesan</span>
                        <i class="fa-solid fa-arrow-right text-[10px]"></i>
                    </span>
                </a>

                <!-- Email Card -->
                <a href="mailto:aflikharatnawati@gmail.com" class="bg-spiderCard border border-slate-800 hover:border-spiderBlue p-8 rounded-2xl flex flex-col items-center text-center group hover:-translate-y-2 transition-all duration-300 shadow-xl">
                    <div class="w-16 h-16 rounded-2xl bg-spiderBlue flex items-center justify-center text-white text-3xl mb-4 group-hover:scale-110 transition-transform shadow-lg shadow-spiderBlue/30">
                        <i class="fa-regular fa-envelope"></i>
                    </div>
                    <h4 class="text-lg font-bold text-white mb-1">Email</h4>
                    <p class="text-sm text-slate-400 mb-4 break-all">aflikharatnawati@gmail.com</p>
                    <span class="text-xs font-bold text-spiderBlueGlow group-hover:underline flex items-center space-x-1">
                        <span>Kirim Email</span>
                        <i class="fa-solid fa-arrow-right text-[10px]"></i>
                    </span>
                </a>

            </div>

            <!-- Interactive Direct Message Form -->
            <div class="mt-12 bg-spiderCard border border-slate-800 rounded-3xl p-8 max-w-3xl mx-auto relative overflow-hidden">
                <div class="absolute top-0 right-0 w-32 h-32 bg-spiderRed/10 rounded-full filter blur-xl"></div>
                <h4 class="text-xl font-bold text-white mb-6 text-center">Kirim Pesan Langsung</h4>
                
                <form id="contact-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-medium text-slate-400 mb-1">Nama Lengkap</label>
                            <input type="text" required placeholder="Masukkan nama Anda" class="w-full bg-spiderDark border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-spiderBlue">
                        </div>
                        <div>
                            <label class="block text-xs font-medium text-slate-400 mb-1">Email / Kontak</label>
                            <input type="text" required placeholder="Masukkan email / whatsapp" class="w-full bg-spiderDark border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-spiderBlue">
                        </div>
                    </div>
                    <div>
                        <label class="block text-xs font-medium text-slate-400 mb-1">Pesan</label>
                        <textarea rows="4" required placeholder="Tuliskan pesan Anda di sini..." class="w-full bg-spiderDark border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-spiderBlue"></textarea>
                    </div>
                    <button type="submit" class="w-full py-3.5 rounded-xl font-bold bg-gradient-to-r from-spiderRed to-spiderBlue text-white shadow-neon-combo hover:opacity-90 transition-all">
                        Kirim Pesan <i class="fa-solid fa-paper-plane ml-2"></i>
                    </button>
                </form>

                <!-- Custom Alert Notification Box (No alert()) -->
                <div id="form-alert" class="hidden mt-4 p-4 rounded-xl bg-emerald-500/20 border border-emerald-500 text-emerald-300 text-sm text-center">
                    <i class="fa-solid fa-circle-check mr-2"></i> Pesan Anda berhasil dikirim! Terima kasih telah menghubungi saya.
                </div>
            </div>
        </div>
    </section>

    <!-- 6. FOOTER -->
    <footer class="bg-black border-t border-slate-900 pt-16 pb-12 relative overflow-hidden">
        <!-- Spidey Web Glow Effect in Footer -->
        <div class="absolute bottom-0 left-1/2 -translate-x-1/2 w-96 h-32 bg-gradient-to-r from-spiderRed/20 to-spiderBlue/20 filter blur-3xl pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 md:grid-cols-12 gap-8 pb-12 border-b border-slate-900">
                
                <!-- Brand Info -->
                <div class="md:col-span-5 space-y-4">
                    <div class="flex items-center space-x-3">
                        <div class="w-9 h-9 rounded-full bg-gradient-to-tr from-spiderRed to-spiderBlue p-[2px] flex items-center justify-center">
                            <div class="w-full h-full bg-spiderDark rounded-full flex items-center justify-center">
                                <i class="fa-solid fa-spider text-spiderRed text-lg"></i>
                            </div>
                        </div>
                        <span class="font-extrabold text-xl tracking-wider text-white">ALTAFUNISA<span class="text-spiderRed">.</span></span>
                    </div>
                    <p class="text-slate-400 text-sm max-w-sm leading-relaxed">
                        Portofolio resmi Altafunisa Aflikha Ratnawati - Siswa SMK Cyber Media jurusan Manajemen Perkantoran dan Layanan Bisnis (MPLB).
                    </p>
                </div>

                <!-- Navigation Quick Links -->
                <div class="md:col-span-4 space-y-3">
                    <h4 class="text-sm font-bold text-white uppercase tracking-wider">Navigasi Menu</h4>
                    <ul class="grid grid-cols-2 gap-2 text-sm text-slate-400">
                        <li><a href="#hero" class="hover:text-spiderRed transition-colors"><i class="fa-solid fa-chevron-right text-[10px] text-spiderRed mr-1.5"></i>Beranda</a></li>
                        <li><a href="#about" class="hover:text-spiderBlueGlow transition-colors"><i class="fa-solid fa-chevron-right text-[10px] text-spiderBlue mr-1.5"></i>Tentang Saya</a></li>
                        <li><a href="#skills" class="hover:text-spiderRed transition-colors"><i class="fa-solid fa-chevron-right text-[10px] text-spiderRed mr-1.5"></i>Keahlian</a></li>
                        <li><a href="#projects" class="hover:text-spiderBlueGlow transition-colors"><i class="fa-solid fa-chevron-right text-[10px] text-spiderBlue mr-1.5"></i>Project</a></li>
                        <li><a href="#contact" class="hover:text-spiderRed transition-colors"><i class="fa-solid fa-chevron-right text-[10px] text-spiderRed mr-1.5"></i>Kontak</a></li>
                    </ul>
                </div>

                <!-- Quick Contact Info -->
                <div class="md:col-span-3 space-y-3">
                    <h4 class="text-sm font-bold text-white uppercase tracking-wider">Kontak Ringkas</h4>
                    <ul class="space-y-2 text-sm text-slate-400">
                        <li class="flex items-center space-x-2">
                            <i class="fa-brands fa-instagram text-pink-500"></i>
                            <span>@nnisaa.alt</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-brands fa-whatsapp text-emerald-500"></i>
                            <span>088291488621</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <i class="fa-regular fa-envelope text-spiderBlueGlow"></i>
                            <span class="truncate">aflikharatnawati@gmail.com</span>
                        </li>
                    </ul>
                </div>

            </div>

            <!-- Footer Bottom Copyright Text -->
            <div class="pt-8 text-center">
                <p class="text-sm text-slate-400">
                    dibuat dengan <span class="text-spiderRed animate-pulse">🤍</span> oleh <span class="text-white font-semibold">Altafunisa Aflikha Ratnawati</span>
                </p>
            </div>
        </div>
    </footer>

    <!-- Project Modal Popup -->
    <div id="project-modal" class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden items-center justify-center p-4">
        <div class="bg-spiderCard border border-slate-800 rounded-2xl max-w-lg w-full p-6 space-y-4 relative shadow-2xl">
            <button onclick="closeProjectModal()" class="absolute top-4 right-4 text-slate-400 hover:text-white text-xl">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <h3 id="modal-title" class="text-xl font-bold text-white"></h3>
            <p id="modal-desc" class="text-sm text-slate-300 leading-relaxed"></p>
            <div class="pt-4 flex justify-end">
                <button onclick="closeProjectModal()" class="px-5 py-2 rounded-xl text-xs font-bold bg-spiderRed text-white">Tutup</button>
            </div>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // Mobile Menu Toggle logic
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const menuIcon = document.getElementById('menu-icon');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
            if(mobileMenu.classList.contains('hidden')) {
                menuIcon.classList.remove('fa-xmark');
                menuIcon.classList.add('fa-bars');
            } else {
                menuIcon.classList.remove('fa-bars');
                menuIcon.classList.add('fa-xmark');
            }
        });

        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
                menuIcon.classList.remove('fa-xmark');
                menuIcon.classList.add('fa-bars');
            });
        });

        // Project Filter Functionality
        const filterBtns = document.querySelectorAll('.project-filter-btn');
        const projectCards = document.querySelectorAll('.project-card');

        filterBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                filterBtns.forEach(b => {
                    b.classList.remove('bg-spiderRed', 'text-white', 'shadow-neon-red');
                    b.classList.add('bg-spiderDark', 'text-slate-300', 'border', 'border-slate-800');
                });

                btn.classList.remove('bg-spiderDark', 'text-slate-300', 'border', 'border-slate-800');
                btn.classList.add('bg-spiderRed', 'text-white', 'shadow-neon-red');

                const filter = btn.getAttribute('data-filter');

                projectCards.forEach(card => {
                    if (filter === 'all' || card.getAttribute('data-category') === filter) {
                        card.style.display = 'block';
                    } else {
                        card.style.display = 'none';
                    }
                });
            });
        });

        // Project Modal Logic
        function openProjectModal(title, description) {
            document.getElementById('modal-title').innerText = title;
            document.getElementById('modal-desc').innerText = description;
            const modal = document.getElementById('project-modal');
            modal.classList.remove('hidden');
            modal.classList.add('flex');
        }

        function closeProjectModal() {
            const modal = document.getElementById('project-modal');
            modal.classList.remove('flex');
            modal.classList.add('hidden');
        }

        // Contact Form Custom Alert Handling
        function handleFormSubmit(e) {
            e.preventDefault();
            const alertBox = document.getElementById('form-alert');
            alertBox.classList.remove('hidden');
            document.getElementById('contact-form').reset();
            
            setTimeout(() => {
                alertBox.classList.add('hidden');
            }, 4000);
        }
    </script>
</body>
</html>
