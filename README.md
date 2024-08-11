<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="index.css" />
    <title>Ambudi makmur2</title>
    <style>
      @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800&display=swap");
      @import url("https://fonts.googleapis.com/css2?family=Outfit:wght@200;300;400;500;600;700;800&family=Roboto:wght@100;300;400&display=swap");

      :root {
        --primary-color: #b48b0e;
        --primary-dark: #1f252e;
      }

      * {
        margin: 0;
        padding: 0;
        scroll-behavior: smooth;
      }

      body {
        font-family: "Outfit", sans-serif;
        background: hsl(32, 88%, 25%);
        height: 100vh;
        color: whitesmoke;
      }

      /* General */
      .container {
        padding: 0 8.4rem;
      }

      .img-w {
        width: 100%;
        height: auto;
      }

      button {
        background-color: var(--primary-color);
        border: 2px solid var(--primary-color);
        font-family: "Outfit", sans-serif;
        padding: 1rem 1.5rem;
        font-weight: 600;
        font-size: 1rem;
        border-radius: 10px;
      }

      /* Nav */
      header {
        background-color: hsl(32, 88%, 25%);
        position: sticky;
        top: 0;
        z-index: 1;
      }

      .page-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1rem 0;
      }

      .logo {
        font-size: 1.5rem;
        font-weight: 800;
        opacity: 0;
        animation: leftSideAni 1s ease forwards;
      }

      .logo a {
        color: whitesmoke;
        text-decoration: none;
      }

      ul {
        display: flex;
        gap: 0.6rem;
        list-style-type: none;
        background-color: transparent;
        overflow: hidden;
      }

      li a {
        display: inline-block;
        padding: 0.3rem 1rem;
        color: #fff;
        text-decoration: none;
        font-size: 1.05rem;
        font-weight: 300;
        letter-spacing: 0.7px;
        border-radius: 36px;
        line-height: 2;
        transition: 0.3s;
        opacity: 0;
        animation: navani 0.3s ease forwards;
        animation-delay: calc(0.15s * var(--navAni));
      }

      li a.active,
      li a:hover {
        color: var(--primary-color);
      }

      .nav-btn {
        font-size: 0.9rem;
        padding: 0.6rem 1.5rem;
        opacity: 0;
        animation: rightSideAni 1s ease forwards;
      }

      #click {
        display: none;
      }

      .menu {
        display: none;
      }

      .nav-btn {
        display: block;
      }

      .nav-btn-mobile {
        display: none;
      }

      /* Nav End */

      /* Section 1 */

      .main {
        padding-top: 4rem;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: center;
      }

      .main .detail {
        width: 50%;
      }

      .main .discount {
        color: #fff;
        font-size: 1rem;
        font-weight: 300;
        word-spacing: 8px;
        opacity: 0;
        animation: topSideAni 1s ease forwards;
      }

      .main .discount::before {
        content: "";
        height: 3px;
        width: 60px;
        display: inline-block;
        background-color: var(--primary-color);
        margin-bottom: 5px;
        margin-right: 10px;
      }

      .main h1 {
        color: #f7f2f2;
        font-size: 4rem;
        font-weight: 600;
        opacity: 0;
        animation: leftSideAni 1s ease forwards;
        animation-delay: 1s;
      }

      .main button {
        margin-top: 1.5rem;
        opacity: 0;
        animation: topSideAni 1s ease forwards;
        animation-duration: 1s;
      }

      .images {
        width: 45%;
        text-align: end;
      }

      .images img {
        background-color: var(--primary-color);
        width: 560px;
        border-radius: 100%;
      }
      .product-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 20px;
      }

      .product {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 20px;
        border: 1px solid #ddd;
        border-radius: 10px;
      }

      .product img {
        width: 115%;
        height: 275px;
        object-fit: cover;
        border-radius: 10px 10px 0 0;
      }

      .product h3 {
        margin-top: 10px;
        font-size: 18px;
        font-weight: bold;
      }

      /* Section 1 End */

      /* Animation */
      @keyframes leftSideAni {
        0% {
          transform: translateX(-100px);
          opacity: 0;
        }

        100% {
          transform: translateX(0);
          opacity: 1;
        }
      }

      @keyframes navani {
        0% {
          transform: translateY(100px);
          opacity: 0;
        }

        100% {
          transform: translateY(0);
          opacity: 1;
        }
      }

      @keyframes rightSideAni {
        0% {
          transform: translateX(100px);
          opacity: 0;
        }

        100% {
          transform: translateX(0);
          opacity: 1;
        }
      }

      @keyframes topSideAni {
        0% {
          transform: translateY(-100px);
          opacity: 0;
        }

        100% {
          transform: translateY(0);
          opacity: 1;
        }
      }

      @keyframes imageAni {
        0% {
          opacity: 0;
          transform: scale(0);
        }

        100% {
          opacity: 1;
          transform: scale(1);
        }
      }

      @media screen and (max-width: 1024px) {
        .container {
          padding: 0 4.4rem;
        }

        .main h3 {
          color: #000;
          margin-top: 1rem;
        }
      }

      @media screen and (max-width: 768px) {
        html {
          font-size: 75%;
        }

        .container {
          padding: 0 1.6rem;
        }

        .images img {
          width: 330px;
        }
      }

      @media screen and (max-width: 600px) {
        body {
          height: auto;
        }

        header {
          height: auto;
        }

        ul {
          background: hsl(51, 81%, 38%);
          width: 100%;
          height: 100vh;
          position: absolute;
          display: flex;
          flex-direction: column;
          text-align: center;
          top: 3.4rem;
          left: -100%;
          z-index: 111111;
        }

        .menu {
          display: block;
          font-size: 1.5rem;
          font-weight: bold;
          color: var(--primary-color);
        }

        #click:checked ~ ul {
          left: 0%;
          transition: all 0.3s ease;
        }

        .nav-btn {
          display: none;
        }

        .nav-btn-mobile {
          display: block;
        }

        .main .detail {
          width: 100%;
        }

        .images {
          text-align: center;
          width: 50%;
        }

        .main {
          margin-top: 2rem;
        }
      }

      @media screen and (max-width: 375px) {
        .images img {
          width: 280px;
        }
      }
    </style>
  </head>

  <body>
    <header class="container">
      <div class="page-header">
        <div class="logo">
          <a href="#">Central Salak Rindang Desa Kramat</a>
        </div>
        <input type="checkbox" id="click" />

        <label for="click" class="mainicon">
          <div class="menu">
            <i class="bx bx-menu"></i>
          </div>
        </label>
        <ul>
          <!-- Mengarahkan ke bagian dengan id yang sesuai -->
          <li><a href="#home" class="active" style="--navAni: 1">Home</a></li>
          <li><a href="#about" style="--navAni: 2">About</a></li>
          <li><a href="#menu" style="--navAni: 3">Menu</a></li>
          <li><a href="#contact" style="--navAni: 5">Contact</a></li>
        </ul>
      </div>
    </header>

    <!-- Tambahkan id="home" pada section utama -->
    <section class="container" id="home">
      <div class="main">
        <div class="detail">
          <p class="discount">WELCOME</p>
          <h1>Ambudi Makmur 2</h1>
        </div>
        <div class="images">
          <img src="busaniah.jpg" alt="" class="img-w" />
        </div>
      </div>
    </section>

    <!-- Bagian About dengan id="about" -->
    <section class="container" id="about">
      <div class="main">
        <div class="detail">
          <h2>About Us</h2>
          <p>
            Ambudi Makmur 2 berawal dari keinginan untuk memanfaatkan hasil bumi
            lokal dan memberdayakan masyarakat sekitar. Dengan semangat inovasi
            dan keuletan, kami mengolah buah salak menjadi berbagai produk yang
            tidak hanya lezat tetapi juga bernilai tambah tinggi.
          </p>
          <p>
            Didirikan pada tahun 1999, Ambudi Makmur adalah UMKM yang berfokus
            pada pengolahan buah salak menjadi berbagai produk berkualitas
            tinggi. Berlokasi di Desa Kramat, Kecamatan Bangkalan, kami
            berkomitmen untuk menghadirkan inovasi dan kualitas dalam setiap
            produk yang kami hasilkan.
          </p>
        </div>
      </div>
    </section>

    <!-- Bagian Menu dengan id="menu" -->
    <section class="container" id="menu">
      <div class="main">
        <div class="detail">
          <h2>Menu</h2>
          <p>
            Nikmati kelezatan cemilan salak kami yang khas. Terbuat dari buah
            salak berkualitas, kami menghadirkan berbagai varian rasa yang
            menggugah selera. Temukan favorit Anda dan rasakan kenikmatan alami
            dari buah eksotis ini. Cocok untuk teman bersantai, hadiah, atau
            camilan sehari-hari!
          </p>
          <div class="product-grid">
            <div class="product">
              <h3>Coklat Salak</h3>
              <img src="Coklat salak.png" alt="Product 1" class="img-w" />
            </div>
            <div class="product">
              <h3>Kismis Salak</h3>
              <img src="Kismis salak.png" alt="Product 2" class="img-w" />
            </div>
            <div class="product">
              <h3>Kopi Salak</h3>
              <img src="kopi salak.png" alt="Product 3" class="img-w" />
            </div>
            <div class="product">
              <h3>Kurma Salak</h3>
              <img src="Kurma salak.png" alt="Product 4" class="img-w" />
            </div>
            <div class="product">
              <h3>Manisan Salak</h3>
              <img src="Manisan salak.png" alt="Product 5" class="img-w" />
            </div>
            <div class="product">
              <h3>Selai Salak</h3>
              <img src="Selai salak.png" alt="Product 6" class="img-w" />
            </div>
            <div class="product">
              <h3>Sirup Salak</h3>
              <img src="Sirup salak.png" alt="Product 7" class="img-w" />
            </div>
            <div class="product">
              <h3>Dudul Salak</h3>
              <img src="dudul salak.jpg" alt="Product 8" class="img-w" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Bagian Contact dengan id="contact" -->
    <section class="container" id="contact">
      <div class="main">
        <div class="detail">
          <h2>Contact Us</h2>
          <div class="contact-details">
            <h3>Our Contact Details</h3>
            <p>
              Address: Markolak Barat, Desa Kramat, Kecamatan Bangkalan,
              Kabupaten Bangkalan<br />
              Phone: +62 857 3039 3129<br />
            </p>
          </div>
        </div>
      </div>
    </section>
  </body>
</html>
