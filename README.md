<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sora Louveré — Exportación & Moda Global</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400;1,600&family=Raleway:wght@200;300;400;500;600&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
:root{
  --black:#0a0a0a;--deep:#111111;--charcoal:#1a1a1a;--card:#1e1e1e;
  --rose:#c8a98a;--gold:#d4af6a;--champagne:#e8d5b0;--cream:#f5efe6;
  --white:#fdfaf6;--muted:#888880;--border:rgba(212,175,106,0.18);--borderhov:rgba(212,175,106,0.5);
}
html{scroll-behavior:smooth;}
body{background:var(--black);color:var(--cream);font-family:'Raleway',sans-serif;font-weight:300;overflow-x:hidden;}
img{max-width:100%;display:block;object-fit:cover;}
a{text-decoration:none;color:inherit;}
::-webkit-scrollbar{width:4px;}
::-webkit-scrollbar-track{background:var(--black);}
::-webkit-scrollbar-thumb{background:var(--gold);}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:1000;padding:1.2rem 2rem;display:flex;justify-content:space-between;align-items:center;background:linear-gradient(to bottom,rgba(10,10,10,.96) 0%,transparent 100%);transition:background .4s;}
nav.scrolled{background:rgba(10,10,10,.97);border-bottom:1px solid var(--border);}
.nav-logo{font-family:'Playfair Display',serif;font-size:1.5rem;font-weight:400;letter-spacing:.12em;color:var(--gold);}
.nav-logo span{font-style:italic;color:var(--champagne);}
.nav-links{display:flex;gap:1.8rem;list-style:none;}
.nav-links a{font-size:.62rem;letter-spacing:.22em;text-transform:uppercase;color:var(--muted);transition:color .3s;}
.nav-links a:hover{color:var(--gold);}
.nav-wa{background:var(--gold);color:var(--black);font-size:.6rem;letter-spacing:.2em;text-transform:uppercase;padding:.55rem 1.4rem;font-weight:600;transition:background .3s;}
.nav-wa:hover{background:var(--champagne);}
.hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;z-index:1001;}
.hamburger span{width:24px;height:1.5px;background:var(--gold);transition:all .3s;display:block;}
.mobile-menu{display:none;position:fixed;inset:0;background:rgba(10,10,10,.97);z-index:999;flex-direction:column;align-items:center;justify-content:center;gap:2.5rem;}
.mobile-menu.open{display:flex;}
.mobile-menu a{font-family:'Playfair Display',serif;font-size:1.8rem;color:var(--cream);}
.mobile-menu a:hover{color:var(--gold);}
@media(max-width:900px){.nav-links,.nav-wa{display:none;}.hamburger{display:flex;}}

