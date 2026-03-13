<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Swarnima Photography Portfolio</title>

<style>

body{
font-family:Arial, sans-serif;
margin:0;
background:#111;
color:white;
}

header{
background:black;
padding:15px;
display:flex;
justify-content:space-between;
align-items:center;
}

header h1{
margin:0;
}

nav a{
color:white;
text-decoration:none;
margin:15px;
font-size:18px;
}

nav a:hover{
color:orange;
}

.hero{
height:70vh;
display:flex;
justify-content:center;
align-items:center;
font-size:40px;
background:url('https://images.unsplash.com/photo-1500530855697-b586d89ba3ee') center/cover;
}

section{
padding:50px;
text-align:center;
}

.gallery{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:15px;
}

.gallery img{
width:100%;
height:250px;
object-fit:cover;
border-radius:10px;
cursor:pointer;
transition:0.3s;
}

.gallery img:hover{
transform:scale(1.05);
}

/* Popup Lightbox */

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
}

.lightbox span{
position:absolute;
top:20px;
right:40px;
font-size:40px;
cursor:pointer;
color:white;
}

footer{
background:black;
padding:10px;
text-align:center;
}

</style>
</head>

<body>

<header>
<h1>Swarnima Photography</h1>

<nav>
<a href="#home">Home</a>
<a href="#gallery">Gallery</a>
<a href="#about">About</a>
<a href="#contact">Contact</a>
</nav>
</header>

<div class="hero" id="home">
Capturing Beautiful Moments
</div>

<section id="gallery">
<h2>My Gallery</h2>

<div class="gallery">

<img src="https://images.unsplash.com/photo-1503023345310-bd7c1de61c7d">
<img src="https://images.unsplash.com/photo-1492724441997-5dc865305da7">
<img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470">
<img src="https://images.unsplash.com/photo-1500534314209-a25ddb2bd429">
<img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb">
<img src="https://images.unsplash.com/photo-1472214103451-9374bd1c798e">

</div>

</section>

<section id="about">

<h2>About Me</h2>

<p>
Hello! My name is Swarnima. I am passionate about photography and love capturing
nature, people and special moments through my lens.
</p>

</section>

<section id="contact">

<h2>Contact</h2>

<p>Email: swarnima@email.com</p>

</section>

<footer>

<p>© 2026 Swarnima Photography Portfolio</p>

</footer>

<!-- Lightbox popup -->

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
