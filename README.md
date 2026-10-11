<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>CV | Varel Lucky Kurniawan</title>

    <style>

        /* =========================
           RESET
        ========================= */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #f5f7fb;
            color: #172033;
            line-height: 1.7;
        }

        .container {
            width: 90%;
            max-width: 1100px;
            margin: auto;
        }


        /* =========================
           NAVBAR
        ========================= */

        .navbar {
            position: sticky;
            top: 0;
            z-index: 1000;

            background: #0f172a;

            padding: 18px 0;
        }

        .nav-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            color: white;
            font-size: 25px;
        }

        .logo span {
            color: #3b82f6;
        }

        .nav-menu {
            list-style: none;

            display: flex;
            gap: 30px;
        }

        .nav-menu a {
            color: #dbeafe;
            text-decoration: none;
            font-size: 14px;

            transition: 0.3s;
        }

        .nav-menu a:hover {
            color: #60a5fa;
        }


        /* =========================
           HERO
        ========================= */

        .hero {
            min-height: 650px;

            display: flex;
            align-items: center;

            background:
                radial-gradient(
                    circle at 80% 20%,
                    #1d4ed8 0,
                    transparent 30%
                ),
                #0f172a;

            color: white;
        }

        .hero-content {
            display: grid;

            grid-template-columns: 1.3fr 0.7fr;

            align-items: center;

            gap: 70px;
        }

        .small-title {
            color: #60a5fa;

            font-size: 14px;
            font-weight: bold;

            letter-spacing: 5px;

            margin-bottom: 15px;
        }

        .hero h1 {
            font-size: 65px;

            line-height: 1.05;

            margin-bottom: 25px;
        }

        .hero h1 span {
            color: #60a5fa;
        }

        .description {
            max-width: 600px;

            color: #cbd5e1;

            font-size: 17px;

            margin-bottom: 35px;
        }

        .button {
            display: inline-block;

            padding: 13px 25px;

            border-radius: 8px;

            background: #2563eb;

            color: white;

            text-decoration: none;

            font-weight: bold;

            transition: 0.3s;
        }

        .button:hover {
            background: #3b82f6;
            transform: translateY(-3px);
        }


        /* =========================
           PROFILE CARD
        ========================= */

        .profile-card {
            text-align: center;

            background: rgba(255, 255, 255, 0.08);

            border: 1px solid rgba(255, 255, 255, 0.15);

            border-radius: 20px;

            padding: 40px 25px;

            backdrop-filter: blur(10px);
        }

        .profile-circle {
            width: 130px;
            height: 130px;

            margin: 0 auto 20px;

            display: flex;
            align-items: center;
            justify-content: center;

            border-radius: 50%;

            background: #2563eb;

            border: 5px solid #60a5fa;

            font-size: 40px;

            font-weight: bold;
        }

        .profile-card h2 {
            font-size: 23px;

            margin-bottom: 5px;
        }

        .profile-card > p {
            color: #94a3b8;
        }

        .profile-info {
            display: flex;

            justify-content: space-around;

            margin-top: 30px;

            padding-top: 25px;

            border-top: 1px solid rgba(255, 255, 255, 0.15);
        }

        .profile-info div {
            display: flex;

            flex-direction: column;
        }

        .profile-info strong {
            font-size: 20px;
            color: #60a5fa;
        }

        .profile-info span {
            color: #94a3b8;
            font-size: 12px;
        }


        /* =========================
           SECTION
        ========================= */

        .section {
            padding: 90px 0;
        }

        .section-title {
            margin-bottom: 45px;
        }

        .section-title p {
            color: #2563eb;

            font-size: 13px;

            font-weight: bold;

            letter-spacing: 4px;

            margin-bottom: 5px;
        }

        .section-title h2 {
            font-size: 38px;
        }


        /* =========================
           ABOUT
        ========================= */

        .about {
            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 60px;

            align-items: start;
        }

        .about-text p {
            margin-bottom: 20px;

            color: #64748b;
        }

        .about-box {
            background: white;

            padding: 30px;

            border-radius: 15px;

            box-shadow:
                0 10px 30px rgba(15, 23, 42, 0.08);
        }

        .data {
            display: flex;

            justify-content: space-between;

            gap: 20px;

            padding: 15px 0;

            border-bottom: 1px solid #e2e8f0;
        }

        .data:last-child {
            border-bottom: none;
        }

        .data span {
            color: #64748b;
        }

        .data strong {
            text-align: right;
        }


        /* =========================
           PENDIDIKAN
        ========================= */

        .dark-section {
            background: #0f172a;

            color: white;
        }

        .dark-section .section-title h2 {
            color: white;
        }

        .education-card {
            display: flex;

            gap: 25px;

            padding: 35px;

            background: #172033;

            border: 1px solid #26334d;

            border-radius: 15px;
        }

        .education-icon {
            font-size: 35px;
        }

        .education-card .year {
            color: #60a5fa;

            font-size: 13px;

            font-weight: bold;

            text-transform: uppercase;
        }

        .education-card h3 {
            margin: 5px 0;

            font-size: 24px;
        }

        .education-card p {
            color: #94a3b8;
        }

        .education-description {
            margin-top: 15px;
        }


        /* =========================
           PENGALAMAN
        ========================= */

        .experience-grid {
            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 25px;
        }

        .experience-card {
            background: white;

            padding: 35px;

            border-radius: 15px;

            border: 1px solid #e2e8f0;

            transition: 0.3s;
        }

        .experience-card:hover {
            transform: translateY(-7px);

            box-shadow:
                0 15px 30px rgba(15, 23, 42, 0.1);
        }

        .number {
            color: #2563eb;

            font-size: 13px;

            font-weight: bold;

            margin-bottom: 20px;
        }

        .experience-card h3 {
            font-size: 23px;

            margin-bottom: 15px;
        }

        .experience-card p {
            color: #64748b;

            margin-bottom: 20px;
        }

        .tag {
            display: inline-block;

            padding: 6px 12px;

            background: #dbeafe;

            color: #2563eb;

            border-radius: 20px;

            font-size: 12px;

            font-weight: bold;
        }


        /* =========================
           KEAHLIAN
        ========================= */

        .skills-section {
            background: #eef2ff;
        }

        .skills {
            display: grid;

            grid-template-columns:
                repeat(4, 1fr);

            gap: 20px;
        }

        .skill {
            background: white;

            padding: 30px;

            border-radius: 15px;

            transition: 0.3s;
        }

        .skill:hover {
            transform: translateY(-5px);
        }

        .skill > span {
            color: #2563eb;

            font-weight: bold;

            font-size: 13px;
        }

        .skill h3 {
            margin: 15px 0 8px;
        }

        .skill p {
            color: #64748b;

            font-size: 14px;
        }


        /* =========================
           MOTTO
        ========================= */

        .motto {
            padding: 100px 0;

            text-align: center;

            background: #2563eb;

            color: white;
        }

        .motto-label {
            font-size: 13px;

            letter-spacing: 5px;

            font-weight: bold;

            opacity: 0.8;

            margin-bottom: 15px;
        }

        .motto h2 {
            font-size: 45px;

            line-height: 1.2;

            margin-bottom: 20px;
        }

        .motto p:last-child {
            opacity: 0.8;
        }


        /* =========================
           FOOTER
        ========================= */

        footer {
            padding: 40px 0;

            text-align: center;

            background: #020617;

            color: white;
        }

        footer h3 {
            font-size: 25px;

            margin-bottom: 5px;
        }

        footer span {
            color: #3b82f6;
        }

        footer p {
            color: #94a3b8;
        }

        .copyright {
            margin-top: 20px;

            font-size: 12px;
        }


        /* =========================
           RESPONSIVE
        ========================= */

        @media (max-width: 850px) {

            .hero-content {
                grid-template-columns: 1fr;

                gap: 40px;

                padding: 70px 0;
            }

            .hero h1 {
                font-size: 50px;
            }

            .profile-card {
                max-width: 500px;

                width: 100%;

                margin: auto;
            }

            .about {
                grid-template-columns: 1fr;
            }

            .skills {
                grid-template-columns: 1fr 1fr;
            }
        }


        @media (max-width: 600px) {

            .nav-menu {
                display: none;
            }

            .hero h1 {
                font-size: 40px;
            }

            .section {
                padding: 65px 0;
            }

            .section-title h2 {
                font-size: 30px;
            }

            .experience-grid {
                grid-template-columns: 1fr;
            }

            .skills {
                grid-template-columns: 1fr;
            }

            .education-card {
                flex-direction: column;
            }

            .data {
                flex-direction: column;

                gap: 3px;
            }

            .data strong {
                text-align: left;
            }

            .motto h2 {
                font-size: 32px;
            }
        }

    </style>
