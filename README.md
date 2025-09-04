<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Landing Page</title>
  <style>
    /* Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
    }

    /* Navbar */
    nav {
      position: fixed;         /* Fixed on top */
      top: 0;
      left: 0;
      width: 100%;
      background: transparent; /* Transparent by default */
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 20px 50px;
      transition: background 0.4s ease, box-shadow 0.4s ease;
      z-index: 1000;           /* Stay above all sections */
    }

    /* Change on scroll */
    nav.scrolled {
      background: #111;
      box-shadow: 0 2px 10px rgba(0,0,0,0.3);
    }

    /* Logo */
    nav .logo {
      font-size: 1.5rem;
      font-weight: bold;
      color: #fff;
    }

    /* Menu */
    nav ul {
      list-style: none;
      display: flex;
    }

    nav ul li {
      margin: 0 15px;
    }

    nav ul li a {
      text-decoration: none;
      color: #fff;
      font-weight: 500;
      padding: 5px 10px;
      transition: color 0.3s ease, background 0.3s ease;
    }

    /* Hover effect */
    nav ul li a:hover {
      background: #fff;
      color: #111;
      border-radius: 4px;
    }

    /* Page Sections */
    section {
      height: 100vh;  /* Full-screen sections */
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 2rem;
      color: #fff;
    }

    #home { background: #3498db; }
    #about { background: #e67e22; }
    #services { background: #2ecc71; }
    #contact { background: #9b59b6; }

    /* Responsive */
    @media(max-width: 768px) {
      nav {
        flex-direction: column;
      }
      nav ul {
        flex-direction: column;
        margin-top: 10px;
      }
      nav ul li {
        margin: 10px 0;
      }
    }
  </style>
</head>
<body>

  <!-- Navigation -->
  <nav id="navbar">
    <div class="logo">MyLogo</div>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- Page Sections -->
  <section id="home">Home Section</section>
  <section id="about">About Section</section>
  <section id="services">Services Section</section>
  <section id="contact">Contact Section</section>

  <script>
    // Add/remove "scrolled" class when page is scrolled
    window.addEventListener("scroll", function() {
      const navbar = document.getElementById("navbar");
      if (window.scrollY > 50) {
        navbar.classList.add("scrolled");
      } else {
        navbar.classList.remove("scrolled");
      }
    });
  </script>

</body>
</html>
