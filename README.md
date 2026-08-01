1️⃣🟢
<html lang="ckb" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>کرافا | CRAVA — جوسی تازە و سیبی فرای ترسقاو</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Lalezar&family=Vazirmatn:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#10150f;
    --surface:#182018;
    --surface2:#1e281e;
    --cream:#f5f1e4;
    --muted:#a7b3a2;
    --leaf:#3d8a49;
    --leaf-deep:#1f4a29;
    --leaf-bright:#5cb85c;
    --gold:#f2ae28;
    --gold-soft:#ffd873;
    --radius:18px;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background:var(--bg);
    color:var(--cream);
    font-family:'Vazirmatn', 'Tahoma', sans-serif;
    overflow-x:hidden;
    line-height:1.7;
  }
  .brand-font{ font-family:'Lalezar', 'Vazirmatn', sans-serif; letter-spacing:1px; }

  /* ---------- NAV ---------- */
  nav{
    position:fixed; top:0; right:0; left:0; z-index:50;
    display:flex; align-items:center; justify-content:space-between;
    padding:14px 6vw;
    background:linear-gradient(to bottom, rgba(16,21,15,.9), transparent);
    backdrop-filter:blur(6px);
  }
  nav .logo img{ height:34px; display:block; filter:drop-shadow(0 2px 8px rgba(0,0,0,.4)); }
  nav ul{ list-style:none; display:flex; gap:28px; }
  nav a{ color:var(--cream); text-decoration:none; font-size:.95rem; opacity:.85; transition:opacity .2s, color .2s; }
  nav a:hover{ opacity:1; color:var(--gold); }

  /* ---------- HERO ---------- */
  .hero{
    position:relative; height:100svh; width:100%;
    overflow:hidden;
    display:flex; align-items:center; justify-content:center;
    background:radial-gradient(ellipse at 50% 30%, #1a2418 0%, #10150f 70%);
  }
  #hero-canvas{ position:absolute; inset:0; width:100%; height:100%; touch-action:none; }
  .hero-copy{
    position:relative; z-index:5; text-align:center; pointer-events:none;
    padding-top:4vh;
  }
  .hero-copy h1{
    font-family:'Lalezar', sans-serif;
    font-size:clamp(3.2rem, 11vw, 7.5rem);
    color:var(--gold-soft);
    text-shadow:0 0 40px rgba(60,150,70,.45);
    line-height:1;
  }
  .hero-copy p{
    margin-top:10px;
    font-size:clamp(1rem,2.2vw,1.35rem);
    color:var(--muted);
  }
  .drag-hint{
    position:absolute; bottom:110px; right:0; left:0; z-index:5;
    text-align:center; font-size:.85rem; color:var(--muted); opacity:.85;
  }
  .scroll-cue{
    position:absolute; bottom:34px; right:0; left:0; z-index:5;
    display:flex; flex-direction:column; align-items:center; gap:6px;
    text-decoration:none; color:var(--cream); font-size:.85rem;
    animation:bob 2.2s ease-in-out infinite;
  }
  .scroll-cue span.chev{
    width:14px; height:14px; border-left:2px solid var(--gold); border-bottom:2px solid var(--gold);
    transform:rotate(-45deg);
  }
  @keyframes bob{ 0%,100%{transform:translateY(0);} 50%{transform:translateY(10px);} }

  /* ---------- SECTIONS ---------- */
  section.menu{ position:relative; padding:90px 6vw 60px; }
  .menu.juice{ background:radial-gradient(ellipse at 20% 0%, #1a2617 0%, var(--bg) 55%); }
  .menu.fries{ background:radial-gradient(ellipse at 80% 0%, #1a2417 0%, var(--bg) 55%); }
  .section-head{ text-align:center; margin-bottom:34px; }
  .section-head .eyebrow{ color:var(--gold); font-size:.85rem; letter-spacing:2px; }
  .section-head h2{
    font-family:'Lalezar', sans-serif;
    font-size:clamp(2rem,5vw,3.2rem);
    margin-top:6px;
    color:var(--cream);
  }
  .section-head p{ color:var(--muted); margin-top:8px; }

  /* ---------- photo cube (real image, spinning) ---------- */
  .photocube-wrap{ width:150px; height:150px; margin:0 auto 26px; perspective:900px; }
  .photocube{ width:100%; height:100%; position:relative; transform-style:preserve-3d; animation:spin3d 16s linear infinite; }
  .photocube .

  pf{ position:absolute; inset:0; border-radius:16px; border:2px solid var(--gold); overflow:hidden; background-size:cover; background-position:center; box-shadow:0 18px 34px rgba(0,0,0,.5); }
  .photocube .pf1{ transform:translateZ(75px); }
  .photocube .pf2{ transform:rotateY(180deg) translateZ(75px); background:var(--leaf-deep); }
  .photocube .pf3, .photocube .pf4{ width:150px; }
  .photocube .pf3{ transform:rotateY(90deg) translateZ(75px); background:var(--leaf); }
  .photocube .pf4{ transform:rotateY(-90deg) translateZ(75px); background:var(--leaf); }

  .grid{
    display:grid;
    grid-template-columns:repeat(auto-fill, minmax(220px, 1fr));
    gap:22px;
    max-width:1300px;
    margin:0 auto;
  }

  /* ---------- 3D CARD ---------- */
  .card{
    background:linear-gradient(160deg, var(--surface), var(--surface2));
    border:1px solid rgba(255,255,255,.06);
    border-radius:var(--radius);
    padding:26px 18px 20px;
    text-align:center;
    transition:transform .35s ease, box-shadow .35s ease, border-color .35s ease;
  }
  .card:hover{
    transform:translateY(-8px) scale(1.02);
    box-shadow:0 20px 40px rgba(0,0,0,.5);
    border-color:rgba(242,174,40,.4);
  }
  .card-shape{ perspective:700px; height:120px; display:flex; align-items:center; justify-content:center; margin-bottom:14px; position:relative; }
  .card-inner3d{
    width:78px; height:96px; position:relative; transform-style:preserve-3d;
    animation:spin3d 9s linear infinite;
  }
  .card:nth-child(3n+1) .card-inner3d{ animation-duration:8s; }
  .card:nth-child(3n+2) .card-inner3d{ animation-duration:10.5s; animation-direction:reverse; }
  @keyframes spin3d{
    from{ transform:rotateX(10deg) rotateY(0deg); }
    to{ transform:rotateX(10deg) rotateY(360deg); }
  }
  .card-inner3d .face{
    position:absolute; border-radius:9px;
    background:linear-gradient(160deg, var(--c1), var(--c2));
    border:1px solid rgba(255,255,255,.22);
    box-shadow:inset 0 0 18px rgba(0,0,0,.28);
  }
  .card-inner3d .f1, .card-inner3d .f2{ width:78px; height:96px; top:0; left:0; }
  .card-inner3d .f1{ transform:translateZ(19px); }
  .card-inner3d .f2{ transform:rotateY(180deg) translateZ(19px); }
  .card-inner3d .f3, .card-inner3d .f4{ width:38px; height:96px; top:0; left:20px; }
  .card-inner3d .f3{ transform:rotateY(90deg) translateZ(39px); }
  .card-inner3d .f4{ transform:rotateY(-90deg) translateZ(39px); }
  .card-inner3d .lid{
    position:absolute; right:6px; left:6px; top:-7px; height:16px; border-radius:50%;
    background:var(--c1); transform:translateZ(10px); opacity:.95;
  }
  .straw{
    position:absolute; top:-20px; right:34px; width:5px; height:46px; border-radius:3px;
    background:linear-gradient(var(--leaf-bright), #fff); transform:rotate(18deg); opacity:.9; z-index:3;
  }
  .fry1,.fry2,.fry3{
    position:absolute; top:-16px; width:7px; height:38px; border-radius:2px;
    background:linear-gradient(var(--gold), var(--gold-soft)); z-index:3;
  }
  .fry1{ right:26px; transform:rotate(-12deg); }
  .fry2{ right:38px; transform:rotate(4deg); top:-20px; }
  .fry3{ right:50px; transform:rotate(16deg); }

  .card h3{ font-size:1.05rem; margin-bottom:6px; }
  .card p{ color:var(--muted); font-size:.82rem; min-height:2.4em; }
  .card .price{
    display:inline-block; margin-top:12px; padding:6px 16px;
    border-radius:999px; font-size:.85rem; font-weight:700;
    background:rgba(242,174,40,.14); color:var(--gold);
    border:1px solid rgba(242,174,40,.35);
  }

  /* ---------- FOOTER ---------- */
  footer{
    text-align:center; padding:50px 6vw 40px;
    border-top:1px solid rgba(255,255,255,.06);
    color:var(--muted); font-size:.85rem;
  }
  footer .logo img{ height:30px; margin-bottom:10px; }

  @media (prefers-reduced-motion: reduce){
    .card-inner3d, .photocube{ animation:none; }
    .scroll-cue{ animation:none; }
  }
  @media (max-width:640px){
    nav ul{ gap:16px; font-size:.85rem; }
    .drag-hint{ bottom:90px; }
  }
</style>
</head>
<body>

<nav>
  <div class="logo"><img src="logo.png" alt="کرافا CRAVA"></div>
  <ul>

    <li><a href="#home">سەرەکی</a></li>
    <li><a href="#juice">جوس</a></li>
    <li><a href="#fries">سیبی فرای</a></li>
  </ul>
</nav>

<section class="hero" id="home">
  <canvas id="hero-canvas"></canvas>
  <div class="hero-copy">
    <h1 class="brand-font">CRAVA</h1>
    <p>تازەترین جوسی میوە و سیبی فرایی ترسقاو</p>
  </div>
  <div class="drag-hint">بۆ سوڕاندنی شێوەکان ڕایانبکێشە 🖐</div>
  <a href="#juice" class="scroll-cue"><span>بەرەو مینو</span><span class="chev"></span></a>
</section>

<section class="menu juice" id="juice">
  <div class="section-head">
    <div class="photocube-wrap">
      <div class="photocube">
        <span class="pf pf1" style="background-image:url('juice.png')"></span>
        <span class="pf pf2"></span>
        <span class="pf pf3"></span>
        <span class="pf pf4"></span>
      </div>
    </div>
    <div class="eyebrow">١٥ تام</div>
    <h2 class="brand-font">جوسی میوەی تازە</h2>
    <p>هەموو جوسەکانمان لە میوەی تازە و سروشتی دروستدەکرێن</p>
  </div>
  <div class="grid" id="juice-grid"></div>
</section>

<section class="menu fries" id="fries">
  <div class="section-head">
    <div class="photocube-wrap">
      <div class="photocube">
        <span class="pf pf1" style="background-image:url('fries.png')"></span>
        <span class="pf pf2"></span>
        <span class="pf pf3"></span>
        <span class="pf pf4"></span>
      </div>
    </div>
    <div class="eyebrow">٥ جۆر</div>
    <h2 class="brand-font">سیبی فرای ترسقاو</h2>
    <p>زەردەی گەرم و ترسقاو، بە تامی جۆراوجۆر</p>
  </div>
  <div class="grid" id="fries-grid"></div>
</section>

<footer>
  <div class="logo"><img src="logo.png" alt="کرافا CRAVA"></div>
  <p>تامی تازە، هەر ڕۆژێک</p>
</footer>

<script>
  const juices = [
    {name:"پرتەقاڵ", desc:"ترش و سارد، سروشتی ١٠٠٪", price:"2000 د.ع", c1:"#FFC26B", c2:"#E8792E"},
    {name:"سێو", desc:"شیرین و تازە لە باخ", price:"2000 د.ع", c1:"#B7DC6B", c2:"#4C8C3F"},
    {name:"مۆز", desc:"قەت و تامی نەرم", price:"2000 د.ع", c1:"#FFE98A", c2:"#E8C22E"},
    {name:"مانگۆ", desc:"شیرینی گەرمیانی، بۆنی خۆش", price:"2500 د.ع", c1:"#FFC24D", c2:"#E89A1E"},
    {name:"فراولە", desc:"سوور و شیرین، هەستی هاوین", price:"2500 د.ع", c1:"#FF8FA3", c2:"#E23955"},
    {name:"هەنار", desc:"ترشوشیرین، سروشتی و تەندروست", price:"3000 د.ع", c1:"#E8677A", c2:"#A1122A"},
    {name:"کیوی", desc:"ترشوشیرین و پڕ ڤیتامین", price:"2500 د.ع", c1:"#B9DE6F", c2:"#3D8A49"},
    {name:"ئەناناس", desc:"تامی تروپیکاڵی و تازە", price:"2500 د.ع", c1:"#FDE87A", c2:"#E8B71E"},
    {name:"زەبەش", desc:"سارد و پڕ ئاو، هەستی هاوین", price:"2000 د.ع", c1:"#FF95A0", c2:"#3D8A49"},
    {name:"لیمۆ", desc:"ترش و ئارامبەخش", price:"1500 د.ع", c1:"#F1F08A", c2:"#C7D62E"},
    {name:"ترێ", desc:"شیرین و پڕ وزە", price:"2500 د.ع", c1:"#B792D9", c2:"#6A3E96"},
    {name:"قەیسی", desc:"شیرین و بۆنخۆش", price:"2500 د.ع", c1:"#FFC79A", c2:"#E88A3D"},
    {name:"شەفتاڵوو", desc:"نەرم و بۆنی خۆش", price:"2500 د.ع", c1:"#FFD1B8", c2:"#E8946E"},
    {name:"بێری تێکەڵ", desc:"تێکەڵەیەک لە بێری تازە", price:"3000 د.ع", c1:"#C98AD1", c2:"#7A2E8C"},
    {name:"تێکەڵاوی کرافا", desc:"تایبەتی کرافا، تێکەڵی چەند میوە", price:"3500 د.ع", c1:"#F2AE28", c2:"#3D8A49"},
  ];

  const fries = [
    {name:"سیبی فرایی ساکار", desc:"زەردەی ترسقاو بە خوێی سروشتی", price:"2000 د.ع", c1:"#FFF6E0", c2:"#E8C86A"},
    {name:"سیبی فرایی پەنیر", desc:"داپۆشراو بە پەنیری تواوە", price:"3500 د.ع", c1:"#FFEFA0", c2:"#E8B93D"},
    {name:"سیبی فرایی تیژ", desc:"تامی تیژ و گەرم", price:"3000 د.ع", c1:"#FFD37A", c2:"#D8452E"},
    {name:"سیبی فرایی باربیکیو", desc:"سۆسی باربیکیوی تایبەت", price:"3500 د.ع", c1:"#E8B98A", c2:"#8A4A1E"},
    {name:"تایبەتی کرافا", desc:"تێکەڵەی تایبەتی کرافا بە چێشت", price:"5000 د.ع", c1:"#F2AE28", c2:"#1F4A29"},
  ];

  function renderGrid(items, elId, isJuice){
    const el = document.getElementById(elId);
    el.innerHTML = items.map(it => `
      <article class="card" style="--c1:${it.c1};--c2:${it.c2}">
        <div class="card-shape">
      ${isJuice ? '<span class="straw"></span>' : '<span class="fry1"></span><span class="fry2"></span><span class="fry3"></span>'}
          <div class="card-inner3d">
            <span class="face f1"></span>
            <span class="face f2"></span>
            <span class="face f3"></span>
            <span class="face f4"></span>
            <span class="lid"></span>
          </div>
        </div>
        <h3>${it.name}</h3>
        <p>${it.desc}</p>
        <span class="price">${it.price}</span>
      </article>
    `).join('');
  }
  renderGrid(juices, 'juice-grid', true);
  renderGrid(fries, 'fries-grid', false);
</script>

<script type="importmap">
{ "imports": { "three": "https://unpkg.com/three@0.160.0/build/three.module.js" } }
</script>
<script type="module">
import * as THREE from 'three';

const canvas = document.getElementById('hero-canvas');
const scene = new THREE.Scene();
const bgColor = 0x10150f;
scene.background = new THREE.Color(bgColor);
scene.fog = new THREE.FogExp2(bgColor, 0.055);

const camera = new THREE.PerspectiveCamera(45, window.innerWidth/window.innerHeight, 0.1, 100);
camera.position.set(0, 1.1, 9.5);

const renderer = new THREE.WebGLRenderer({canvas, antialias:true, alpha:true});
renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
renderer.setSize(window.innerWidth, window.innerHeight);
renderer.outputColorSpace = THREE.SRGBColorSpace;
renderer.toneMapping = THREE.ACESFilmicToneMapping;
renderer.toneMappingExposure = 1.15;

scene.add(new THREE.AmbientLight(0xffffff, 0.6));
const key = new THREE.DirectionalLight(0xfff2e0, 1.2);
key.position.set(4, 6, 5);
scene.add(key);
const rim1 = new THREE.PointLight(0xf2ae28, 3, 20);
rim1.position.set(-4, 2, -2);
scene.add(rim1);
const rim2 = new THREE.PointLight(0x3d8a49, 2.6, 20);
rim2.position.set(4, -1, -2);
scene.add(rim2);

const carousel = new THREE.Group();
carousel.position.y = -0.3;
scene.add(carousel);

const loader = new THREE.TextureLoader();

// Builds a "framed photo standee": a thin colored frame box with the photo
// inset on its front face, so real product photos read as 3D objects.
function makePhotoStandee(url, w, h, frameColor){
  const group = new THREE.Group();

  const frameMat = new THREE.MeshStandardMaterial({color:frameColor, roughness:0.55, metalness:0.08});
  const frameGeo = new THREE.BoxGeometry(w + 0.14, h + 0.14, 0.1);
  group.add(new THREE.Mesh(frameGeo, frameMat));

  const backMat = new THREE.MeshStandardMaterial({color:0x14200f, roughness:0.7});
  const photoMat = new THREE.MeshStandardMaterial({color:0xffffff, roughness:0.4});
  const photoGeo = new THREE.BoxGeometry(w, h, 0.06);
  const photoMesh = new THREE.Mesh(photoGeo, [backMat, backMat, backMat, backMat, photoMat, backMat]);
  photoMesh.position.z = 0.08;
  group.add(photoMesh);

  loader.load(url, (tex) => {
    tex.colorSpace = THREE.SRGBColorSpace;
    photoMat.map = tex;
    photoMat.needsUpdate = true;
  });

  return group;
}

const logoPivot = makePhotoStandee('logo.png', 2.7, 2.7 * (382/1224), 0x1f4a29);
logoPivot.position.set(0, 0.35, 3);
carousel.add(logoPivot);

const friesGroup = makePhotoStandee('fries.png', 1.9, 1.9, 0xf2ae28);
friesGroup.position.set(2.7, -0.2, -1.6);
carousel.add(friesGroup);

const glassGroup = makePhotoStandee('juice.png', 1.9, 1.9, 0x3d8a49);
glassGroup.position.set(-2.7, -0.1, -1.6);
carousel.add(glassGroup);

// ---- interaction ----
let autoRotate = true;
let dragging = false;
let lastX = 0;
let resumeTimer = null;

canvas.addEventListener('pointerdown', (e) => {
  dragging = true; autoRotate = false; lastX = e.clientX;
  clearTimeout(resumeTimer);
});
window.addEventListener('pointerup', () => {
  dragging = false;
  resumeTimer = setTimeout(() => autoRotate = true, 1800);
});
window.addEventListener('pointermove', (e) => {
  if(!dragging) return;
  const dx = e.clientX - lastX;
  lastX = e.clientX;
  carousel.rotation.y += dx * 0.006;
});

window.addEventListener('resize', () => {
  camera.aspect = window.innerWidth/window.innerHeight;
  camera.updateProjectionMatrix();
  renderer.setSize(window.
    innerWidth, window.innerHeight);
});

const clock = new THREE.Clock();
function animate(){
  requestAnimationFrame(animate);
  const t = clock.getElapsedTime();
  if(autoRotate) carousel.rotation.y += 0.0035;
  logoPivot.rotation.y = Math.sin(t * 0.6) * 0.15;
  logoPivot.position.y = 0.35 + Math.sin(t * 0.8) * 0.08;
  friesGroup.rotation.y += 0.01;
  friesGroup.position.y = -0.2 + Math.sin(t * 0.9 + 1) * 0.08;
  glassGroup.rotation.y -= 0.008;
  glassGroup.position.y = -0.1 + Math.sin(t * 0.7 + 2) * 0.08;
  renderer.render(scene, camera);
}
animate();
</script>
</body>
</html>
