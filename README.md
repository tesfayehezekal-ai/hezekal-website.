<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hezekal Platform</title>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&family=Montserrat:wght@600;700&display=swap" rel="stylesheet">

<!-- Font Awesome Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<style>
body { margin:0; font-family:'Roboto', sans-serif; background:#f4f4f4; color:#333; }
a { text-decoration:none; }
h2 { color:#333; }
.cta-button { background:#ff9800; color:white; padding:12px 25px; border-radius:8px; font-weight:bold; transition:0.3s; cursor:pointer; display:inline-block; }
.cta-button:hover { background:#e68900; transform:scale(1.05); }

/* Header */
header { 
  background: linear-gradient(135deg, #ff9800, #ff5722); 
  color:white; text-align:center; padding:120px 20px; position:relative; 
  border-bottom-left-radius:30px; border-bottom-right-radius:30px;
}
header img.logo { position:absolute; top:20px; left:20px; width:100px; height:auto; border-radius:50%; border:2px solid white; }
header h1 { font-size:3rem; margin:0; font-family:'Montserrat', sans-serif; }
header p { font-size:1.2rem; margin-top:10px; color:#fff; }

/* Navigation */
nav { background:#111; display:flex; justify-content:center; flex-wrap:wrap; padding:15px; position:sticky; top:0; z-index:1000; }
nav a { color:white; margin:0 15px; font-weight:bold; padding:5px 10px; transition:0.3s; cursor:pointer; }
nav a:hover { background:white; color:#111; border-radius:5px; }

/* Sections */
section { padding:60px 20px; max-width:1200px; margin:auto; display:none; }
section.active { display:block; text-align:center; }
.center { text-align:center; }

/* Service Cards */
.services { display:grid; grid-template-columns:repeat(auto-fit, minmax(280px, 1fr)); gap:20px; }
.service-card { background:#fff; padding:0; border-radius:12px; overflow:hidden; box-shadow:0 4px 15px rgba(0,0,0,0.1); transition:0.3s; cursor:pointer; }
.service-card:hover { transform:translateY(-10px) scale(1.05); box-shadow:0 8px 20px rgba(0,0,0,0.2); }
.service-card img { width:100%; height:180px; object-fit:cover; }
.card-content { padding:20px; text-align:left; }
.card-content i { color:#ff9800; margin-right:10px; font-size:1.5rem; }
.card-content h3 { margin:10px 0 5px 0; }
.service-details { display:none; margin-top:15px; background:#f4f4f4; padding:15px; border-left:5px solid #ff9800; border-radius:8px; text-align:left; }
.pricing-tabs { display:flex; justify-content:space-around; margin-top:10px; }
.pricing-tabs span { cursor:pointer; padding:8px 12px; border-radius:8px; background:#eee; transition:0.3s; }
.pricing-tabs span.active { background:#ff9800; color:white; }

/* Forms */
.form-container { max-width:600px; margin:auto; background:white; padding:30px; border-radius:12px; box-shadow:0 4px 15px rgba(0,0,0,0.1); text-align:left; }
.form-container input, .form-container textarea { width:100%; padding:12px; margin:10px 0; border:1px solid #ddd; border-radius:8px; font-size:1rem; }
.form-container button { width:100%; margin-top:10px; }

/* Promote Skills Section */
.promote-section { background:#ffcc80; color:#333; padding:50px 20px; border-radius:12px; text-align:center; margin-bottom:40px; }

/* Footer */
footer { background:#000; color:#ddd; text-align:center; padding:20px; margin-top:50px; }
footer a { color:#ff9800; margin:0 10px; }

/* Service Colors Meaning */
.service-card.content { border-top:4px solid #ff5722; }   
.service-card.social { border-top:4px solid #0077cc; }   
.service-card.analytics { border-top:4px solid #6a1b9a; } 
.service-card.advice { border-top:4px solid #009688; }  
.service-card.book { border-top:4px solid #f44336; }    
</style>

<script src="https://cdn.emailjs.com/dist/email.min.js"></script>
<script> 
  emailjs.init("YOUR_PUBLIC_KEY"); // Replace with your EmailJS Public Key
</script>
</head>
<body>

<!-- Header -->
<header>
  <img src="https://via.placeholder.com/100x100?text=HT" alt="Hezekal Logo" class="logo">
  <h1>Hezekal Platform</h1>
  <p>Social Media Management, Content, Advice & Book Editing</p>
  <span class="cta-button" onclick="showSection('services')"><i class="fa-solid fa-arrow-right"></i> Explore Services</span>
</header>

<!-- Navigation -->
<nav>
  <a onclick="showSection('home')">Home</a>
  <a onclick="showSection('services')">Services</a>
  <a onclick="showSection('promote')">Promote Skills</a>
  <a onclick="showSection('contact')">Contact</a>
</nav>

<!-- Home -->
<section id="home" class="active" style="background: linear-gradient(120deg, #fdd835, #ff5722); padding:80px 20px; border-radius:20px; color:white; margin-top:40px;">
  <h2 class="center" style="font-size:2.5rem; margin-bottom:20px;">Who We Are</h2>
  <p class="center" style="font-size:1.2rem; max-width:800px; margin:auto;">We help businesses grow online and provide a platform for talented individuals to promote their skills. Join us to create, manage, and showcase your brand effectively!</p>
  <span class="cta-button" style="background:white; color:#ff5722; padding:12px 25px; margin-top:20px;" onclick="showSection('promote')"><i class="fa-solid fa-star"></i> Promote Your Skill</span>
</section>

<!-- Services -->
<section id="services">
  <h2 class="center">Our Services</h2>
  <div class="services">

    <!-- Content Writing -->
    <div class="service-card content" onclick="toggleDetails('content')">
      <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?auto=format&fit=crop&w=400&q=80" alt="Content Writing">
      <div class="card-content">
        <i class="fa-solid fa-pen-nib"></i><h3>Content Writing</h3>
        <p>Engaging posts & blogs</p>
        <div class="pricing-tabs">
          <span onclick="showPrice('content','basic')" class="active">Basic</span>
          <span onclick="showPrice('content','standard')">Standard</span>
          <span onclick="showPrice('content','premium')">Premium</span>
        </div>
        <div class="service-details" id="content">
          <p id="content-price">Basic: $100</p>
          <p>Basic: Short posts<br>Standard: Long posts + blogs<br>Premium: Full content package with SEO</p>
        </div>
      </div>
    </div>

    <!-- Social Media -->
    <div class="service-card social" onclick="toggleDetails('social')">
      <img src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=400&q=80" alt="Social Media">
      <div class="card-content">
        <i class="fa-brands fa-facebook"></i><h3>Social Media Management</h3>
        <p>Boost online presence</p>
        <div class="pricing-tabs">
          <span onclick="showPrice('social','basic')" class="active">Basic</span>
          <span onclick="showPrice('social','standard')">Standard</span>
          <span onclick="showPrice('social','premium')">Premium</span>
        </div>
        <div class="service-details" id="social">
          <p id="social-price">Basic: $200</p>
          <p>Basic: 5 posts/week<br>Standard: 10 posts + engagement<br>Premium: Full management + analytics</p>
        </div>
      </div>
    </div>

    <!-- Advice -->
    <div class="service-card social" onclick="toggleDetails('advice')">
      <img src="https://images.unsplash.com/photo-1605902711622-cfb43c4432f4?auto=format&fit=crop&w=400&q=80" alt="Advice">
      <div class="card-content">
        <i class="fa-solid fa-lightbulb"></i><h3>Advice & Consultation</h3>
        <p>Business & social guidance</p>
        <div class="pricing-tabs">
          <span onclick="showPrice('advice','basic')" class="active">Basic</span>
          <span onclick="showPrice('advice','standard')">Standard</span>
          <span onclick="showPrice('advice','premium')">Premium</span>
        </div>
        <div class="service-details" id="advice">
          <p id="advice-price">Basic: $50</p>
          <p>Basic: 30-min session<br>Standard: 1-hour session<br>Premium: 2-hour in-depth session</p>
        </div>
      </div>
    </div>

    <!-- Book Editing -->
    <div class="service-card book" onclick="toggleDetails('book')">
      <img src="https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?auto=format&fit=crop&w=400&q=80" alt="Book Editing">
      <div class="card-content">
        <i class="fa-solid fa-book"></i><h3>Book Editing</h3>
        <p>Professional editing services</p>
        <div class="pricing-tabs">
          <span onclick="showPrice('book','basic')" class="active">Basic</span>
          <span onclick="showPrice('book','standard')">Standard</span>
          <span onclick="showPrice('book','premium')">Premium</span>
        </div>
        <div class="service-details" id="book">
          <p id="book-price">Basic: $100</p>
          <p>Basic: Proofreading<br>Standard: Proofreading + formatting<br>Premium: Full editing + design</p>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- Promote Skills -->
<section id="promote" class="promote-section">
  <h2>Promote Your Skills</h2>
  <p>Share your talents with the world!</p>
  <div class="form-container">
    <form id="promote-form">
      <input type="text" name="from_name" placeholder="Full Name" required>
      <input type="email" name="from_email" placeholder="Email" required>
      <input type="text" name="skill" placeholder="Your Skill" required>
      <button type="submit" class="cta-button"><i class="fa-solid fa-paper-plane"></i> Submit Skill</button>
    </form>
    <p id="promote-status"></p>
  </div>
</section>

<!-- Contact -->
<section id="contact">
  <h2 class="center">Contact Us</h2>
  <div class="form-container">
    <form id="contact-form">
      <input type="text" name="from_name" placeholder="Your Name" required>
      <input type="email" name="from_email" placeholder="Your Email" required>
      <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
      <button type="submit" class="cta-button"><i class="fa-solid fa-envelope"></i> Send Message</button>
    </form>
    <p id="contact-status"></p>
  </div>
</section>

<footer>
  <p>&copy; 2025 Hezekal Platform | <a href="#">LinkedIn</a> | <a href="#">Twitter</a></p>
</footer>

<script>
function showSection(id){
  const sections = ['home','services','promote','contact'];
  sections.forEach(sec => document.getElementById(sec).classList.remove('active'));
  document.getElementById(id).classList.add('active');
}

function toggleDetails(id){
  const details = document.getElementById(id);
  details.style.display = details.style.display === "block" ? "none" : "block";
}

// Pricing tabs
function showPrice(service, level){
  const prices = {
    content: {basic:'$100', standard:'$200', premium:'$250'},
    social: {basic:'$200', standard:'$350', premium:'$500'},
    advice: {basic:'$50', standard:'$100', premium:'$150'},
    book: {basic:'$100', standard:'$200', premium:'$350'}
  };
  document.getElementById(service+'-price').innerText = level.charAt(0).toUpperCase()+level.slice(1)+': '+prices[service][level];
  // Update active class
  document.querySelectorAll(`.service-card.${service} .pricing-tabs span`).forEach(span=>span.classList.remove('active'));
  event.target.classList.add('active');
}

// EmailJS
const SERVICE_ID = "service_bjpkwtv"; 
const TEMPLATE_CONTACT_ID = "template_s1xs8lq"; 
const TEMPLATE_REGISTER_ID = "template_ox0vn0a";

document.getElementById('contact-form').addEventListener('submit', function(e){
  e.preventDefault();
  emailjs.sendForm(SERVICE_ID, TEMPLATE_CONTACT_ID, this)
    .then(() => { document.getElementById('contact-status').innerText='✅ Message sent!'; this.reset(); },
          (err) => { document.getElementById('contact-status').innerText='❌ Failed.'; console.log(err); });
});

document.getElementById('promote-form').addEventListener('submit', function(e){
  e.preventDefault();
  emailjs.sendForm(SERVICE_ID, TEMPLATE_REGISTER_ID, this)
    .then(() => { document.getElementById('promote-status').innerText='✅ Skill submitted!'; this.reset(); },
          (err) => { document.getElementById('promote-status').innerText='❌ Failed.'; console.log(err); });
});
</script>

</body>
</html>

