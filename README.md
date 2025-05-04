<!doctype html>
<html lang="en"> 
 <head> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>Menu Example</title> 
  <link rel="stylesheet" href="style.css"> 
 </head> 
 <body> <!-- Hamburger icon --> 
  <div class="menu-toggle" onclick="toggleMenu()">
    ☰ 
  </div> <!-- Side menu --> <!-- Side menu --> <!-- Side menu --> 
  <nav id="sideMenu" class="side-menu hidden"> 
   <ul> 
    <li><a href="#">Home</a></li> 
    <li><a href="#" onclick="showAbout()">About</a></li> 
    <li><a href="#" onclick="showContact()">Contact</a></li> 
   </ul> <!-- About Section --> 
   <div id="aboutInfo" class="info-box hidden"> 
    <h3>About Rambo</h3> 
    <p>Rambo is a dynamic and forward-thinking company committed to delivering innovative solutions and outstanding services in [your industry].</p> 
    <p>Founded with a vision to redefine excellence, Rambo combines passion, precision, and purpose to create impactful experiences for clients and communities alike.</p> 
    <p>Our team is driven by creativity, integrity, and a relentless pursuit of excellence. Whether it's through [products/services], strategic partnerships, or community engagement, Rambo strives to lead with purpose and deliver with pride.</p> 
    <h4>Mission</h4> 
    <p>To empower progress through innovation, quality, and customer satisfaction.</p> 
    <h4>Vision</h4> 
    <p>To become a recognized leader in [industry] by building sustainable and meaningful solutions.</p> 
    <h4>Core Values</h4> 
    <ul> 
     <li><strong>Innovation</strong> – We think ahead to deliver cutting-edge solutions.</li> 
     <li><strong>Integrity</strong> – We do what’s right, always.</li> 
     <li><strong>Excellence</strong> – We aim for the highest standards in everything we do.</li> 
     <li><strong>Customer Focus</strong> – Your success is our success.</li> 
    </ul> 
   </div> <!-- Contact Section --> 
   <div id="contactInfo" class="info-box hidden"> 
    <p><strong>Mobile:</strong> <a href="tel:9483979770">9483979770</a></p> 
    <p><strong>Address:</strong><br> NO 57, #27 Sherkhan Kote Village,<br> Chelur Taluk,<br> Chikkaballapur District </p> 
   </div> 
  </nav>
 </body>
</html>
csss
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

/* Hamburger icon */
.menu-toggle {
  font-size: 30px;
  padding: 15px;
  cursor: pointer;
  background: #333;
  color: white;
  width: fit-content;
}

/* Side menu styling */
.side-menu {
  position: fixed;
  top: 0;
  left: 0;
  background: #444;
  width: 200px;
  height: 100%;
  padding-top: 60px;
  transition: transform 0.3s ease;
}

.side-menu.hidden {
  transform: translateX(-100%);
}

.side-menu ul {
  list-style: none;
  padding: 0;
}

.side-menu li {
  margin: 20px;
}

.side-menu a {
  color: white;
  text-decoration: none;
  font-size: 18px;
}

main {
  margin-left: 20px;
  padding: 20px;
}
.contact-info {
  color: white;
  font-size: 14px;
  padding: 15px;
  border-top: 1px solid #666;
}

.contact-info a {
  color: #aee;
  text-decoration: none;
}

.hidden {
  display: none;
.info-box {
  color: white;
  font-size: 14px;
  padding: 15px;
  border-top: 1px solid #666;
  max-height: 60vh;
  overflow-y: auto;
}

.info-box a {
  color: #aee;
  text-decoration: none;
}

.hidden {
  display: none;
}

.info-box ul {
  margin-top: 10px;
  padding-left: 20px;
}
javascript 
function toggleMenu() {
  const menu = document.getElementById("sideMenu");
  menu.classList.toggle("hidden");

  // Add or remove the outside click listener
  if (!menu.classList.contains("hidden")) {
    document.addEventListener("click", outsideClickListener);
  } else {
    document.removeEventListener("click", outsideClickListener);
  }
}

function outsideClickListener(event) {
  const menu = document.getElementById("sideMenu");
  const toggle = document.querySelector(".menu-toggle");

  // If click is outside the menu and not on the toggle button
  if (!menu.contains(event.target) && !toggle.contains(event.target)) {
    menu.classList.add("hidden");
    document.removeEventListener("click", outsideClickListener);
  }
}function toggleMenu() {
  const menu = document.getElementById("sideMenu");
  menu.classList.toggle("hidden");

  // Close contact info if menu closes
  if (menu.classList.contains("hidden")) {
    document.getElementById("contactInfo").classList.add("hidden");
    document.removeEventListener("click", outsideClickListener);
  } else {
    document.addEventListener("click", outsideClickListener);
  }
}

function outsideClickListener(event) {
  const menu = document.getElementById("sideMenu");
  const toggle = document.querySelector(".menu-toggle");

  if (!menu.contains(event.target) && !toggle.contains(event.target)) {
    menu.classList.add("hidden");
    document.getElementById("contactInfo").classList.add("hidden");
    document.removeEventListener("click", outsideClickListener);
  }
}

function showContact() {
  document.getElementById("contactInfo").classList.toggle("hidden");
}function toggleMenu() {
  const menu = document.getElementById("sideMenu");
  menu.classList.toggle("hidden");

  if (menu.classList.contains("hidden")) {
    hideAllInfo();
    document.removeEventListener("click", outsideClickListener);
  } else {
    document.addEventListener("click", outsideClickListener);
  }
}

function outsideClickListener(event) {
  const menu = document.getElementById("sideMenu");
  const toggle = document.querySelector(".menu-toggle");

  if (!menu.contains(event.target) && !toggle.contains(event.target)) {
    menu.classList.add("hidden");
    hideAllInfo();
    document.removeEventListener("click", outsideClickListener);
  }
}

function hideAllInfo() {
  document.getElementById("contactInfo").classList.add("hidden");
  document.getElementById("aboutInfo").classList.add("hidden");
}

function showContact() {
  hideAllInfo();
  document.getElementById("contactInfo").classList.remove("hidden");
}

function showAbout() {
  hideAllInfo();
  document.getElementById("aboutInfo").classList.remove("hidden");
}
