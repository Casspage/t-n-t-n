<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Coffee Toss</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
/* CARD HIỆN KHI CUỘN */

.card{
opacity:0;
transform:translateY(40px);
transition:0.8s;
}

.card.show{
opacity:1;
transform:translateY(0);
}

/* NAVBAR ĐỔI MÀU */

/* NAV */
nav{
position:fixed;
top:0;
width:100%;
display:flex;
justify-content:space-between;
align-items:center;
padding:15px 40px;
background:rgba(0,0,0,.65);
backdrop-filter:blur(10px);
z-index:999;
}

nav h1{color:#fff;}
nav a{
color:#fff;
margin-left:18px;
text-decoration:none;
font-size:14px;
}
nav a:hover{color:#c58b45;}

/* HERO HIỆN MƯỢT */

.hero div{
animation:fadeUp 1.2s ease;
}

@keyframes fadeUp{
from{
opacity:0;
transform:translateY(40px);
}
to{
opacity:1;
transform:translateY(0);
}
}

/* NÚT PHÁT SÁNG */

.btn{
animation:pulse 2s infinite;
}

@keyframes pulse{
0%{
box-shadow:0 0 0 rgba(197,139,69,.4);
}
50%{
box-shadow:0 0 20px rgba(197,139,69,.8);
}
100%{
box-shadow:0 0 0 rgba(197,139,69,.4);
}
}
<style>

*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins,sans-serif;scroll-behavior:smooth;}

body{
background:#f6f1ea;
color:#2b2b2b;
}

/* NAV */
nav{
position:fixed;
top:0;
width:100%;
display:flex;
justify-content:space-between;
align-items:center;
padding:15px 40px;
background:rgba(0,0,0,.65);
backdrop-filter:blur(10px);
z-index:999;
}

nav h1{color:#fff;}
nav a{
color:#fff;
margin-left:18px;
text-decoration:none;
font-size:14px;
}
nav a:hover{color:#c58b45;}

.hero{
height:100vh;
background:
linear-gradient(rgba(0,0,0,.6),rgba(0,0,0,.6)),
url('https://images.unsplash.com/photo-1442512595331-e89e73853f31?q=80&w=1600');
background-size:cover;
background-position:center;
display:flex;
align-items:center;
justify-content:center;
text-align:center;
color:white;
padding:20px;
}

.hero h2{font-size:60px;}
.hero p{font-size:18px;margin-top:10px;opacity:.9;}

.btn{
display:inline-block;
margin-top:20px;
padding:12px 28px;
background:#c58b45;
color:white;
border-radius:40px;
text-decoration:none;
transition:.3s;
}
.btn:hover{transform:scale(1.05);}

/* SECTION */
section{
max-width:1100px;
margin:auto;
padding:100px 20px;
}

.title{
text-align:center;
font-size:36px;
margin-bottom:40px;
color:#3b2415;
}

/* ABOUT */
.about{
display:grid;
grid-template-columns:1fr 1fr;
gap:40px;
align-items:center;
}

.about img{
width:100%;
border-radius:15px;
}

/* FILTER */
.filter{
text-align:center;
margin-bottom:30px;
}

.filter button{
padding:10px 18px;
border:none;
border-radius:25px;
margin:5px;
cursor:pointer;
background:#ddd;
transition:.3s;
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
#booking{
  padding: 40px 20px;
  text-align: center;
}

#booking .title{
  font-size: 28px;
  margin-bottom: 20px;
}

.booking{
  max-width: 400px;
  margin: auto;
}

.booking input,
.booking textarea{
  width: 100%;
  padding: 12px 15px;
  margin-bottom: 12px;
  border: 1px solid #ddd;
  border-radius: 10px;
  outline: none;
  font-size: 15px;
  transition: 0.3s;
}

.booking input:focus,
.booking textarea:focus{
  border-color: #c58b45;
  box-shadow: 0 0 8px rgba(197,139,69,0.3);
}

.booking textarea{
  min-height: 100px;
  resize: none;
}

/* BUTTON */
.btn{
  display: inline-block;
  width: 100%;
  padding: 12px;
  background: linear-gradient(135deg, #c58b45, #e2b36a);
  color: #fff;
  border: none;
  border-radius: 10px;
  font-size: 16px;
  font-weight: 600;
  cursor: pointer;
  transition: 0.3s ease;
  box-shadow: 0 6px 15px rgba(0,0,0,0.15);
}

.btn:hover{
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(0,0,0,0.2);
}

.btn:active{
  transform: scale(0.98);
}
/* CONTACT */
.contact{
text-align:center;
}

iframe{
width:100%;
height:320px;
border:0;
border-radius:12px;
margin-top:20px;
box-shadow:0 10px 20px rgba(0,0,0,.2);
}

/* FLOAT BUTTON */
.float{
position:fixed;
bottom:20px;
right:20px;
display:flex;
flex-direction:column;
gap:10px;
}

.float a{
background:#c58b45;
color:white;
padding:12px 15px;
border-radius:50px;
text-decoration:none;
font-size:14px;
text-align:center;
}

/* FOOTER */
footer{
text-align:center;
padding:20px;
background:#1e120b;
color:white;
margin-top:40px;
}

/* MOBILE */
@media(max-width:768px){
.hero h2{font-size:38px;}
.about{grid-template-columns:1fr;}
nav{flex-direction:column;}
}

.hide{display:none;}
/* NAVBAR */

window.addEventListener("scroll",()=>{

const nav=document.querySelector("nav");

if(window.scrollY>80){
nav.classList.add("scrolled");
}else{
nav.classList.remove("scrolled");
}

});

/* CARD ANIMATION */

const cards=document.querySelectorAll(".card");

function revealCards(){

cards.forEach(card=>{

const top=card.getBoundingClientRect().top;

if(top < window.innerHeight-100){
card.classList.add("show");
}

});

}

window.addEventListener("scroll",revealCards);

revealCards();
</style>
</head>

<body>

<!-- NAV -->
<nav>
<h1>Coffee Toss</h1>
<div>
<a href="#about">Giới thiệu</a>
<a href="#menu">Menu</a>
<a href="#booking">Đặt bàn</a>
<a href="#contact">Liên hệ</a>
</div>
</nav>

<!-- HERO -->
<div class="hero">
<div>
<h2>☕ Coffee Toss</h2>
<p>Cà phê phin Việt Nam – Đậm đà & hiện đại</p>
<a href="#menu" class="btn">Khám phá menu</a>
</div>
</div>

<!-- ABOUT -->
<section id="about">
<h2 class="title">Về Coffee Toss</h2>

<div class="about">
<img src="https://images.unsplash.com/photo-1509042239860-f550ce710b93">

<div>
<p>
Coffee Toss là quán cà phê phong cách hiện đại nhưng giữ trọn hương vị cà phê phin Việt Nam truyền thống.
Không gian yên tĩnh, phù hợp học tập – làm việc – thư giãn.
</p>

<br>

<p>
Mỗi ly cà phê là một khoảnh khắc chậm lại giữa cuộc sống vội vã.
</p>
</div>

</div>
</section>

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
<h3>Trà đào cam sả</h3>
<p>Thanh mát tự nhiên</p>
<div class="price">39.000đ</div>
</div>
</div>

<div class="card tea">
<img src="https://images.unsplash.com/photo-1544145945-f90425340c7e">
<div class="card-content">
<h3>Trà chanh</h3>
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

<h2 class="title">Đặt bàn nhanh</h2>

<div class="booking">

<input type="text" placeholder="Tên của bạn">
<input type="tel" placeholder="Số điện thoại">
<textarea placeholder="Ghi chú..."></textarea>

<br><br>

<button class="btn" type="button">
    Gửi yêu cầu
</button>

</div>

</section>

<!-- CONTACT -->
<section id="contact">

<h2 class="title">Liên hệ</h2>

<div class="contact">

<p>📍 Coffee Toss - 144 Xuân Thủy, Cầu Giấy, Hà Nội</p>
<p>📞 0989098098</p>
<p>🕒 07:00 – 22:00</p>

 <div class="map-container">
    <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3723.8957756946384!2d105.77971787391395!3d21.03685588061443!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3135ab4aaba35b15%3A0x67f4d40e3636c6ed!2zdHJvbmcga2h1w7RuIHZpw6puIHRyxrDhu51uZywgxJDhuqFpIGjhu41jIFF14buRYyBnaWEgSMOgIE7hu5lpLzE0NCDEkC4gWHXDom4gVGjhu6d5LCBD4bqndSBHaeG6pXksIEjDoCBO4buZaSAxMDAwMDAsIFZp4buHdCBOYW0!5e0!3m2!1svi!2s!4v1780229005207!5m2!1svi!2s"
        width="100%"
        height="450"
        style="border:0;"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade">
    </iframe>
</div>

</div>

</section>

<!-- FLOAT -->
<div class="float">
<a href="tel:0989098098">📞 Gọi</a>
<a href="https://zalo.me/0989098098" target="_blank"> 💬Zalo
</a>
</div>

<!-- FOOTER -->
<footer>
2026 Coffee Toss
</footer>

<script>

function filterMenu(type){
let cards = document.querySelectorAll('.card');
let buttons = document.querySelectorAll('.filter button');

buttons.forEach(b=>b.classList.remove('active'));
event.target.classList.add('active');

cards.forEach(card=>{
if(type=='all'){
card.classList.remove('hide');
}else{
card.classList.toggle('hide', !card.classList.contains(type));
}
});
}

</script>

</body>
</html>
