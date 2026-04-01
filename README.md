<!DOCTYPE html>
<html lang="en">
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Computer Repair Waterbury CT | OnyxTech Solutions</title>
<meta name="description" content="OnyxTech Solutions provides computer repair, networking, POS systems, and virus removal in Waterbury CT and surrounding areas.">

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600&display=swap" rel="stylesheet">

<style>

/* GLOBAL */
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, #02050d, #050814);
  color: white;
  overflow-x: hidden;
}

/* CIRCUIT BACKGROUND */
body::before {
  content: "";
  position: fixed;
  width: 200%;
  height: 200%;
  background-image:
    linear-gradient(rgba(0,255,255,0.08) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,255,255,0.08) 1px, transparent 1px);
  background-size: 60px 60px;
  animation: moveBG 30s linear infinite;
  z-index: -1;
}

@keyframes moveBG {
  0% { transform: translate(0,0); }
  100% { transform: translate(-400px,-400px); }
}

/* NAVBAR */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 30px;
  background: #050814;
  border-bottom: 1px solid #00ffff33;
  position: relative;
}

/* GLOW LINE */
.navbar::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background: linear-gradient(90deg, transparent, #00ffff, transparent);
  box-shadow: 0 0 10px #00ffff;
}

/* LOGO */
.logo img {
  height: 50px;
  filter: drop-shadow(0 0 8px #00ffff) drop-shadow(0 0 15px #00ffff55);
  animation: logoPulse 3s infinite;
  transition: 0.3s;
}

.logo img:hover {
  transform: scale(1.05);
}

@keyframes logoPulse {
  0% { filter: drop-shadow(0 0 5px #00ffff); }
  50% { filter: drop-shadow(0 0 20px #00ffff); }
  100% { filter: drop-shadow(0 0 5px #00ffff); }
}

/* NAV LINKS */
.nav-links {
  display: flex;
  gap: 20px;
  list-style: none;
}

.nav-links a {
  color: white;
  text-decoration: none;
}

.nav-links a:hover {
  color: #00ffff;
}

/* SECTIONS */
.section {
  padding: 70px 20px;
  text-align: center;
  border-top: 1px solid #00ffff22;
}

.section h2 {
  font-family: Orbitron;
  color: #00ffff;
}

/* HERO */
.hero h1 {
  font-size: 38px;
  color: #00ffff;
}

.hero-btn {
  background: #00ffff;
  color: black;
  padding: 12px 25px;
  text-decoration: none;
  border-radius: 5px;
}

/* GRID */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
  gap: 20px;
  max-width: 1100px;
  margin: auto;
}

/* CARDS */
.card {
  background: #0b0f1c;
  padding: 20px;
  border-radius: 10px;
  border: 1px solid #00ffff22;
  transition: 0.3s;
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 0 20px #00ffff55;
}

/* FORM */
input, textarea, select {
  width: 100%;
  max-width: 400px;
  padding: 10px;
  margin: 10px auto;
  display: block;
  background: #0b0f1c;
  border: 1px solid #00ffff33;
  color: white;
}

button {
  background: #00ffff;
  border: none;
  padding: 12px 20px;
  cursor: pointer;
}

/* MAP */
iframe {
  width: 100%;
  height: 350px;
  border: none;
  margin-top: 20px;
}

/* MOBILE */
@media(max-width:768px){
  .nav-links { display:none; }
}

</style>

</head>
<body>

<!-- NAV -->
<nav class="navbar">
  <div class="logo">
    <img src="logo.png" alt="OnyxTech Solutions Logo">
  </div>
  <ul class="nav-links">
    <li><a href="#services">Services</a></li>
    <li><a href="#booking">Book</a></li>
    <li><a href="#areas">Areas</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="section hero">
  <h1>OnyxTech Solutions L.L.C.</h1>
  <p>Professional Computer Repair & IT Services in Waterbury CT</p>

  <p>Network+ • Security+ • BBB Accredited</p>

  <br>
  <a href="#booking" class="hero-btn">Book Service</a>
</section>

<!-- CERTIFICATIONS -->
<section class="section">
  <h2>Certifications & Memberships</h2>

  <div class="grid">
    <div class="card">CompTIA Network+</div>
    <div class="card">CompTIA Security+</div>
    <div class="card">Retail IT Field Technician</div>
    <div class="card">Better Business Bureau</div>
    <div class="card">Waterbury Chamber</div>
    <div class="card">Milford Chamber</div>
  </div>
</section>

<!-- SERVICES -->
<section id="services" class="section">
  <h2>Services</h2>

  <div class="grid">

    <div class="card">
      <h3>Computer Repair</h3>
      <p>PC, Gaming, Tablet, Phone, Builds</p>
    </div>

    <div class="card">
      <h3>POS Systems</h3>
      <p>Install, Repair, Self Checkout, Printers</p>
    </div>

    <div class="card">
      <h3>Networking</h3>
      <p>CAT6, Access Points, MDF, Cradlepoint</p>
    </div>

    <div class="card">
      <h3>Security & Data</h3>
      <p>Virus Removal, Hard Drive, Optimization</p>
    </div>

  </div>
</section>

<!-- QUOTE -->
<section class="section">
  <h2>Instant Quote</h2>

  <select id="service">
    <option value="">Select</option>
    <option value="120">Computer Repair</option>
    <option value="100">Virus Removal</option>
    <option value="200">Networking</option>
  </select>

  <button onclick="calc()">Calculate</button>
  <p id="price"></p>
</section>

<!-- BOOKING -->
<section id="booking" class="section">
  <h2>Book Service</h2>

  <form action="https://formsubmit.co/robert@onyxtechsolutions.info" method="POST">
    <input type="hidden" name="_captcha" value="false">

    <input type="text" name="name" placeholder="Full Name" required>
    <input type="email" name="email" placeholder="Email" required>
    <input type="tel" name="phone" placeholder="Phone" required>

    <textarea name="message" placeholder="Describe issue"></textarea>

    <button type="submit">Submit</button>
  </form>
</section>

<!-- SERVICE AREA -->
<section id="areas" class="section">
  <h2>Service Areas</h2>

  <p>Waterbury • Naugatuck • Meriden • Watertown • Oxford • Milford</p>

  <iframe src="https://maps.google.com/maps?q=Waterbury%20CT&z=10&output=embed"></iframe>
</section>

<!-- CONTACT -->
<section class="section">
  <h2>Contact</h2>

  <p>📞 203-819-8645</p>
  <p>✉️ robert@onyxtechsolutions.info</p>
</section>

<script>
function calc(){
  let val = document.getElementById("service").value;
  document.getElementById("price").innerText =
    val ? "Estimated: $" + val : "";
}
</script>

</body>
</html>
