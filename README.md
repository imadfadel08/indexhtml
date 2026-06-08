<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Movie Hub</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Tahoma,sans-serif;
}

body{
background:#141414;
color:white;
}

header{
background:linear-gradient(rgba(0,0,0,.5),rgba(0,0,0,.8)),
url("https://images.unsplash.com/photo-1489599849927-2ee91cede3ba?w=1600");
background-size:cover;
background-position:center;
height:70vh;
display:flex;
flex-direction:column;
justify-content:center;
padding:40px;
}

.logo{
font-size:40px;
font-weight:bold;
color:#e50914;
margin-bottom:20px;
}

.hero-title{
font-size:48px;
max-width:700px;
margin-bottom:15px;
}

.hero-text{
max-width:600px;
font-size:18px;
line-height:1.7;
}

.search-box{
padding:25px;
background:#181818;
}

.search{
width:100%;
max-width:600px;
padding:14px;
border:none;
border-radius:30px;
font-size:16px;
display:block;
margin:auto;
}

.section-title{
padding:25px;
font-size:28px;
}

.movies{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(240px,1fr));
gap:20px;
padding:0 25px 25px;
}

.movie{
background:#202020;
border-radius:12px;
overflow:hidden;
transition:.3s;
}

.movie:hover{
transform:scale(1.04);
}

.movie img{
width:100%;
height:350px;
object-fit:cover;
}

.info{
padding:15px;
}

.info h3{
margin-bottom:10px;
}

.rating{
color:gold;
font-weight:bold;
}

.desc{
margin-top:10px;
color:#ccc;
font-size:14px;
line-height:1.5;
}

footer{
text-align:center;
padding:30px;
background:#0f0f0f;
margin-top:20px;
}
</style>
</head>

<body>

<header>
<div class="logo">MOVIE HUB</div>
<h1 class="hero-title">اكتشف أفضل الأفلام العالمية</h1>
<p class="hero-text">
مكتبة أفلام بتصميم حديث مع البحث والتقييمات.
</p>
</header>

<div class="search-box">
<input
type="text"
class="search"
id="search"
placeholder="ابحث عن فيلم..."
>
</div>

<h2 class="section-title">الأفلام المميزة</h2>

<div class="movies">

<div class="movie">
<img src="https://upload.wikimedia.org/wikipedia/en/8/8a/Dark_Knight.jpg">
<div class="info">
<h3>The Dark Knight</h3>
<div class="rating">⭐ 9.0</div>
<div class="desc">باتمان يواجه الجوكر في واحدة من أشهر الأفلام.</div>
</div>
</div>

<div class="movie">
<img src="https://upload.wikimedia.org/wikipedia/en/7/7f/Inception_ver3.jpg">
<div class="info">
<h3>Inception</h3>
<div class="rating">⭐ 8.8</div>
<div class="desc">رحلة داخل الأحلام والأفكار المعقدة.</div>
</div>
</div>

<div class="movie">
<img src="https://upload.wikimedia.org/wikipedia/en/b/bc/Interstellar_film_poster.jpg">
<div class="info">
<h3>Interstellar</h3>
<div class="rating">⭐ 8.7</div>
<div class="desc">رحلة فضائية لإنقاذ مستقبل البشرية.</div>
</div>
</div>

<div class="movie">
<img src="https://upload.wikimedia.org/wikipedia/en/1/13/Avengers_Endgame_poster.jpg">
<div class="info">
<h3>Avengers: Endgame</h3>
<div class="rating">⭐ 8.4</div>
<div class="desc">المعركة الأخيرة ضد ثانوس.</div>
</div>
</div>

<div class="movie">
<img src="https://upload.wikimedia.org/wikipedia/en/f/f9/TheAvengers2012Poster.jpg">
<div class="info">
<h3>The Avengers</h3>
<div class="rating">⭐ 8.0</div>
<div class="desc">اجتماع أشهر أبطال مارفل.</div>
</div>
</div>

<div class="movie">
<img src="https://upload.wikimedia.org/wikipedia/en/c/c3/Spider-Man_No_Way_Home_poster.jpg">
<div class="info">
<h3>Spider-Man</h3>
<div class="rating">⭐ 8.2</div>
<div class="desc">مغامرة متعددة الأكوان للرجل العنكبوت.</div>
</div>
</div>

</div>

<footer>
Movie Hub © 2026
</footer>

<script>
const search=document.getElementById("search");

search.addEventListener("keyup",function(){

let value=this.value.toLowerCase();

document.querySelectorAll(".movie").forEach(movie=>{

let text=movie.innerText.toLowerCase();

movie.style.display=
text.includes(value)
? "block"
: "none";

});

});
</script>

</body>
</html>