/* HERO */
.hero{min-height:100vh;display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden;}
.hero-bg{position:absolute;inset:0;background:url('https://images.unsplash.com/photo-1558769132-cb1aea458c5e?w=1600&q=80') center/cover no-repeat;filter:brightness(.28);}
.hero-overlay{position:absolute;inset:0;background:linear-gradient(135deg,rgba(10,10,10,.85) 0%,rgba(30,15,5,.55) 50%,rgba(10,10,10,.8) 100%);}
.hero-particles{position:absolute;inset:0;overflow:hidden;pointer-events:none;}
.particle{position:absolute;width:2px;height:2px;background:var(--gold);border-radius:50%;opacity:0;animation:drift var(--d,20s) ease-in-out infinite var(--delay,0s);}
@keyframes drift{0%{opacity:0;transform:translateY(100vh);}10%{opacity:.5;}90%{opacity:.2;}100%{opacity:0;transform:translateY(-10vh) translateX(var(--dx,30px));}}
.hero-content{position:relative;z-index:2;text-align:center;padding:2rem;}
.hero-badge{font-size:.6rem;letter-spacing:.35em;text-transform:uppercase;color:var(--gold);margin-bottom:1.5rem;display:flex;align-items:center;justify-content:center;gap:1rem;}
.hero-badge::before,.hero-badge::after{content:'';display:block;width:40px;height:1px;background:var(--gold);}
.hero-title{font-family:'Playfair Display',serif;font-size:clamp(3rem,11vw,9rem);font-weight:400;line-height:.9;color:var(--white);}
.hero-title em{font-style:italic;color:var(--gold);display:block;}
.hero-tagline{font-size:clamp(.75rem,1.8vw,.95rem);letter-spacing:.22em;text-transform:uppercase;color:var(--champagne);margin:2rem auto;max-width:520px;line-height:2.2;}
.hero-btns{display:flex;gap:1.5rem;justify-content:center;flex-wrap:wrap;margin-top:2.5rem;}
.btn-gold{background:var(--gold);color:var(--black);font-size:.65rem;letter-spacing:.2em;text-transform:uppercase;padding:1rem 2.5rem;font-weight:600;transition:all .3s;border:2px solid var(--gold);display:inline-block;}
.btn-gold:hover{background:transparent;color:var(--gold);}
.btn-outline{border:1px solid rgba(212,175,106,.4);color:var(--champagne);font-size:.65rem;letter-spacing:.2em;text-transform:uppercase;padding:1rem 2.5rem;transition:all .3s;display:inline-block;}
.btn-outline:hover{border-color:var(--gold);color:var(--gold);}
.hero-scroll{position:absolute;bottom:2rem;left:50%;transform:translateX(-50%);display:flex;flex-direction:column;align-items:center;gap:.5rem;}
.hero-scroll span{font-size:.55rem;letter-spacing:.25em;text-transform:uppercase;color:var(--muted);}
.scroll-line{width:1px;height:50px;background:linear-gradient(to bottom,var(--gold),transparent);animation:scrolldrop 2s ease-in-out infinite;}
@keyframes scrolldrop{0%{transform:scaleY(0);transform-origin:top;}50%{transform:scaleY(1);transform-origin:top;}51%{transform-origin:bottom;}100%{transform:scaleY(0);transform-origin:bottom;}}
@keyframes fadeUp{from{opacity:0;transform:translateY(30px);}to{opacity:1;transform:none;}}
.a1{animation:fadeUp .8s ease .2s both;}.a2{animation:fadeUp .8s ease .4s both;}.a3{animation:fadeUp .8s ease .6s both;}.a4{animation:fadeUp .8s ease .8s both;}

/* SHARED */
section{padding:6rem 2rem;}
.container{max-width:1200px;margin:0 auto;}
.sec-label{font-size:.58rem;letter-spacing:.3em;text-transform:uppercase;color:var(--gold);margin-bottom:.8rem;display:flex;align-items:center;gap:.8rem;}
.sec-label::before{content:'';display:block;width:20px;height:1px;background:var(--gold);}
.sec-title{font-family:'Playfair Display',serif;font-size:clamp(1.8rem,4vw,3.2rem);font-weight:400;line-height:1.1;color:var(--white);}
.sec-title em{font-style:italic;color:var(--gold);}
.sec-body{font-size:.88rem;line-height:2;color:var(--muted);margin-top:1rem;}
.reveal{opacity:0;transform:translateY(40px);transition:opacity .9s ease,transform .9s ease;}
.reveal.vis{opacity:1;transform:none;}
.divider{width:60px;height:1px;background:linear-gradient(to right,var(--gold),transparent);margin:1.5rem 0;}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:center;}
.g3{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;}
.g4{display:grid;grid-template-columns:repeat(4,1fr);gap:1rem;}
@media(max-width:900px){.g2{grid-template-columns:1fr;gap:2.5rem;}.g3{grid-template-columns:repeat(2,1fr);}.g4{grid-template-columns:repeat(2,1fr);}}
@media(max-width:500px){.g3,.g4{grid-template-columns:1fr;}}

