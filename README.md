<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CellStart - ChronoNAD+ | Cellular Energy Revolution</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cabin:wght@400;600;700&family=Poppins:wght@400;600;700&family=Source+Sans+Pro:wght@400;600&display=swap" rel="stylesheet">

<style>
:root{
    --primary-blue:#002f5c;
    --secondary-blue:#0057a6;
    --accent-blue:#4a90e2;
    --light-blue:#e8f4fd;
    --white:#ffffff;
    --light-gray:#f8f9fa;
    --text-gray:#6c757d;
    --gradient:linear-gradient(135deg,#002f5c 0%,#0057a6 100%);
}
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Source Sans Pro',sans-serif;color:var(--secondary-blue);line-height:1.6;overflow-x:hidden;}
.container{max-width:1200px;margin:0 auto;padding:0 20px;}
nav{background:rgba(255,255,255,0.95);backdrop-filter:blur(10px);position:fixed;top:0;width:100%;z-index:1000;padding:1rem 0;box-shadow:0 2px 20px rgba(0,47,92,0.1);}
.nav-container{display:flex;justify-content:space-between;align-items:center;}
.logo{font-family:'Cabin',sans-serif;font-weight:700;font-size:1.8rem;color:var(--primary-blue);text-decoration:none;}
.nav-links{display:flex;list-style:none;gap:2rem;}
.nav-links a{color:var(--secondary-blue);text-decoration:none;font-weight:600;transition:color 0.3s ease;}
.nav-links a:hover{color:var(--accent-blue);}
/* Hero Section */
.hero{background:var(--gradient);min-height:100vh;display:flex;align-items:center;position:relative;overflow:hidden;}
.hero::before{content:'';position:absolute;top:-50%;right:-20%;width:100%;height:200%;background:radial-gradient(circle,rgba(255,255,255,0.1)0%,transparent 70%);transform:rotate(-15deg);}
.hero-content{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:center;position:relative;z-index:2;}
.hero-text h1{font-family:'Poppins',sans-serif;font-weight:700;font-size:3.5rem;color:var(--white);margin-bottom:1rem;line-height:1.2;}
.hero-text .subtitle{font-family:'Poppins',sans-serif;font-weight:600;font-size:1.5rem;color:rgba(255,255,255,0.9);}
.hero-text p{font-size:1.2rem;color:rgba(255,255,255,0.8);margin-bottom:2rem;line-height:1.8;}
.cta-button{display:inline-block;background:var(--white);color:var(--primary-blue);padding:1rem 2.5rem;border-radius:50px;text-decoration:none;font-weight:600;font-size:1.1rem;transition:all 0.3s ease;box-shadow:0 8px 25px rgba(0,47,92,0.3);}
.cta-button:hover{transform:translateY(-3px);box-shadow:0 12px 35px rgba(0,47,92,0.4);}
.hero-visual{display:flex;justify-content:center;align-items:center;}
.product-showcase{position:relative;width:300px;height:400px;background:rgba(255,255,255,0.1);backdrop-filter:blur(10px);border-radius:20px;display:flex;align-items:center;justify-content:center;border:1px solid rgba(255,255,255,0.2);}
.product-icon{width:120px;height:120px;background:var(--white);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:3rem;color:var(--primary-blue);box-shadow:0 20px 40px rgba(0,47,92,0.3);}
/* Features Section */
.features{padding:6rem 0;background:var(--light-gray);}
.section-header{text-align:center;margin-bottom:4rem;}
.section-header h2{font-family:'Poppins',sans-serif;font-weight:700;font-size:2.5rem;color:var(--primary-blue);margin-bottom:1rem;}
.section-header p{font-size:1.2rem;color:var(--text-gray);max-width:600px;margin:0 auto;}
.features-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:2rem;}
.feature-card{background:var(--white);padding:2.5rem;border-radius:15px;text-align:center;box-shadow:0 10px 30px rgba(0,47,92,0.08);transition:transform 0.3s ease,box-shadow 0.3s ease;}
.feature-card:hover{transform:translateY(-5px);box-shadow:0 20px 50px rgba(0,47,92,0.15);}
.feature-icon{width:80px;height:80px;background:var(--light-blue);border-radius:50%;display:flex;align-items:center;justify-content:center;margin:0 auto 1.5rem;font-size:2rem;color:var(--secondary-blue);}
.feature-card h3{font-family:'Cabin',sans-serif;font-weight:600;font-size:1.4rem;color:var(--primary-blue);margin-bottom:1rem;}
.feature-card p{color:var(--text-gray);font-size:1rem;}
/* Portfolio / Slider */
.portfolio{padding:6rem 0;background:var(--light-gray);}
.slider{position:relative;overflow:hidden;border-radius:15px;box-shadow:0 10px 30px rgba(0,47,92,0.08);}
.slides{display:flex;transition:transform 0.5s ease-in-out;}
.slide{min-width:100%;flex-shrink:0;}
.slide img{width:100%;display:block;border-radius:15px;}
.prev,.next{position:absolute;top:50%;transform:translateY(-50%);background:rgba(0,87,166,0.7);color:#fff;border:none;font-size:2rem;padding:0.5rem 1rem;cursor:pointer;border-radius:50%;z-index:10;transition:0.3s;}
.prev:hover,.next:hover{background:rgba(0,87,166,0.9);}
.prev{left:15px;} .next{right:15px;}
/* Science Section */
.science{padding:6rem 0;background:var(--white);}
.science-content{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:center;}
.science-text h2{font-family:'Poppins',sans-serif;font-weight:700;font-size:2.5rem;color:var(--primary-blue);margin-bottom:1.5rem;}
.science-stats{display:grid;grid-template-columns:repeat(2,1fr);gap:1.5rem;margin-top:2rem;}
.stat-item{text-align:center;padding:1.5rem;background:var(--light-blue);border-radius:10px;}
.stat-number{font-family:'Poppins',sans-serif;font-weight:700;font-size:2rem;color:var(--primary-blue);display:block;}
.stat-label{font-size:0.9rem;color:var(--text-gray);margin-top:0.5rem;}
.science-visual{background:var(--gradient);border-radius:20px;height:400px;display:flex;align-items:center;justify-content:center;color:var(--white);font-size:4rem;}
/* CTA Section */
.final-cta{padding:4rem 0;background:var(--gradient);text-align:center;}
.final-cta h2{font-family:'Poppins',sans-serif;font-weight:700;font-size:2.5rem;color:var(--white);margin-bottom:1rem;}
.final-cta p{font-size:1.2rem;color:rgba(255,255,255,0.9);margin-bottom:2rem;max-width:600px;margin-left:auto;margin-right:auto;}
/* Footer */
footer{background:var(--primary-blue);color:var(--white);text-align:center;padding:2rem 0;}
/* Mobile */
@media(max-width:768px){.nav-links{display:none;}.hero-content{grid-template-columns:1fr;text-align:center;gap:2rem;}.hero-text h1{font-size:2.5rem;}.science-content{grid-template-columns:1fr;gap:2rem;}.science-stats{grid-template-columns:1fr;}.container{padding:0 15px;}}
@media(max-width:480px){.hero{padding-top:2rem;}.hero-text h1{font-size:2rem;}.hero-text .subtitle{font-size:1.2rem;}.section-header h2{font-size:2rem;}.features-grid{grid-template-columns:1fr;}}
</style>
</head>
<body>
<!-- Navigation -->
<nav>
<div class="container">
<div class="nav-container">
<a href="#" class="logo">CellStart</a>
<ul class="nav-links">
<li><a href="#features">Benefits</a></li>
<li><a href="#portfolio">Portfolio</a></li>
<li><a href="#science">Science</a></li>
<li><a href="#contact">Contact</a></li>
</ul>
</div>
</div>
</nav>

<!-- Hero -->
<section class="hero">
<div class="container">
<div class="hero-content">
<div class="hero-text">
<h1>Unlock Your<br><span class="subtitle">Cellular Potential</span></h1>
<p>ChronoNAD+ represents the next generation of cellular energy support. Our scientifically-formulated NAD+ precursor helps restore youthful cellular function, supporting energy, focus, and longevity from within.</p>
<a href="#" class="cta-button">Start Your Journey</a>
</div>
<div class="hero-visual">
<div class="product-showcase"><div class="product-icon">⚡</div></div>
</div>
</div>
</div>
</section>

<!-- Features -->
<section class="features" id="features">
<div class="container">
<div class="section-header">
<h2>Why ChronoNAD+ Works</h2>
<p>Experience the transformative power of optimized cellular energy with our advanced NAD+ support formula</p>
</div>
<div class="features-grid">
<div class="feature-card">
<div class="feature-icon">🧬</div>
<h3>Enhanced Cellular Energy</h3>
<p>Boost your cellular powerhouses with bioavailable NAD+ precursors that support mitochondrial function and ATP production for sustained energy throughout the day.</p>
</div>
<div class="feature-card">
<div class="feature-icon">🧠</div>
<h3>Cognitive Clarity</h3>
<p>Support brain health and mental clarity with ingredients that promote neuronal function and protect against oxidative stress for sharper focus and memory.</p>
</div>
<div class="feature-card">
<div class="feature-icon">🌟</div>
<h3>Healthy Aging Support</h3>
<p>Activate longevity pathways naturally with scientifically-backed compounds that support cellular repair mechanisms and promote graceful aging.</p>
</div>
</div>
</div>
</section>

<!-- Portfolio / Slider -->
<section class="portfolio" id="portfolio">
<div class="container">
<div class="section-header">
<h2>ChronoNAD+ Visuals</h2>
<p>Explore product images, lifestyle shots, and illustrations highlighting ChronoNAD+ benefits.</p>
</div>
<div class="slider">
<div class="slides">
<div class="slide"><img src="C:\Users\ratho\OneDrive\Desktop\intern.html2\image copy 2.png" alt="ChronoNAD+ 1"></div>
<div class="slide"><img src="C:\Users\ratho\OneDrive\Desktop\intern.html2\image copy 3.png" alt="ChronoNAD+ 2"></div>
<div class="slide"><img src="C:\Users\ratho\OneDrive\Desktop\intern.html2\image copy.png" alt="ChronoNAD+ 3"></div>
<div class="slide"><img src="C:\Users\ratho\OneDrive\Desktop\intern.html2\image.png" alt="ChronoNAD+ 4"></div>
</div>
<button class="prev">&#10094;</button>
<button class="next">&#10095;</button>
</div>
</div>
</section>

<!-- Science -->
<section class="science" id="science">
<div class="container">
<div class="science-content">
<div class="science-text">
<h2>Backed by Science</h2>
<p>ChronoNAD+ is formulated based on cutting-edge research in cellular biology and longevity science. Our proprietary blend combines the most effective NAD+ precursors with complementary compounds for maximum bioavailability and effectiveness.</p>
<div class="science-stats">
<div class="stat-item"><span class="stat-number">500mg</span><div class="stat-label">NMN per serving</div></div>
<div class="stat-item"><span class="stat-number">98%</span><div class="stat-label">Purity tested</div></div>
<div class="stat-item"><span class="stat-number">30</span><div class="stat-label">Day supply</div></div>
<div class="stat-item"><span class="stat-number">3rd</span><div class="stat-label">Party verified</div></div>
</div>
</div>
<div class="science-visual">🔬</div>
</div>
</div>
</section>

<!-- CTA -->
<section class="final-cta">
<div class="container">
<h2>Ready to Transform Your Energy?</h2>
<p>Join thousands of customers who have already experienced the ChronoNAD+ difference. Start your journey to optimized cellular health today.</p>
<a href="#" class="cta-button">Order ChronoNAD+ Now</a>
</div>
</section>

<!-- Footer -->
<footer>
<div class="container">
<p>&copy; 2024 CellStart. All rights reserved. | Statements have not been evaluated by the FDA.</p>
</div>
</footer>

<script>
// Smooth scrolling
document.querySelectorAll('a[href^="#"]').forEach(anchor=>{
anchor.addEventListener('click',function(e){
    e.preventDefault();
    const target=document.querySelector(this.getAttribute('href'));
    if(target){target.scrollIntoView({behavior:'smooth',block:'start'});}
});
});

// Slider
let slideIndex=0;
const slides=document.querySelectorAll('.slide');
const totalSlides=slides.length;
const sliderContainer=document.querySelector('.slides');
document.querySelector('.next').addEventListener('click',()=>{slideIndex=(slideIndex+1)%totalSlides;updateSlider();});
document.querySelector('.prev').addEventListener('click',()=>{slideIndex=(slideIndex-1+totalSlides)%totalSlides;updateSlider();});
function updateSlider(){sliderContainer.style.transform=`translateX(-${slideIndex*100}%)`;}
setInterval(()=>{slideIndex=(slideIndex+1)%totalSlides;updateSlider();},5000);

// Scroll animation
const observerOptions={threshold:0.1,rootMargin:'0px 0px -50px 0px'};
const observer=new IntersectionObserver(function(entries){
entries.forEach(entry=>{if(entry.isIntersecting){entry.target.style.opacity='1';entry.target.style.transform='translateY(0)';}});
},observerOptions);
document.querySelectorAll('.feature-card, .science-text, .science-visual').forEach(el=>{el.style.opacity='0';el.style.transform='translateY(30px)';el.style.transition='all 0.6s ease-out';observer.observe(el);});
</script>
</body>
</html>
