<html lang="vi">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Coffee Toss</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
scroll-behavior:smooth;
}

body{
background:linear-gradient(-45deg,#f6f1ea,#fff8f0,#f8efe5,#f6f1ea);
background-size:400% 400%;
animation:bgMove 12s ease infinite;
overflow-x:hidden;
color:#2b2b2b;
}

@keyframes bgMove{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

/* FLOATING COFFEE */

.beans span{
position:fixed;
font-size:28px;
opacity:.15;
z-index:-1;
animation:floatBean linear infinite;
}

.beans span:nth-child(1){
left:5%;
animation-duration:15s;
}

.beans span:nth-child(2){
left:20%;
animation-duration:20s;
animation-delay:2s;
}

.beans span:nth-child(3){
left:40%;
animation-duration:17s;
animation-delay:4s;
}

.beans span:nth-child(4){
left:60%;
animation-duration:22s;
animation-delay:1s;
}

.beans span:nth-child(5){
left:80%;
animation-duration:18s;
animation-delay:6s;
}

.beans span:nth-child(6){
left:92%;
animation-duration:25s;
animation-delay:3s;
}

@keyframes floatBean{
0%{
top:110%;
transform:rotate(0deg);
}
100%{
top:-10%;
transform:rotate(360deg);
}
}

/* NAV */

nav{
position:fixed;
top:0;
width:100%;
padding:15px 40px;
display:flex;
justify-content:space-between;
align-items:center;
background:rgba(0,0,0,.45);
backdrop-filter:blur(10px);
z-index:999;
transition:.4s;
}

nav.scrolled{
background:#1e120b;
}

nav h1{
color:#fff;
font-size:28px;
}

nav a{
color:#fff;
text-decoration:none;
margin-left:20px;
font-size:14px;
transition:.3s;
}

nav a:hover{
color:#c58b45;
}

/* HERO */

.hero{
height:100vh;
background:
linear-gradient(rgba(0,0,0,.6),rgba(0,0,0,.6)),
url('https://images.unsplash.com/photo-1442512595331-e89e73853f31?q=80&w=1600');
background-size:cover;
background-position:center;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
position:relative;
overflow:hidden;
}

.hero-content{
color:#fff;
animation:fadeUp 1.5s ease;
position:relative;
}

.hero h2{
font-size:70px;
animation:glow 2s infinite alternate;
}

.hero p{
margin-top:15px;
font-size:18px;
opacity:.9;
}

@keyframes glow{
from{
text-shadow:0 0 10px #c58b45;
}
to{
text-shadow:
0 0 20px #c58b45,
0 0 40px #c58b45;
}
}

@keyframes fadeUp{
from{
opacity:0;
transform:translateY(50px);
}
to{
opacity:1;
transform:translateY(0);
}
}

/* STEAM */

.steam{
position:absolute;
width:10px;
height:80px;
background:rgba(255,255,255,.25);
border-radius:50%;
top:35%;
left:50%;
filter:blur(8px);
animation:steam 3s infinite;
}

.s2{
left:47%;
animation-delay:1s;
}

.s3{
left:53%;
animation-delay:2s;
}

@keyframes steam{
0%{
opacity:0;
transform:translateY(0);
}
50%{
opacity:1;
}
100%{
opacity:0;
transform:translateY(-100px);
}
}

/* BUTTON */

.btn{
display:inline-block;
margin-top:25px;
padding:14px 32px;
border:none;
border-radius:40px;
background:linear-gradient(135deg,#c58b45,#e2b36a);
color:#fff;
font-size:16px;
font-weight:600;
text-decoration:none;
cursor:pointer;
transition:.3s;
box-shadow:0 10px 20px rgba(0,0,0,.2);
animation:pulse 2s infinite;
}

.btn:hover{
transform:translateY(-4px);
}

@keyframes pulse{
0%{transform:scale(1);}
50%{transform:scale(1.04);}
100%{transform:scale(1);}
}

/* SECTION */

section{
max-width:1200px;
margin:auto;
padding:100px 20px;
}

.title{
text-align:center;
font-size:40px;
margin-bottom:50px;
color:#3b2415;
}

/* ABOUT */

.about{
display:grid;
grid-template-columns:1fr 1fr;
gap:50px;
align-items:center;
}

.about img{
width:100%;
border-radius:20px;
box-shadow:0 10px 30px rgba(0,0,0,.15);
transition:.4s;
}

.about img:hover{
transform:scale(1.03);
}

/* FILTER */

.filter{
text-align:center;
margin-bottom:35px;
}

.filter button{
padding:10px 18px;
border:none;
border-radius:30px;
margin:5px;
cursor:pointer;
background:#ddd;
transition:.3s;
font-weight:500;
}

.filter button.active,
.filter button:hover{
background:#c58b45;
color:white;
}

/* MENU */
.menu{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}

.card{
background:white;
border-radius:15px;
overflow:hidden;
box-shadow:0 8px 20px rgba(0,0,0,.08);
transition:.3s;
}
.card:hover{transform:translateY(-10px);}

.card img{
width:100%;
height:180px;
object-fit:cover;
}

.card-content{padding:15px;}

.price{
color:#c58b45;
font-weight:bold;
margin-top:8px;
}


/* BOOKING */

.booking{
max-width:500px;
margin:auto;
background:#fff;
padding:30px;
border-radius:20px;
box-shadow:0 10px 25px rgba(0,0,0,.1);
}

.booking input,
.booking textarea{
width:100%;
padding:14px;
margin-bottom:15px;
border-radius:12px;
border:1px solid #ddd;
font-size:15px;
outline:none;
transition:.3s;
}

.booking input:focus,
.booking textarea:focus{
border-color:#c58b45;
box-shadow:0 0 10px rgba(197,139,69,.3);
}

.booking textarea{
height:120px;
resize:none;
}

/* CONTACT */

.contact{
text-align:center;
}

.contact p{
margin:10px 0;
font-size:16px;
}

iframe{
width:100%;
height:350px;
border:none;
border-radius:18px;
margin-top:25px;
box-shadow:0 10px 25px rgba(0,0,0,.2);
}

/* FLOAT BUTTON */

.float{
position:fixed;
right:20px;
bottom:20px;
display:flex;
flex-direction:column;
gap:12px;
z-index:999;
}

.float a{
background:#c58b45;
color:#fff;
padding:14px 16px;
border-radius:50px;
text-decoration:none;
font-size:14px;
box-shadow:0 8px 20px rgba(0,0,0,.2);
transition:.3s;
}

.float a:hover{
transform:scale(1.08);
}

/* FOOTER */

footer{
background:#1e120b;
padding:25px;
text-align:center;
color:#fff;
margin-top:50px;
}

/* MOBILE */

@media(max-width:768px){

nav{
flex-direction:column;
gap:10px;
padding:15px;
}

.hero h2{
font-size:42px;
}

.about{
grid-template-columns:1fr;
}

.title{
font-size:32px;
}

}

/* HIDE */

.hide{
display:none;
}

</style>
</head>

<body>

<!-- FLOATING ICONS -->

<div class="beans">
<span>☕</span>
<span>☕</span>
<span>☕</span>
<span>☕</span>
<span>☕</span>
<span>☕</span>
</div>

<!-- NAV -->

<nav id="navbar">

<h1>CF Toss</h1>

<div>
<a href="#about">Giới thiệu</a>
<a href="#menu">Menu</a>
<a href="#booking">Đặt bàn</a>
<a href="#contact">Liên hệ</a>
</div>

</nav>

<!-- HERO -->

<section class="hero">

<div class="hero-content">

<div class="steam"></div>
<div class="steam s2"></div>
<div class="steam s3"></div>

<h2>☕ Coffee Toss</h2>

<p>
Cà phê phin Việt Nam – Đậm đà & hiện đại
</p>

<a href="#menu" class="btn">
Khám phá menu
</a>

</div>

</section>

<!-- ABOUT -->

<section id="about">

<h2 class="title">
Về Coffee Toss
</h2>

<div class="about">

<img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93">

<div>

<p>
Coffee Toss là quán cà phê phong cách hiện đại nhưng vẫn giữ trọn hương vị cà phê phin Việt Nam truyền thống.
</p>

<br>

<p>
Không gian yên tĩnh phù hợp học tập, làm việc và thư giãn.
</p>

<br>

<p>
Mỗi ly cà phê là một khoảnh khắc chậm lại giữa cuộc sống vội vã.
</p>

</div>

</div>

</section>

<!-- MENU -->


<!-- MENU FILTER -->
<section id="menu">
<h2 class="title">Menu nổi bật</h2>

<div class="filter">
<button class="active" onclick="filterMenu('all')">Tất cả</button>
<button onclick="filterMenu('coffee')">Cà phê</button>
<button onclick="filterMenu('tea')">Trà</button>
<button onclick="filterMenu('cake')">Bánh</button>
</div>

<div class="menu">

<!-- COFFEE -->
<div class="card coffee">
<img src="https://images.unsplash.com/photo-1511920170033-f8396924c348">
<div class="card-content">
<h3>Cà phê phin đen</h3>
<p>Đậm vị truyền thống</p>
<div class="price">29.000đ</div>
</div>
</div>

<div class="card coffee">
<img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93">
<div class="card-content">
<h3>Cà phê sữa đá</h3>
<p>Ngọt béo cân bằng</p>
<div class="price">35.000đ</div>
</div>
</div>

<div class="card coffee">
<img src="https://images.unsplash.com/photo-1461023058943-07fcbe16d735">
<div class="card-content">
<h3>Bạc xỉu</h3>
<p>Nhẹ nhàng dễ uống</p>
<div class="price">39.000đ</div>
</div>
</div>

<!-- TEA -->
<div class="card tea">
<img src="https://images.unsplash.com/photo-1551024709-8f23befc6f87">
<div class="card-content">
<h3>Trà hoa quả</h3>
<p>Thanh mát tự nhiên</p>
<div class="price">39.000đ</div>
</div>
</div>

<div class="card tea">
<img src="https://images.unsplash.com/photo-1544145945-f90425340c7e">
<div class="card-content">
<h3>Nước ép</h3>
<p>Giải khát sảng khoái</p>
<div class="price">25.000đ</div>
</div>
</div>

<!-- CAKE -->
<div class="card cake">
<img src="https://images.unsplash.com/photo-1555507036-ab1f4038808a">
<div class="card-content">
<h3>Croissant</h3>
<p>Giòn xốp thơm bơ</p>
<div class="price">25.000đ</div>
</div>
</div>

<div class="card cake">
<img src="https://images.unsplash.com/photo-1563805042-7684c019e1cb">
<div class="card-content">
<h3>Bánh mousse</h3>
<p>Ngọt nhẹ tan chảy</p>
<div class="price">45.000đ</div>
</div>
</div>

</div>
</section>

<!-- BOOKING -->

<section id="booking">

<h2 class="title">
Đặt bàn nhanh
</h2>

<div class="booking">

<input type="text" placeholder="Tên của bạn">

<input type="tel" placeholder="Số điện thoại">

<textarea placeholder="Ghi chú..."></textarea>

<a href="https://zalo.me/0989098098" class="btn" target="_blank">
Gửi yêu cầu
</a>

</div>

</section>

<!-- CONTACT -->

<section id="contact">

<h2 class="title">
Liên hệ
</h2>

<div class="contact">

<p>📍 144 Xuân Thủy, Cầu Giấy, Hà Nội</p>

<p>📞 0989098098</p>

<p>🕒 07:00 – 22:00</p>

<iframe
src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3723.8957756946384!2d105.77971787391395!3d21.03685588061443!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3135ab4aaba35b15%3A0x67f4d40e3636c6ed!2zdHJvbmcga2h1w7RuIHZpw6puIHRyxrDhu51uZywgxJDhuqFpIGjhu41jIFF14buRYyBnaWEgSMOgIE7hu5lpLzE0NCDEkC4gWHXDom4gVGjhu6d5LCBD4bqndSBHaeG6pXksIEjDoCBO4buZaSAxMDAwMDAsIFZp4buHdCBOYW0!5e0!3m2!1svi!2s!4v1780229005207!5m2!1svi!2s"
allowfullscreen=""
loading="lazy">
</iframe>

</div>

</section>

<!-- FLOAT -->

<div class="float">

<a href="tel:0989098098">
📞 Gọi
</a>

<a href="https://zalo.me/0989098098" target="_blank">
💬 Zalo
</a>

</div>

<!-- FOOTER -->

<footer>
2026 Coffee Toss ☕
</footer>

<script>

/* FILTER */

function filterMenu(type,event){

let cards=document.querySelectorAll('.card');
let buttons=document.querySelectorAll('.filter button');

buttons.forEach(btn=>{
btn.classList.remove('active');
});

event.target.classList.add('active');

cards.forEach(card=>{

if(type==='all'){
card.classList.remove('hide');
}else{
card.classList.toggle(
'hide',
!card.classList.contains(type)
);
}

});

}

/* NAVBAR */

window.addEventListener('scroll',()=>{

const nav=document.getElementById('navbar');

if(window.scrollY>80){
nav.classList.add('scrolled');
}else{
nav.classList.remove('scrolled');
}

});

/* SCROLL ANIMATION */

const cards=document.querySelectorAll('.card');

function revealCards(){

cards.forEach(card=>{

const top=card.getBoundingClientRect().top;

if(top<window.innerHeight-80){
card.classList.add('show');
}

});

}

window.addEventListener('scroll',revealCards);

revealCards();

</script>

</body>
</html>