/* INTRO */
.intro-sec{background:var(--deep);}
.intro-img{width:100%;height:520px;object-fit:cover;}
.intro-frame{position:absolute;bottom:-20px;right:-20px;width:70%;height:70%;border:1px solid var(--border);pointer-events:none;}
.intro-right{position:relative;}
.stats-row{display:flex;gap:2rem;margin-top:3rem;flex-wrap:wrap;}
.stat{border-left:2px solid var(--gold);padding-left:1.2rem;}
.stat-n{font-family:'Playfair Display',serif;font-size:2.4rem;color:var(--gold);}
.stat-l{font-size:.62rem;letter-spacing:.15em;text-transform:uppercase;color:var(--muted);margin-top:.2rem;}

/* PHOTO SECTIONS */
.photo-full{position:relative;height:70vh;overflow:hidden;}
.photo-full img{width:100%;height:100%;object-fit:cover;transition:transform .6s;}
.photo-full:hover img{transform:scale(1.04);}
.photo-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(10,10,10,.85) 0%,transparent 50%);}
.photo-caption{position:absolute;bottom:3rem;left:3rem;right:3rem;}
.photo-caption h3{font-family:'Playfair Display',serif;font-size:clamp(1.5rem,3vw,2.5rem);color:var(--white);}
.photo-caption p{font-size:.8rem;color:var(--champagne);margin-top:.5rem;letter-spacing:.1em;}
.photo-g2{display:grid;grid-template-columns:1fr 1fr;height:60vh;}
.photo-g3{display:grid;grid-template-columns:repeat(3,1fr);height:55vh;}
.photo-asymm{display:grid;grid-template-columns:2fr 1fr;height:65vh;gap:4px;}
.pg-item{position:relative;overflow:hidden;}
.pg-item img{width:100%;height:100%;object-fit:cover;transition:transform .6s;}
.pg-item:hover img{transform:scale(1.07);}
.pg-label{position:absolute;bottom:1.2rem;left:1.2rem;font-size:.6rem;letter-spacing:.18em;text-transform:uppercase;color:var(--gold);background:rgba(10,10,10,.65);padding:.35rem .8rem;}
@media(max-width:700px){.photo-g2,.photo-g3,.photo-asymm{grid-template-columns:1fr;height:auto;}.photo-g2 .pg-item,.photo-g3 .pg-item,.photo-asymm .pg-item{height:56vw;}}

/* PRODUCTS */
.products-sec{background:var(--charcoal);}
.prod-card{background:var(--card);border:1px solid var(--border);overflow:hidden;transition:border-color .3s,transform .3s;}
.prod-card:hover{border-color:var(--gold);transform:translateY(-6px);}
.prod-img{height:260px;overflow:hidden;}
.prod-img img{width:100%;height:100%;object-fit:cover;transition:transform .5s;}
.prod-card:hover .prod-img img{transform:scale(1.08);}
.prod-info{padding:1.5rem;}
.prod-cat{font-size:.55rem;letter-spacing:.22em;text-transform:uppercase;color:var(--gold);margin-bottom:.4rem;}
.prod-name{font-family:'Playfair Display',serif;font-size:1.15rem;color:var(--white);}
.prod-desc{font-size:.78rem;line-height:1.8;color:var(--muted);margin-top:.5rem;}
.prod-badge{display:inline-block;margin-top:.8rem;font-size:.55rem;letter-spacing:.15em;text-transform:uppercase;padding:.3rem .8rem;border:1px solid rgba(212,175,106,.3);color:var(--champagne);}

