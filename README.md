```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">

  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <meta name="description"
        content="Portfolio personal Jihan Maharani Putri, seorang pelajar aktif, tangguh, dan berjiwa juang.">
  <meta name="keywords"
        content="Jihan Maharani Putri, portfolio, pelajar, SMKN 42 Jakarta, desain, web, foto">
  <meta name="author" content="Jihan Maharani Putri">

  <title>Jihan Maharani Putri | Personal Portfolio</title>

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>

  <!-- Google Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Pacifico&display=swap" rel="stylesheet">

  <!-- Icons -->
  <link rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

  <style>
    :root {
      --pink: #f472b6;
      --pink-dark: #db2777;
      --pink-soft: #fce7f3;
      --cream: #fffaf5;
      --text: #4a3040;
    }

    * {
      scroll-behavior: smooth;
      box-sizing: border-box;
    }

    body {
      margin: 0;
      background:
        radial-gradient(circle at 10% 10%, rgba(244,114,182,.14), transparent 25%),
        radial-gradient(circle at 90% 20%, rgba(251,207,232,.35), transparent 25%),
        var(--cream);
      color: var(--text);
      font-family: "DM Sans", sans-serif;
      overflow-x: hidden;
    }

    .cute-font {
      font-family: "Pacifico", cursive;
    }

    /* Glitter */
    .glitter {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 9999;
      overflow: hidden;
    }

    .sparkle {
      position: absolute;
      color: rgba(236,72,153,.55);
      font-size: 12px;
      animation: sparkle 3s ease-in-out infinite;
    }

    @keyframes sparkle {
      0%, 100% {
        opacity: .15;
        transform: scale(.7) rotate(0deg);
      }

      50% {
        opacity: 1;
        transform: scale(1.3) rotate(180deg);
      }
    }

    /* Floating decorations */
    .float {
      animation: float 4s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% {
        transform: translateY(0);
      }

      50% {
        transform: translateY(-12px);
      }
    }

    /* Scroll reveal */
    .reveal {
      opacity: 0;
      transform: translateY(35px);
      transition: all .8s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    /* Cards */
    .cute-card {
      background: rgba(255,255,255,.78);
      border: 1px solid rgba(244,114,182,.18);
      box-shadow: 0 15px 45px rgba(219,39,119,.08);
      backdrop-filter: blur(12px);
    }

    .cute-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 20px 50px rgba(219,39,119,.14);
    }

    /* Buttons */
    .pink-btn {
      background: linear-gradient(135deg, #f472b6, #ec4899);
      color: white;
      transition: .3s;
      box-shadow: 0 8px 25px rgba(236,72,153,.22);
    }

    .pink-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 30px rgba(236,72,153,.35);
    }

    .outline-btn {
      border: 1.5px solid #f472b6;
      color: #db2777;
      transition: .3s;
    }

    .outline-btn:hover {
      background: #fce7f3;
      transform: translateY(-3px);
    }

    /* Navigation */
    .nav-link {
      position: relative;
      transition: .25s;
    }

    .nav-link:hover {
      color: #db2777;
    }

    .nav-link::after {
      content: "";
      position: absolute;
      width: 0;
      height: 2px;
      bottom: -5px;
      left: 50%;
      background: #ec4899;
      transition: .3s;
      transform: translateX(-50%);
    }

    .nav-link:hover::after {
      width: 70%;
    }

    /* Image placeholder */
    .photo-placeholder {
      background:
        linear-gradient(135deg, #fce7f3, #fff1f2);
      border: 2px dashed rgba(236,72,153,.35);
      color: #db2777;
    }

    .gallery-img {
      transition: .4s;
    }

    .gallery-item:hover .gallery-img {
      transform: scale(1.06);
    }

    /* Timeline */
    .timeline-line {
      position: absolute;
      left: 16px;
      top: 0;
      bottom: 0;
      width: 2px;
      background: linear-gradient(#f9a8d4, #f472b6, #fbcfe8);
    }

    /* Social */
    .social-btn {
      transition: .3s;
    }

    .social-btn:hover {
      transform: translateY(-6px) rotate(-2deg);
    }

    /* Music player */
    .music-player {
      position: fixed;
      right: 20px;
      bottom: 20px;
      z-index: 1000;
    }

    /* Modal */
    #galleryModal {
      background: rgba(42, 20, 32, .82);
      backdrop-filter: blur(8px);
    }

    /* Mobile menu */
    #mobileMenu {
      display: none;
    }

    #mobileMenu.show {
      display: block;
    }

    @media (max-width: 768px) {
      .hero-title {
        font-size: 2.8rem;
      }

      .music-player {
        right: 12px;
        bottom: 12px;
      }
    }
  </style>
</head>

<body>

  <!-- Glitter -->
  <div class="glitter" aria-hidden="true">
    <span class="sparkle" style="left:5%;top:15%">✦</span>
    <span class="sparkle" style="left:15%;top:65%;animation-delay:.8s">✧</span>
    <span class="sparkle" style="left:28%;top:30%;animation-delay:1.2s">✦</span>
    <span class="sparkle" style="left:42%;top:80%;animation-delay:.4s">✧</span>
    <span class="sparkle" style="left:58%;top:18%;animation-delay:1.5s">✦</span>
    <span class="sparkle" style="left:70%;top:55%;animation-delay:.7s">✧</span>
    <span class="sparkle" style="left:82%;top:25%;animation-delay:1s">✦</span>
    <span class="sparkle" style="left:94%;top:75%;animation-delay:.3s">✧</span>
  </div>

  <!-- NAVBAR -->
  <header class="fixed top-0 left-0 right-0 z-50">
    <nav class="mx-auto max-w-7xl px-4 py-4">
      <div class="cute-card rounded-full px-5 py-3 flex items-center justify-between">

        <a href="#beranda"
           class="cute-font text-xl text-pink-500">
          Jihan ♡
        </a>

        <!-- Desktop -->
        <div class="hidden lg:flex items-center gap-6 text-sm font-semibold">
          <a class="nav-link" href="#beranda">Beranda</a>
          <a class="nav-link" href="#tentang">Tentang</a>
          <a class="nav-link" href="#cv">CV</a>
          <a class="nav-link" href="#karya">Karya</a>
          <a class="nav-link" href="#foto">Foto</a>
          <a class="nav-link" href="#artikel">Artikel</a>
          <a class="nav-link" href="#sosial">Sosial</a>
          <a class="nav-link" href="#kontak">Kontak</a>
          <a class="nav-link" href="#testimoni">Testimoni</a>
        </div>

        <!-- Mobile Button -->
        <button id="menuBtn"
                class="lg:hidden w-10 h-10 rounded-full bg-pink-100 text-pink-600">
          <i class="fa-solid fa-bars"></i>
        </button>
      </div>

      <!-- Mobile Menu -->
      <div id="mobileMenu"
           class="cute-card mt-2 rounded-3xl p-5 lg:hidden">
        <div class="grid grid-cols-2 gap-3 text-sm font-semibold">
          <a href="#beranda">Beranda</a>
          <a href="#tentang">Tentang</a>
          <a href="#cv">CV</a>
          <a href="#karya">Karya</a>
          <a href="#foto">Foto</a>
          <a href="#artikel">Artikel</a>
          <a href="#sosial">Sosial</a>
          <a href="#kontak">Kontak</a>
          <a href="#testimoni">Testimoni</a>
        </div>
      </div>
    </nav>
  </header>


  <!-- HERO -->
  <main>

    <section id="beranda"
             class="min-h-screen flex items-center pt-32 pb-20 px-5">

      <div class="max-w-7xl mx-auto w-full grid lg:grid-cols-2 gap-14 items-center">

        <div class="reveal">

          <span class="inline-block px-4 py-2 rounded-full bg-pink-100 text-pink-600 text-sm font-bold mb-5">
            ✨ Welcome to my little world
          </span>

          <h1 class="hero-title text-5xl md:text-6xl font-bold leading-tight">
            Halo, aku
            <span class="text-pink-500">Jihan</span>
            🎀
          </h1>

          <p class="cute-font text-2xl text-pink-400 mt-4">
            Jihan Maharani Putri
          </p>

          <p class="mt-5 text-lg text-gray-600 max-w-xl leading-relaxed">
            Seorang <b>pelajar</b> yang aktif, berjiwa juang,
            tangguh, kreatif, dan senang mencoba hal-hal baru.
          </p>

          <div class="flex flex-wrap gap-4 mt-8">
            <a href="#karya"
               class="pink-btn px-6 py-3 rounded-full font-bold">
              ✨ Lihat Karya
            </a>

            <a href="#kontak"
               class="outline-btn px-6 py-3 rounded-full font-bold">
              💌 Hubungi Saya
            </a>
          </div>

          <div class="flex gap-5 mt-8 text-pink-400 text-xl">
            <span>♡</span>
            <span>✦</span>
            <span>୨୧</span>
            <span>✧</span>
            <span>♡</span>
          </div>
        </div>


        <div class="reveal flex justify-center relative">

          <div class="absolute -top-8 -left-4 text-4xl float">🎀</div>
          <div class="absolute -bottom-5 -right-2 text-4xl float">✨</div>
          <div class="absolute top-1/2 -right-8 text-3xl float">💗</div>

          <div class="w-72 h-72 md:w-96 md:h-96 rounded-[45%] p-3 bg-gradient-to-br from-pink-200 via-white to-pink-300 shadow-2xl">

            <div class="w-full h-full rounded-[42%] overflow-hidden photo-placeholder flex flex-col items-center justify-center">

              <!-- GANTI DENGAN FOTO PROFILE -->
              <img src="assets/images/profile.jpg"
                   alt="Foto profil Jihan"
                   class="w-full h-full object-cover"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">

              <div class="hidden flex-col items-center justify-center text-center p-5">
                <i class="fa-solid fa-image text-5xl mb-3"></i>
                <span class="font-bold">Foto Profil</span>
                <small>profile.jpg</small>
              </div>

            </div>
          </div>
        </div>

      </div>
    </section>


    <!-- TENTANG -->
    <section id="tentang" class="py-24 px-5">

      <div class="max-w-7xl mx-auto">

        <div class="text-center reveal">
          <span class="text-pink-500 font-bold">♡ ABOUT ME ♡</span>
          <h2 class="text-4xl font-bold mt-2">Tentang Saya</h2>
          <p class="text-gray-500 mt-3">
            Sedikit cerita tentang Jihan ✨
          </p>
        </div>

        <div class="grid lg:grid-cols-2 gap-10 mt-14 items-center">

          <div class="reveal">
            <div class="cute-card rounded-[35px] p-4">

              <div class="aspect-[4/3] rounded-[28px] overflow-hidden photo-placeholder">

                <img src="assets/images/profile.jpg"
                     alt="Tentang Jihan"
                     class="w-full h-full object-cover"
                     onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">

                <div class="hidden w-full h-full flex-col items-center justify-center">
                  <i class="fa-solid fa-camera text-4xl mb-2"></i>
                  <span>Foto Tentang Saya</span>
                </div>

              </div>

            </div>
          </div>

          <div class="reveal">

            <h3 class="text-3xl font-bold">
              Hai! Aku <span class="text-pink-500">Jihan</span> 🎀
            </h3>

            <p class="text-gray-600 leading-relaxed mt-5">
              Aku adalah seorang pelajar yang aktif dan memiliki
              semangat untuk terus belajar serta berkembang.
              Aku percaya bahwa setiap proses memberikan pengalaman
              yang berharga.
            </p>

            <p class="text-gray-600 leading-relaxed mt-4">
              Aku juga memiliki jiwa juang dan tangguh dalam
              menghadapi berbagai tantangan. Bagiku, mencoba,
              belajar, dan terus berkembang adalah bagian dari
              perjalanan yang menyenangkan.
            </p>

            <div class="grid grid-cols-2 gap-4 mt-8">

              <div class="cute-card rounded-3xl p-5 text-center">
                <div class="text-3xl">💻</div>
                <h4 class="font-bold mt-2">Web</h4>
                <p class="text-sm text-gray-500">Basic Web Development</p>
              </div>

              <div class="cute-card rounded-3xl p-5 text-center">
                <div class="text-3xl">🎨</div>
                <h4 class="font-bold mt-2">Desain</h4>
                <p class="text-sm text-gray-500">Creative Design</p>
              </div>

            </div>
          </div>

        </div>


        <!-- HOBI -->
        <div class="mt-24 reveal">

          <div class="text-center mb-10">
            <span class="text-pink-500 font-bold">୨୧ MY HOBBIES ୨୧</span>
            <h3 class="text-3xl font-bold mt-2">Hal yang Aku Suka</h3>
          </div>

          <div class="grid md:grid-cols-3 gap-6">

            <div class="cute-card rounded-3xl overflow-hidden gallery-item">
              <div class="h-64 photo-placeholder overflow-hidden">
                <img src="assets/images/hobi-1.jpg"
                     alt="Hobi Jihan 1"
                     class="gallery-img w-full h-full object-cover"
                     onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">

                <div class="hidden w-full h-full items-center justify-center flex-col">
                  <i class="fa-solid fa-image text-4xl"></i>
                  <span class="mt-2">hobi-1.jpg</span>
                </div>
              </div>

              <div class="p-5">
                <h4 class="font-bold text-lg">Hobi Pertama 🎀</h4>
                <p class="text-gray-500 text-sm mt-2">
                  Deskripsi foto hobimu nanti.
                </p>
              </div>
            </div>


            <div class="cute-card rounded-3xl overflow-hidden gallery-item">
              <div class="h-64 photo-placeholder overflow-hidden">
                <img src="assets/images/hobi-2.jpg"
                     alt="Hobi Jihan 2"
                     class="gallery-img w-full h-full object-cover"
                     onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">

                <div class="hidden w-full h-full items-center justify-center flex-col">
                  <i class="fa-solid fa-image text-4xl"></i>
                  <span class="mt-2">hobi-2.jpg</span>
                </div>
              </div>

              <div class="p-5">
                <h4 class="font-bold text-lg">Hobi Kedua 💗</h4>
                <p class="text-gray-500 text-sm mt-2">
                  Deskripsi foto hobimu nanti.
                </p>
              </div>
            </div>


            <div class="cute-card rounded-3xl overflow-hidden gallery-item">
              <div class="h-64 photo-placeholder overflow-hidden">
                <img src="assets/images/hobi-3.jpg"
                     alt="Hobi Jihan 3"
                     class="gallery-img w-full h-full object-cover"
                     onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">

                <div class="hidden w-full h-full items-center justify-center flex-col">
                  <i class="fa-solid fa-image text-4xl"></i>
                  <span class="mt-2">hobi-3.jpg</span>
                </div>
              </div>

              <div class="p-5">
                <h4 class="font-bold text-lg">Hobi Ketiga ✨</h4>
                <p class="text-gray-500 text-sm mt-2">
                  Deskripsi foto hobimu nanti.
                </p>
              </div>
            </div>

          </div>
        </div>

      </div>
    </section>


    <!-- CV -->
    <section id="cv" class="py-24 px-5 bg-white/50">

      <div class="max-w-5xl mx-auto">

        <div class="text-center reveal">
          <span class="text-pink-500 font-bold">✦ MY JOURNEY ✦</span>
          <h2 class="text-4xl font-bold mt-2">Curriculum Vitae</h2>
        </div>

        <div class="relative mt-14">

          <div class="timeline-line"></div>

          <div class="relative pl-12 pb-12 reveal">

            <div class="absolute left-0 top-1 w-8 h-8 rounded-full bg-pink-500 text-white flex items-center justify-center">
              🎓
            </div>

            <div class="cute-card rounded-3xl p-7">
              <span class="text-sm text-pink-500 font-bold">
                PENDIDIKAN
              </span>

              <h3 class="text-2xl font-bold mt-2">
                SMKN 42 Jakarta
              </h3>

              <p class="text-gray-600 mt-3 leading-relaxed">
                Saya adalah seorang pelajar yang aktif,
                berjiwa juang, kreatif, dan tangguh.
                Saya terus berusaha mengembangkan kemampuan
                melalui proses belajar dan berbagai pengalaman.
              </p>
            </div>

          </div>


          <div class="relative pl-12 reveal">

            <div class="absolute left-0 top-1 w-8 h-8 rounded-full bg-pink-300 flex items-center justify-center">
              ✨
            </div>

            <div class="cute-card rounded-3xl p-7">
              <span class="text-sm text-pink-500 font-bold">
                PERSONAL VALUES
              </span>

              <h3 class="text-2xl font-bold mt-2">
                Aktif • Tangguh • Berjiwa Juang
              </h3>

              <div class="flex flex-wrap gap-3 mt-5">
                <span class="px-4 py-2 bg-pink-100 text-pink-600 rounded-full text-sm">
                  Kreatif 🎨
                </span>

                <span class="px-4 py-2 bg-pink-100 text-pink-600 rounded-full text-sm">
                  Aktif 🌸
                </span>

                <span class="px-4 py-2 bg-pink-100 text-pink-600 rounded-full text-sm">
                  Tangguh 💪
                </span>

                <span class="px-4 py-2 bg-pink-100 text-pink-600 rounded-full text-sm">
                  Mau Belajar 📚
                </span>
              </div>

            </div>
          </div>

        </div>

      </div>
    </section>


    <!-- KARYA -->
    <section id="karya" class="py-24 px-5">

      <div class="max-w-7xl mx-auto">

        <div class="text-center reveal">
          <span class="text-pink-500 font-bold">♡ MY WORK ♡</span>
          <h2 class="text-4xl font-bold mt-2">Hasil Karya</h2>
          <p class="text-gray-500 mt-3">
            Beberapa project dan karya kreatifku ✨
          </p>
        </div>

        <!-- Filter -->
        <div class="flex justify-center flex-wrap gap-3 mt-8 reveal">

          <button class="filter-btn pink-btn px-5 py-2 rounded-full"
                  data-filter="all">
            Semua
          </button>

          <button class="filter-btn outline-btn px-5 py-2 rounded-full"
                  data-filter="web">
            Web
          </button>

          <button class="filter-btn outline-btn px-5 py-2 rounded-full"
                  data-filter="desain">
            Desain
          </button>

          <button class="filter-btn outline-btn px-5 py-2 rounded-full"
                  data-filter="foto">
            Foto
          </button>

        </div>


        <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6 mt-10">

          <!-- KARYA 1-9 -->

          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="web">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-1.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Web 1"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-1.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">WEB</span>
              <h3 class="font-bold text-lg mt-1">Project Web 01</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi project.</p>
              <button onclick="openProject('Project Web 01','Karya website pertama Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>


          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="web">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-2.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Web 2"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-2.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">WEB</span>
              <h3 class="font-bold text-lg mt-1">Project Web 02</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi project.</p>
              <button onclick="openProject('Project Web 02','Karya website kedua Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>


          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="web">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-3.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Web 3"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-3.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">WEB</span>
              <h3 class="font-bold text-lg mt-1">Project Web 03</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi project.</p>
              <button onclick="openProject('Project Web 03','Karya website ketiga Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>


          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="desain">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-4.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Desain 1"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-4.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">DESAIN</span>
              <h3 class="font-bold text-lg mt-1">Design Project 01</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi desain.</p>
              <button onclick="openProject('Design Project 01','Karya desain pertama Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>


          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="desain">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-5.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Desain 2"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-5.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">DESAIN</span>
              <h3 class="font-bold text-lg mt-1">Design Project 02</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi desain.</p>
              <button onclick="openProject('Design Project 02','Karya desain kedua Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>


          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="desain">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-6.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Desain 3"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-6.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">DESAIN</span>
              <h3 class="font-bold text-lg mt-1">Design Project 03</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi desain.</p>
              <button onclick="openProject('Design Project 03','Karya desain ketiga Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>


          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="foto">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-7.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Foto 1"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-7.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">FOTO</span>
              <h3 class="font-bold text-lg mt-1">Photography 01</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi foto.</p>
              <button onclick="openProject('Photography 01','Karya fotografi pertama Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>


          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="foto">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-8.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Foto 2"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-8.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">FOTO</span>
              <h3 class="font-bold text-lg mt-1">Photography 02</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi foto.</p>
              <button onclick="openProject('Photography 02','Karya fotografi kedua Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>


          <div class="project cute-card rounded-3xl overflow-hidden"
               data-category="foto">
            <div class="h-60 photo-placeholder overflow-hidden">
              <img src="assets/images/karya-9.jpg"
                   class="w-full h-full object-cover gallery-img"
                   alt="Karya Foto 3"
                   onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
              <div class="hidden w-full h-full items-center justify-center flex-col">
                <i class="fa-solid fa-image text-4xl"></i>
                <span>karya-9.jpg</span>
              </div>
            </div>

            <div class="p-5">
              <span class="text-xs text-pink-500 font-bold">FOTO</span>
              <h3 class="font-bold text-lg mt-1">Photography 03</h3>
              <p class="text-gray-500 text-sm mt-2">Deskripsi foto.</p>
              <button onclick="openProject('Photography 03','Karya fotografi ketiga Jihan.')"
                      class="mt-4 text-pink-600 font-bold text-sm">
                Lihat Detail →
              </button>
            </div>
          </div>

        </div>
      </div>
    </section>


    <!-- FOTO -->
    <section id="foto" class="py-24 px-5 bg-white/50">

      <div class="max-w-7xl mx-auto">

        <div class="text-center reveal">
          <span class="text-pink-500 font-bold">📸 MY MEMORIES 📸</span>
          <h2 class="text-4xl font-bold mt-2">Galeri Foto</h2>
          <p class="text-gray-500 mt-3">
            Klik foto untuk memperbesar ✨
          </p>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-3 gap-4 mt-12">

          <!-- Galeri menggunakan foto hobi + karya -->
          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/hobi-1.jpg')">
            <img src="assets/images/hobi-1.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 1">
          </div>

          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/hobi-2.jpg')">
            <img src="assets/images/hobi-2.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 2">
          </div>

          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/hobi-3.jpg')">
            <img src="assets/images/hobi-3.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 3">
          </div>

          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/karya-1.jpg')">
            <img src="assets/images/karya-1.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 4">
          </div>

          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/karya-2.jpg')">
            <img src="assets/images/karya-2.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 5">
          </div>

          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/karya-3.jpg')">
            <img src="assets/images/karya-3.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 6">
          </div>

          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/karya-4.jpg')">
            <img src="assets/images/karya-4.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 7">
          </div>

          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/karya-5.jpg')">
            <img src="assets/images/karya-5.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 8">
          </div>

          <div class="gallery-item h-64 rounded-3xl overflow-hidden photo-placeholder cursor-pointer"
               onclick="zoomImage('assets/images/karya-6.jpg')">
            <img src="assets/images/karya-6.jpg"
                 class="gallery-img w-full h-full object-cover"
                 alt="Galeri 9">
          </div>

        </div>
      </div>
    </section>


    <!-- ARTIKEL -->
    <section id="artikel" class="py-24 px-5">

      <div class="max-w-7xl mx-auto">

        <div class="text-center reveal">
          <span class="text-pink-500 font-bold">📝 MY STORIES 📝</span>
          <h2 class="text-4xl font-bold mt-2">Artikel</h2>
        </div>

        <div class="grid md:grid-cols-3 gap-6 mt-12">

          <article class="cute-card rounded-3xl p-6 reveal">
            <div class="text-4xl">🌷</div>
            <p class="text-sm text-pink-500 font-bold mt-5">
              09 September 2026
            </p>
            <h3 class="font-bold text-xl mt-2">
              Perjalanan Menjadi Pelajar Aktif
            </h3>
            <p class="text-gray-500 mt-3 text-sm leading-relaxed">
              Cerita tentang pengalaman belajar,
              berkembang, dan mencoba hal baru.
            </p>
            <button onclick="openProject('Perjalanan Menjadi Pelajar Aktif','Artikel tentang perjalanan dan pengalaman Jihan sebagai pelajar.')"
                    class="mt-5 text-pink-600 font-bold">
              Baca Selengkapnya →
            </button>
          </article>


          <article class="cute-card rounded-3xl p-6 reveal">
            <div class="text-4xl">💻</div>
            <p class="text-sm text-pink-500 font-bold mt-5">
              01 September 2026
            </p>
            <h3 class="font-bold text-xl mt-2">
              Belajar Membuat Website
            </h3>
            <p class="text-gray-500 mt-3 text-sm leading-relaxed">
              Pengalaman mengenal dunia website dan
              kreativitas digital.
            </p>
            <button onclick="openProject('Belajar Membuat Website','Artikel tentang pengalaman belajar membuat website.')"
                    class="mt-5 text-pink-600 font-bold">
              Baca Selengkapnya →
            </button>
          </article>


          <article class="cute-card rounded-3xl p-6 reveal">
            <div class="text-4xl">✨</div>
            <p class="text-sm text-pink-500 font-bold mt-5">
              25 Agustus 2026
            </p>
            <h3 class="font-bold text-xl mt-2">
              Berani Mencoba Hal Baru
            </h3>
            <p class="text-gray-500 mt-3 text-sm leading-relaxed">
              Mengapa mencoba hal baru dapat memberikan
              pengalaman berharga.
            </p>
            <button onclick="openProject('Berani Mencoba Hal Baru','Artikel tentang keberanian mencoba pengalaman baru.')"
                    class="mt-5 text-pink-600 font-bold">
              Baca Selengkapnya →
            </button>
          </article>

        </div>

      </div>
    </section>


    <!-- SOSIAL -->
    <section id="sosial" class="py-24 px-5 bg-white/50">

      <div class="max-w-5xl mx-auto text-center">

        <div class="reveal">
          <span class="text-pink-500 font-bold">♡ LET'S CONNECT ♡</span>
          <h2 class="text-4xl font-bold mt-2">
            Media Sosial
          </h2>

          <p class="text-gray-500 mt-3">
            Yuk terhubung denganku di media sosial! 🎀
          </p>
        </div>


        <div class="grid sm:grid-cols-2 gap-5 mt-12">

          <!-- Link 1 -->
          <a href="https://www.instagram.com/xwlzz_yannsj/"
             target="_blank"
             rel="noopener noreferrer"
             class="social-btn cute-card rounded-3xl p-6 flex items-center gap-5 text-left">

            <div class="w-14 h-14 rounded-2xl bg-pink-100 text-pink-500 flex items-center justify-center text-2xl">
              <i class="fa-brands fa-instagram"></i>
            </div>

            <div>
              <h3 class="font-bold text-lg">Instagram</h3>
              <p class="text-gray-500">@xwlzz_yannsj</p>
            </div>

            <i class="fa-solid fa-arrow-up-right-from-square ml-auto text-pink-400"></i>
          </a>


          <!-- Link 2 -->
          <a href="https://www.instagram.com/iluv_an0/"
             target="_blank"
             rel="noopener noreferrer"
             class="social-btn cute-card rounded-3xl p-6 flex items-center gap-5 text-left">

            <div class="w-14 h-14 rounded-2xl bg-pink-100 text-pink-500 flex items-center justify-center text-2xl">
              <i class="fa-brands fa-instagram"></i>
            </div>

            <div>
              <h3 class="font-bold text-lg">Instagram</h3>
              <p class="text-gray-500">@iluv_an0</p>
            </div>

            <i class="fa-solid fa-arrow-up-right-from-square ml-auto text-pink-400"></i>
          </a>

        </div>

      </div>
    </section>


    <!-- KONTAK -->
    <section id="kontak" class="py-24 px-5">

      <div class="max-w-7xl mx-auto">

        <div class="text-center reveal">
          <span class="text-pink-500 font-bold">💌 CONTACT ME 💌</span>
          <h2 class="text-4xl font-bold mt-2">
            Hubungi Saya
          </h2>
        </div>


        <div class="grid lg:grid-cols-2 gap-8 mt-12">

          <!-- Form -->
          <div class="cute-card rounded-[35px] p-7 reveal">

            <h3 class="text-2xl font-bold">
              Kirim Pesan 💗
            </h3>

            <form onsubmit="sendMessage(event)" class="mt-7 space-y-5">

              <div>
                <label class="font-semibold text-sm">
                  Nama
                </label>

                <input id="name"
                       type="text"
                       required
                       placeholder="Nama kamu"
                       class="w-full mt-2 px-5 py-3 rounded-2xl border border-pink-100 outline-none focus:border-pink-400 bg-white">
              </div>


              <div>
                <label class="font-semibold text-sm">
                  Email
                </label>

                <input id="email"
                       type="email"
                       required
                       placeholder="email@example.com"
                       class="w-full mt-2 px-5 py-3 rounded-2xl border border-pink-100 outline-none focus:border-pink-400 bg-white">
              </div>


              <div>
                <label class="font-semibold text-sm">
                  Pesan
                </label>

                <textarea id="message"
                          rows="5"
                          required
                          placeholder="Tulis pesan..."
                          class="w-full mt-2 px-5 py-3 rounded-2xl border border-pink-100 outline-none focus:border-pink-400 bg-white"></textarea>
              </div>


              <button type="submit"
                      class="pink-btn w-full py-3 rounded-full font-bold">
                💌 Kirim Pesan
              </button>

            </form>

          </div>


          <!-- Info -->
          <div class="space-y-5 reveal">

            <div class="cute-card rounded-3xl p-6 flex gap-5">
              <div class="w-12 h-12 bg-pink-100 rounded-2xl flex items-center justify-center text-pink-500">
                <i class="fa-solid fa-location-dot"></i>
              </div>

              <div>
                <h3 class="font-bold">Alamat</h3>
                <p class="text-gray-500 mt-1">
                  [ISI ALAMAT DI SINI]
                </p>
              </div>
            </div>


            <div class="cute-card rounded-3xl p-6 flex gap-5">
              <div class="w-12 h-12 bg-pink-100 rounded-2xl flex items-center justify-center text-pink-500">
                <i class="fa-solid fa-envelope"></i>
              </div>

              <div>
                <h3 class="font-bold">Email</h3>

                <a href="mailto:[EMAIL-KAMU]"
                   class="text-pink-500 hover:underline">
                  [EMAIL-KAMU]
                </a>
              </div>
            </div>


            <div class="cute-card rounded-3xl p-6 flex gap-5">
              <div class="w-12 h-12 bg-pink-100 rounded-2xl flex items-center justify-center text-pink-500">
                <i class="fa-brands fa-whatsapp"></i>
              </div>

              <div>
                <h3 class="font-bold">WhatsApp</h3>

                <a href="https://wa.me/[NOMOR-WA]"
                   target="_blank"
                   rel="noopener noreferrer"
                   class="text-pink-500 hover:underline">
                  Chat WhatsApp
                </a>
              </div>
            </div>


            <!-- Google Maps -->
            <div class="cute-card rounded-3xl overflow-hidden h-72">

              <iframe
                title="Google Maps"
                src="https://www.google.com/maps?q=Jakarta%2C%20Indonesia&output=embed"
                width="100%"
                height="100%"
                style="border:0;"
                loading="lazy"
                allowfullscreen>
              </iframe>

            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- TESTIMONI -->
    <section id="testimoni" class="py-24 px-5 bg-white/50">

      <div class="max-w-4xl mx-auto text-center">

        <div class="reveal">
          <span class="text-pink-500 font-bold">💗 TESTIMONIAL 💗</span>
          <h2 class="text-4xl font-bold mt-2">
            Kata Mereka
          </h2>
        </div>


        <div class="cute-card rounded-[35px] p-8 mt-12 reveal">

          <div id="testimonialContent">

            <div class="text-5xl mb-5">💗</div>

            <p id="testimonialText"
               class="text-lg text-gray-600 italic leading-relaxed">
              "Jihan adalah pribadi yang aktif,
              kreatif, dan memiliki semangat yang luar biasa."
            </p>

            <h3 id="testimonialName"
                class="font-bold text-xl mt-6">
              Nama Testimoni
            </h3>

            <p id="testimonialRole"
               class="text-pink-500 text-sm mt-1">
              Pelajar / Teman
            </p>

          </div>


          <div class="flex justify-center gap-3 mt-8">

            <button onclick="previousTestimonial()"
                    class="w-11 h-11 rounded-full bg-pink-100 text-pink-500">
              ←
            </button>

            <button onclick="nextTestimonial()"
                    class="w-11 h-11 rounded-full bg-pink-100 text-pink-500">
              →
            </button>

          </div>

        </div>

      </div>
    </section>

  </main>


  <!-- FOOTER -->
  <footer class="py-10 px-5">

    <div class="max-w-7xl mx-auto text-center">

      <div class="cute-font text-2xl text-pink-500">
        Jihan Maharani Putri 🎀
      </div>

      <p class="text-gray-500 mt-3">
        Dibuat dengan ♡ dan sedikit glitter ✨
      </p>

      <div class="flex justify-center gap-4 mt-5 text-pink-400">
        <span>♡</span>
        <span>✦</span>
        <span>୨୧</span>
        <span>✧</span>
        <span>♡</span>
      </div>

      <p class="text-sm text-gray-400 mt-6">
        © 2026 Jihan Maharani Putri. All rights reserved.
      </p>

    </div>

  </footer>


  <!-- MUSIC PLAYER -->
  <div class="music-player">

    <audio id="bgMusic" loop>
      <source src="assets/music/lagu.mp3" type="audio/mpeg">
    </audio>

    <button id="musicBtn"
            onclick="toggleMusic()"
            class="w-14 h-14 rounded-full pink-btn flex items-center justify-center text-lg"
            title="Putar musik">

      <i id="musicIcon" class="fa-solid fa-music"></i>

    </button>

  </div>


  <!-- MODAL GALLERY -->
  <div id="galleryModal"
       class="hidden fixed inset-0 z-[9998] items-center justify-center p-5">

    <button onclick="closeZoom()"
            class="absolute top-6 right-6 text-white text-3xl">
      ×
    </button>

    <img id="zoomedImage"
         src=""
         alt="Foto diperbesar"
         class="max-w-full max-h-[90vh] rounded-3xl shadow-2xl">
  </div>


  <!-- PROJECT MODAL -->
  <div id="projectModal"
       class="hidden fixed inset-0 z-[9997] bg-black/50 backdrop-blur-sm items-center justify-center p-5">

    <div class="cute-card max-w-lg w-full rounded-[35px] p-8 relative">

      <button onclick="closeProject()"
              class="absolute top-5 right-6 text-2xl text-pink-500">
        ×
      </button>

      <div class="text-4xl">✨</div>

      <h3 id="projectTitle"
          class="text-2xl font-bold mt-4">
      </h3>

      <p id="projectDescription"
         class="text-gray-600 mt-4 leading-relaxed">
      </p>

      <button onclick="closeProject()"
              class="pink-btn px-6 py-3 rounded-full mt-6 font-bold">
        Tutup ♡
      </button>

    </div>

  </div>


  <script>

    /* =========================
       MOBILE MENU
    ========================= */

    const menuBtn = document.getElementById("menuBtn");
    const mobileMenu = document.getElementById("mobileMenu");

    menuBtn.addEventListener("click", () => {
      mobileMenu.classList.toggle("show");
    });

    document.querySelectorAll("#mobileMenu a").forEach(link => {
      link.addEventListener("click", () => {
        mobileMenu.classList.remove("show");
      });
    });


    /* =========================
       SCROLL REVEAL
    ========================= */

    const revealElements = document.querySelectorAll(".reveal");

    const observer = new IntersectionObserver(
      entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add("active");
          }
        });
      },
      {
        threshold: 0.12
      }
    );

    revealElements.forEach(element => {
      observer.observe(element);
    });


    /* =========================
       PROJECT FILTER
    ========================= */

    const filterButtons = document.querySelectorAll(".filter-btn");
    const projects = document.querySelectorAll(".project");

    filterButtons.forEach(button => {

      button.addEventListener("click", () => {

        const filter = button.dataset.filter;

        filterButtons.forEach(btn => {
          btn.classList.remove("pink-btn");
          btn.classList.add("outline-btn");
        });

        button.classList.remove("outline-btn");
        button.classList.add("pink-btn");

        projects.forEach(project => {

          if (
            filter === "all" ||
            project.dataset.category === filter
          ) {
            project.style.display = "block";
          } else {
            project.style.display = "none";
          }

        });

      });

    });


    /* =========================
       IMAGE ZOOM
    ========================= */

    const galleryModal = document.getElementById("galleryModal");
    const zoomedImage = document.getElementById("zoomedImage");

    function zoomImage(image) {

      zoomedImage.src = image;

      galleryModal.classList.remove("hidden");
      galleryModal.classList.add("flex");

    }

    function closeZoom() {

      galleryModal.classList.add("hidden");
      galleryModal.classList.remove("flex");

      zoomedImage.src = "";

    }


    galleryModal.addEventListener("click", event => {

      if (event.target === galleryModal) {
        closeZoom();
      }

    });


    /* =========================
       PROJECT MODAL
    ========================= */

    const projectModal = document.getElementById("projectModal");

    function openProject(title, description) {

      document.getElementById("projectTitle").textContent = title;
      document.getElementById("projectDescription").textContent = description;

      projectModal.classList.remove("hidden");
      projectModal.classList.add("flex");

    }

    function closeProject() {

      projectModal.classList.add("hidden");
      projectModal.classList.remove("flex");

    }


    /* =========================
       MUSIC
    ========================= */

    const music = document.getElementById("bgMusic");
    const musicIcon = document.getElementById("musicIcon");

    function toggleMusic() {

      if (music.paused) {

        music.play()
          .then(() => {
            musicIcon.className = "fa-solid fa-pause";
          })
          .catch(() => {
            alert("Tambahkan file lagu.mp3 ke folder assets/music/");
          });

      } else {

        music.pause();
        musicIcon.className = "fa-solid fa-music";

      }

    }


    /* =========================
       CONTACT FORM
    ========================= */

    function sendMessage(event) {

      event.preventDefault();

      const name = document.getElementById("name").value;

      alert(
        "Terima kasih, " +
        name +
        "! 💗\n\nForm berhasil diisi. Untuk website statis, pesan perlu dihubungkan ke layanan form/email agar benar-benar terkirim."
      );

    }


    /* =========================
       TESTIMONIAL SLIDER
    ========================= */

    const testimonials = [

      {
        text: "Jihan adalah pribadi yang aktif, kreatif, dan memiliki semangat yang luar biasa.",
        name: "Testimoni 01",
        role: "Teman"
      },

      {
        text: "Jihan selalu berusaha menyelesaikan sesuatu dengan penuh tanggung jawab dan semangat.",
        name: "Testimoni 02",
        role: "Teman"
      },

      {
        text: "Pribadi yang tangguh dan tidak mudah menyerah ketika menghadapi tantangan.",
        name: "Testimoni 03",
        role: "Teman"
      }

    ];

    let testimonialIndex = 0;

    function showTestimonial(index) {

      const testimonial = testimonials[index];

      document.getElementById("testimonialText").textContent =
        `"${testimonial.text}"`;

      document.getElementById("testimonialName").textContent =
        testimonial.name;

      document.getElementById("testimonialRole").textContent =
        testimonial.role;

    }


    function nextTestimonial() {

      testimonialIndex++;

      if (testimonialIndex >= testimonials.length) {
        testimonialIndex = 0;
      }

      showTestimonial(testimonialIndex);

    }


    function previousTestimonial() {

      testimonialIndex--;

      if (testimonialIndex < 0) {
        testimonialIndex = testimonials.length - 1;
      }

      showTestimonial(testimonialIndex);

    }


    /* Auto slider */

    setInterval(() => {
      nextTestimonial();
    }, 5000);


    /* ESC untuk menutup modal */

    document.addEventListener("keydown", event => {

      if (event.key === "Escape") {
        closeZoom();
        closeProject();
      }

    });

  </script>

</body>
</html>
```
