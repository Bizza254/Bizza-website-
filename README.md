<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Bizza Electronics and Phone Accessories</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    :root {
      --primary: #0d6efd;
      --secondary: #6c757d;
      --light: #f8f9fa;
      --dark: #212529;
      --success: #198754;
      --warning: #ffc107;
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #f5f7fa 0%, #e4e7ec 100%);
      color: #333;
      line-height: 1.6;
    }
    
    header {
      background: linear-gradient(135deg, var(--primary) 0%, #0b5ed7 100%);
      color: white;
      padding: 1em 2em;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 100;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    
    .header-content {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    
    .logo {
      display: flex;
      align-items: center;
      gap: 15px;
      margin-bottom: 10px;
    }
    
    .logo i {
      font-size: 2.5rem;
      background: white;
      color: var(--primary);
      padding: 10px;
      border-radius: 50%;
    }
    
    .logo h1 {
      font-size: 1.8rem;
      font-weight: 700;
      letter-spacing: 0.5px;
    }
    
    nav {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 1em;
      margin-top: 1em;
    }
    
    nav a {
      color: white;
      text-decoration: none;
      padding: 0.7em 1.5em;
      border-radius: 50px;
      transition: all 0.3s ease;
      font-weight: 600;
      background: rgba(255,255,255,0.1);
      display: flex;
      align-items: center;
      gap: 8px;
    }
    
    nav a:hover, nav a.active {
      background: rgba(255,255,255,0.25);
      transform: translateY(-2px);
    }
    
    section {
      padding: 3em 2em;
      background: white;
      margin: 1.5em auto;
      max-width: 1200px;
      border-radius: 15px;
      box-shadow: 0 5px 25px rgba(0,0,0,0.08);
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    
    footer {
      background: linear-gradient(135deg, #2c3e50 0%, #1a2530 100%);
      color: white;
      text-align: center;
      padding: 2.5em 1em;
      margin-top: 3em;
    }
    
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2em;
    }
    
    .product-card {
      background: #fff;
      padding: 1.8em;
      border-radius: 12px;
      text-align: center;
      box-shadow: 0 8px 20px rgba(0,0,0,0.06);
      transition: all 0.3s ease;
      border: 1px solid #eaeaea;
      display: flex;
      flex-direction: column;
      height: 100%;
    }
    
    .product-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 15px 30px rgba(0,0,0,0.12);
      border-color: var(--primary);
    }
    
    .product-img {
      width: 100%;
      height: 200px;
      object-fit: contain;
      border-radius: 10px;
      margin-bottom: 1.5em;
      background: linear-gradient(135deg, #f5f7fa 0%, #e4e7ec 100%);
      padding: 15px;
    }
    
    .price {
      font-weight: bold;
      color: var(--primary);
      font-size: 1.4em;
      margin: 0.8em 0;
    }
    
    .btn {
      display: inline-block;
      background: var(--primary);
      color: white;
      padding: 12px 28px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      margin-top: auto;
      transition: all 0.3s ease;
      border: 2px solid var(--primary);
    }
    
    .btn:hover {
      background: white;
      color: var(--primary);
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(13, 110, 253, 0.3);
    }
    
    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 1.8em;
      margin-top: 1.5em;
    }
    
    .gallery-item {
      border-radius: 12px;
      overflow: hidden;
      height: 250px;
      box-shadow: 0 6px 15px rgba(0,0,0,0.1);
      transition: all 0.4s ease;
      position: relative;
    }
    
    .gallery-item:hover {
      transform: scale(1.03);
    }
    
    .gallery-img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }
    
    .gallery-item:hover .gallery-img {
      transform: scale(1.1);
    }
    
    .gallery-caption {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      background: rgba(0,0,0,0.7);
      color: white;
      padding: 12px;
      text-align: center;
      transform: translateY(100%);
      transition: transform 0.3s ease;
    }
    
    .gallery-item:hover .gallery-caption {
      transform: translateY(0);
    }
    
    h2 {
      text-align: center;
      color: var(--primary);
      margin-bottom: 1.8em;
      position: relative;
      font-size: 2.2rem;
    }
    
    h2::after {
      content: '';
      position: absolute;
      bottom: -15px;
      left: 50%;
      transform: translateX(-50%);
      width: 100px;
      height: 5px;
      background: var(--primary);
      border-radius: 3px;
    }
    
    .contact-info {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1.2em;
      font-size: 1.2em;
      max-width: 700px;
      margin: 0 auto;
    }
    
    .contact-card {
      display: flex;
      align-items: center;
      gap: 15px;
      padding: 20px;
      background: #f8f9fa;
      border-radius: 12px;
      width: 100%;
      transition: all 0.3s ease;
      border-left: 4px solid var(--primary);
    }
    
    .contact-card:hover {
      background: #e9f0ff;
      transform: translateX(5px);
    }
    
    .contact-icon {
      background: var(--primary);
      color: white;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.4rem;
    }
    
    .hero {
      text-align: center;
      padding: 5em 2em;
      background: linear-gradient(rgba(13, 110, 253, 0.8), rgba(13, 110, 253, 0.9)), url('https://images.unsplash.com/photo-1595941069915-4ebc5197c14a?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80');
      background-size: cover;
      background-position: center;
      color: white;
      border-radius: 0;
      margin: 0;
    }
    
    .hero h2 {
      color: white;
      font-size: 3rem;
      margin-bottom: 0.5em;
    }
    
    .hero h2::after {
      display: none;
    }
    
    .hero p {
      font-size: 1.3rem;
      max-width: 800px;
      margin: 0 auto 2em;
    }
    
    .btn-large {
      padding: 15px 40px;
      font-size: 1.1rem;
      background: var(--warning);
      color: var(--dark);
      border-color: var(--warning);
    }
    
    .btn-large:hover {
      background: white;
      color: var(--dark);
    }
    
    .features {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2em;
      margin-top: 3em;
    }
    
    .feature-card {
      background: white;
      padding: 2em;
      border-radius: 12px;
      text-align: center;
      box-shadow: 0 5px 20px rgba(0,0,0,0.05);
      transition: all 0.3s ease;
    }
    
    .feature-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 30px rgba(0,0,0,0.1);
    }
    
    .feature-icon {
      font-size: 3rem;
      color: var(--primary);
      margin-bottom: 20px;
    }
    
    .social-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 1.5em;
    }
    
    .social-icon {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      background: white;
      color: var(--primary);
      font-size: 1.5rem;
      transition: all 0.3s ease;
    }
    
    .social-icon:hover {
      background: var(--primary);
      color: white;
      transform: translateY(-5px);
    }
    
    .testimonials {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2em;
      margin-top: 2em;
    }
    
    .testimonial-card {
      background: #f8f9fa;
      padding: 2em;
      border-radius: 12px;
      border-left: 4px solid var(--primary);
    }
    
    .testimonial-content {
      font-style: italic;
      margin-bottom: 1.5em;
    }
    
    .testimonial-author {
      display: flex;
      align-items: center;
      gap: 15px;
    }
    
    .author-avatar {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      object-fit: cover;
    }
    
    @media (max-width: 768px) {
      section {
        padding: 2em 1.5em;
      }
      
      .product-grid, .gallery-grid {
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      }
      
      .hero {
        padding: 3em 1.5em;
      }
      
      .hero h2 {
        font-size: 2.2rem;
      }
      
      h2 {
        font-size: 1.8rem;
      }
    }
    
    @media (max-width: 480px) {
      nav {
        flex-direction: column;
        width: 100%;
      }
      
      nav a {
        width: 100%;
        justify-content: center;
      }
      
      .logo h1 {
        font-size: 1.5rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="header-content">
      <div class="logo">
        <i class="fas fa-mobile-alt"></i>
        <h1>Bizza Electronics & Phone Accessories</h1>
      </div>
      <nav>
        <a href="#home" class="active"><i class="fas fa-home"></i> Home</a>
        <a href="#about"><i class="fas fa-info-circle"></i> About</a>
        <a href="#products"><i class="fas fa-box-open"></i> Products</a>
        <a href="#gallery"><i class="fas fa-images"></i> Gallery</a>
        <a href="#testimonials"><i class="fas fa-comments"></i> Testimonials</a>
        <a href="#contact"><i class="fas fa-phone-alt"></i> Contact</a>
      </nav>
    </div>
  </header>

  <section id="home" class="hero">
    <div class="container">
      <h2>Premium Electronics & Phone Accessories</h2>
      <p>Your trusted source for quality gadgets, accessories, and expert technical support in Nairobi</p>
      <a href="#products" class="btn btn-large"><i class="fas fa-shopping-cart"></i> Shop Now</a>
    </div>
  </section>

  <section id="about">
    <div class="container">
      <h2>About Us</h2>
      <p style="text-align: center; max-width: 800px; margin: 0 auto 2em; font-size: 1.1em; line-height: 1.8;">
        Founded in 2015, Bizza Electronics has grown to become Nairobi's trusted destination for quality electronics and phone accessories. With over 10,000 satisfied customers, we pride ourselves on offering the latest gadgets at competitive prices, backed by exceptional customer service and technical expertise.
      </p>
      
      <div class="features">
        <div class="feature-card">
          <div class="feature-icon">
            <i class="fas fa-award"></i>
          </div>
          <h3>Quality Products</h3>
          <p>We source directly from manufacturers to ensure authenticity and quality.</p>
        </div>
        
        <div class="feature-card">
          <div class="feature-icon">
            <i class="fas fa-headset"></i>
          </div>
          <h3>Expert Support</h3>
          <p>Our knowledgeable staff provides expert advice and technical support.</p>
        </div>
        
        <div class="feature-card">
          <div class="feature-icon">
            <i class="fas fa-tags"></i>
          </div>
          <h3>Best Prices</h3>
          <p>Competitive pricing without compromising on quality.</p>
        </div>
        
        <div class="feature-card">
          <div class="feature-icon">
            <i class="fas fa-shield-alt"></i>
          </div>
          <h3>Warranty</h3>
          <p>All products come with a minimum 6-month warranty.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="products">
    <div class="container">
      <h2>Our Products</h2>
      <div class="product-grid">
        <div class="product-card">
          <img src="https://images.unsplash.com/photo-1598327105666-5b89351aff97?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Smartphones" class="product-img">
          <h3>Smartphones</h3>
          <p>Latest Android and iPhone models with warranty</p>
          <div class="price">From Ksh 15,000</div>
          <a href="#contact" class="btn"><i class="fas fa-cart-plus"></i> Order Now</a>
        </div>
        
        <div class="product-card">
          <img src="https://images.unsplash.com/photo-1605787020600-b9ebd5df3d07?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Chargers & Cables" class="product-img">
          <h3>Chargers & Cables</h3>
          <p>Durable and fast-charging accessories</p>
          <div class="price">From Ksh 800</div>
          <a href="#contact" class="btn"><i class="fas fa-cart-plus"></i> Order Now</a>
        </div>
        
        <div class="product-card">
          <img src="https://images.unsplash.com/photo-1546435770-a3e426bf472b?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Bluetooth Speakers" class="product-img">
          <h3>Bluetooth Speakers</h3>
          <p>High-quality sound on the go</p>
          <div class="price">From Ksh 2,500</div>
          <a href="#contact" class="btn"><i class="fas fa-cart-plus"></i> Order Now</a>
        </div>
        
        <div class="product-card">
          <img src="https://images.unsplash.com/photo-1600086827875-1a0b2d17c62e?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Phone Cases" class="product-img">
          <h3>Phone Cases</h3>
          <p>Stylish and protective designs</p>
          <div class="price">From Ksh 600</div>
          <a href="#contact" class="btn"><i class="fas fa-cart-plus"></i> Order Now</a>
        </div>
      </div>
    </div>
  </section>

  <section id="gallery">
    <div class="container">
      <h2>Our Gallery</h2>
      <div class="gallery-grid">
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1496171367470-9ed9a91ea931?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Store Front" class="gallery-img">
          <div class="gallery-caption">Our Nairobi CBD Showroom</div>
        </div>
        
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1550009158-9ebf69173e03?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Product Display" class="gallery-img">
          <div class="gallery-caption">Latest Product Collection</div>
        </div>
        
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1584438784894-089d6a62b8fa?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Workshop" class="gallery-img">
          <div class="gallery-caption">Professional Repair Center</div>
        </div>
        
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Team" class="gallery-img">
          <div class="gallery-caption">Our Expert Team</div>
        </div>
        
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1583394838336-acd977736f90?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="New Arrivals" class="gallery-img">
          <div class="gallery-caption">New Arrivals Section</div>
        </div>
        
        <div class="gallery-item">
          <img src="https://images.unsplash.com/photo-1519162584292-56dfc9eb5db4?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Customer Service" class="gallery-img">
          <div class="gallery-caption">Customer Service Excellence</div>
        </div>
      </div>
    </div>
  </section>

  <section id="testimonials">
    <div class="container">
      <h2>Customer Testimonials</h2>
      <div class="testimonials">
        <div class="testimonial-card">
          <div class="testimonial-content">
            "Bizza Electronics has been my go-to shop for all my phone accessories. Their prices are fair and the staff is incredibly knowledgeable. Highly recommended!"
          </div>
          <div class="testimonial-author">
            <img src="https://randomuser.me/api/portraits/women/45.jpg" alt="Sarah K." class="author-avatar">
            <div>
              <strong>Sarah K.</strong>
              <div>Nairobi</div>
            </div>
          </div>
        </div>
        
        <div class="testimonial-card">
          <div class="testimonial-content">
            "I bought my smartphone from Bizza six months ago and it's been perfect. They even threw in a free screen protector. Great service!"
          </div>
          <div class="testimonial-author">
            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="James M." class="author-avatar">
            <div>
              <strong>James M.</strong>
              <div>Kikuyu</div>
            </div>
          </div>
        </div>
        
        <div class="testimonial-card">
          <div class="testimonial-content">
            "When my phone stopped charging, Bizza fixed it in under an hour at a reasonable price. Their technicians really know their stuff!"
          </div>
          <div class="testimonial-author">
            <img src="https://randomuser.me/api/portraits/women/68.jpg" alt="Amina J." class="author-avatar">
            <div>
              <strong>Amina J.</strong>
              <div>Westlands</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="container">
      <h2>Contact Us</h2>
      <div class="contact-info">
        <div class="contact-card">
          <div class="contact-icon">
            <i class="fas fa-phone-alt"></i>
          </div>
          <div>
            <strong>Phone:</strong> 0707160005<br>
            <strong>WhatsApp:</strong> 0707160005
          </div>
        </div>
        
        <div class="contact-card">
          <div class="contact-icon">
            <i class="fas fa-envelope"></i>
          </div>
          <div>
            <strong>Email:</strong> info@bizzaelectronics.com<br>
            <strong>Support:</strong> support@bizzaelectronics.com
          </div>
        </div>
        
        <div class="contact-card">
          <div class="contact-icon">
            <i class="fas fa-map-marker-alt"></i>
          </div>
          <div>
            <strong>Address:</strong> Nairobi CBD, Moi Avenue, Electronics Plaza, Shop 24<br>
            <strong>Hours:</strong> Mon-Sat: 8:30 AM - 6:00 PM | Sun: 10:00 AM - 4:00 PM
          </div>
        </div>
        
        <div class="social-links">
          <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
          <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
          <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
          <a href="#" class="social-icon"><i class="fab fa-whatsapp"></i></a>
        </div>
      </div>
    </div>
  </section>

  <footer>
    <div class="container">
      <p>&copy; 2025 Bizza Electronics and Phone Accessories. All rights reserved.</p>
      <p>Proudly serving Nairobi since 2015</p>
      <div class="social-links" style="margin-top: 1em;">
        <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-tiktok"></i></a>
      </div>
    </div>
  </footer>

  <script>
    // Smooth scrolling for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener('click', function (e) {
        e.preventDefault();
        
        document.querySelector(this.getAttribute('href')).scrollIntoView({
          behavior: 'smooth'
        });
        
        // Update active nav item
        document.querySelectorAll('nav a').forEach(link => {
          link.classList.remove('active');
        });
        this.classList.add('active');
      });
    });
    
    // Simple animation on scroll
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.style.opacity = 1;
          entry.target.style.transform = 'translateY(0)';
        }
      });
    }, { threshold: 0.1 });
    
    document.querySelectorAll('section, .product-card, .feature-card, .gallery-item, .testimonial-card').forEach(el => {
      el.style.opacity = 0;
      el.style.transform = 'translateY(30px)';
      el.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
      observer.observe(el);
    });
  </script>
</body>
</html># Bizza-website-
