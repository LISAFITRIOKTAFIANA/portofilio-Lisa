<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portofolio Lisa</title>
  <style>
    body {
      margin: 0;
      font-family: 'Times New Roman', Times, serif;
      background-color: #2a003f; /* ungu tua */
      color: white;
      overflow: hidden; /* biar ga bisa scroll */
    }

    /* ===== HEADER SELALU DI ATAS ===== */
    header {
      background-color: #3b005a;
      padding: 15px 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
    }

    header nav a {
      color: white;
      text-decoration: none;
      margin: 0 15px;
      font-size: 18px;
    }

    header nav a:hover {
      text-decoration: underline;
    }

    /* ===== KONTEN SETIAP MENU ===== */
    .section {
      display: none;
      height: calc(100vh - 70px);
      text-align: center;
      padding: 100px 20px 50px;
    }

    .section.active {
      display: block;
    }

    /* foto bulat */
    .profile-pic {
      width: 220px;
      height: 220px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 20px;
    }

    .section h1 {
      font-size: 40px;
      font-family: Arial, Helvetica, sans-serif;
      margin-bottom: 20px;
    }

    .section p {
      font-size: 15px;
      font-family: Verdana, Geneva, Tahoma, sans-serif;
    }

    .btn {
      display: inline-block;
      margin-top: 20px;
      padding: 12px 25px;
      font-size: 18px;
      background-color: rgb(162, 0, 255);
      color: black;
      font-weight: bold;
      border-radius: 10px;
      text-decoration: none;
      transition: 0.3s;
    }

    .btn:hover {
      background-color: #00bcd4;
    }

    /* ===== SERTIFIKAT ===== */
    .sertifikat-menu button {
      background-color: #6a1b9a;
      color: white;
      border: none;
      padding: 10px 18px;
      margin: 5px;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
    }

    .sertifikat-menu button:hover {
      background-color: #8e24aa;
    }

    .sertifikat-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      grid-gap: 20px;
      justify-items: center;
      margin-top: 20px;
    }

    .sertifikat-item img {
      width: 100%;
      max-width: 400px;
      border-radius: 12px;
      box-shadow: 0px 4px 10px rgba(0,0,0,0.3);
    }
  </style>
