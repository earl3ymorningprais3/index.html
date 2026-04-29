

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Miss Earley | Music Producer</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
--purple:#BEA9DF;
--purple-dark:#8A6DBF;
--purple-deep:#3D2A6E;
--cream:#F0EBE0;
--green:#9FD48A;
--deep:#1A1525;
--surface:#221C30;
--surface2:#2A2240;
--text:#F0EBE0;
--muted:#BEB0A0;
--dim:#7A6E60;
--border:rgba(190,169,223,.2);
}
html{scroll-behavior:smooth}
body{
font-family:Georgia,serif;
background:var(--deep);
color:var(--text);
line-height:1.7;
}
nav{
position:fixed;
top:0;left:0;right:0;
z-index:100;
display:flex;
justify-content:space-between;
align-items:center;
padding:1rem 2rem;
background:rgba(26,21,37,.92);
backdrop-filter:blur(8px);
border-bottom:.5px solid var(--border);
}
.nav-logo{
letter-spacing:.14em;
text-transform:uppercase;
color:var(--purple)
}
.nav-links{display:flex;gap:1.5rem;flex-wrap:wrap}
.nav-links a{
text-decoration:none;
font-family:Helvetica,sans-serif;
font-size:.75rem;
letter-spacing:.12em;
text-transform:uppercase;
color:var(--muted)
}
.nav-links a:hover,.nav-links a.active{color:var(--purple)}

#hero{
min-height:100vh;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
padding:8rem 2rem 4rem;
position:relative;
overflow:hidden;
}
.hero-photo{
position:absolute;
inset:0;
background:
linear-gradient(rgba(26,21,37,.55),rgba(26,21,37,.78)),
url('https://images.unsplash.com/photo-1511379938547-c1f69419868d?q=80&w=1800') center/cover;
opacity:.5;
}
.hero-bg{
position:absolute;
inset:0;
background:radial-gradient(circle at center,rgba(190,169,223,.16),transparent 65%);
}
#hero:after{
content:'';
position:absolute;
inset:0;
background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.05'/%3E%3C/svg%3E");
}
.cross-accent,.hero-name,.hero-tagline,.hero-verse,.hero-cta{position:relative;z-index:2}
.cross-accent{letter-spacing:.5em;color:#9f87ca;margin-bottom:1.4rem}
.hero-name{font-size:clamp(3rem,8vw,6rem);font-weight:normal}
.hero-name span{color:var(--purple)}
.hero-tagline{
margin-top:1rem;
font-family:Helvetica,sans-serif;
letter-spacing:.22em;
font-size:.8rem;
text-transform:uppercase;
color:var(--muted)
}
.hero-verse{
margin-top:2rem;
font-style:italic;
color:var(--green);
max-width:500px
}
.hero-cta{margin-top:3rem;display:flex;gap:1rem;flex-wrap:wrap}
.btn{
padding:.8rem 1.8rem;
text-decoration:none;
border:.5px solid var(--purple);
font-family:Helvetica,sans-serif;
font-size:.75rem;
letter-spacing:.14em;
text-transform:uppercase;
color:var(--purple);
transition:.3s;
}
.btn:hover{background:var(--purple);color:var(--deep)}
.btn-filled{background:var(--purple);color:var(--deep)}

section{max-width:1050px;margin:auto;padding:6rem 2rem}
.section-label{
font-family:Helvetica,sans-serif;
letter-spacing:.24em;
font-size:.72rem;
text-transform:uppercase;
color:var(--purple);
margin-bottom:1rem
}
.section-title{
font-size:clamp(2rem,4vw,3rem);
font-weight:normal;
margin-bottom:1.5rem
}

.about-grid{
display:grid;
grid-template-columns:1fr 1fr;
gap:3rem;
align-items:center
}
.about-photo{
aspect-ratio:3/4;
background:var(--surface2);
display:flex;
align-items:center;
justify-content:center;
border:.5px solid var(--border);
transition:.3s;
}
.about-photo:hover,.track:hover,.gallery-item:hover,.release-card:hover{
transform:translateY(-6px);
box-shadow:0 12px 30px rgba(0,0,0,.25)
}
.about-text p{margin-bottom:1.2rem;color:var(--muted)}

#music{
background:var(--surface);
max-width:none
}
.track{
display:flex;
align-items:center;
gap:1rem;
padding:1rem 0;
border-bottom:.5px solid var(--border);
transition:.3s
}
.track-play{
width:32px;height:32px;
border-radius:50%;
border:.5px solid var(--purple);
display:flex;
align-items:center;
justify-content:center
}
.track-info{flex:1}
.track-sub{display:block;font-size:.75rem;color:var(--dim)}
.track-tag{font-size:.7rem;color:var(--green)}
.eq{display:inline-flex;gap:2px;margin-left:8px}
.eq span{
width:2px;height:10px;
background:var(--green);
animation:bounce 1s infinite ease-in-out
}
.eq span:nth-child(2){animation-delay:.2s}
.eq span:nth-child(3){animation-delay:.4s}
@keyframes bounce{
0%,100%{transform:scaleY(.5)}
50%{transform:scaleY(1.4)}
}
.embed-wrap{display:grid;gap:1rem;margin-top:2rem}
iframe{width:100%;border:0;border-radius:12px}

.release-grid{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:1.5rem;
margin-top:2rem
}
.release-card{
background:var(--surface2);
padding:1.4rem;
transition:.3s
}
.album-cover{
aspect-ratio:1;
background:linear-gradient(135deg,var(--purple-deep),var(--surface));
margin-bottom:1rem
}

