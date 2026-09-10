```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Ananda Fatma Febriyani | Portfolio Pelajar</title>
  <meta name="description" content="Portfolio personal Ananda Fatma Febriyani, pelajar SMKN 42 Jakarta kelas X Manajemen Perkantoran 1.">
  <meta name="keywords" content="Ananda Fatma Febriyani, portfolio pelajar, SMKN 42 Jakarta, Manajemen Perkantoran">
  <meta name="author" content="Ananda Fatma Febriyani">
  <meta name="theme-color" content="#0f766e">

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>

  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
          },
          animation: {
            'float-slow': 'float 6s ease-in-out infinite',
            'wave': 'wave 5s ease-in-out infinite',
            'sway': 'sway 4s ease-in-out infinite',
            'fly': 'fly 18s linear infinite',
          },
          keyframes: {
            float: {
              '0%, 100%': { transform: 'translateY(0)' },
              '50%': { transform: 'translateY(-12px)' }
            },
            wave: {
              '0%, 100%': { transform: 'translateX(0) scaleY(1)' },
              '50%': { transform: 'translateX(-25px) scaleY(1.08)' }
            },
            sway: {
              '0%, 100%': { transform: 'rotate(-2deg)' },
              '50%': { transform: 'rotate(3deg)' }
            },
            fly: {
              '0%': { transform: 'translateX(-15vw) translateY(0)' },
              '50%': { transform: 'translateX(50vw) translateY(-60px)' },
              '100%': { transform: 'translateX(115vw) translateY(20px)' }
            }
          }
        }
      }
    }
  </script>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">

  <style>
    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', sans-serif;
      overflow-x: hidden;
    }

    .display-font {
      font-family: 'Playfair Display', serif;
    }

    /* =========================
       NAVBAR
    ========================= */
    .nav-link {
      position: relative;
      transition: .3s ease;
    }

    .nav-link::after {
      content: "";
      position: absolute;
      width: 0;
      height: 2px;
      bottom: -6px;
      left: 50%;
      transform: translateX(-50%);
      background: #14b8a6;
      transition: .3s ease;
    }

    .nav-link:hover::after,
    .nav-link.active::after {
      width: 70%;
    }

    /* =========================
       HERO
    ========================= */
    .hero {
      min-height: 100vh;
      position: relative;
      overflow: hidden;
      background:
        linear-gradient(
          to bottom,
          rgba(255, 160, 90, .15),
          rgba(20, 184, 166, .08)
        ),
        linear-gradient(
          180deg,
          #ffb36b 0%,
          #ff8c69 28%,
          #f97366 43%,
          #0ea5a4 65%,
          #075985 100%
        );
    }

    .sun {
      position: absolute;
      width: 130px;
      height: 130px;
      border-radius: 50%;
      background: #fff3bd;
      box-shadow:
        0 0 45px rgba(255, 239, 168, .8),
        0 0 100px rgba(255, 160, 90, .6);
      top: 16%;
      right: 18%;
      animation: sunPulse 5s ease-in-out infinite;
    }

    @keyframes sunPulse {
      0%, 100% {
        transform: scale(1);
        opacity: .9;
      }
      50% {
        transform: scale(1.05);
        opacity: 1;
      }
    }

    /* =========================
       OCEAN
    ========================= */
    .ocean {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 48%;
      overflow: hidden;
      background:
        linear-gradient(
          to bottom,
          rgba(8, 145, 178, .8),
          #075985 45%,
          #064e3b 100%
        );
    }

    .wave-layer {
      position: absolute;
      left: -10%;
      width: 120%;
      border-radius: 50% 50% 0 0;
    }

    .wave-1 {
      height: 100px;
      top: -35px;
      background: rgba(255,255,255,.20);
      animation: waveMove 7s ease-in-out infinite;
    }

    .wave-2 {
      height: 80px;
      top: 15px;
      background: rgba(255,255,255,.12);
      animation: waveMove 9s ease-in-out infinite reverse;
    }

    .wave-3 {
      height: 65px;
      top: 60px;
      background: rgba(255,255,255,.08);
      animation: waveMove 6s ease-in-out infinite;
    }

    @keyframes waveMove {
      0%, 100% {
        transform: translateX(0) rotate(0deg);
      }
      50% {
        transform: translateX(-45px) rotate(1deg);
      }
    }

    /* =========================
       BEACH
    ========================= */
    .beach {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 58%;
      height: 17%;
      background:
        linear-gradient(
          165deg,
          #f6d99b,
          #d9a866
        );
      clip-path: polygon(
        0 38%,
        18% 24%,
        40% 30%,
        60% 18%,
        78% 22%,
        100% 0,
        100% 100%,
        0 100%
      );
      z-index: 4;
    }

    /* =========================
       PALM TREE
    ========================= */
    .palm {
      position: absolute;
      left: 5%;
      bottom: 12%;
      z-index: 8;
      transform-origin: bottom center;
      animation: palmSway 5s ease-in-out infinite;
    }

    .trunk {
      width: 24px;
      height: 260px;
      background:
        repeating-linear-gradient(
          -15deg,
          #6b4226 0 15px,
          #8b5a32 15px 29px
        );
      border-radius: 50%;
      transform: rotate(-8deg);
      transform-origin: bottom;
    }

    .leaves {
      position: absolute;
      top: -20px;
      left: -100px;
      width: 230px;
      height: 150px;
    }

    .leaf {
      position: absolute;
      width: 130px;
      height: 22px;
      background: #166534;
      border-radius: 100% 0 100% 0;
      transform-origin: right center;
    }

    .leaf:nth-child(1) { transform: rotate(-5deg); }
    .leaf:nth-child(2) { transform: rotate(35deg); }
    .leaf:nth-child(3) { transform: rotate(75deg); }
    .leaf:nth-child(4) { transform: rotate(145deg); }
    .leaf:nth-child(5) { transform: rotate(190deg); }
    .leaf:nth-child(6) { transform: rotate(225deg); }
    .leaf:nth-child(7) { transform: rotate(270deg); }

    @keyframes palmSway {
      0%, 100% { transform: rotate(-1deg); }
      50% { transform: rotate(2deg); }
    }

    /* =========================
       BIRDS
    ========================= */
    .bird {
      position: absolute;
      z-index: 7;
      width: 35px;
      height: 20px;
      animation: birdFly 17s linear infinite;
    }

    .bird::before,
    .bird::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 10px;
      border-top: 3px solid rgba(30,41,59,.7);
      border-radius: 50%;
    }

    .bird::before {
      left: 0;
      transform: rotate(15deg);
    }

    .bird::after {
      right: 0;
      transform: rotate(-15deg);
    }

    .bird-1 {
      top: 22%;
      left: -50px;
      animation-delay: 0s;
    }

    .bird-2 {
      top: 30%;
      left: -100px;
      transform: scale(.7);
      animation-delay: 5s;
    }

    .bird-3 {
      top: 16%;
      left: -150px;
      transform: scale(.5);
      animation-delay: 9s;
    }

    @keyframes birdFly {
      0% {
        left: -70px;
        transform: translateY(0) scale(1);
      }
      25% {
        transform: translateY(-30px) scale(1);
      }
      50% {
        transform: translateY(15px) scale(1);
      }
      75% {
        transform: translateY(-20px) scale(1);
      }
      100% {
        left: 110%;
        transform: translateY(0) scale(1);
      }
    }

    /* =========================
       CRAB
    ========================= */
    .crab {
      position: absolute;
      bottom: 7%;
      left: -100px;
      z-index: 12;
      font-size: 42px;
      animation: crabWalk 22s linear infinite;
    }

    @keyframes crabWalk {
      0% {
        left: -100px;
      }
      100% {
        left: 110%;
      }
    }

    /* =========================
       HERO CONTENT
    ========================= */
    .glass {
      background: rgba(255,255,255,.13);
      border: 1px solid rgba(255,255,255,.25);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
    }

    .profile-ring {
      padding: 5px;
      border-radius: 50%;
      background: linear-gradient(
        135deg,
        rgba(255,255,255,.9),
        rgba(20,184,166,.8)
      );
    }

    /* =========================
       SECTION
    ========================= */
    section {
      scroll-margin-top: 80px;
    }

    .section-title {
      position: relative;
      display: inline-block;
    }

    .section-title::after {
      content: "";
      position: absolute;
      width: 55px;
      height: 4px;
      border-radius: 10px;
      background: #14b8a6;
      bottom: -12px;
      left: 50%;
      transform: translateX(-50%);
    }

    /* =========================
       SCROLL ANIMATION
    ========================= */
    .reveal {
      opacity: 0;
      transform: translateY(35px);
      transition: opacity .8s ease, transform .8s ease;
    }

    .reveal.show {
      opacity: 1;
      transform: translateY(0);
    }

    /* =========================
       PHOTO MODAL
    ========================= */
    .modal {
      opacity: 0;
      visibility: hidden;
      transition: .3s ease;
    }

    .modal.open {
      opacity: 1;
      visibility: visible;
    }

    /* =========================
       TESTIMONIAL
    ========================= */
    .testimonial {
      display: none;
    }

    .testimonial.active {
      display: block;
      animation: testimonialIn .5s ease;
    }

    @keyframes testimonialIn {
      from {
        opacity: 0;
        transform: translateX(20px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    /* =========================
       MOBILE
    ========================= */
    @media (max-width: 768px) {
      .sun {
        width: 90px;
        height: 90px;
        right: 15%;
        top: 17%;
      }

      .ocean {
        height: 43%;
      }

      .beach {
        width: 75%;
        height: 15%;
      }

      .palm {
        left: -25px;
        bottom: 10%;
        transform: scale(.7);
      }

      .hero-content {
        padding-top: 100px;
      }
    }
  </style>
</head>

<body class="bg-slate-50 text-slate-800">

  <!-- =========================
       NAVBAR
  ========================== -->
  <header id="navbar"
    class="fixed top-0 left-0 right-0 z-50 transition-all duration-300">

    <nav class="max-w-7xl mx-auto px-5 lg:px-8 py-4 flex items-center justify-between">

      <a href="#beranda"
        class="text-xl font-extrabold text-white drop-shadow">
        A<span class="text-teal-300">.</span>
      </a>

      <div id="desktopMenu"
        class="hidden lg:flex items-center gap-7 text-sm font-medium text-white">
        <a class="nav-link active" href="#beranda">Beranda</a>
        <a class="nav-link" href="#tentang">Tentang</a>
        <a class="nav-link" href="#cv">CV</a>
        <a class="nav-link" href="#karya">Karya</a>
        <a class="nav-link" href="#foto">Foto</a>
        <a class="nav-link" href="#artikel">Artikel</a>
        <a class="nav-link" href="#kontak">Kontak</a>
      </div>

      <button id="menuBtn"
        class="lg:hidden text-white text-2xl"
        aria-label="Buka menu">
        ☰
      </button>
    </nav>

    <!-- MOBILE MENU -->
    <div id="mobileMenu"
      class="hidden lg:hidden mx-4 mb-3 rounded-2xl glass p-5 text-white">

      <div class="grid gap-4 text-sm">
        <a href="#beranda">Beranda</a>
        <a href="#tentang">Tentang</a>
        <a href="#cv">CV</a>
        <a href="#karya">Hasil Karya</a>
        <a href="#foto">Foto</a>
        <a href="#artikel">Artikel</a>
        <a href="#kontak">Kontak</a>
      </div>
    </div>
  </header>


  <!-- =========================
       HERO
  ========================== -->
  <section id="beranda" class="hero flex items-center">

    <!-- Matahari -->
    <div class="sun"></div>

    <!-- Burung -->
    <div class="bird bird-1"></div>
    <div class="bird bird-2"></div>
    <div class="bird bird-3"></div>

    <!-- Pohon Kelapa -->
    <div class="palm">
      <div class="leaves">
        <div class="leaf"></div>
        <div class="leaf"></div>
        <div class="leaf"></div>
        <div class="leaf"></div>
        <div class="leaf"></div>
        <div class="leaf"></div>
        <div class="leaf"></div>
      </div>
      <div class="trunk"></div>
    </div>

    <!-- Laut -->
    <div class="ocean">
      <div class="wave-layer wave-1"></div>
      <div class="wave-layer wave-2"></div>
      <div class="wave-layer wave-3"></div>
    </div>

    <!-- Pantai -->
    <div class="beach"></div>

    <!-- Kepiting -->
    <div class="crab">🦀</div>

    <!-- HERO CONTENT -->
    <div class="hero-content relative z-20 w-full max-w-7xl mx-auto px-6 py-32">

      <div class="grid lg:grid-cols-2 gap-12 items-center">

        <div class="text-white">

          <div class="inline-flex items-center gap-2 glass rounded-full px-4 py-2 text-sm mb-6">
            <span class="w-2 h-2 rounded-full bg-green-300 animate-pulse"></span>
            Selamat datang di portfolio saya
          </div>

          <h1 class="display-font text-5xl sm:text-6xl lg:text-7xl font-bold leading-tight">
            Ananda Fatma
            <span class="block text-teal-100">
              Febriyani
            </span>
          </h1>

          <p class="mt-5 text-xl text-white/90">
            Pelajar • Kreatif • Aktif • Pantang Menyerah
          </p>

          <p class="mt-5 max-w-xl text-white/75 leading-relaxed">
            Seorang pelajar yang aktif, berjiwa juang dan tangguh.
            Terus belajar, berkembang, dan menciptakan sesuatu yang bermakna.
          </p>

          <div class="flex flex-wrap gap-4 mt-8">

            <a href="#karya"
              class="px-6 py-3 rounded-full bg-white text-teal-800 font-bold shadow-lg hover:scale-105 transition">
              Lihat Karya →
            </a>

            <a href="#kontak"
              class="px-6 py-3 rounded-full border border-white/60 bg-white/10 backdrop-blur text-white font-bold hover:bg-white hover:text-teal-800 transition">
              Hubungi Saya
            </a>

          </div>
        </div>


        <!-- PROFILE -->
        <div class="flex justify-center lg:justify-end">

          <div class="glass p-5 rounded-[2rem] shadow-2xl max-w-sm">

            <div class="profile-ring">
              <img
                src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&w=600&q=80"
                alt="Foto profil Ananda Fatma Febriyani"
                class="w-64 h-64 sm:w-72 sm:h-72 object-cover rounded-full">
            </div>

            <div class="text-center text-white mt-5">
              <h2 class="font-bold text-xl">
                Ananda Fatma Febriyani
              </h2>
              <p class="text-white/70 text-sm mt-1">
                X Manajemen Perkantoran 1
              </p>
            </div>

          </div>

        </div>

      </div>
    </div>

    <!-- Scroll indicator -->
    <div class="absolute bottom-6 left-1/2 -translate-x-1/2 z-20 text-white text-center">
      <div class="text-xs mb-2 opacity-70">Scroll untuk menjelajah</div>
      <div class="w-5 h-8 border border-white/60 rounded-full mx-auto flex justify-center">
        <div class="w-1 h-2 bg-white rounded-full mt-2 animate-bounce"></div>
      </div>
    </div>

  </section>


  <!-- =========================
       TENTANG
  ========================== -->
  <section id="tentang" class="py-24 bg-white">

    <div class="max-w-6xl mx-auto px-6">

      <div class="text-center mb-16 reveal">
        <span class="text-teal-600 font-semibold text-sm uppercase tracking-widest">
          Tentang Saya
        </span>

        <h2 class="section-title text-4xl font-bold mt-3">
          Kenali Saya Lebih Dekat
        </h2>
      </div>

      <div class="grid lg:grid-cols-2 gap-14 items-center">

        <div class="reveal">

          <img
            src="https://images.unsplash.com/photo-1524504388940-b1c1722653e1?auto=format&fit=crop&w=900&q=80"
            alt="Foto Ananda"
            class="rounded-[2rem] shadow-xl w-full h-[500px] object-cover">

        </div>

        <div class="reveal">

          <h3 class="text-3xl font-bold mb-5">
            Halo, saya Ananda 👋
          </h3>

          <p class="text-slate-600 leading-relaxed mb-5">
            Saya adalah seorang pelajar di SMKN 42 Jakarta yang saat ini
            duduk di kelas X Manajemen Perkantoran 1.
          </p>

          <p class="text-slate-600 leading-relaxed mb-8">
            Saya merupakan pribadi yang aktif, memiliki semangat juang,
            tangguh, dan senang mempelajari hal-hal baru. Bagi saya,
            setiap pengalaman adalah kesempatan untuk berkembang.
          </p>

          <h4 class="font-bold text-lg mb-4">
            Skill Utama
          </h4>

          <div class="grid grid-cols-2 gap-3">

            <div class="bg-teal-50 text-teal-800 rounded-xl p-4 font-semibold">
              💻 Web
            </div>

            <div class="bg-sky-50 text-sky-800 rounded-xl p-4 font-semibold">
              🎨 Desain
            </div>

            <div class="bg-amber-50 text-amber-800 rounded-xl p-4 font-semibold">
              📷 Fotografi
            </div>

            <div class="bg-purple-50 text-purple-800 rounded-xl p-4 font-semibold">
              ✨ Kreativitas
            </div>

          </div>

        </div>

      </div>
    </div>
  </section>


  <!-- =========================
       CV
  ========================== -->
  <section id="cv" class="py-24 bg-slate-50">

    <div class="max-w-5xl mx-auto px-6">

      <div class="text-center mb-16 reveal">
        <span class="text-teal-600 font-semibold text-sm uppercase tracking-widest">
          Curriculum Vitae
        </span>

        <h2 class="section-title text-4xl font-bold mt-3">
          Perjalanan Pendidikan
        </h2>
      </div>


      <div class="relative">

        <!-- vertical line -->
        <div class="absolute left-4 md:left-1/2 top-0 bottom-0 w-px bg-teal-200"></div>


        <div class="relative mb-14 reveal">

          <div class="md:flex items-center justify-between">

            <div class="md:w-[45%] md:text-right pl-12 md:pl-0">
              <span class="text-teal-600 font-bold">
                2026 — Sekarang
              </span>

              <h3 class="text-2xl font-bold mt-2">
                SMKN 42 Jakarta
              </h3>

              <p class="text-slate-500 mt-2">
                Kelas X — Manajemen Perkantoran 1
              </p>
            </div>

            <div class="absolute left-1 md:left-1/2 md:-translate-x-1/2
              w-7 h-7 rounded-full bg-teal-500 border-4 border-white shadow">
            </div>

            <div class="md:w-[45%] pl-12 md:pl-0 md:pt-0 mt-5 md:mt-0">
              <div class="bg-white rounded-2xl p-6 shadow-sm">
                <p class="text-slate-600 leading-relaxed">
                  Saat ini sedang menempuh pendidikan di bidang
                  Manajemen Perkantoran dengan semangat untuk terus
                  belajar dan mengembangkan kemampuan.
                </p>
              </div>
            </div>

          </div>
        </div>


        <div class="relative reveal">

          <div class="md:flex items-center justify-between">

            <div class="md:w-[45%] order-2 md:order-1 pl-12 md:pl-0">

              <div class="bg-white rounded-2xl p-6 shadow-sm">
                <p class="text-slate-600 leading-relaxed">
                  Saya percaya bahwa menjadi pelajar bukan hanya
                  tentang mendapatkan nilai, tetapi juga membangun
                  karakter, pengalaman, keberanian, dan kemampuan
                  menghadapi tantangan.
                </p>
              </div>

            </div>

            <div class="absolute left-1 md:left-1/2 md:-translate-x-1/2
              w-7 h-7 rounded-full bg-sky-500 border-4 border-white shadow">
            </div>

            <div class="md:w-[45%] pl-12 md:pl-0 order-1 md:order-2 mb-5 md:mb-0">

              <span class="text-sky-600 font-bold">
                Personal Statement
              </span>

              <h3 class="text-2xl font-bold mt-2">
                Aktif & Berjiwa Juang
              </h3>

              <p class="text-slate-500 mt-2">
                Tangguh dalam menghadapi tantangan.
              </p>

            </div>

          </div>
        </div>

      </div>
    </div>
  </section>


  <!-- =========================
       HASIL KARYA
  ========================== -->
  <section id="karya" class="py-24 bg-white">

    <div class="max-w-6xl mx-auto px-6">

      <div class="text-center mb-12 reveal">

        <span class="text-teal-600 font-semibold text-sm uppercase tracking-widest">
          Portfolio
        </span>

        <h2 class="section-title text-4xl font-bold mt-3">
          Hasil Karya
        </h2>

        <p class="text-slate-500 mt-7 max-w-xl mx-auto">
          Beberapa contoh karya yang dapat dikembangkan dan
          diperbarui sesuai project terbaru.
        </p>

      </div>


      <!-- FILTER -->
      <div class="flex justify-center gap-3 flex-wrap mb-10 reveal">

        <button class="filter-btn px-5 py-2 rounded-full bg-teal-600 text-white"
          data-filter="all">
          Semua
        </button>

        <button class="filter-btn px-5 py-2 rounded-full bg-slate-100"
          data-filter="web">
          Web
        </button>

        <button class="filter-btn px-5 py-2 rounded-full bg-slate-100"
          data-filter="desain">
          Desain
        </button>

        <button class="filter-btn px-5 py-2 rounded-full bg-slate-100"
          data-filter="foto">
          Foto
        </button>

      </div>


      <div id="projectGrid"
        class="grid md:grid-cols-2 lg:grid-cols-3 gap-7">

        <!-- PROJECT 1 -->
        <article class="project-card web reveal"
          data-category="web">

          <div class="overflow-hidden rounded-2xl">
            <img
              src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=900&q=80"
              alt="Project website"
              class="w-full h-64 object-cover hover:scale-105 transition duration-500">
          </div>

          <div class="pt-5">
            <span class="text-xs font-bold text-teal-600 uppercase">
              Web
            </span>

            <h3 class="text-xl font-bold mt-2">
              Personal Website
            </h3>

            <p class="text-slate-500 text-sm mt-2">
              Konsep website personal modern dan responsif.
            </p>
          </div>
        </article>


        <!-- PROJECT 2 -->
        <article class="project-card desain reveal"
          data-category="desain">

          <div class="overflow-hidden rounded-2xl">
            <img
              src="https://images.unsplash.com/photo-1561070791-2526d30994b5?auto=format&fit=crop&w=900&q=80"
              alt="Project desain"
              class="w-full h-64 object-cover hover:scale-105 transition duration-500">
          </div>

          <div class="pt-5">
            <span class="text-xs font-bold text-purple-600 uppercase">
              Desain
            </span>

            <h3 class="text-xl font-bold mt-2">
              Creative Design
            </h3>

            <p class="text-slate-500 text-sm mt-2">
              Eksplorasi desain visual dan kreativitas.
            </p>
          </div>
        </article>


        <!-- PROJECT 3 -->
        <article class="project-card foto reveal"
          data-category="foto">

          <div class="overflow-hidden rounded-2xl">
            <img
              src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=900&q=80"
              alt="Project fotografi"
              class="w-full h-64 object-cover hover:scale-105 transition duration-500">
          </div>

          <div class="pt-5">
            <span class="text-xs font-bold text-amber-600 uppercase">
              Foto
            </span>

            <h3 class="text-xl font-bold mt-2">
              Sunset Photography
            </h3>

            <p class="text-slate-500 text-sm mt-2">
              Eksplorasi fotografi dengan suasana sunset.
            </p>
          </div>
        </article>

      </div>
    </div>
  </section>


  <!-- =========================
       FOTO
  ========================== -->
  <section id="foto" class="py-24 bg-slate-950 text-white">

    <div class="max-w-6xl mx-auto px-6">

      <div class="text-center mb-14 reveal">

        <span class="text-teal-400 font-semibold text-sm uppercase tracking-widest">
          Gallery
        </span>

        <h2 class="section-title text-4xl font-bold mt-3">
          Foto
        </h2>

        <p class="text-slate-400 mt-7">
          Klik foto untuk memperbesar.
        </p>

      </div>


      <div class="grid grid-cols-2 md:grid-cols-3 gap-4">

        <img class="gallery-img reveal"
          src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?auto=format&fit=crop&w=800&q=80"
          alt="Pantai"
          loading="lazy">

        <img class="gallery-img reveal"
          src="https://images.unsplash.com/photo-1473116763249-2faaef81ccda?auto=format&fit=crop&w=800&q=80"
          alt="Laut"
          loading="lazy">

        <img class="gallery-img reveal"
          src="https://images.unsplash.com/photo-1476673160081-cf065607f449?auto=format&fit=crop&w=800&q=80"
          alt="Sunset"
          loading="lazy">

        <img class="gallery-img reveal"
          src="https://images.unsplash.com/photo-1500534623283-312aade485b7?auto=format&fit=crop&w=800&q=80"
          alt="Pemandangan"
          loading="lazy">

        <img class="gallery-img reveal"
          src="https://images.unsplash.com/photo-1510414842594-a61c69b5ae57?auto=format&fit=crop&w=800&q=80"
          alt="Pantai tropis"
          loading="lazy">

        <img class="gallery-img reveal"
          src="https://images.unsplash.com/photo-1505881502353-a1986add3762?auto=format&fit=crop&w=800&q=80"
          alt="Laut dan langit"
          loading="lazy">

      </div>

    </div>
  </section>


  <!-- PHOTO MODAL -->
  <div id="photoModal"
    class="modal fixed inset-0 z-[100] bg-black/90 flex items-center justify-center p-5">

    <button id="closeModal"
      class="absolute top-5 right-6 text-white text-4xl">
      ×
    </button>

    <img id="modalImage"
      src=""
      alt="Foto diperbesar"
      class="max-w-full max-h-[90vh] object-contain rounded-xl shadow-2xl">

  </div>


  <!-- =========================
       ARTIKEL
  ========================== -->
  <section id="artikel" class="py-24 bg-slate-50">

    <div class="max-w-6xl mx-auto px-6">

      <div class="text-center mb-14 reveal">

        <span class="text-teal-600 font-semibold text-sm uppercase tracking-widest">
          Blog
        </span>

        <h2 class="section-title text-4xl font-bold mt-3">
          Artikel Terbaru
        </h2>

      </div>


      <div class="grid md:grid-cols-3 gap-7">

        <article class="bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-xl transition reveal">

          <img
            src="https://images.unsplash.com/photo-1455390582262-044cdead277a?auto=format&fit=crop&w=900&q=80"
            alt="Belajar dan berkembang"
            class="w-full h-52 object-cover">

          <div class="p-6">

            <span class="text-sm text-teal-600">
              10 September 2026
            </span>

            <h3 class="text-xl font-bold mt-3">
              Belajar Menjadi Versi Terbaik Diri Sendiri
            </h3>

            <p class="text-slate-500 text-sm mt-3">
              Tentang proses belajar, berkembang, dan tidak takut mencoba.
            </p>

            <button class="text-teal-600 font-bold text-sm mt-5">
              Baca Selengkapnya →
            </button>

          </div>
        </article>


        <article class="bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-xl transition reveal">

          <img
            src="https://images.unsplash.com/photo-1524178232363-1fb2b075b655?auto=format&fit=crop&w=900&q=80"
            alt="Pendidikan"
            class="w-full h-52 object-cover">

          <div class="p-6">

            <span class="text-sm text-teal-600">
              2026
            </span>

            <h3 class="text-xl font-bold mt-3">
              Pengalaman Menjadi Pelajar SMK
            </h3>

            <p class="text-slate-500 text-sm mt-3">
              Cerita dan pengalaman menjalani kehidupan sebagai pelajar.
            </p>

            <button class="text-teal-600 font-bold text-sm mt-5">
              Baca Selengkapnya →
            </button>

          </div>
        </article>


        <article class="bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-xl transition reveal">

          <img
            src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3?auto=format&fit=crop&w=900&q=80"
            alt="Teknologi"
            class="w-full h-52 object-cover">

          <div class="p-6">

            <span class="text-sm text-teal-600">
              2026
            </span>

            <h3 class="text-xl font-bold mt-3">
              Mengembangkan Skill di Era Digital
            </h3>

            <p class="text-slate-500 text-sm mt-3">
              Mengapa pelajar perlu terus belajar teknologi dan kreativitas.
            </p>

            <button class="text-teal-600 font-bold text-sm mt-5">
              Baca Selengkapnya →
            </button>

          </div>
        </article>

      </div>
    </div>
  </section>


  <!-- =========================
       SOCIAL MEDIA
  ========================== -->
  <section class="py-20 bg-white">

    <div class="max-w-4xl mx-auto px-6 text-center reveal">

      <span class="text-teal-600 font-semibold text-sm uppercase tracking-widest">
        Social Media
      </span>

      <h2 class="text-4xl font-bold mt-3">
        Temukan Saya di Media Sosial
      </h2>

      <div class="flex justify-center gap-5 mt-10 flex-wrap">

        <a href="https://instagram.com/m0odynanana"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center gap-3 px-6 py-4 rounded-2xl bg-gradient-to-r from-pink-500 via-purple-500 to-orange-400 text-white font-bold hover:-translate-y-1 transition shadow-lg">
          <span class="text-2xl">◎</span>
          Instagram
        </a>

        <a href="https://tiktok.com/@salvatore7877"
          target="_blank"
          rel="noopener noreferrer"
          class="flex items-center gap-3 px-6 py-4 rounded-2xl bg-black text-white font-bold hover:-translate-y-1 transition shadow-lg">
          <span class="text-2xl">♪</span>
          TikTok
        </a>

      </div>
    </div>
  </section>


  <!-- =========================
       TESTIMONI
  ========================== -->
  <section class="py-24 bg-teal-900 text-white">

    <div class="max-w-4xl mx-auto px-6">

      <div class="text-center mb-12 reveal">

        <span class="text-teal-300 font-semibold text-sm uppercase tracking-widest">
          Testimoni
        </span>

        <h2 class="text-4xl font-bold mt-3">
          Apa Kata Mereka?
        </h2>

      </div>


      <div id="testimonialSlider" class="relative">

        <div class="testimonial active text-center">

          <img
            src="https://i.pravatar.cc/150?img=47"
            alt="Testimoni"
            class="w-20 h-20 rounded-full mx-auto object-cover border-4 border-teal-400">

          <p class="text-lg md:text-xl text-teal-50 leading-relaxed mt-6">
            “Ananda adalah pribadi yang aktif, kreatif, dan
            selalu berusaha memberikan hasil terbaik.”
          </p>

          <h4 class="font-bold mt-6">
            Sarah Putri
          </h4>

          <span class="text-teal-300 text-sm">
            Student
          </span>

        </div>


        <div class="testimonial text-center">

          <img
            src="https://i.pravatar.cc/150?img=32"
            alt="Testimoni"
            class="w-20 h-20 rounded-full mx-auto object-cover border-4 border-teal-400">

          <p class="text-lg md:text-xl text-teal-50 leading-relaxed mt-6">
            “Semangat belajar dan keberanian Ananda dalam mencoba
            hal baru sangat menginspirasi.”
          </p>

          <h4 class="font-bold mt-6">
            Raka Pratama
          </h4>

          <span class="text-teal-300 text-sm">
            Creative Partner
          </span>

        </div>


        <div class="testimonial text-center">

          <img
            src="https://i.pravatar.cc/150?img=44"
            alt="Testimoni"
            class="w-20 h-20 rounded-full mx-auto object-cover border-4 border-teal-400">

          <p class="text-lg md:text-xl text-teal-50 leading-relaxed mt-6">
            “Pribadi yang tangguh dan tidak mudah menyerah ketika
            menghadapi tantangan.”
          </p>

          <h4 class="font-bold mt-6">
            Dinda Amelia
          </h4>

          <span class="text-teal-300 text-sm">
            Student
          </span>

        </div>


        <div class="flex justify-center gap-2 mt-8">

          <button class="testimonial-dot w-3 h-3 rounded-full bg-white"
            data-slide="0"></button>

          <button class="testimonial-dot w-3 h-3 rounded-full bg-white/30"
            data-slide="1"></button>

          <button class="testimonial-dot w-3 h-3 rounded-full bg-white/30"
            data-slide="2"></button>

        </div>

      </div>
    </div>
  </section>


  <!-- =========================
       KONTAK
  ========================== -->
  <section id="kontak" class="py-24 bg-slate-50">

    <div class="max-w-6xl mx-auto px-6">

      <div class="text-center mb-14 reveal">

        <span class="text-teal-600 font-semibold text-sm uppercase tracking-widest">
          Contact
        </span>

        <h2 class="section-title text-4xl font-bold mt-3">
          Hubungi Saya
        </h2>

      </div>


      <div class="grid lg:grid-cols-2 gap-10">

        <!-- FORM -->
        <div class="bg-white rounded-3xl p-7 md:p-10 shadow-sm reveal">

          <form id="contactForm">

            <div class="mb-5">
              <label class="block font-semibold mb-2">
                Nama
              </label>

              <input
                type="text"
                id="name"
                required
                placeholder="Nama kamu"
                class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-teal-500">
            </div>


            <div class="mb-5">

              <label class="block font-semibold mb-2">
                Email
              </label>

              <input
                type="email"
                id="email"
                required
                placeholder="nama@email.com"
                class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-teal-500">

            </div>


            <div class="mb-5">

              <label class="block font-semibold mb-2">
                Pesan
              </label>

              <textarea
                id="message"
                required
                rows="5"
                placeholder="Tulis pesan kamu..."
                class="w-full px-4 py-3 rounded-xl border border-slate-200 focus:outline-none focus:ring-2 focus:ring-teal-500"></textarea>

            </div>


            <button
              type="submit"
              class="w-full py-3 rounded-xl bg-teal-600 text-white font-bold hover:bg-teal-700 transition">
              Kirim Pesan
            </button>

          </form>

          <p id="formMessage"
            class="hidden mt-4 text-center text-teal-600 font-medium">
            Terima kasih! Pesan kamu sudah disiapkan.
          </p>

        </div>


        <!-- INFO -->
        <div class="space-y-6 reveal">

          <div class="bg-white rounded-2xl p-6 shadow-sm">

            <div class="flex gap-4">

              <div class="w-12 h-12 rounded-xl bg-teal-100 flex items-center justify-center text-xl">
                📍
              </div>

              <div>
                <h3 class="font-bold">
                  Alamat
                </h3>

                <p class="text-slate-500 mt-1">
                  Jl. H. Mali RT.010/RW.001
                </p>
              </div>

            </div>

          </div>


          <div class="bg-white rounded-2xl p-6 shadow-sm">

            <div class="flex gap-4">

              <div class="w-12 h-12 rounded-xl bg-sky-100 flex items-center justify-center text-xl">
                ✉️
              </div>

              <div>
                <h3 class="font-bold">
                  Email
                </h3>

                <a
                  href="mailto:nd4alifeisg0od@gmail.com"
                  class="text-slate-500 mt-1 block hover:text-teal-600">
                  nd4alifeisg0od@gmail.com
                </a>
              </div>

            </div>

          </div>


          <div class="bg-white rounded-2xl p-6 shadow-sm">

            <div class="flex gap-4">

              <div class="w-12 h-12 rounded-xl bg-green-100 flex items-center justify-center text-xl">
                💬
              </div>

              <div>
                <h3 class="font-bold">
                  WhatsApp
                </h3>

                <a
                  href="https://wa.me/6283188526369"
                  target="_blank"
                  rel="noopener noreferrer"
                  class="text-slate-500 mt-1 block hover:text-teal-600">
                  0831-8852-6369
                </a>
              </div>

            </div>

          </div>


          <!-- GOOGLE MAPS -->
          <div class="rounded-2xl overflow-hidden shadow-sm h-64">

            <iframe
              src="https://www.google.com/maps?q=Jl.+H.+Mali+RT.010/RW.001,+Jakarta&output=embed"
              width="100%"
              height="100%"
              style="border:0;"
              loading="lazy"
              allowfullscreen
              referrerpolicy="no-referrer-when-downgrade">
            </iframe>

          </div>

        </div>

      </div>
    </div>
  </section>


  <!-- =========================
       FOOTER
  ========================== -->
  <footer class="bg-slate-950 text-white py-10">

    <div class="max-w-6xl mx-auto px-6">

      <div class="flex flex-col md:flex-row items-center justify-between gap-5">

        <div>
          <div class="text-xl font-bold">
            Ananda<span class="text-teal-400">.</span>
          </div>

          <p class="text-slate-500 text-sm mt-1">
            Personal Portfolio
          </p>
        </div>


        <div class="flex gap-5 text-sm text-slate-400">

          <a href="#beranda" class="hover:text-white transition">
            Beranda
          </a>

          <a href="#tentang" class="hover:text-white transition">
            Tentang
          </a>

          <a href="#karya" class="hover:text-white transition">
            Karya
          </a>

          <a href="#kontak" class="hover:text-white transition">
            Kontak
          </a>

        </div>

      </div>


      <div class="border-t border-slate-800 mt-8 pt-7 text-center text-slate-500 text-sm">

        © 2026 Ananda Fatma Febriyani.
        Dibuat dengan kreativitas dan semangat belajar 🌊

      </div>

    </div>
  </footer>


  <!-- =========================
       JAVASCRIPT
  ========================== -->
  <script>

    /* =========================
       NAVBAR SCROLL
    ========================== */

    const navbar = document.getElementById("navbar");

    window.addEventListener("scroll", () => {

      if (window.scrollY > 40) {
        navbar.classList.add(
          "bg-slate-950/80",
          "backdrop-blur-lg",
          "shadow-lg"
        );
      } else {
        navbar.classList.remove(
          "bg-slate-950/80",
          "backdrop-blur-lg",
          "shadow-lg"
        );
      }

    });


    /* =========================
       MOBILE MENU
    ========================== */

    const menuBtn = document.getElementById("menuBtn");
    const mobileMenu = document.getElementById("mobileMenu");

    menuBtn.addEventListener("click", () => {
      mobileMenu.classList.toggle("hidden");
    });

    document.querySelectorAll("#mobileMenu a").forEach(link => {

      link.addEventListener("click", () => {
        mobileMenu.classList.add("hidden");
      });

    });


    /* =========================
       SCROLL REVEAL
    ========================== */

    const revealElements =
      document.querySelectorAll(".reveal");

    const revealObserver =
      new IntersectionObserver(
        (entries, observer) => {

          entries.forEach(entry => {

            if (entry.isIntersecting) {

              entry.target.classList.add("show");

              observer.unobserve(entry.target);

            }

          });

        },
        {
          threshold: 0.12
        }
      );

    revealElements.forEach(el => {
      revealObserver.observe(el);
    });


    /* =========================
       ACTIVE NAVIGATION
    ========================= */

    const sections =
      document.querySelectorAll("section[id]");

    const navLinks =
      document.querySelectorAll(".nav-link");

    window.addEventListener("scroll", () => {

      let current = "";

      sections.forEach(section => {

        const sectionTop =
          section.offsetTop - 150;

        if (window.scrollY >= sectionTop) {
          current = section.getAttribute("id");
        }

      });

      navLinks.forEach(link => {

        link.classList.remove("active");

        if (
          link.getAttribute("href") === "#" + current
        ) {
          link.classList.add("active");
        }

      });

    });


    /* =========================
       PROJECT FILTER
    ========================== */

    const filterButtons =
      document.querySelectorAll(".filter-btn");

    const projectCards =
      document.querySelectorAll(".project-card");

    filterButtons.forEach(button => {

      button.addEventListener("click", () => {

        const filter =
          button.dataset.filter;

        filterButtons.forEach(btn => {

          btn.classList.remove(
            "bg-teal-600",
            "text-white"
          );

          btn.classList.add(
            "bg-slate-100"
          );

        });

        button.classList.remove(
          "bg-slate-100"
        );

        button.classList.add(
          "bg-teal-600",
          "text-white"
        );


        projectCards.forEach(card => {

          if (
            filter === "all" ||
            card.dataset.category === filter
          ) {

            card.style.display = "block";

            setTimeout(() => {
              card.classList.add("show");
            }, 30);

          } else {

            card.style.display = "none";

          }

        });

      });

    });


    /* =========================
       PHOTO ZOOM
    ========================== */

    const galleryImages =
      document.querySelectorAll(".gallery-img");

    const photoModal =
      document.getElementById("photoModal");

    const modalImage =
      document.getElementById("modalImage");

    const closeModal =
      document.getElementById("closeModal");


    galleryImages.forEach(image => {

      image.classList.add(
        "w-full",
        "h-64",
        "object-cover",
        "rounded-2xl",
        "cursor-pointer",
        "hover:opacity-80",
        "transition"
      );

      image.addEventListener("click", () => {

        modalImage.src = image.src;

        photoModal.classList.add("open");

        document.body.style.overflow = "hidden";

      });

    });


    function closePhotoModal() {

      photoModal.classList.remove("open");

      document.body.style.overflow = "";

    }


    closeModal.addEventListener(
      "click",
      closePhotoModal
    );


    photoModal.addEventListener("click", event => {

      if (event.target === photoModal) {
        closePhotoModal();
      }

    });


    document.addEventListener("keydown", event => {

      if (event.key === "Escape") {
        closePhotoModal();
      }

    });


    /* =========================
       TESTIMONIAL SLIDER
    ========================== */

    const testimonials =
      document.querySelectorAll(".testimonial");

    const dots =
      document.querySelectorAll(".testimonial-dot");

    let currentSlide = 0;


    function showSlide(index) {

      testimonials.forEach(item => {
        item.classList.remove("active");
      });

      dots.forEach(dot => {
        dot.classList.remove("bg-white");
        dot.classList.add("bg-white/30");
      });

      testimonials[index].classList.add("active");

      dots[index].classList.remove("bg-white/30");
      dots[index].classList.add("bg-white");

    }


    dots.forEach((dot, index) => {

      dot.addEventListener("click", () => {

        currentSlide = index;

        showSlide(currentSlide);

      });

    });


    setInterval(() => {

      currentSlide++;

      if (currentSlide >= testimonials.length) {
        currentSlide = 0;
      }

      showSlide(currentSlide);

    }, 5000);


    /* =========================
       CONTACT FORM
    ========================== */

    const contactForm =
      document.getElementById("contactForm");

    const formMessage =
      document.getElementById("formMessage");


    contactForm.addEventListener(
      "submit",
      function(event) {

        event.preventDefault();

        const name =
          document.getElementById("name").value;

        const email =
          document.getElementById("email").value;

        const message =
          document.getElementById("message").value;


        /*
          Membuka WhatsApp dengan pesan.
          Jadi website tetap static dan tidak membutuhkan backend.
        */

        const whatsappMessage =
          `Halo Ananda, saya ${name}.\n\n` +
          `Email: ${email}\n\n` +
          `Pesan:\n${message}`;


        const whatsappURL =
          "https://wa.me/6283188526369?text=" +
          encodeURIComponent(whatsappMessage);


        window.open(
          whatsappURL,
          "_blank"
        );


        formMessage.classList.remove(
          "hidden"
        );

      }
    );


    /* =========================
       IMAGE ERROR FALLBACK
    ========================== */

    document.querySelectorAll("img").forEach(img => {

      img.addEventListener("error", () => {

        img.style.background =
          "linear-gradient(135deg,#0f766e,#075985)";

        img.alt =
          "Foto belum tersedia";

      });

    });

  </script>

</body>
</html>
```
