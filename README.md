<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Glow Salon</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #FDF7F1;
      color: #4A2E2A;
      scroll-behavior: smooth;
    }

    header {
      background: #D4A373;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 20px;
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .logo {
      font-size: 24px;
      font-weight: bold;
      color: white;
    }

    .nav-links {
      list-style: none;
      padding: 0;
      display: flex;
    }

    .nav-links li {
      margin: 0 15px;
    }

    .nav-links a {
      text-decoration: none;
      color: white;
      font-weight: bold;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: #4A2E2A;
    }

    .hero {
      background: url('https://sdmntpritalynorth.oaiusercontent.com/files/00000000-7950-6246-a743-b5fbfbbec0b5/raw?se=2025-04-19T22%3A46%3A30Z&sp=r&sv=2024-08-04&sr=b&scid=7927aa3d-96b3-5ff3-9fb0-607a91ad2fe2&skoid=9370dd2b-ca43-4270-bed5-18b1b71f8fa0&sktid=a48cca56-e6da-484e-a814-9c849652bcb3&skt=2025-04-19T06%3A40%3A21Z&ske=2025-04-20T06%3A40%3A21Z&sks=b&skv=2024-08-04&sig=6ElSCpJb%2BKqQvjW1btn8ItBQhEtD7hlKDIZGuZEF7Qg%3D') no-repeat center center/cover;
      height: 90vh;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      position: relative;
      color: white;
    }

    .hero::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
    }

    .hero-content {
      position: relative;
      padding: 20px;
      backdrop-filter: blur(5px);
    }

    .hero h1 {
      font-size: 40px;
      margin-bottom: 10px;
    }

    .hero p {
      font-size: 18px;
      margin-bottom: 20px;
    }

    .btn {
      display: inline-block;
      background: #F4A261;
      color: white;
      padding: 12px 24px;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
      transition: 0.3s;
    }

    .btn:hover {
      background: #E76F51;
      transform: scale(1.05);
    }

    .small-btn {
      margin-top: 10px;
      font-size: 14px;
      padding: 8px 16px;
      background-color: #D4A373;
      display: inline-block;
    }

    .small-btn:hover {
      background-color: #E76F51;
      color: #fff;
    }

    .services {
      padding: 50px 20px;
      text-align: center;
    }

    .service-container {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }

    .service {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      width: 250px;
      transition: transform 0.3s ease-in-out;
    }

    .service:hover {
      transform: scale(1.05);
    }

    .service img {
      width: 100%;
      height: auto;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      margin-top: 10px;
    }

    .booking {
      background: #D4A373;
      padding: 40px;
      text-align: center;
      color: white;
    }

    .booking input, .booking button {
      width: 80%;
      padding: 10px;
      margin: 10px 0;
      border: none;
      border-radius: 5px;
    }

    .booking button {
      background: #F4A261;
      color: white;
      font-weight: bold;
      cursor: pointer;
    }

    .booking button:hover {
      background: #E76F51;
    }

    .reviews {
      padding: 50px 20px;
      text-align: center;
      background-color: #fff8f1;
    }

    .review-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 30px;
    }

    .review {
      background: white;
      padding: 20px;
      border-radius: 10px;
      width: 250px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    .review img {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      margin-bottom: 10px;
    }

    footer {
      background: #4A2E2A;
      color: white;
      text-align: center;
      padding: 20px;
    }

    @media (max-width: 768px) {
      .nav-links {
        flex-direction: column;
        text-align: center;
      }

      .service-container {
        flex-direction: column;
        align-items: center;
      }

      .service {
        width: 80%;
        margin-bottom: 20px;
      }

      .hero h1 {
        font-size: 30px;
      }

      .hero p {
        font-size: 16px;
      }
    }
  </style>
</head>

<body>
  <header>
    <div class="logo">Glow Salon</div>
    <ul class="nav-links">
      <li><a href="#home">Home</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#reviews">Reviews</a></li>
      <li><a href="#booking">Book Now</a></li>
    </ul>
  </header>

  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Luxury Hair & Beauty Services</h1>
      <p>Pamper yourself with expert haircare, makeup, nails, and haircuts.</p>
      <a href="#services" class="btn">Explore Services</a>
    </div>
  </section>

  <section id="services" class="services">
    <h2>Our Services ($50 Each)</h2>
    <div class="service-container">
      <div class="service">
        <h3>Haircuts & Styling</h3>
        <p>Trendy cuts & styles from professional hairstylists.</p>
        <img src="images/haircut.jpg" alt="Haircut and Styling Image">
        <a href="#booking" class="btn small-btn">Book Now</a>
      </div>
      <div class="service">
        <h3>Haircare & Treatments</h3>
        <p>Deep conditioning, keratin, and scalp treatments.</p>
        <img src="images/haircare.jpg" alt="Haircare and Treatments Image">
        <a href="#booking" class="btn small-btn">Book Now</a>
      </div>
      <div class="service">
        <h3>Nails & Manicure</h3>
        <p>Luxurious nail care, gel polish, and nail art.</p>
        <img src="images/nails-manicure.jpg" alt="Nails and Manicure Image">
        <a href="#booking" class="btn small-btn">Book Now</a>
      </div>
      <div class="service">
        <h3>Makeup & Beauty</h3>
        <p>Bridal, glam, and natural makeup for every occasion.</p>
        <img src="images/makeup.jpg" alt="Makeup and Beauty Image">
        <a href="#booking" class="btn small-btn">Book Now</a>
      </div>
    </div>
  </section>

  <section id="reviews" class="reviews">
    <h2>What Our Clients Say</h2>
    <div class="review-container">
      <div class="review">
        <img src="https://randomuser.me/api/portraits/women/45.jpg" alt="Client">
        <p>"Glow Salon transformed my look!"</p>
        <h4>- Emily R.</h4>
      </div>
      <div class="review">
        <img src="https://randomuser.me/api/portraits/women/50.jpg" alt="Client">
        <p>"Best salon experience ever! My hair has never felt this amazing."</p>
        <h4>- Sarah L.</h4>
      </div>
      <div class="review">
        <img src="https://randomuser.me/api/portraits/men/42.jpg" alt="Client">
        <p>"The staff is super friendly and skilled. Highly recommended!"</p>
        <h4>- James K.</h4>
      </div>
    </div>
  </section>

  <section id="booking" class="booking">
    <h2>Book Your Appointment</h2>
    <input type="text" placeholder="Your Name" />
    <input type="email" placeholder="Your Email" />
    <input type="date" />
    <button>Book Now</button>
  </section>

  <footer>&copy; 2025 Glow Salon | All Rights Reserved</footer>
</body>
</html>