/* COLLECTIONS */
.coll-sec{background:var(--deep);}
.coll-item{position:relative;overflow:hidden;cursor:pointer;}
.coll-img{height:370px;width:100%;object-fit:cover;transition:transform .6s;}
.coll-item:hover .coll-img{transform:scale(1.06);}
.coll-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(10,10,10,.9) 0%,transparent 55%);transition:opacity .4s;}
.coll-info{position:absolute;bottom:1.5rem;left:1.5rem;}
.coll-info h4{font-family:'Playfair Display',serif;font-size:1.2rem;color:var(--white);}
.coll-info p{font-size:.65rem;color:var(--gold);letter-spacing:.15em;text-transform:uppercase;margin-top:.3rem;}

/* FEATURES */
.features-sec{background:linear-gradient(135deg,#0f0a05,#1a1008,#0a0a0a);}
.feat-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:2px;margin-top:4rem;}
.feat-item{background:var(--card);padding:2.5rem 2rem;border:1px solid var(--border);transition:border-color .3s,background .3s;}
.feat-item:hover{border-color:var(--gold);background:#222;}
.feat-icon{font-size:1.8rem;margin-bottom:1.2rem;}
.feat-title{font-family:'Playfair Display',serif;font-size:1.05rem;color:var(--white);margin-bottom:.6rem;}
.feat-desc{font-size:.78rem;line-height:1.9;color:var(--muted);}
@media(max-width:700px){.feat-grid{grid-template-columns:1fr;}}

/* QUOTE */
.quote-banner{background:var(--gold);padding:5rem 2rem;text-align:center;}
.quote-banner blockquote{font-family:'Playfair Display',serif;font-size:clamp(1.3rem,3.5vw,2.4rem);font-style:italic;color:var(--black);line-height:1.5;max-width:800px;margin:0 auto;}
.quote-banner cite{display:block;margin-top:1.5rem;font-size:.65rem;letter-spacing:.22em;text-transform:uppercase;color:rgba(10,10,10,.6);font-style:normal;}

/* EXPORT */
.export-sec{background:var(--charcoal);}
.export-grid{display:grid;grid-template-columns:1fr 1fr;gap:4rem;align-items:start;margin-top:4rem;}
.export-list{list-style:none;}
.export-list li{display:flex;align-items:center;gap:1rem;padding:1.2rem 0;border-bottom:1px solid var(--border);font-size:.85rem;color:var(--champagne);}
.export-list li::before{content:'→';color:var(--gold);}
.exp-cards{display:grid;grid-template-columns:1fr 1fr;gap:1rem;}
.exp-card{background:var(--card);border:1px solid var(--border);padding:1.5rem;text-align:center;transition:border-color .3s;}
.exp-card:hover{border-color:var(--gold);}
.exp-n{font-family:'Playfair Display',serif;font-size:2rem;color:var(--gold);}
.exp-l{font-size:.6rem;letter-spacing:.15em;text-transform:uppercase;color:var(--muted);margin-top:.3rem;}
@media(max-width:700px){.export-grid{grid-template-columns:1fr;}.exp-cards{grid-template-columns:1fr 1fr;}}

/* GALLERY CAROUSEL */
.gal-sec{background:var(--deep);padding:6rem 0;}
.gal-header{padding:0 2rem;margin-bottom:3rem;}
.gal-track-wrap{overflow:hidden;}
.gal-track{display:flex;gap:1rem;transition:transform .7s cubic-bezier(.77,0,.18,1);padding:0 2rem;}
.gal-slide{min-width:300px;height:400px;flex-shrink:0;overflow:hidden;position:relative;}
.gal-slide img{width:100%;height:100%;object-fit:cover;transition:transform .5s;}
.gal-slide:hover img{transform:scale(1.07);}
.gal-label{position:absolute;bottom:1rem;left:1rem;font-size:.6rem;letter-spacing:.18em;text-transform:uppercase;color:var(--gold);background:rgba(0,0,0,.7);padding:.3rem .8rem;}
.gal-controls{display:flex;gap:1rem;justify-content:center;margin-top:2rem;padding:0 2rem;}
.gal-btn{width:44px;height:44px;border:1px solid rgba(212,175,106,.35);background:transparent;color:var(--gold);cursor:pointer;font-size:1rem;transition:all .3s;}
.gal-btn:hover{background:var(--gold);color:var(--black);}
@media(max-width:600px){.gal-slide{min-width:240px;height:300px;}}

/* PROCESS */
.process-sec{background:var(--black);}
.p-steps{display:grid;grid-template-columns:repeat(4,1fr);gap:0;margin-top:4rem;}
.p-step{padding:2rem 1.5rem;border-top:1px solid var(--border);border-right:1px solid var(--border);}
.p-step:last-child{border-right:none;}
.p-num{font-family:'Playfair Display',serif;font-size:4rem;color:rgba(212,175,106,.08);line-height:1;margin-bottom:1rem;}
.p-title{font-size:.72rem;letter-spacing:.18em;text-transform:uppercase;color:var(--white);margin-bottom:.7rem;}
.p-desc{font-size:.78rem;line-height:1.9;color:var(--muted);}
@media(max-width:700px){.p-steps{grid-template-columns:1fr 1fr;}.p-step:nth-child(2n){border-right:none;}}

/* TESTIMONIALS */
.test-sec{background:var(--charcoal);}
.test-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;margin-top:4rem;}
.test-card{background:var(--card);border:1px solid var(--border);padding:2rem;transition:border-color .3s;}
.test-card:hover{border-color:var(--gold);}
.test-q{font-family:'Playfair Display',serif;font-size:1rem;font-style:italic;color:var(--cream);line-height:1.7;margin-bottom:1.5rem;}
.test-div{width:30px;height:1px;background:var(--gold);margin-bottom:1rem;}
.test-name{font-size:.62rem;letter-spacing:.2em;text-transform:uppercase;color:var(--gold);}
.test-role{font-size:.7rem;color:var(--muted);margin-top:.2rem;}
@media(max-width:700px){.test-grid{grid-template-columns:1fr;}}

/* VALUES */
.commit-sec{background:var(--deep);}
.commit-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:2px;margin-top:4rem;}
.commit-item{background:var(--card);padding:3rem 2rem;border:1px solid var(--border);text-align:center;transition:all .3s;}
.commit-item:hover{background:#1f1f1f;border-color:var(--gold);}
.commit-icon{font-size:2.2rem;margin-bottom:1.2rem;}
.commit-title{font-family:'Playfair Display',serif;font-size:1.05rem;color:var(--white);margin-bottom:.7rem;}
.commit-desc{font-size:.78rem;line-height:1.9;color:var(--muted);}
@media(max-width:700px){.commit-grid{grid-template-columns:1fr;}}

/* FOUNDER */
.founder-sec{background:var(--black);}
.founder-inner{display:grid;grid-template-columns:1fr 1.2fr;gap:5rem;align-items:center;}
.founder-img-wrap{position:relative;}
.founder-img{width:100%;height:500px;object-fit:cover;}
.founder-badge{position:absolute;bottom:-1.5rem;right:-1.5rem;background:var(--gold);color:var(--black);padding:1.5rem;text-align:center;width:130px;}
.f-year{font-family:'Playfair Display',serif;font-size:2rem;font-weight:700;line-height:1;}
.f-label{font-size:.55rem;letter-spacing:.15em;text-transform:uppercase;margin-top:.3rem;}
.founder-name{font-family:'Playfair Display',serif;font-size:clamp(1.6rem,3vw,2.4rem);color:var(--white);margin-top:1.5rem;}
.founder-role{font-size:.65rem;letter-spacing:.22em;text-transform:uppercase;color:var(--gold);margin-top:.5rem;}
@media(max-width:800px){.founder-inner{grid-template-columns:1fr;gap:3rem;}.founder-img{height:350px;}}

/* CTA BANNER */
.cta-banner{position:relative;overflow:hidden;padding:8rem 2rem;text-align:center;}
.cta-bg{position:absolute;inset:0;background:url('https://images.unsplash.com/photo-1490481651871-ab68de25d43d?w=1400&q=80') center/cover;filter:brightness(.18);}
.cta-overlay{position:absolute;inset:0;background:linear-gradient(135deg,rgba(212,175,106,.1),transparent);}
.cta-content{position:relative;z-index:2;}
.cta-content h2{font-family:'Playfair Display',serif;font-size:clamp(2rem,5vw,4rem);color:var(--white);margin-bottom:1.5rem;}
.cta-content p{font-size:.88rem;color:var(--champagne);max-width:500px;margin:0 auto 2.5rem;line-height:2;}

/* CONTACT */
.contact-sec{background:var(--charcoal);}
.contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:start;}
.c-item{display:flex;gap:1.2rem;margin-bottom:2rem;align-items:flex-start;}
.c-icon{width:44px;height:44px;border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:1.1rem;flex-shrink:0;color:var(--gold);}
.c-text label{font-size:.58rem;letter-spacing:.2em;text-transform:uppercase;color:var(--gold);display:block;margin-bottom:.3rem;}
.c-text p{font-size:.85rem;color:var(--champagne);}
.soc-links{display:flex;flex-direction:column;gap:.8rem;margin-top:.5rem;}
.soc-link{display:flex;align-items:center;gap:1rem;padding:.9rem 1.2rem;border:1px solid var(--border);transition:all .3s;}
.soc-link:hover{border-color:var(--gold);background:rgba(212,175,106,.05);}
.soc-icon{width:32px;height:32px;display:flex;align-items:center;justify-content:center;font-size:1.1rem;}
.soc-name{font-size:.65rem;letter-spacing:.18em;text-transform:uppercase;color:var(--champagne);}
.soc-handle{font-size:.7rem;color:var(--muted);margin-top:.12rem;}
.wa-big{display:flex;align-items:center;justify-content:center;gap:1rem;background:#25D366;color:#fff;font-size:.75rem;letter-spacing:.18em;text-transform:uppercase;padding:1.3rem 2.5rem;font-weight:600;margin-top:2rem;transition:background .3s;width:100%;}
.wa-big:hover{background:#1da851;}
.wa-big svg{width:22px;height:22px;flex-shrink:0;}
@media(max-width:800px){.contact-grid{grid-template-columns:1fr;gap:3rem;}}

/* FOOTER */
footer{background:#050505;padding:5rem 2rem 2rem;border-top:1px solid var(--border);}
.footer-top{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:3rem;margin-bottom:4rem;}
.f-logo{font-family:'Playfair Display',serif;font-size:2rem;color:var(--gold);letter-spacing:.1em;}
.f-logo em{font-style:italic;color:var(--champagne);}
.footer-brand p{font-size:.78rem;line-height:1.9;color:var(--muted);margin-top:1rem;max-width:280px;}
.footer-col h5{font-size:.62rem;letter-spacing:.22em;text-transform:uppercase;color:var(--gold);margin-bottom:1.5rem;}
.footer-col ul{list-style:none;}
.footer-col ul li{margin-bottom:.8rem;}
.footer-col ul li a{font-size:.78rem;color:var(--muted);transition:color .3s;}
.footer-col ul li a:hover{color:var(--gold);}
.f-socials{display:flex;gap:.8rem;margin-top:1.5rem;}
.f-soc{width:36px;height:36px;border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:.95rem;transition:all .3s;color:var(--muted);}
.f-soc:hover{border-color:var(--gold);color:var(--gold);}
.footer-bottom{border-top:1px solid var(--border);padding-top:1.5rem;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:1rem;}
.footer-copy{font-size:.65rem;color:var(--muted);}
.footer-credits{font-size:.65rem;color:var(--muted);}
.footer-credits a{color:var(--gold);}
@media(max-width:900px){.foo