</head>
<body>
  <header>
    <nav>
      <a href="#home" onclick="showSection('home')">Home</a>
      <a href="#profil" onclick="showSection('profil')">Profil Diri</a>
      <a href="#pengalaman" onclick="showSection('pengalaman')">Pengalaman</a>
      <a href="#skill" onclick="showSection('skill')">Skill</a>
      <a href="#sertifikat" onclick="showSection('sertifikat')">Sertifikat</a>
      <a href="#kontak" onclick="showSection('kontak')">Kontak</a>
    </nav>
  </header>

  <!-- HOME -->
  <section id="home" class="section active">
    <h1>Haii, Kenalan Yukk!!</h1>
    <img src="profile.jpg" alt="Foto Lisa" class="profile-pic">
    <p>Aku Lisa, dan ini sedikit cerita tentang aku,
        skill-ku, dan perjalanan belajarku di dunia teknologi.<br>
        Semoga portofolio ini bisa mengenalkan aku lebih baik.🚀</p>
  </section>

  <!-- PROFIL DIRI -->
  <section id="profil" class="section">
    <h2>Profil Diri</h2>
    <img src="profile2.jpg" alt="Foto Profil Lisa" class="profile-pic">
    <p>
      Halo! Aku <b>Lisa Fitri Oktafiana</b>, seorang siswi SMKN 1 NGLEGOK jurusan Teknik Komputer dan Jaringan (TKJ).<br>
      Aku suka belajar hal baru, terutama yang berkaitan dengan jaringan komputer dan server.<br>
      Saat ini, aku mengembangkan skill melalui project sekolah, pelatihan online, dan sertifikasi.<br><br>
      Aku percaya bahwa belajar tidak harus langsung hebat, tapi harus terus konsisten 💪✨
    </p>
    <a href="CV.Lisa Fitri2.pdf" class="btn" download>Unduh CV</a>
  </section>

  <!-- PENGALAMAN -->
  <section id="pengalaman" class="section">
    <h2>Pengalaman</h2>
    <p>
      Mengikuti bootcamp networking dan berhasil mendapatkan sertifikat MTCNA <br>
      melakukan instalasi dan konfigurasi Debian Server<br>
      Merancang topologi jaringan komputer dengan Cisco Packet Tracer<br>
      Mengikuti lomba Invention jaringan di sekolah<br>
      Mengkonfigurasi router Mikrotik untuk pengaturan IP, firewall, dan NAT<br>
      Mengatur hotspot login page di router Mikrotik<br>
      Crimping kabel UTP sesuai standar T568A/T568B<br>
      Menguji dan memperbaiki kabel UTP dengan LAN tester<br>
      Melakukan konfigurasi firewall untuk membatasi akses internet<br>
      Membuat website sederhana menggunakan HTML & CSS<br>
    </p>
  </section>

  <!-- SKILL -->
  <section id="skill" class="section">
    <h2>Skill</h2>
    <p>Cisco Packet Tracer (Routing, Switching, Inter-VLAN)<br>
        Mikrotik (DHCP, Firewall, QoS, Wireless, Routing, Bridging, Tunnel)<br>
        Debian (basic server configuration)<br>
        IP Configuration<br>
        Troubleshooting Jaringan<br>
        Instalasi Jaringan Kabel & Nirkabel<br>
  </section>

  <!-- SERTIFIKAT -->
  <section id="sertifikat" class="section">
    <h2>Sertifikat</h2>

    <div class="sertifikat-menu">
      <button onclick="showCategory('aguna')">Aguna Course</button>
      <button onclick="showCategory('fortinet')">Fortinet</button>
      <button onclick="showCategory('ccna')">CCNA</button>
      <button onclick="showCategory('invention')">Invention</button>
      <button onclick="showCategory('mtcna')">MTCNA</button>
    </div>

    <div id="sertifikat-gallery">
      <div class="sertifikat-item aguna">
        <img src="sertfkt-AGUNA.jpg" alt="Aguna Course">
        <img src="sertfkt-AGUNA2.jpg" alt="Aguna Course">
        <h3>Aguna Course</h3>
        <p>2024</p>
      </div>

      <div class="sertifikat-item fortinet">
        <img src="sertfkt-FORTINET.jpg" alt="Fortinet">
        <img src="sertfkt-FORTINET2.jpg" alt="Fortinet">
        <img src="sertfkt-FORTINET3.jpg" alt="Fortinet">
        <h3>Fortinet Network Security</h3>
        <p>2024</p>
      </div>

      <div class="sertifikat-item ccna">
        <img src="sertfkt-CCNA.jpg" alt="CCNA">
        <h3>Cisco CCNA</h3>
        <p>2025</p>
      </div>

      <div class="sertifikat-item invention">
        <img src="sertfkt-INVENTION.jpg" alt="Invention">
        <img src="sertfkt-INVENTION2.jpg" alt="Invention">
        <h3>Invention Workshop</h3>
        <p>2025</p>
      </div>

      <div class="sertifikat-item mtcna">
        <img src="sertfkt-MTCNA.jpg" alt="MTCNA">
        <h3>MikroTik MTCNA</h3>
        <p>2025</p>
      </div>
    </div>
  </section>

  <!-- KONTAK -->
  <section id="kontak" class="section">
    <h2>Kontak</h2>
    <p>Email: lisa89456@gmail.com<br>
       Instagram: @lisaftrioct<br>
       WhatsApp: 085645012237
    </p>
  </section>

  <script>
    function showSection(sectionId) {
      document.querySelectorAll('.section').forEach(sec => {
        sec.classList.remove('active');
      });
      document.getElementById(sectionId).classList.add('active');
    }

    function showCategory(category) {
      let items = document.querySelectorAll('.sertifikat-item');
      items.forEach(item => {
        item.style.display = 'none';
        if (item.classList.contains(category)) {
          item.style.display = 'block';
        }
      });
    }
  </script>
</body>
</html>

