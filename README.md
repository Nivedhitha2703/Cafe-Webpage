# Cafe-Webpage
A simple webpage created for cafe using HTML and CSS
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Brew & Bliss Cafe</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    scroll-behavior:smooth;
}

body{
    font-family:'Poppins',sans-serif;
    background:#f5f0e6;
    color:#333;
    transition:0.5s;
}

/* Navbar */

nav{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:20px 10%;
    background:#2c1810;
    position:sticky;
    top:0;
    z-index:1000;
}

.logo{
    color:white;
    font-size:28px;
    font-family:'Playfair Display',serif;
}

nav ul{
    list-style:none;
    display:flex;
    gap:25px;
}

nav ul li a{
    text-decoration:none;
    color:white;
    font-weight:500;
}

nav ul li a:hover{
    color:#d4a373;
}

.toggle{
    cursor:pointer;
    color:white;
    font-size:20px;
}

/* Hero */

.hero{
    height:100vh;
    background:
    linear-gradient(rgba(0,0,0,.5),
    rgba(0,0,0,.5)),
    url("https://images.unsplash.com/photo-1509042239860-f550ce710b93");
    background-size:cover;
    background-position:center;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    color:white;
}

.hero-content h1{
    font-size:60px;
    margin-bottom:15px;
    font-family:'Playfair Display',serif;
}

.hero-content p{
    font-size:22px;
    margin-bottom:25px;
}

.btn{
    padding:12px 28px;
    border:none;
    background:#c68e52;
    color:white;
    border-radius:30px;
    cursor:pointer;
    text-decoration:none;
}

.btn:hover{
    background:#a36c33;
}

/* About */

.about{
    padding:80px 10%;
    display:flex;
    gap:50px;
    align-items:center;
    flex-wrap:wrap;
}

.about img{
    width:450px;
    max-width:100%;
    border-radius:20px;
}

.about-text{
    flex:1;
}

.about-text h2{
    margin-bottom:20px;
    font-size:40px;
}

.about-text p{
    line-height:1.8;
}

/* Menu */

.menu{
    padding:80px 10%;
    text-align:center;
}

.menu h2{
    margin-bottom:40px;
    font-size:40px;
}

.menu-container{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:30px;
}

.card{
    background:white;
    border-radius:20px;
    overflow:hidden;
    transition:.4s;
    box-shadow:0 5px 15px rgba(0,0,0,.1);
}

.card:hover{
    transform:translateY(-10px);
}

.card img{
    width:100%;
    height:220px;
    object-fit:cover;
}

.card h3{
    margin:15px 0;
}

.card p{
    margin-bottom:20px;
}

/* Gallery */

.gallery{
    padding:80px 10%;
    text-align:center;
}

.gallery-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
}

.gallery-grid img{
    width:100%;
    border-radius:15px;
    transition:.4s;
}

.gallery-grid img:hover{
    transform:scale(1.05);
}

/* Reviews */

.reviews{
    padding:80px 10%;
    text-align:center;
}

.review-box{
    background:white;
    padding:30px;
    border-radius:15px;
    margin:20px auto;
    max-width:600px;
}

/* Reservation */

.booking{
    padding:80px 10%;
    text-align:center;
}

form{
    max-width:500px;
    margin:auto;
}

input{
    width:100%;
    padding:15px;
    margin:10px 0;
    border:1px solid #ccc;
    border-radius:10px;
}

/* Footer */

footer{
    background:#2c1810;
    color:white;
    text-align:center;
    padding:30px;
}

/* Dark Mode */

.dark{
    background:#121212;
    color:white;
}

.dark .card,
.dark .review-box{
    background:#1f1f1f;
}

</style>
</head>

<body>

<nav>
    <div class="logo">☕ Brew & Bliss</div>

    <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#gallery">Gallery</a></li>
        <li><a href="#booking">Reserve</a></li>
    </ul>

    <div class="toggle" onclick="darkMode()">🌙</div>
</nav>

<section class="hero">
    <div class="hero-content">
        <h1>Brew & Bliss Cafe</h1>
        <p>Crafted with Passion, Served with Love</p>
        <a href="#menu" class="btn">Explore Menu</a>
    </div>
</section>

<section class="about" id="about">

<img src="https://images.unsplash.com/photo-1495474472287-4d71bcdd2085">

<div class="about-text">
<h2>About Us</h2>

<p>
At Brew & Bliss Cafe, we serve freshly brewed coffee,
delicious pastries, and unforgettable moments.
Our warm atmosphere and handcrafted beverages
make every visit special.
</p>

</div>
</section>

<section class="menu" id="menu">

<h2>Our Specials</h2>

<div class="menu-container">

<div class="card">
<img src="https://images.unsplash.com/photo-1511920170033-f8396924c348">
<h3>Cappuccino</h3>
<p>₹149</p>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93">
<h3>Latte</h3>
<p>₹179</p>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1504674900247-0877df9cc836">
<h3>Chocolate Cake</h3>
<p>₹199</p>
</div>

</div>

</section>

<section class="gallery" id="gallery">

<h2>Gallery</h2>

<div class="gallery-grid">

<img src="https://images.unsplash.com/photo-1495474472287-4d71bcdd2085">

<img src="https://images.unsplash.com/photo-1445116572660-236099ec97a0">

<img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93">

<img src="https://images.unsplash.com/photo-1453614512568-c4024d13c247">

</div>

</section>

<section class="reviews">

<h2>Customer Reviews</h2>

<div class="review-box">
⭐⭐⭐⭐⭐
<p>"Best coffee experience ever!"</p>
</div>

<div class="review-box">
⭐⭐⭐⭐⭐
<p>"Amazing ambience and friendly staff."</p>
</div>

</section>

<section class="booking" id="booking">

<h2>Reserve a Table</h2>

<form>

<input type="text" placeholder="Your Name">

<input type="tel" placeholder="Phone Number">

<input type="date">

<input type="time">

<input type="number" placeholder="Guests">

<button class="btn">Reserve</button>

</form>

</section>

<footer>

<h3>Brew & Bliss Cafe</h3>

<p>📍 Coimbatore, India</p>
<p>📞 +91 9876543210</p>
<p>☕ Fresh Coffee Everyday</p>

</footer>

<script>

function darkMode(){
document.body.classList.toggle("dark");
}

</script>

</body>
</html>
