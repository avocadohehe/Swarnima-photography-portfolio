<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Swarnima | Photography Portfolio</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
background:#0f0f0f;
color:white;
scroll-behavior:smooth;
}

/* Header */

header{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 60px;
background:black;
position:sticky;
top:0;
z-index:1000;
}

.logo{
font-size:26px;
font-weight:600;
letter-spacing:1px;
}

nav a{
margin-left:30px;
text-decoration:none;
color:white;
font-size:16px;
transition:0.3s;
}

nav a:hover{
color:#f39c12;
}

/* Hero */

.hero{
height:90vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
background:url("https://images.unsplash.com/photo-1500530855697-b586d89ba3ee") center/cover;
}

.hero h1{
font-size:60px;
letter-spacing:3px;
}

.hero p{
font-size:20px;
margin-top:10px;
}

/* Section */

section{
padding:80px 10%;
}

.section-title{
text-align:center;
font-size:36px;
margin-bottom:40px;
}

/* Gallery */

.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}

.gallery img{
width:100%;
height:260px;
object-fit:cover;
border-radius:12px;
cursor:pointer;
transition:0.4s;
}

.gallery img:hover{
transform:scale(1.07);
}

/* Lightbox */

.lightbox{
display:none;
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.9);
justify-content:center;
align-items:center;
}

.lightbox img{
max-width:90%;
max-height:90%;
border-radius:10px;
}

.lightbox span{
position:absolute;
top:25px;
right:40px;
font-size:40px;
cursor:pointer;
}

/* About */

.about{
max-width:700px;
margin:auto;
text-align:center;
line-height:1.8;
font-size:18px;
}

/* Contact */

.contact{
text-align:center;
}

.contact p{
font-size:18px;
}

/* Footer */

footer{
text-align:center;
padding:20px;
background:black;
}

</style>
</head>

<body>

<header>

<div class="logo">Swarnima Photography</div>

<nav>
<a href="#home">Home</a>
<a href="#gallery">Gallery</a>
<a href="#about">About</a>
<a href="#contact">Contact</a>
</nav>

</header>

<!-- Hero -->

<section class="hero" id="home">

<h1>Swarnima</h1>
<p>Capturing Moments Through My Lens</p>

</section>

<!-- Gallery -->

<section id="gallery">

<h2 class="section-title">My Photography</h2>

<div class="gallery">

<img src="https://images.unsplash.com/photo-1503023345310-bd7c1de61c7d">
<img src="https://images.unsplash.com/photo-1492724441997-5dc865305da7">
<img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470">
<img src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429">
<img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb">
<img src="https://images.unsplash.com/photo-1472214103451-9374bd1c798e">

</div>

</section>

<!-- About -->

<section id="about">

<h2 class="section-title">About Me</h2>

<div class="about">

<p>
Hello! I am Swarnima, a passionate photographer who loves capturing
nature, portraits, and creative moments. Photography allows me to tell
stories through images and preserve beautiful memories.
</p>

</div>

</section>

<!-- Contact -->

<section id="contact">

<h2 class="section-title">Contact</h2>

<div class="contact">

<p>Email: swarnima@email.com</p>
<p>Instagram: @swarnima.photography</p>

</div>

</section>

<footer>

<p>© 2026 Swarnima Photography Portfolio</p>

</footer>

<!-- Lightbox -->

<div class="lightbox" id="lightbox">

<span onclick="closeLightbox()">&times;</span>
<img id="lightbox-img">

</div>

<script>

const images = document.querySelectorAll(".gallery img");
const lightbox = document.getElementById("lightbox");
const lightboxImg = document.getElementById("lightbox-img");

images.forEach(img=>{
img.addEventListener("click",()=>{
lightbox.style.display="flex";
lightboxImg.src = img.src;
});
});

function closeLightbox(){
lightbox.style.display="none";
}

</script>

</body>
</html>
