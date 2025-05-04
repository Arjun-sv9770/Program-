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