.gallery-grid{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:1rem
}
.gallery-item{
background:var(--surface2);
aspect-ratio:1;
display:flex;
justify-content:center;
align-items:center;
transition:.3s
}
.gallery-item:first-child{
grid-column:span 2;
aspect-ratio:2/1
}

#connect{text-align:center;max-width:700px}
.social-links{
display:flex;
justify-content:center;
flex-wrap:wrap;
gap:1.2rem;
margin-top:2rem
}
.social-link{
text-decoration:none;
color:var(--muted);
font-family:Helvetica,sans-serif;
letter-spacing:.12em;
font-size:.75rem
}
.social-link:hover{color:var(--purple)}
footer{
padding:2rem;
text-align:center;
border-top:.5px solid var(--border);
color:var(--dim)
}

@media(max-width:700px){
.about-grid{grid-template-columns:1fr}
.gallery-grid{grid-template-columns:1fr 1fr}
.gallery-item:first-child{grid-column:span 2}
nav{padding:1rem}
.nav-links{gap:.7rem}
}
</style>
</head>
<body>

<nav>
<div class="nav-logo">Miss Earley</div>
<div class="nav-links">
<a href="#about">About</a>
<a href="#music">Music</a>
<a href="#releases">Releases</a>
<a href="#gallery">Gallery</a>
<a href="#connect">Connect</a>
</div>
</nav>

<section id="hero">
<div class="hero-photo"></div>
<div class="hero-bg"></div>
<div class="cross-accent">✦ ✦ ✦</div>
<h1 class="hero-name">Miss <span>Earley</span></h1>
<p class="hero-tagline">Music Producer · Sound Rooted in Faith</p>
<p class="hero-verse">Whatever you do, work at it with all your heart, as working for the Lord. Colossians 3:23</p>
<div class="hero-cta">
<a href="#music" class="btn btn-filled">Listen Now</a>
<a href="#about" class="btn">My Story</a>
</div>
</section>

<section id="about">
<div class="section-label">About</div>
<div class="about-grid">
<div class="about-photo">Artist Photo Here</div>
<div class="about-text">
<h2 class="section-title">Beats with a purpose.</h2>
<p>I'm Miss Earley, a producer shaping cinematic gospel, soul, and contemporary sound built to carry meaning.</p>
<p>My work blends faith, atmosphere, rhythm, and storytelling to move people spiritually and sonically.</p>
<p>Every project is built with purpose, precision, and prayer.</p>
</div>
</div>
</section>

<section id="music">
<div class="section-label">Music</div>
<h2 class="section-title">Latest tracks</h2>

<div class="track">
<div>01</div>
<div class="track-play">▶</div>
<div class="track-info">
Mercy in Motion
<span class="eq"><span></span><span></span><span></span></span>
<span class="track-sub">Gospel Soul</span>
</div>
<div class="track-tag">New</div>
</div>

<div class="track"><div>02</div><div class="track-play">▶</div><div class="track-info">Kingdom Echoes<span class="track-sub">R&B Worship</span></div></div>
<div class="track"><div>03</div><div class="track-play">▶</div><div class="track-info">Midnight Psalms<span class="track-sub">Cinematic Instrumental</span></div></div>
<div class="track"><div>04</div><div class="track-play">▶</div><div class="track-info">Glory Over Drums<span class="track-sub">Trap Soul</span></div></div>

<div class="embed-wrap">
<iframe height="152" src="https://open.spotify.com/embed/track/11dFghVXANMlKmJXsNCbNl"></iframe>
<iframe height="166" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/293"></iframe>
</div>
</section>

<section id="releases">
<div class="section-label">Discography</div>
<h2 class="section-title">Recent Releases</h2>
<div class="release-grid">
<div class="release-card">
<div class="album-cover"></div>
<h3>Sanctified Frequencies</h3>
<p>Producer EP blending worship and soul textures.</p>
</div>
<div class="release-card">
<div class="album-cover"></div>
<h3>Night Prayer Loops</h3>
<p>Instrumental beat collection.</p>
</div>
<div class="release-card">
<div class="album-cover"></div>
<h3>Kingdom Bounce</h3>
<p>Faith rooted contemporary production set.</p>
</div>
</div>
</section>

<section id="gallery">
<div class="section-label">Gallery</div>
<h2 class="section-title">Visual Story</h2>
<div class="gallery-grid">
<div class="gallery-item">Feature Photo</div>
<div class="gallery-item">Studio</div>
<div class="gallery-item">Live Set</div>
<div class="gallery-item">Behind Scenes</div>
</div>
</section>

<section id="connect">
<div class="section-label">Connect</div>
<h2 class="section-title">Let's Stay Connected</h2>
<p>Sing to the Lord a new song, Psalm 96:1</p>
<div class="social-links">
<a href="#" class="social-link">YouTube</a>
<a href="#" class="social-link">Instagram</a>
<a href="#" class="social-link">TikTok</a>
<a href="#" class="social-link">Spotify</a>
<a href="#" class="social-link">SoundCloud</a>
</div>
</section>

<footer>
© 2026 Miss Earley. Music rooted in faith.
</footer>

<script>
const sections=document.querySelectorAll('section[id]');
const links=document.querySelectorAll('.nav-links a');
window.addEventListener('scroll',()=>{
let current='';
sections.forEach(sec=>{
if(scrollY>=sec.offsetTop-140){current=sec.id}
});
links.forEach(link=>{
link.classList.remove('active');
if(link.getAttribute('href')==='#'+current){
link.classList.add('active')
}
})
});
</script>

</body>
</html>
```

