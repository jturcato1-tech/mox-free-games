# mox-free-games
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ZONA GAMER PRO 🎮🔥</title>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"/>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
scroll-behavior:smooth;
}

body{
font-family:Segoe UI,sans-serif;
background:linear-gradient(180deg,#0a0a15,#111133,#0a0a15);
color:white;
overflow-x:hidden;
}

/* HEADER */
header{
position:sticky;
top:0;
z-index:1000;
background:rgba(0,0,0,.7);
backdrop-filter:blur(8px);
padding:15px;
text-align:center;
font-size:28px;
font-weight:bold;
color:#00f0ff;
box-shadow:0 0 15px #00f0ff;
}

/* NAV */
nav{
display:flex;
justify-content:center;
flex-wrap:wrap;
gap:15px;
padding:15px;
background:#111;
}

nav a{
color:white;
text-decoration:none;
padding:10px 15px;
border-radius:10px;
transition:.3s;
}

nav a:hover{
background:#8a2be2;
transform:translateY(-3px);
}

/* SECCIONES */
section{
padding:60px 30px;
min-height:100vh;
}

.hero{
text-align:center;
padding-top:80px;
}

.hero h1{
font-size:55px;
margin-bottom:20px;
color:#00f0ff;
text-shadow:0 0 20px #00f0ff;
}

.hero p{
font-size:20px;
margin-bottom:25px;
}

/* BOTONES */
button{
background:linear-gradient(90deg,#00f0ff,#8a2be2);
border:none;
padding:12px 20px;
border-radius:12px;
color:white;
font-weight:bold;
cursor:pointer;
transition:.3s;
margin:5px;
}

button:hover{
transform:scale(1.08);
box-shadow:0 0 15px #00f0ff;
}

/* TARJETAS */
.grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:25px;
margin-top:30px;
}

.card{
background:#181830;
padding:18px;
border-radius:18px;
box-shadow:0 0 10px rgba(0,240,255,.2);
transition:.3s;
}

.card:hover{
transform:translateY(-8px);
box-shadow:0 0 20px #8a2be2;
}

.card img{
width:100%;
height:220px;
object-fit:cover;
border-radius:15px;
margin-bottom:10px;
}

.card h3{
margin-bottom:10px;
color:#00f0ff;
}

/* STATS */
.stats{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
gap:20px;
margin-top:30px;
text-align:center;
}

.stat{
background:#181830;
padding:20px;
border-radius:15px;
}

.stat h2{
color:#00f0ff;
font-size:35px;
}

/* INPUT */
input{
padding:12px;
width:100%;
max-width:350px;
margin:8px 0;
border:none;
border-radius:10px;
}

/* QUIZ */
.option{
background:#222244;
padding:12px;
margin:10px 0;
border-radius:10px;
cursor:pointer;
transition:.3s;
}

.option:hover{
background:#8a2be2;
}

/* FOOTER */
footer{
text-align:center;
padding:25px;
background:#111;
color:#aaa;
}

/* TOP BUTTON */
#topBtn{
position:fixed;
bottom:20px;
right:20px;
display:none;
}
</style>
</head>

<body>

<header class="animate__animated animate__fadeInDown">
ZONA GAMER PRO 🎮🔥
</header>

<nav>
<a href="#inicio">Inicio</a>
<a href="#juegos">Juegos</a>
<a href="#trivia">Trivia</a>
<a href="#tienda">Tienda</a>
<a href="#cuenta">Cuenta</a>
</nav>

<!-- INICIO -->
<section id="inicio" class="hero">
<h1 class="animate__animated animate__zoomIn">Bienvenido Gamer 😎</h1>
<p>Tu portal definitivo para jugar, comprar y demostrar que no eres manco 💀</p>
<button onclick="document.getElementById('juegos').scrollIntoView()">Explorar</button>

<div class="stats">
<div class="stat">
<h2 id="num1">0</h2>
<p>Gamers conectados</p>
</div>

<div class="stat">
<h2 id="num2">0</h2>
<p>Juegos disponibles</p>
</div>

<div class="stat">
<h2 id="num3">0</h2>
<p>Retos completados</p>
</div>
</div>
</section>

<!-- JUEGOS -->
<section id="juegos">
<h1>🔥 Juegos Populares</h1>

<div class="grid">