</head>


<body>

    <!-- NAVBAR -->
    <nav class="navbar">

        <div class="container nav-content">

            <h2 class="logo">
                Varel<span>.</span>
            </h2>

            <ul class="nav-menu">

                <li>
                    <a href="#tentang">Tentang</a>
                </li>

                <li>
                    <a href="#pendidikan">Pendidikan</a>
                </li>

                <li>
                    <a href="#pengalaman">Pengalaman</a>
                </li>

                <li>
                    <a href="#keahlian">Keahlian</a>
                </li>

            </ul>

        </div>

    </nav>


    <!-- HERO -->
    <section class="hero">

        <div class="container hero-content">

            <div class="hero-text">

                <p class="small-title">
                    HALO, SAYA
                </p>

                <h1>
                    Varel Lucky<br>
                    <span>Kurniawan</span>
                </h1>

                <p class="description">
                    Pelajar SMK jurusan Teknik Komputer dan Jaringan
                    yang memiliki minat di bidang informatika,
                    jaringan komputer, dan Artificial Intelligence.
                </p>

                <a href="#tentang" class="button">
                    Lihat Profil
                </a>

            </div>


            <div class="profile-card">

                <div class="profile-circle">
                    VK
                </div>

                <h2>
                    Varel Lucky Kurniawan
                </h2>

                <p>
                    Pelajar SMK
                </p>

                <div class="profile-info">

                    <div>
                        <strong>17</strong>
                        <span>Umur</span>
                    </div>

                    <div>
                        <strong>11</strong>
                        <span>Kelas</span>
                    </div>

                    <div>
                        <strong>TKJ</strong>
                        <span>Jurusan</span>
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- TENTANG -->
    <section id="tentang" class="section">

        <div class="container">

            <div class="section-title">

                <p>
                    PROFILE
                </p>

                <h2>
                    Tentang Saya
                </h2>

            </div>


            <div class="about">

                <div class="about-text">

                    <p>
                        Saya adalah
                        <strong>Varel Lucky Kurniawan</strong>,
                        seorang pelajar berusia 17 tahun yang sedang
                        menempuh pendidikan SMK.
                    </p>

                    <p>
                        Saat ini saya duduk di kelas
                        <strong>11 TKJ 2</strong> dengan jurusan
                        <strong>Teknik Komputer dan Jaringan</strong>.
                    </p>

                    <p>
                        Saya memiliki ketertarikan terhadap dunia
                        teknologi, khususnya informatika, jaringan
                        komputer, pemrograman, dan kecerdasan buatan.
                    </p>

                </div>


                <div class="about-box">

                    <div class="data">

                        <span>Nama</span>

                        <strong>
                            Varel Lucky Kurniawan
                        </strong>

                    </div>


                    <div class="data">

                        <span>Umur</span>

                        <strong>
                            17 Tahun
                        </strong>

                    </div>


                    <div class="data">

                        <span>Status</span>

                        <strong>
                            Pelajar
                        </strong>

                    </div>


                    <div class="data">

                        <span>Kelas</span>

                        <strong>
                            11 TKJ 2
                        </strong>

                    </div>


                    <div class="data">

                        <span>Jurusan</span>

                        <strong>
                            Teknik Komputer dan Jaringan
                        </strong>

                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- PENDIDIKAN -->
    <section id="pendidikan" class="section dark-section">

        <div class="container">

            <div class="section-title">

                <p>
                    EDUCATION
                </p>

                <h2>
                    Pendidikan
                </h2>

            </div>


            <div class="education-card">

                <div class="education-icon">
                    🎓
                </div>

                <div>

                    <p class="year">
                        Saat Ini
                    </p>

                    <h3>
                        SMK - Teknik Komputer dan Jaringan
                    </h3>

                    <p>
                        Kelas 11 TKJ 2
                    </p>

                    <p class="education-description">
                        Mempelajari teknologi komputer, jaringan
                        komputer, sistem komputer, perangkat jaringan,
                        serta teknologi informasi.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- PENGALAMAN -->
    <section id="pengalaman" class="section">

        <div class="container">

            <div class="section-title">

                <p>
                    EXPERIENCE
                </p>

                <h2>
                    Pengalaman & Prestasi
                </h2>

            </div>


            <div class="experience-grid">


                <div class="experience-card">

                    <div class="number">
                        01
                    </div>

                    <h3>
                        Olimpiade Informatika
                    </h3>

                    <p>
                        Mengikuti Olimpiade Informatika sebagai pengalaman
                        untuk mengembangkan kemampuan berpikir logis,
                        pemrograman, dan pemecahan masalah.
                    </p>

                    <span class="tag">
                        Informatika
                    </span>

                </div>


                <div class="experience-card">

                    <div class="number">
                        02
                    </div>

                    <h3>
                        Olimpiade AI
                    </h3>

                    <p>
                        Mengikuti Olimpiade Artificial Intelligence (AI)
                        untuk menambah pengalaman dan wawasan dalam
                        bidang kecerdasan buatan.
                    </p>

                    <span class="tag">
                        Artificial Intelligence
                    </span>

                </div>


            </div>

        </div>

    </section>


    <!-- KEAHLIAN -->
    <section id="keahlian" class="section skills-section">

        <div class="container">

            <div class="section-title">

                <p>
                    SKILLS
                </p>

                <h2>
                    Keahlian
                </h2>

            </div>


            <div class="skills">


                <div class="skill">

                    <span>01</span>

                    <h3>
                        Jaringan Komputer
                    </h3>

                    <p>
                        Dasar-dasar jaringan dan teknologi komputer.
                    </p>

                </div>


                <div class="skill">

                    <span>02</span>

                    <h3>
                        Informatika
                    </h3>

                    <p>
                        Logika komputer dan pemecahan masalah.
                    </p>

                </div>


                <div class="skill">

                    <span>03</span>

                    <h3>
                        Artificial Intelligence
                    </h3>

                    <p>
                        Pengetahuan dasar mengenai teknologi AI.
                    </p>

                </div>


                <div class="skill">

                    <span>04</span>

                    <h3>
                        Problem Solving
                    </h3>

                    <p>
                        Menganalisis dan menyelesaikan masalah.
                    </p>

                </div>


            </div>

        </div>

    </section>


    <!-- MOTTO -->
    <section class="motto">

        <div class="container">

            <p class="motto-label">
                MOTTO HIDUP
            </p>

            <h2>
                "Belum dicoba kalau<br>
                belum nyoba."
            </h2>

            <p>
                Berani mencoba adalah langkah pertama untuk berkembang.
            </p>

        </div>

    </section>


    <!-- FOOTER -->
    <footer>

        <div class="container">

            <h3>
                Varel<span>.</span>
            </h3>

            <p>
                CV Personal Website
            </p>

            <p class="copyright">
                © 2026 Varel Lucky Kurniawan.
                All Rights Reserved.
            </p>

        </div>

    </footer>

</body>
</html>