<div class="card">
<img src="https://images.unsplash.com/photo-1542751371-adc38448a05e">
<h3>Fortnite</h3>
<p>Battle Royale donde todos construyen menos tú 😔</p>
<button onclick="fav('Fortnite')">❤️ Favorito</button>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1511512578047-dfb367046420">
<h3>Minecraft</h3>
<p>Bloques infinitos y horas sin tocar pasto.</p>
<button onclick="fav('Minecraft')">❤️ Favorito</button>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1493711662062-fa541adb3fc8">
<h3>Call of Duty</h3>
<p>Insultos en lobby y balazos gratis.</p>
<button onclick="fav('COD')">❤️ Favorito</button>
</div>

</div>
</section>

<!-- TRIVIA -->
<section id="trivia">
<h1>🧠 Trivia Gamer</h1>
<div id="quiz"></div>
<button onclick="next()">Siguiente</button>
<h2 id="resultado"></h2>
</section>

<!-- TIENDA -->
<section id="tienda">
<h1>🛒 Tienda Gamer</h1>

<div class="grid">

<div class="card">
<img src="https://images.unsplash.com/photo-1587202372775-e229f172b9d7">
<h3>Control Pro</h3>
<p>$899 MXN</p>
<button onclick="agregar('Control Pro')">Agregar</button>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1612287230202-1ff1d85d1bdf">
<h3>Headset RGB</h3>
<p>$1299 MXN</p>
<button onclick="agregar('Headset RGB')">Agregar</button>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1593305841991-05c297ba4575">
<h3>Teclado Mecánico</h3>
<p>$1499 MXN</p>
<button onclick="agregar('Teclado')">Agregar</button>
</div>

</div>

<h2 style="margin-top:25px;">Carrito</h2>
<ul id="carrito"></ul>
</section>

<!-- CUENTA -->
<section id="cuenta">
<h1>👤 Cuenta</h1>

<input type="text" id="usuario" placeholder="Usuario">
<br>
<input type="password" placeholder="Contraseña">
<br>
<button onclick="login()">Entrar</button>

<h2 id="saludo"></h2>
</section>

<footer>
Hecho por un gamer con estilo 😎🎮
</footer>

<button id="topBtn" onclick="window.scrollTo(0,0)">⬆️</button>

<script>
/* FAVORITOS */
function fav(juego){
alert(juego + " añadido a favoritos ❤️");
}

/* LOGIN */
function login(){
let user=document.getElementById("usuario").value;
document.getElementById("saludo").innerText="Bienvenido "+user+" 🔥";
}

/* CARRITO */
let carrito=[];

function agregar(item){
carrito.push(item);
render();
}

function render(){
let lista=document.getElementById("carrito");
lista.innerHTML="";
carrito.forEach(x=>{
let li=document.createElement("li");
li.innerText="🎮 "+x;
lista.appendChild(li);
});
}

/* QUIZ */
const preguntas=[
{q:"¿Qué juego usa bloques?",o:["COD","Minecraft","FIFA","Halo"],a:1},
{q:"¿Qué juego es battle royale?",o:["Fortnite","Mario","GTA","PES"],a:0},
{q:"¿Qué juego es shooter?",o:["Minecraft","COD","Roblox","Tetris"],a:1},
{q:"¿Mario usa qué color?",o:["Azul/Rojo","Negro","Verde","Morado"],a:0}
];

let i=0,score=0;

function cargar(){
let p=preguntas[i];
let html="<h2>"+p.q+"</h2>";
p.o.forEach((op,index)=>{
html+=`<div class="option" onclick="responder(${index})">${op}</div>`;
});
document.getElementById("quiz").innerHTML=html;
}

function responder(r){
if(r==preguntas[i].a) score++;
}

function next(){
i++;
if(i<preguntas.length){
cargar();
}else{
document.getElementById("quiz").innerHTML="";
document.getElementById("resultado").innerText="Puntaje final: "+score+" 🎯";
}
}
cargar();

/* CONTADORES */
function animar(id,fin){
let n=0;
let inter=setInterval(()=>{
n+=5;
document.getElementById(id).innerText=n;
if(n>=fin){
document.getElementById(id).innerText=fin;
clearInterval(inter);
}
},20);
}
animar("num1",500);
animar("num2",120);
animar("num3",999);

/* BOTON ARRIBA */
window.onscroll=function(){
document.getElementById("topBtn").style.display=
window.scrollY>300?"block":"none";
}
</script>

</body>
</html>
