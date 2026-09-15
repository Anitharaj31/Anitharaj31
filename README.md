<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Anitha Raj Bale — Senior Data Engineer</title>
<meta name="description" content="Anitha Raj Bale — Senior Data Engineer specializing in AI/ML and streaming cloud platforms. Kafka, Spark, Airflow, dbt, Snowflake, Databricks, AWS, RAG and vector retrieval.">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,400;12..96,500;12..96,600;12..96,700;12..96,800&family=Plus+Jakarta+Sans:ital,wght@0,400;0,500;0,600;0,700;1,500&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<style>
:root{
  --void:#07060a;
  --charcoal:#121017;
  --surface:#171420;
  --surface-2:#1d1927;
  --line:rgba(245,243,247,0.08);
  --text:#f4f2f7;
  --text-dim:#b3aebd;
  --text-faint:#726c81;
  --violet:#9b4dff;
  --violet-bright:#c69bff;
  --violet-deep:#5b1fb0;
  --violet-glow:rgba(155,77,255,0.45);
  --font-display:'Bricolage Grotesque', serif;
  --font-body:'Plus Jakarta Sans', sans-serif;
  --ease:cubic-bezier(.16,.84,.44,1);
}

*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
html,body{background:var(--void);}

body{
  font-family:var(--font-body);
  color:var(--text);
  background:var(--void);
  overflow-x:hidden;
  position:relative;
  -webkit-font-smoothing:antialiased;
}

/* grain overlay */
body::before{
  content:"";
  position:fixed;
  inset:0;
  z-index:9998;
  pointer-events:none;
  opacity:0.05;
  mix-blend-mode:overlay;
  background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
}

::selection{background:var(--violet); color:#fff;}

a{color:inherit; text-decoration:none;}
ul{list-style:none;}
img{max-width:100%; display:block;}
button{font-family:inherit; cursor:pointer; border:none; background:none; color:inherit;}

.wrap{
  max-width:1240px;
  margin:0 auto;
  padding:0 32px;
}

section{
  position:relative;
  padding:140px 0;
}

.eyebrow{
  display:inline-flex;
  align-items:center;
  gap:10px;
  font-size:12.5px;
  letter-spacing:0.22em;
  text-transform:uppercase;
  color:var(--violet-bright);
  font-weight:600;
  margin-bottom:22px;
}
.eyebrow::before{
  content:"";
  width:22px;
  height:1px;
  background:var(--violet);
  display:inline-block;
}

h1,h2,h3,h4{
  font-family:var(--font-display);
  font-weight:700;
  letter-spacing:-0.01em;
  line-height:1.05;
}

.section-title{
  font-size:clamp(2rem, 4.4vw, 3.4rem);
  margin-bottom:16px;
}

.section-sub{
  color:var(--text-dim);
  font-size:1.05rem;
  max-width:560px;
  line-height:1.6;
}

/* ============ CURSOR (desktop only) ============ */
.cursor-dot, .cursor-ring{
  position:fixed;
  top:0; left:0;
  border-radius:50%;
  pointer-events:none;
  z-index:9999;
  transform:translate(-50%,-50%);
  will-change:transform;
}
.cursor-dot{
  width:6px; height:6px;
  background:var(--violet-bright);
  box-shadow:0 0 10px 2px var(--violet-glow);
  transition:opacity .2s;
}
.cursor-ring{
  width:34px; height:34px;
  border:1px solid rgba(155,77,255,0.55);
  transition:width .25s var(--ease), height .25s var(--ease), border-color .25s, opacity .2s, background .25s;
}
.cursor-ring.swell{
  width:64px; height:64px;
  background:rgba(155,77,255,0.08);
  border-color:var(--violet-bright);
}
body.touch .cursor-dot, body.touch .cursor-ring{display:none;}

/* ============ SCROLL PROGRESS ============ */
.progress-h{
  position:fixed; top:0; left:0; height:3px; width:0%;
  background:linear-gradient(90deg, var(--violet-deep), var(--violet), var(--violet-bright));
  z-index:9997;
  box-shadow:0 0 12px var(--violet-glow);
}
.progress-h .dot{
  position:absolute; right:-4px; top:50%; transform:translateY(-50%);
  width:8px; height:8px; border-radius:50%;
  background:var(--violet-bright);
  box-shadow:0 0 10px 3px var(--violet-glow);
}
.progress-v{
  position:fixed; top:0; right:14px; width:3px; height:100%;
  z-index:9997; pointer-events:none;
}
.progress-v .track{
  position:absolute; top:0; right:0; width:100%; height:100%;
  background:var(--line);
  border-radius:2px;
}
.progress-v .fill{
  position:absolute; bottom:0; right:0; width:100%; height:0%;
  background:linear-gradient(180deg, var(--violet-bright), var(--violet), var(--violet-deep));
  border-radius:2px;
  box-shadow:0 0 12px var(--violet-glow);
}
.progress-v .dot{
  position:absolute; left:50%; transform:translate(-50%,50%); bottom:0%;
  width:8px; height:8px; border-radius:50%;
  background:var(--violet-bright);
  box-shadow:0 0 10px 3px var(--violet-glow);
}
@media (max-width:860px){ .progress-v{display:none;} }

/* ============ NAV ============ */
header{
  position:fixed;
  top:0; left:0; right:0;
  z-index:900;
  padding:22px 0;
  transition:background .35s var(--ease), border-color .35s var(--ease), padding .35s var(--ease);
  border-bottom:1px solid transparent;
}
header.scrolled{
  background:rgba(7,6,10,0.78);
  backdrop-filter:blur(14px);
  -webkit-backdrop-filter:blur(14px);
  border-bottom:1px solid var(--line);
  padding:14px 0;
}
nav.wrap{
  display:flex;
  align-items:center;
  justify-content:space-between;
}
.logo{
  font-family:var(--font-display);
  font-weight:700;
  font-size:1.05rem;
  letter-spacing:-0.01em;
  display:flex;
  align-items:center;
  gap:10px;
  user-select:none;
  white-space:nowrap;
}
.logo .mark{
  width:11px; height:11px; border-radius:3px;
  background:var(--violet);
  box-shadow:0 0 14px 2px var(--violet-glow);
  transition:transform .4s var(--ease), background .4s;
  flex-shrink:0;
}
.logo:hover .mark{transform:rotate(135deg) scale(1.15);}

.nav-links{
  display:flex;
  align-items:center;
  gap:22px;
}
.nav-links a{
  font-size:0.87rem;
  color:var(--text-dim);
  font-weight:500;
  position:relative;
  padding:4px 0;
  transition:color .25s;
}
.nav-links a::after{
  content:"";
  position:absolute;
  left:0; bottom:-2px;
  width:0%; height:1px;
  background:var(--violet-bright);
  transition:width .3s var(--ease);
}
.nav-links a:hover, .nav-links a.active{color:var(--text);}
.nav-links a:hover::after, .nav-links a.active::after{width:100%;}

.nav-cta{
  display:inline-flex;
  align-items:center;
  gap:8px;
  padding:9px 18px;
  border-radius:100px;
  border:1px solid var(--line);
  font-size:0.85rem;
  font-weight:600;
  transition:border-color .3s, background .3s;
}
.nav-cta:hover{border-color:var(--violet); background:rgba(155,77,255,0.08);}
.nav-toggle{display:none; font-size:1.3rem;}

@media (max-width:1180px){
  .nav-links{
    position:fixed; top:0; right:0; height:100vh; width:min(78vw,320px);
    background:rgba(10,9,14,0.98);
    backdrop-filter:blur(20px);
    flex-direction:column; justify-content:center; align-items:flex-start;
    gap:26px; padding:40px;
    transform:translateX(100%);
    transition:transform .45s var(--ease);
    border-left:1px solid var(--line);
  }
  .nav-links.open{transform:translateX(0);}
  .nav-links a{font-size:1.1rem;}
  .nav-toggle{display:block;}
  .nav-cta{display:none;}
}

/* ============ HERO ============ */
.hero{
  min-height:100vh;
  display:flex;
  align-items:center;
  position:relative;
  padding-top:120px;
  overflow:hidden;
}
.hero-canvas{
  position:absolute; inset:0;
  z-index:0;
  opacity:0.9;
}
.hero-canvas canvas{width:100%; height:100%; display:block;}
.hero .wrap{position:relative; z-index:2;}

.hero-top{
  display:flex; align-items:center; gap:16px;
  margin-bottom:34px;
}
.avatar{
  width:52px; height:52px; border-radius:50%;
  display:flex; align-items:center; justify-content:center;
  background:linear-gradient(145deg, var(--violet-deep), var(--violet));
  font-family:var(--font-display);
  font-weight:700; font-size:1.05rem;
  border:1px solid rgba(255,255,255,0.15);
  box-shadow:0 0 30px -4px var(--violet-glow);
  flex-shrink:0;
}
.hero-badge{
  font-size:0.82rem; color:var(--text-dim);
  display:flex; align-items:center; gap:8px;
}
.hero-badge .pulse{
  width:7px; height:7px; border-radius:50%;
  background:#57e08a;
  box-shadow:0 0 8px 2px rgba(87,224,138,0.6);
  animation:pulse 2s ease-in-out infinite;
}
@keyframes pulse{0%,100%{opacity:1;}50%{opacity:0.35;}}

.hero-name{
  font-size:clamp(3rem, 9.4vw, 7.6rem);
  line-height:0.92;
  font-weight:800;
  letter-spacing:-0.03em;
  overflow:hidden;
}
.hero-name .line{display:block; overflow:hidden;}
.hero-name span{
  display:inline-block;
  transform:translateY(115%);
  animation:riseIn 0.95s var(--ease) forwards;
}
@keyframes riseIn{to{transform:translateY(0);}}

.hero-title{
  font-family:var(--font-display);
  font-size:clamp(1.2rem, 2.4vw, 1.9rem);
  color:var(--violet-bright);
  font-weight:600;
  margin-top:18px;
  opacity:0;
  animation:fadeUp .8s var(--ease) forwards;
  animation-delay:0.55s;
}

.hero-tagline{
  margin-top:26px;
  max-width:640px;
  font-size:clamp(1rem, 1.6vw, 1.18rem);
  color:var(--text-dim);
  line-height:1.65;
  opacity:0;
  animation:fadeUp .8s var(--ease) forwards;
  animation-delay:0.72s;
}
.scramble{color:var(--text); font-weight:600; border-bottom:1px dashed rgba(155,77,255,0.5);}

@keyframes fadeUp{
  from{opacity:0; transform:translateY(16px);}
  to{opacity:1; transform:translateY(0);}
}

.hero-ctas{
  margin-top:42px;
  display:flex;
  flex-wrap:wrap;
  gap:16px;
  opacity:0;
  animation:fadeUp .8s var(--ease) forwards;
  animation-delay:0.9s;
}

.btn{
  position:relative;
  display:inline-flex;
  align-items:center;
  gap:10px;
  padding:15px 30px;
  border-radius:100px;
  font-weight:600;
  font-size:0.95rem;
  transition:transform .3s var(--ease), box-shadow .3s var(--ease), background .3s, border-color .3s;
  will-change:transform;
}
.btn-primary{
  background:linear-gradient(135deg, var(--violet), var(--violet-deep));
  color:#fff;
  box-shadow:0 8px 30px -8px var(--violet-glow);
}
.btn-primary:hover{box-shadow:0 12px 40px -6px var(--violet-glow); transform:translateY(-2px);}
.btn-ghost{
  border:1px solid var(--line);
  color:var(--text);
}
.btn-ghost:hover{border-color:var(--violet); background:rgba(155,77,255,0.07);}

.scroll-cue{
  position:absolute;
  bottom:38px; left:50%;
  transform:translateX(-50%);
  display:flex; flex-direction:column; align-items:center; gap:8px;
  font-size:0.72rem; letter-spacing:0.15em; text-transform:uppercase;
  color:var(--text-faint);
  opacity:0;
  animation:fadeUp 1s var(--ease) forwards;
  animation-delay:1.2s;
}
.scroll-cue .stick{
  width:1px; height:34px;
  background:linear-gradient(180deg, var(--violet-bright), transparent);
  animation:stick 1.8s ease-in-out infinite;
}
@keyframes stick{0%{opacity:0.2;}50%{opacity:1;}100%{opacity:0.2;}}

/* ============ REVEAL ============ */
.reveal{opacity:0; transform:translateY(36px); transition:opacity .8s var(--ease), transform .8s var(--ease);}
.reveal.in{opacity:1; transform:translateY(0);}
.reveal-stagger > *{opacity:0; transform:translateY(28px); transition:opacity .7s var(--ease), transform .7s var(--ease);}
.reveal-stagger.in > *{opacity:1; transform:translateY(0);}
.reveal-stagger.in > *:nth-child(1){transition-delay:.05s;}
.reveal-stagger.in > *:nth-child(2){transition-delay:.12s;}
.reveal-stagger.in > *:nth-child(3){transition-delay:.19s;}
.reveal-stagger.in > *:nth-child(4){transition-delay:.26s;}
.reveal-stagger.in > *:nth-child(5){transition-delay:.33s;}
.reveal-stagger.in > *:nth-child(6){transition-delay:.4s;}

/* ============ ABOUT / BENTO ============ */
.about-grid{
  display:grid;
  grid-template-columns:repeat(6, 1fr);
  grid-auto-rows:minmax(120px,auto);
  gap:16px;
  margin-top:52px;
}
.bento-cell{
  position:relative;
  border:1px solid var(--line);
  border-radius:20px;
  background:linear-gradient(160deg, var(--surface), var(--charcoal));
  padding:30px;
  overflow:hidden;
  transition:border-color .35s, transform .12s linear;
  transform-style:preserve-3d;
}
.bento-cell::before{
  content:"";
  position:absolute; inset:0;
  background:radial-gradient(320px circle at var(--x,50%) var(--y,50%), rgba(155,77,255,0.16), transparent 65%);
  opacity:0;
  transition:opacity .4s;
  pointer-events:none;
}
.bento-cell:hover::before{opacity:1;}
.bento-cell:hover{border-color:rgba(155,77,255,0.4);}

.bio-cell{grid-column:span 3; grid-row:span 2; display:flex; flex-direction:column; justify-content:center;}
.bio-cell p{color:var(--text-dim); font-size:1.05rem; line-height:1.75;}
.bio-cell p + p{margin-top:14px;}
.bio-cell .quote-mark{
  font-family:var(--font-display); font-size:3rem; color:var(--violet); line-height:0.5; margin-bottom:14px; display:block;
}

.stat-cell{grid-column:span 3; display:flex; flex-direction:column; justify-content:center; align-items:flex-start;}
.stat-cell .num{
  font-family:var(--font-display); font-weight:800;
  font-size:clamp(2.1rem, 3.6vw, 2.9rem);
  color:var(--text);
  background:linear-gradient(135deg, var(--text), var(--violet-bright));
  -webkit-background-clip:text; background-clip:text; color:transparent;
}
.stat-cell .label{color:var(--text-faint); font-size:0.85rem; margin-top:6px; letter-spacing:0.02em;}

@media (max-width:900px){
  .about-grid{grid-template-columns:repeat(2,1fr);}
  .bio-cell{grid-column:span 2; grid-row:auto;}
  .stat-cell{grid-column:span 1;}
}

/* ============ ARCHITECTURE ============ */
.arch-frame{
  margin-top:52px;
  border:1px solid var(--line);
  border-radius:24px;
  background:linear-gradient(160deg, var(--surface), var(--charcoal));
  padding:36px 28px;
  position:relative;
  overflow:hidden;
}
.arch-frame::before{
  content:"";
  position:absolute; inset:0;
  background-image:linear-gradient(rgba(155,77,255,0.05) 1px, transparent 1px), linear-gradient(90deg, rgba(155,77,255,0.05) 1px, transparent 1px);
  background-size:34px 34px;
  pointer-events:none;
}
.arch-frame .arch-caption{
  display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; gap:10px;
  margin-bottom:8px; position:relative; z-index:1;
}
.arch-caption .tag-pill{
  font-size:0.72rem; letter-spacing:0.12em; text-transform:uppercase;
  color:var(--violet-bright); font-weight:700;
  border:1px solid rgba(155,77,255,0.3); border-radius:100px; padding:6px 14px;
}
.arch-caption .legend{display:flex; gap:18px; font-size:0.78rem; color:var(--text-faint);}
.arch-caption .legend span{display:inline-flex; align-items:center; gap:6px;}
.arch-caption .legend i{width:9px; height:9px; border-radius:2px; display:inline-block;}
.legend .streaming-dot{background:var(--violet-bright);}
.legend .batch-dot{background:#5b8dff;}
.legend .quality-dot{background:#57e08a;}

.arch-svg{width:100%; height:auto; display:block; position:relative; z-index:1;}
.arch-node rect{
  fill:var(--surface-2);
  stroke:var(--line);
  stroke-width:1.4;
  transition:stroke .3s;
}
.arch-node:hover rect{stroke:var(--violet);}
.arch-node .n-title{font-family:'Plus Jakarta Sans',sans-serif; font-weight:700; fill:var(--text); font-size:15px;}
.arch-node .n-sub{font-family:'Plus Jakarta Sans',sans-serif; fill:var(--text-faint); font-size:11.5px;}
.arch-node .n-icon{fill:var(--violet-bright);}
.arch-flow-line{
  fill:none; stroke:rgba(155,77,255,0.55); stroke-width:1.6;
  stroke-dasharray:6 7;
  animation:flowdash 1.6s linear infinite;
}
.arch-flow-line.batch{stroke:rgba(91,141,255,0.55);}
.arch-flow-line.quality{stroke:rgba(87,224,138,0.6);}
@keyframes flowdash{to{stroke-dashoffset:-52;}}
.arch-pulse{fill:var(--violet-bright); filter:drop-shadow(0 0 5px var(--violet-bright));}

.competency-strip{
  margin-top:16px;
  display:grid;
  grid-template-columns:repeat(6,1fr);
  gap:14px;
}
.competency-chip{
  border:1px solid var(--line);
  border-radius:16px;
  padding:20px 16px;
  background:rgba(255,255,255,0.015);
  text-align:center;
  transition:border-color .3s, transform .3s;
}
.competency-chip:hover{border-color:var(--violet); transform:translateY(-3px);}
.competency-chip i{font-size:1.3rem; color:var(--violet-bright); margin-bottom:12px; display:block;}
.competency-chip .c-title{font-weight:700; font-size:0.85rem; margin-bottom:4px;}
.competency-chip .c-sub{font-size:0.72rem; color:var(--text-faint); line-height:1.4;}

@media (max-width:900px){
  .competency-strip{grid-template-columns:repeat(3,1fr);}
}
@media (max-width:600px){
  .competency-strip{grid-template-columns:repeat(2,1fr);}
  .arch-frame{padding:24px 14px;}
}

/* ============ CERTIFICATIONS ============ */
.cert-stats{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:16px;
  margin:52px 0 44px;
}
.cert-stat{
  border:1px solid var(--line);
  border-radius:18px;
  padding:26px 24px;
  background:linear-gradient(160deg, var(--surface), var(--charcoal));
  text-align:center;
}
.cert-stat .num{
  font-family:var(--font-display); font-weight:800;
  font-size:clamp(1.9rem, 3vw, 2.5rem);
  background:linear-gradient(135deg, var(--text), var(--violet-bright));
  -webkit-background-clip:text; background-clip:text; color:transparent;
}
.cert-stat .label{color:var(--text-faint); font-size:0.82rem; margin-top:6px;}

.cert-group-label{
  font-size:0.72rem; letter-spacing:0.16em; text-transform:uppercase;
  color:var(--violet-bright); font-weight:700;
  margin:36px 0 20px;
  display:flex; align-items:center; gap:12px;
}
.cert-group-label::after{
  content:""; flex:1; height:1px; background:var(--line);
}
.cert-group-label:first-of-type{margin-top:0;}

.cert-grid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:20px;
}
.cert-card{
  position:relative;
  border-radius:22px;
  padding:30px 26px;
  background:rgba(255,255,255,0.035);
  backdrop-filter:blur(18px);
  -webkit-backdrop-filter:blur(18px);
  border:1px solid rgba(245,243,247,0.1);
  overflow:hidden;
  transition:transform .35s var(--ease), border-color .35s, box-shadow .35s;
  transform-style:preserve-3d;
}
.cert-card::before{
  content:"";
  position:absolute; inset:0;
  border-radius:22px;
  padding:1px;
  background:linear-gradient(140deg, rgba(155,77,255,0.5), transparent 40%, transparent 70%, rgba(155,77,255,0.35));
  -webkit-mask:linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0);
  -webkit-mask-composite:xor;
  mask-composite:exclude;
  pointer-events:none;
  opacity:.6;
  transition:opacity .35s;
}
.cert-card::after{
  content:"";
  position:absolute; inset:0;
  background:radial-gradient(280px circle at var(--x,50%) var(--y,50%), rgba(155,77,255,0.18), transparent 65%);
  opacity:0;
  transition:opacity .4s;
  pointer-events:none;
}
.cert-card:hover::after{opacity:1;}
.cert-card:hover{
  border-color:rgba(155,77,255,0.45);
  box-shadow:0 20px 50px -20px rgba(155,77,255,0.35);
}

.cert-card-top{
  display:flex; align-items:flex-start; justify-content:space-between; gap:12px; margin-bottom:20px;
}
.cert-icon{
  width:52px; height:52px; border-radius:14px;
  display:flex; align-items:center; justify-content:center;
  background:linear-gradient(150deg, rgba(155,77,255,0.22), rgba(155,77,255,0.05));
  border:1px solid rgba(155,77,255,0.3);
  font-size:1.3rem;
  color:var(--violet-bright);
  flex-shrink:0;
}
.cert-icon.aws{color:#ff9900; border-color:rgba(255,153,0,0.35); background:linear-gradient(150deg, rgba(255,153,0,0.18), rgba(255,153,0,0.04));}

.featured-badge{
  font-size:0.65rem; letter-spacing:0.08em; text-transform:uppercase; font-weight:700;
  color:#0d0715; background:var(--violet-bright);
  padding:5px 11px; border-radius:100px;
  display:inline-flex; align-items:center; gap:5px;
  white-space:nowrap;
}
.featured-badge i{font-size:0.65rem;}

.cert-card h3{
  font-size:1.12rem; margin-bottom:8px; line-height:1.3;
}
.cert-org{
  color:var(--violet-bright); font-size:0.85rem; font-weight:600; margin-bottom:14px;
}
.cert-meta-row{
  display:flex; flex-wrap:wrap; gap:8px 16px;
  font-size:0.78rem; color:var(--text-faint);
  margin-bottom:18px;
}
.cert-meta-row span{display:inline-flex; align-items:center; gap:6px;}
.cert-meta-row i{color:var(--violet); font-size:0.75rem;}

.cert-verify{
  display:inline-flex; align-items:center; gap:8px;
  font-size:0.83rem; font-weight:600; color:var(--text);
  padding:9px 16px;
  border-radius:100px;
  border:1px solid var(--line);
  transition:border-color .3s, background .3s, gap .3s;
}
.cert-verify:hover{border-color:var(--violet); background:rgba(155,77,255,0.1); gap:11px;}

@media (max-width:900px){
  .cert-stats{grid-template-columns:1fr; }
  .cert-grid{grid-template-columns:1fr 1fr;}
}
@media (max-width:600px){
  .cert-grid{grid-template-columns:1fr;}
}

/* ============ MARQUEE ============ */
.marquee-strip{
  border-top:1px solid var(--line);
  border-bottom:1px solid var(--line);
  padding:26px 0;
  overflow:hidden;
  background:var(--charcoal);
  white-space:nowrap;
  position:relative;
}
.marquee-track{
  display:inline-flex;
  gap:0;
  animation:scroll-x 38s linear infinite;
}
.marquee-strip:hover .marquee-track{animation-play-state:paused;}
.marquee-track span{
  font-family:var(--font-display);
  font-size:1.35rem;
  font-weight:600;
  color:var(--text-faint);
  padding:0 28px;
  display:inline-flex;
  align-items:center;
  gap:28px;
}
.marquee-track span i{color:var(--violet); font-size:0.5rem;}
@keyframes scroll-x{from{transform:translateX(0);}to{transform:translateX(-50%);}}

/* ============ SKILLS ============ */
.skills-grid{
  display:grid;
  grid-template-columns:repeat(6,1fr);
  gap:16px;
  margin-top:52px;
}
.skill-cell{grid-column:span 2;}
.skill-cell:nth-child(1), .skill-cell:nth-child(4){grid-column:span 3;}
.skill-cell h4{
  font-size:0.72rem; letter-spacing:0.16em; text-transform:uppercase;
  color:var(--violet-bright); margin-bottom:18px; font-weight:700;
}
.tag-row{display:flex; flex-wrap:wrap; gap:9px;}
.tag{
  font-size:0.83rem;
  padding:8px 14px;
  border-radius:100px;
  border:1px solid var(--line);
  color:var(--text-dim);
  background:rgba(255,255,255,0.02);
  transition:border-color .25s, color .25s, transform .2s;
}
.bento-cell:hover .tag{transition-delay:.02s;}
.tag:hover{border-color:var(--violet); color:var(--text); transform:translateY(-2px);}

@media (max-width:900px){
  .skills-grid{grid-template-columns:repeat(2,1fr);}
  .skill-cell, .skill-cell:nth-child(1), .skill-cell:nth-child(4){grid-column:span 2;}
}

/* ============ PROJECTS ============ */
.project-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:20px;
  margin-top:52px;
}
.project-card{
  border:1px solid var(--line);
  border-radius:20px;
  padding:34px;
  background:linear-gradient(160deg, var(--surface), var(--charcoal));
  transition:border-color .3s, transform .12s linear;
  transform-style:preserve-3d;
  display:flex; flex-direction:column;
}
.project-card:hover{border-color:rgba(155,77,255,0.4);}
.project-index{
  font-family:var(--font-display);
  font-size:0.85rem; color:var(--violet-bright); font-weight:700; letter-spacing:0.05em;
  margin-bottom:18px;
  display:flex; align-items:center; justify-content:space-between; gap:10px;
}
.de-badge{
  font-family:var(--font-body);
  font-size:0.68rem; letter-spacing:0.08em; text-transform:uppercase; font-weight:700;
  color:#0d0715; background:var(--violet-bright);
  padding:5px 11px; border-radius:100px;
}

.project-card h3{
  font-size:1.4rem; margin-bottom:12px;
}
.project-card p{
  color:var(--text-dim); font-size:0.95rem; line-height:1.65; flex-grow:1; margin-bottom:20px;
}
.project-tags{display:flex; flex-wrap:wrap; gap:8px;}
.project-tags span{
  font-size:0.75rem;
  padding:5px 12px;
  border-radius:100px;
  background:rgba(155,77,255,0.09);
  color:var(--violet-bright);
  border:1px solid rgba(155,77,255,0.22);
}
.project-github{
  display:inline-flex; align-items:center; gap:8px;
  margin-top:22px;
  font-size:0.85rem; font-weight:600; color:var(--text);
  padding:10px 18px;
  border-radius:100px;
  border:1px solid var(--line);
  align-self:flex-start;
  transition:border-color .3s, background .3s, gap .3s;
}
.project-github:hover{border-color:var(--violet); background:rgba(155,77,255,0.09); gap:11px;}
.other-projects{margin-top:60px;}
.other-projects h4{
  font-size:0.72rem; letter-spacing:0.16em; text-transform:uppercase;
  color:var(--text-faint); margin-bottom:22px; font-weight:700;
}
.other-list{display:grid; grid-template-columns:repeat(4,1fr); gap:16px;}
.other-item{
  border:1px solid var(--line); border-radius:16px; padding:22px;
  background:rgba(255,255,255,0.015); transition:border-color .3s;
}
.other-item:hover{border-color:rgba(155,77,255,0.35);}
.other-item h5{font-size:1rem; margin-bottom:8px; font-family:var(--font-display);}
.other-item p{color:var(--text-faint); font-size:0.85rem; line-height:1.55;}
.other-github{
  display:inline-flex; align-items:center; gap:6px; margin-top:14px;
  font-size:0.78rem; font-weight:600; color:var(--text-dim); transition:color .25s;
}
.other-github:hover{color:var(--violet-bright);}
@media (max-width:1000px){ .other-list{grid-template-columns:repeat(2,1fr);} }
@media (max-width:640px){ .other-list{grid-template-columns:1fr;} }
@media (max-width:760px){ .project-grid{grid-template-columns:1fr;} }

/* ============ EXPERIENCE ============ */
.timeline{
  margin-top:60px;
  position:relative;
  padding-left:36px;
}
.timeline::before{
  content:"";
  position:absolute; left:0; top:6px; bottom:6px; width:1px;
  background:linear-gradient(180deg, var(--violet), rgba(155,77,255,0.05));
}
.timeline-item{
  position:relative;
  padding-bottom:56px;
}
.timeline-item:last-child{padding-bottom:0;}
.timeline-item::before{
  content:"";
  position:absolute; left:-40px; top:6px;
  width:11px; height:11px; border-radius:50%;
  background:var(--void);
  border:2px solid var(--violet);
  box-shadow:0 0 0 4px rgba(155,77,255,0.12);
}
.timeline-head{
  display:flex; flex-wrap:wrap; align-items:baseline; justify-content:space-between; gap:10px;
  margin-bottom:14px;
}
.timeline-head h3{font-size:1.3rem;}
.timeline-head h3 span{color:var(--violet-bright);}
.timeline-meta{color:var(--text-faint); font-size:0.85rem; white-space:nowrap;}
.timeline-item ul{display:flex; flex-direction:column; gap:10px;}
.timeline-item li{
  color:var(--text-dim); font-size:0.97rem; line-height:1.65;
  padding-left:20px; position:relative;
}
.timeline-item li::before{
  content:"—"; position:absolute; left:0; color:var(--violet);
}

/* ============ EDUCATION / CERTS ============ */
.edu-single{
  margin-top:52px;
  max-width:640px;
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:40px;
}
.edu-single .edu-item{margin-bottom:0;}
.edu-item:last-child{margin-bottom:0;}
.edu-item .deg{font-family:var(--font-display); font-weight:700; font-size:1.08rem;}
.edu-item .school{color:var(--text-dim); font-size:0.92rem; margin-top:4px;}
.edu-item .meta{color:var(--text-faint); font-size:0.82rem; margin-top:4px;}

@media (max-width:760px){ .edu-single{grid-template-columns:1fr; gap:30px;} }

/* ============ CLOSER ============ */
.closer{
  text-align:center;
  padding:180px 0 140px;
  position:relative;
}
.closer-glow{
  position:absolute; left:50%; top:20%; transform:translateX(-50%);
  width:600px; height:600px;
  background:radial-gradient(circle, rgba(155,77,255,0.28), transparent 70%);
  filter:blur(40px);
  z-index:0;
  pointer-events:none;
}
.closer .wrap{position:relative; z-index:1;}
.closer h2{
  font-size:clamp(2.2rem, 6vw, 4.4rem);
  max-width:800px; margin:0 auto 26px;
}
.closer p{color:var(--text-dim); font-size:1.1rem; max-width:520px; margin:0 auto 44px;}
.closer .hero-ctas{justify-content:center; margin-top:0;}

.contact-links{
  margin-top:70px;
  display:flex; flex-wrap:wrap; justify-content:center; gap:14px;
}
.contact-links a{
  display:inline-flex; align-items:center; gap:10px;
  padding:13px 22px;
  border-radius:100px;
  border:1px solid var(--line);
  font-size:0.9rem; font-weight:500;
  transition:border-color .3s, background .3s, transform .3s;
}
.contact-links a:hover{border-color:var(--violet); background:rgba(155,77,255,0.08); transform:translateY(-2px);}
.contact-links a i{color:var(--violet-bright);}

/* ============ FOOTER ============ */
footer{
  border-top:1px solid var(--line);
  padding:34px 0;
  text-align:center;
  color:var(--text-faint);
  font-size:0.82rem;
}
footer .hint{margin-top:6px; font-size:0.74rem; opacity:0.6;}

/* ============ THEME TOAST ============ */
.theme-toast{
  position:fixed; bottom:28px; left:50%; transform:translate(-50%, 20px);
  background:var(--surface-2); border:1px solid var(--violet);
  padding:11px 20px; border-radius:100px;
  font-size:0.85rem; font-weight:600;
  display:flex; align-items:center; gap:10px;
  opacity:0; pointer-events:none;
  transition:opacity .35s var(--ease), transform .35s var(--ease);
  z-index:9999;
  box-shadow:0 10px 40px -10px rgba(0,0,0,0.6);
}
.theme-toast.show{opacity:1; transform:translate(-50%, 0);}
.theme-toast .swatch{width:12px; height:12px; border-radius:50%; background:var(--violet);}

/* utility */
.gradient-text{
  background:linear-gradient(135deg, var(--text), var(--violet-bright));
  -webkit-background-clip:text; background-clip:text; color:transparent;
}

@media (max-width:600px){
  section{padding:90px 0;}
  .wrap{padding:0 22px;}
}
</style>
</head>
<body>

<div class="cursor-dot" id="cursorDot"></div>
<div class="cursor-ring" id="cursorRing"></div>

<div class="progress-h" id="progressH"><div class="dot"></div></div>
<div class="progress-v" id="progressV">
  <div class="track"></div>
  <div class="fill" id="progressVFill"></div>
  <div class="dot" id="progressVDot"></div>
</div>

<div class="theme-toast" id="themeToast"><span class="swatch" id="themeSwatch"></span><span id="themeLabel">Violet Dusk</span></div>

<header id="siteHeader">
  <nav class="wrap">
    <a href="#hero" class="logo" id="logoBtn"><span class="mark"></span>Anitha Raj Bale</a>
    <ul class="nav-links" id="navLinks">
      <li><a href="#about" class="nav-link">About</a></li>
      <li><a href="#architecture" class="nav-link">Architecture</a></li>
      <li><a href="#skills" class="nav-link">Skills</a></li>
      <li><a href="#certifications" class="nav-link">Certifications</a></li>
      <li><a href="#projects" class="nav-link">Projects</a></li>
      <li><a href="#experience" class="nav-link">Experience</a></li>
      <li><a href="#education" class="nav-link">Education</a></li>
      <li><a href="#contact" class="nav-link">Contact</a></li>
    </ul>
    <a href="#contact" class="nav-cta">Let's talk</a>
    <button class="nav-toggle" id="navToggle" aria-label="Toggle menu"><i class="fa-solid fa-bars"></i></button>
  </nav>
</header>

<!-- HERO -->
<section class="hero" id="hero">
  <div class="hero-canvas"><canvas id="heroCanvas"></canvas></div>
  <div class="wrap">
    <div class="hero-top">
      <div class="avatar">AB</div>
      <div class="hero-badge"><span class="pulse"></span> Kafka · Spark · Airflow · dbt · Snowflake · Databricks · AWS · RAG</div>
    </div>
    <h1 class="hero-name">
      <span class="line"><span style="animation-delay:.05s">Anitha</span></span>
      <span class="line"><span style="animation-delay:.15s">Raj Bale</span></span>
    </h1>
    <div class="hero-title">Senior Data Engineer — AI/ML &amp; Streaming Cloud Platforms</div>
    <p class="hero-tagline">I build scalable data platforms across financial, healthcare, and AI-driven environments — streaming ingestion and warehouse modeling joined to ML-ready pipelines, embeddings, and RAG retrieval — with schema governance, lineage, and data quality teams can <span class="scramble" id="scrambleWord">trust</span>.</p>
    <div class="hero-ctas">
      <a href="#projects" class="btn btn-primary magnetic"><i class="fa-solid fa-arrow-down"></i> View my work</a>
      <a href="#contact" class="btn btn-ghost magnetic">Get in touch</a>
      <a href="data:text/html;base64,PCFET0NUWVBFIGh0bWw+CjxodG1sIGxhbmc9ImVuIj4KPGhlYWQ+CjxtZXRhIGNoYXJzZXQ9InV0Zi04Ij4KPG1ldGEgbmFtZT0idmlld3BvcnQiIGNvbnRlbnQ9IndpZHRoPWRldmljZS13aWR0aCwgaW5pdGlhbC1zY2FsZT0xIj4KPHRpdGxlPkFuaXRoYSBSYWogQmFsZSDigJQgUmVzdW1lPC90aXRsZT4KPHN0eWxlPgogIDpyb290ewogICAgLS1pbms6IzFiMTczMDsKICAgIC0tYm9keTojM2EzNTUyOwogICAgLS1tdXRlZDojNmY2YTg2OwogICAgLS1hY2NlbnQ6IzViM2ZhNjsKICAgIC0tcnVsZTojZGRkOWU2OwogICAgLS1wYXBlcjojZmZmZmZmOwogICAgLS13YXNoOiNmNmY0ZmE7CiAgfQogICp7Ym94LXNpemluZzpib3JkZXItYm94O30KICBodG1sey13ZWJraXQtdGV4dC1zaXplLWFkanVzdDoxMDAlO30KICBib2R5ewogICAgbWFyZ2luOjA7CiAgICBiYWNrZ3JvdW5kOnZhcigtLXdhc2gpOwogICAgY29sb3I6dmFyKC0tYm9keSk7CiAgICBmb250LWZhbWlseToiSW50ZXIiLCJTZWdvZSBVSSIsSGVsdmV0aWNhLEFyaWFsLHNhbnMtc2VyaWY7CiAgICBmb250LXNpemU6MTAuNHB0OwogICAgbGluZS1oZWlnaHQ6MS41OwogIH0KICAuc2hlZXR7CiAgICBtYXgtd2lkdGg6OC41aW47CiAgICBtYXJnaW46MjhweCBhdXRvOwogICAgcGFkZGluZzowLjYyaW4gMC43aW4gMC43aW47CiAgICBiYWNrZ3JvdW5kOnZhcigtLXBhcGVyKTsKICAgIGJveC1zaGFkb3c6MCAycHggMThweCByZ2JhKDI3LDIzLDQ4LC4xMCk7CiAgfQoKICAvKiBIZWFkZXIgKi8KICBoZWFkZXJ7bWFyZ2luLWJvdHRvbToxOHB4O30KICBoMXsKICAgIGZvbnQtZmFtaWx5OiJJb3dhbiBPbGQgU3R5bGUiLCJQYWxhdGlubyBMaW5vdHlwZSIsUGFsYXRpbm8sR2VvcmdpYSxzZXJpZjsKICAgIGZvbnQtc2l6ZToyN3B0OwogICAgZm9udC13ZWlnaHQ6NjAwOwogICAgbGV0dGVyLXNwYWNpbmc6LS4wMWVtOwogICAgY29sb3I6dmFyKC0taW5rKTsKICAgIG1hcmdpbjowIDAgM3B4OwogIH0KICAucm9sZXsKICAgIGZvbnQtc2l6ZToxMXB0OwogICAgY29sb3I6dmFyKC0tYWNjZW50KTsKICAgIGZvbnQtd2VpZ2h0OjYwMDsKICAgIG1hcmdpbjowIDAgOXB4OwogIH0KICAuY29udGFjdHsKICAgIGZvbnQtc2l6ZTo5LjRwdDsKICAgIGNvbG9yOnZhcigtLW11dGVkKTsKICAgIGxpbmUtaGVpZ2h0OjEuNzsKICB9CiAgLmNvbnRhY3QgYXtjb2xvcjp2YXIoLS1ib2R5KTt0ZXh0LWRlY29yYXRpb246bm9uZTtib3JkZXItYm90dG9tOjFweCBzb2xpZCB2YXIoLS1ydWxlKTt9CiAgLmNvbnRhY3QgYTpob3ZlciwuY29udGFjdCBhOmZvY3Vze2NvbG9yOnZhcigtLWFjY2VudCk7Ym9yZGVyLWJvdHRvbS1jb2xvcjp2YXIoLS1hY2NlbnQpO30KICAuc2Vwe2NvbG9yOnZhcigtLXJ1bGUpO21hcmdpbjowIDdweDt9CgogIC8qIFNlY3Rpb25zICovCiAgc2VjdGlvbnttYXJnaW4tdG9wOjE5cHg7fQogIGgyewogICAgZm9udC1mYW1pbHk6Iklvd2FuIE9sZCBTdHlsZSIsIlBhbGF0aW5vIExpbm90eXBlIixQYWxhdGlubyxHZW9yZ2lhLHNlcmlmOwogICAgZm9udC1zaXplOjEyLjRwdDsKICAgIGZvbnQtd2VpZ2h0OjYwMDsKICAgIGNvbG9yOnZhcigtLWluayk7CiAgICBtYXJnaW46MCAwIDlweDsKICAgIHBhZGRpbmctYm90dG9tOjVweDsKICAgIGJvcmRlci1ib3R0b206MnB4IHNvbGlkIHZhcigtLWFjY2VudCk7CiAgfQogIHAuc3VtbWFyeXttYXJnaW46MDt9CgogIC8qIFNraWxscyAqLwogIC5za2lsbC1yb3d7CiAgICBkaXNwbGF5OmdyaWQ7CiAgICBncmlkLXRlbXBsYXRlLWNvbHVtbnM6MS40NWluIDFmcjsKICAgIGdhcDo0cHggMTRweDsKICAgIHBhZGRpbmc6NHB4IDA7CiAgICBib3JkZXItYm90dG9tOjFweCBzb2xpZCB2YXIoLS1ydWxlKTsKICB9CiAgLnNraWxsLXJvdzpsYXN0LWNoaWxke2JvcmRlci1ib3R0b206bm9uZTt9CiAgLnNraWxsLXJvdyBkdHtmb250LXdlaWdodDo2NTA7Y29sb3I6dmFyKC0taW5rKTt9CiAgLnNraWxsLXJvdyBkZHttYXJnaW46MDt9CiAgZGx7bWFyZ2luOjA7fQoKICAvKiBFeHBlcmllbmNlICovCiAgLmpvYnttYXJnaW4tYm90dG9tOjE0cHg7fQogIC5qb2I6bGFzdC1jaGlsZHttYXJnaW4tYm90dG9tOjA7fQogIC5qb2ItaGVhZHsKICAgIGRpc3BsYXk6ZmxleDsKICAgIGp1c3RpZnktY29udGVudDpzcGFjZS1iZXR3ZWVuOwogICAgYWxpZ24taXRlbXM6YmFzZWxpbmU7CiAgICBnYXA6MTRweDsKICAgIGZsZXgtd3JhcDp3cmFwOwogIH0KICAuam9iLXRpdGxle2ZvbnQtd2VpZ2h0OjcwMDtjb2xvcjp2YXIoLS1pbmspO2ZvbnQtc2l6ZToxMC45cHQ7fQogIC5jb21wYW55e2NvbG9yOnZhcigtLWFjY2VudCk7Zm9udC13ZWlnaHQ6NjAwO30KICAud2hlbntjb2xvcjp2YXIoLS1tdXRlZCk7Zm9udC1zaXplOjkuM3B0O3doaXRlLXNwYWNlOm5vd3JhcDt9CiAgdWx7bWFyZ2luOjVweCAwIDA7cGFkZGluZy1sZWZ0OjE3cHg7fQogIGxpe21hcmdpbi1ib3R0b206M3B4O30KICBsaTo6bWFya2Vye2NvbG9yOnZhcigtLWFjY2VudCk7fQoKICAvKiBQcm9qZWN0cyAqLwogIC5wcm9qZWN0e21hcmdpbi1ib3R0b206MTFweDt9CiAgLnByb2plY3Q6bGFzdC1jaGlsZHttYXJnaW4tYm90dG9tOjA7fQogIC5wcm9qZWN0LXRpdGxle2ZvbnQtd2VpZ2h0OjcwMDtjb2xvcjp2YXIoLS1pbmspO30KICAuc3RhY2t7Y29sb3I6dmFyKC0tbXV0ZWQpO2ZvbnQtc2l6ZTo5LjNwdDtmb250LXN0eWxlOml0YWxpYzt9CiAgLm1pbm9yewogICAgbWFyZ2luLXRvcDo5cHg7CiAgICBwYWRkaW5nOjlweCAxMnB4OwogICAgYmFja2dyb3VuZDp2YXIoLS13YXNoKTsKICB9CiAgLm1pbm9yIHB7bWFyZ2luOjAgMCA1cHg7fQogIC5taW5vciBwOmxhc3QtY2hpbGR7bWFyZ2luLWJvdHRvbTowO30KCiAgLyogQ2VydGlmaWNhdGlvbnMgKi8KICAuY2VydHN7bGlzdC1zdHlsZTpub25lO21hcmdpbjowO3BhZGRpbmc6MDt9CiAgLmNlcnRzIGxpewogICAgcGFkZGluZy1sZWZ0OjE1cHg7CiAgICBwb3NpdGlvbjpyZWxhdGl2ZTsKICAgIG1hcmdpbi1ib3R0b206NHB4OwogIH0KICAuY2VydHMgbGk6OmJlZm9yZXsKICAgIGNvbnRlbnQ6IiI7CiAgICBwb3NpdGlvbjphYnNvbHV0ZTsKICAgIGxlZnQ6MDt0b3A6LjU1ZW07CiAgICB3aWR0aDo2cHg7aGVpZ2h0OjZweDsKICAgIGJhY2tncm91bmQ6dmFyKC0tYWNjZW50KTsKICB9CiAgLmNlcnRzIGF7Y29sb3I6dmFyKC0tYWNjZW50KTt0ZXh0LWRlY29yYXRpb246bm9uZTtib3JkZXItYm90dG9tOjFweCBzb2xpZCB0cmFuc3BhcmVudDt9CiAgLmNlcnRzIGE6aG92ZXIsLmNlcnRzIGE6Zm9jdXN7Ym9yZGVyLWJvdHRvbS1jb2xvcjp2YXIoLS1hY2NlbnQpO30KICAuaXNzdWVye2NvbG9yOnZhcigtLW11dGVkKTt9CgogIC8qIEVkdWNhdGlvbiAqLwogIC5lZHV7CiAgICBkaXNwbGF5OmZsZXg7CiAgICBqdXN0aWZ5LWNvbnRlbnQ6c3BhY2UtYmV0d2VlbjsKICAgIGFsaWduLWl0ZW1zOmJhc2VsaW5lOwogICAgZ2FwOjE0cHg7CiAgICBmbGV4LXdyYXA6d3JhcDsKICAgIHBhZGRpbmc6NnB4IDA7CiAgICBib3JkZXItYm90dG9tOjFweCBzb2xpZCB2YXIoLS1ydWxlKTsKICB9CiAgLmVkdTpsYXN0LWNoaWxke2JvcmRlci1ib3R0b206bm9uZTt9CiAgLmRlZ3JlZXtmb250LXdlaWdodDo3MDA7Y29sb3I6dmFyKC0taW5rKTt9CiAgLnNjaG9vbHtjb2xvcjp2YXIoLS1ib2R5KTt9CgogIGE6Zm9jdXMtdmlzaWJsZXtvdXRsaW5lOjJweCBzb2xpZCB2YXIoLS1hY2NlbnQpO291dGxpbmUtb2Zmc2V0OjJweDt9CgogIEBtZWRpYSAobWF4LXdpZHRoOjY0MHB4KXsKICAgIC5zaGVldHttYXJnaW46MDtwYWRkaW5nOjIycHggMThweDtib3gtc2hhZG93Om5vbmU7fQogICAgaDF7Zm9udC1zaXplOjIycHQ7fQogICAgLnNraWxsLXJvd3tncmlkLXRlbXBsYXRlLWNvbHVtbnM6MWZyO2dhcDoxcHg7fQogIH0KCiAgQG1lZGlhIHByaW50ewogICAgQHBhZ2V7c2l6ZTpsZXR0ZXI7bWFyZ2luOjAuNWluO30KICAgIGJvZHl7YmFja2dyb3VuZDojZmZmO2ZvbnQtc2l6ZTo5LjlwdDt9CiAgICAuc2hlZXR7bWFyZ2luOjA7cGFkZGluZzowO21heC13aWR0aDpub25lO2JveC1zaGFkb3c6bm9uZTt9CiAgICBzZWN0aW9ue2JyZWFrLWluc2lkZTphdXRvO30KICAgIC5qb2IsLnByb2plY3QsLmVkdXticmVhay1pbnNpZGU6YXZvaWQ7fQogICAgaDJ7YnJlYWstYWZ0ZXI6YXZvaWQ7fQogICAgLmNvbnRhY3QgYXtib3JkZXItYm90dG9tOm5vbmU7fQogIH0KPC9zdHlsZT4KPC9oZWFkPgo8Ym9keT4KPGRpdiBjbGFzcz0ic2hlZXQiPgoKICA8aGVhZGVyPgogICAgPGgxPkFuaXRoYSBSYWogQmFsZTwvaDE+CiAgICA8cCBjbGFzcz0icm9sZSI+U2VuaW9yIERhdGEgRW5naW5lZXIg4oCUIEFJL01MICZhbXA7IFN0cmVhbWluZyBDbG91ZCBQbGF0Zm9ybXM8L3A+CiAgICA8ZGl2IGNsYXNzPSJjb250YWN0Ij4KICAgICAgPGEgaHJlZj0ibWFpbHRvOmFuaXRoYXJhamJhbGxlQGdtYWlsLmNvbSI+YW5pdGhhcmFqYmFsbGVAZ21haWwuY29tPC9hPjxzcGFuIGNsYXNzPSJzZXAiPnw8L3NwYW4+KzEgKDQ3NSkgOTg4LTU4NjU8c3BhbiBjbGFzcz0ic2VwIj58PC9zcGFuPk5KLCBVU0E8YnI+CiAgICAgIDxhIGhyZWY9Imh0dHBzOi8vd3d3LmxpbmtlZGluLmNvbS9pbi9hbml0aGEtcmFqLWJhbGUtYThiYTMxMTdiLyI+TGlua2VkSW48L2E+PHNwYW4gY2xhc3M9InNlcCI+fDwvc3Bhbj48YSBocmVmPSJodHRwczovL2dpdGh1Yi5jb20vQW5pdGhhcmFqMzEiPkdpdEh1YjwvYT48c3BhbiBjbGFzcz0ic2VwIj58PC9zcGFuPjxhIGhyZWY9Imh0dHBzOi8vYW5pdGhhcmFqYmFsZTMxLm5ldGxpZnkuYXBwLyI+UG9ydGZvbGlvPC9hPgogICAgPC9kaXY+CiAgPC9oZWFkZXI+CgogIDxzZWN0aW9uPgogICAgPGgyPlN1bW1hcnk8L2gyPgogICAgPHAgY2xhc3M9InN1bW1hcnkiPlNlbmlvciBEYXRhIEVuZ2luZWVyIHdpdGggNSsgeWVhcnMgYnVpbGRpbmcgc2NhbGFibGUgZGF0YSBwbGF0Zm9ybXMgYW5kIHByb2R1Y3Rpb24gcGlwZWxpbmVzIGFjcm9zcyBmaW5hbmNpYWwsIGhlYWx0aGNhcmUsIGFuZCBBSS1kcml2ZW4gZW52aXJvbm1lbnRzLCBwcm9ncmVzc2luZyBmcm9tIGNvcmUgZGF0YSBlbmdpbmVlcmluZyB0byBpbnRlbGxpZ2VudCBkYXRhIGluZnJhc3RydWN0dXJlLiBDb21iaW5lcyBzdHJlYW1pbmcgaW5nZXN0aW9uIGFuZCB3YXJlaG91c2UgbW9kZWxpbmcg4oCUIEthZmthLCBTcGFyaywgQWlyZmxvdywgZGJ0LCBTbm93Zmxha2UsIFJlZHNoaWZ0LCBEYXRhYnJpY2tzLCBhbmQgQVdTIOKAlCB3aXRoIE1MLXJlYWR5IHBpcGVsaW5lcywgZmVhdHVyZSBlbmdpbmVlcmluZywgTUxmbG93LCBHZW5BSSBhbmQgTExNIGRhdGEgcHJvY2Vzc2luZywgUkFHLCBhbmQgdmVjdG9yLWJhc2VkIHJldHJpZXZhbCwgYmFja2VkIGJ5IGEgY29uc2lzdGVudCBmb2N1cyBvbiBzY2hlbWEgZ292ZXJuYW5jZSwgZGF0YSBxdWFsaXR5LCBsaW5lYWdlLCBhbmQgcGVyZm9ybWFuY2UgdHVuaW5nLjwvcD4KICA8L3NlY3Rpb24+CgogIDxzZWN0aW9uPgogICAgPGgyPlRlY2huaWNhbCBTa2lsbHM8L2gyPgogICAgPGRsPgogICAgICA8ZGl2IGNsYXNzPSJza2lsbC1yb3ciPjxkdD5Qcm9ncmFtbWluZyAmYW1wOyBRdWVyeWluZzwvZHQ+PGRkPlB5dGhvbiwgU1FMIChBZHZhbmNlZCBPcHRpbWl6YXRpb24sIFdpbmRvdyBGdW5jdGlvbnMpLCBKYXZhLCBTY2FsYSwgQmFzaCwgSlNPTjwvZGQ+PC9kaXY+CiAgICAgIDxkaXYgY2xhc3M9InNraWxsLXJvdyI+PGR0PkRhdGEgRW5naW5lZXJpbmc8L2R0PjxkZD5FVEwvRUxULCBEYXRhIE1vZGVsaW5nLCBEaW1lbnNpb25hbCBNb2RlbGluZywgQXBhY2hlIFNwYXJrIChQeVNwYXJrLCBTcGFyayBTUUwsIFN0cnVjdHVyZWQgU3RyZWFtaW5nKSwgQXBhY2hlIEthZmthIChLYWZrYSBDb25uZWN0LCBTY2hlbWEgUmVnaXN0cnkpLCBBcGFjaGUgQWlyZmxvdywgZGJ0LCBDaGFuZ2UgRGF0YSBDYXB0dXJlIChDREMpPC9kZD48L2Rpdj4KICAgICAgPGRpdiBjbGFzcz0ic2tpbGwtcm93Ij48ZHQ+Q2xvdWQgJmFtcDsgUGxhdGZvcm1zPC9kdD48ZGQ+QVdTIChTMywgRU1SLCBHbHVlLCBMYW1iZGEpLCBEYXRhYnJpY2tzIChEZWx0YSBMYWtlLCBVbml0eSBDYXRhbG9nLCBEZWx0YSBMaXZlIFRhYmxlcywgV29ya2Zsb3dzKSwgU25vd2ZsYWtlIChTbm93cGFyayksIEFtYXpvbiBSZWRzaGlmdCwgTWljcm9zb2Z0IEZhYnJpYywgQXBhY2hlIEljZWJlcmcsIFBhcnF1ZXQsIEF2cm88L2RkPjwvZGl2PgogICAgICA8ZGl2IGNsYXNzPSJza2lsbC1yb3ciPjxkdD5BSS9NTCAmYW1wOyBJbnRlbGxpZ2VudCBEYXRhPC9kdD48ZGQ+TWFjaGluZSBMZWFybmluZyBQaXBlbGluZXMsIEZlYXR1cmUgRW5naW5lZXJpbmcsIE1MLVJlYWR5IERhdGEgUGlwZWxpbmVzLCBNTGZsb3csIE1vZGVsIFRyYWluaW5nLCBJbmZlcmVuY2UgJmFtcDsgTW9kZWwgU2VydmluZyBQaXBlbGluZXMsIEdlbmVyYXRpdmUgQUkgRGF0YSBXb3JrZmxvd3MsIExMTSBEYXRhIFByb2Nlc3NpbmcsIExMTS9BUEkgSW50ZWdyYXRpb24sIEVtYmVkZGluZ3MsIFZlY3RvciBEYXRhYmFzZXMgKFBpbmVjb25lLCBwZ3ZlY3RvciksIFZlY3RvciBTZWFyY2gsIFJBRyBQaXBlbGluZXM8L2RkPjwvZGl2PgogICAgICA8ZGl2IGNsYXNzPSJza2lsbC1yb3ciPjxkdD5EZXZPcHMgJmFtcDsgUGxhdGZvcm08L2R0PjxkZD5HaXQsIENJL0NEIChHaXRIdWIgQWN0aW9ucywgSmVua2lucyksIERvY2tlciAoQ29tcG9zZSwgTXVsdGktc3RhZ2UgQnVpbGRzKSwgS3ViZXJuZXRlcyAoUG9kcywgRGVwbG95bWVudHMpLCBUZXJyYWZvcm0gKElhQyksIExpbnV4LCBSRVNUIEFQSXM8L2RkPjwvZGl2PgogICAgICA8ZGl2IGNsYXNzPSJza2lsbC1yb3ciPjxkdD5EYXRhIFF1YWxpdHkgJmFtcDsgQW5hbHl0aWNzPC9kdD48ZGQ+RGF0YSBRdWFsaXR5LCBEYXRhIEdvdmVybmFuY2UsIERhdGEgTGluZWFnZSwgRGF0YSBPYnNlcnZhYmlsaXR5IChHcmVhdCBFeHBlY3RhdGlvbnMpLCBRdWVyeSBPcHRpbWl6YXRpb24sIFBlcmZvcm1hbmNlIFR1bmluZywgUGFydGl0aW9uaW5nLCBNb25pdG9yaW5nLCBQb3N0Z3JlU1FMLCBNeVNRTCwgTW9uZ29EQiwgVGFibGVhdSwgUG93ZXIgQkk8L2RkPjwvZGl2PgogICAgPC9kbD4KICA8L3NlY3Rpb24+CgogIDxzZWN0aW9uPgogICAgPGgyPlByb2Zlc3Npb25hbCBFeHBlcmllbmNlPC9oMj4KCiAgICA8ZGl2IGNsYXNzPSJqb2IiPgogICAgICA8ZGl2IGNsYXNzPSJqb2ItaGVhZCI+CiAgICAgICAgPHNwYW4gY2xhc3M9ImpvYi10aXRsZSI+U2VuaW9yIEFJL01MIERhdGEgRW5naW5lZXIsIDxzcGFuIGNsYXNzPSJjb21wYW55Ij5QaW5lY29uZTwvc3Bhbj48L3NwYW4+CiAgICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPkp1biAyMDI1IOKAkyBQcmVzZW50IMK3IFJlbW90ZSwgVVNBPC9zcGFuPgogICAgICA8L2Rpdj4KICAgICAgPHVsPgogICAgICAgIDxsaT5BcmNoaXRlY3RlZCBtYWNoaW5lIGxlYXJuaW5nIHBpcGVsaW5lcyBmb3IgcmVjb21tZW5kYXRpb24gc2VydmljZXMsIGNvbWJpbmluZyBmZWF0dXJlIGVuZ2luZWVyaW5nIHdpdGggTUxmbG93IHRyYWNraW5nIGFuZCBNTC1yZWFkeSBkYXRhc2V0cyBhY3Jvc3MgMzUgZmVhdHVyZSBncm91cHMgZm9yIHByb2R1Y3Rpb24gbW9kZWwgcHJlcGFyYXRpb24gd29ya2Zsb3dzLjwvbGk+CiAgICAgICAgPGxpPk9wZXJhdGlvbmFsaXplZCBtb2RlbCB0cmFpbmluZywgaW5mZXJlbmNlLCBhbmQgbW9kZWwgc2VydmluZyBwaXBlbGluZXMgZm9yIGludGVsbGlnZW50IHNlYXJjaCwgaW1wcm92aW5nIGRlcGxveW1lbnQgcmVhZGluZXNzIHRocm91Z2ggc3RhbmRhcmRpemVkIHZhbGlkYXRpb24sIGZlYXR1cmUgYXZhaWxhYmlsaXR5LCBhbmQgcmVwZWF0YWJsZSBzZXJ2aW5nIHdvcmtmbG93cy48L2xpPgogICAgICAgIDxsaT5MYXVuY2hlZCBnZW5lcmF0aXZlIEFJIGRhdGEgd29ya2Zsb3dzIGZvciBzdXBwb3J0LWRvY3VtZW50IGludGVsbGlnZW5jZSwgdHJhbnNmb3JtaW5nIExMTSBkYXRhIHByb2Nlc3NpbmcgaW50byBpbmZlcmVuY2UgcGlwZWxpbmVzIHRoYXQgaGFuZGxlZCAxLjYgbWlsbGlvbiBkb2N1bWVudHMgbW9udGhseSB3aXRoIHN5c3RlbWF0aXplZCBlbnJpY2htZW50IGNvbnRyb2xzLjwvbGk+CiAgICAgICAgPGxpPkNvbm5lY3RlZCBQaW5lY29uZSBhbmQgcGd2ZWN0b3IgdmVjdG9yIGRhdGFiYXNlcywgZ2VuZXJhdGluZyBlbWJlZGRpbmdzIGFuZCBpbXBsZW1lbnRpbmcgdmVjdG9yIHNlYXJjaCB0aGF0IGltcHJvdmVkIHJlbGV2YW50LWNvbnRleHQgcmV0cmlldmFsIGJ5IDQzJSBhY3Jvc3MgaW5kZXhlZCBlbnRlcnByaXNlIGtub3dsZWRnZSBjb2xsZWN0aW9ucy48L2xpPgogICAgICAgIDxsaT5Fc3RhYmxpc2hlZCBSQUcgcGlwZWxpbmVzIHdpdGggTExNL0FQSSBpbnRlZ3JhdGlvbiwgZXhwb3NpbmcgUkVTVCBBUElzIHRoYXQgY29ubmVjdGVkIGVudGVycHJpc2UgcmV0cmlldmFsIHdpdGggcHJvZHVjdGlvbiBBSSBhc3Npc3RhbnRzIHdoaWxlIHN1cHBvcnRpbmcgc2VjdXJlIG1vZGVsLXNlcnZpbmcgd29ya2Zsb3dzLjwvbGk+CiAgICAgICAgPGxpPkNvbnRhaW5lcml6ZWQgQUkgYXBwbGljYXRpb25zIHVzaW5nIERvY2tlciAoQ29tcG9zZSwgbXVsdGktc3RhZ2UgYnVpbGRzKSwgaW50ZWdyYXRpbmcgR2l0IGFuZCBHaXRIdWIgQWN0aW9ucyB3aGlsZSBzdHJlbmd0aGVuaW5nIGRhdGEgb2JzZXJ2YWJpbGl0eSBhbmQgcHJvZHVjdGlvbiBtb25pdG9yaW5nIGNhcGFiaWxpdGllcy48L2xpPgogICAgICA8L3VsPgogICAgPC9kaXY+CgogICAgPGRpdiBjbGFzcz0iam9iIj4KICAgICAgPGRpdiBjbGFzcz0iam9iLWhlYWQiPgogICAgICAgIDxzcGFuIGNsYXNzPSJqb2ItdGl0bGUiPlNlbmlvciBEYXRhIEVuZ2luZWVyLCA8c3BhbiBjbGFzcz0iY29tcGFueSI+R0UgSGVhbHRoQ2FyZTwvc3Bhbj48L3NwYW4+CiAgICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPkF1ZyAyMDIyIOKAkyBOb3YgMjAyMyDCtyBSZW1vdGUsIEluZGlhPC9zcGFuPgogICAgICA8L2Rpdj4KICAgICAgPHVsPgogICAgICAgIDxsaT5MZWQgRGF0YWJyaWNrcyBtb2Rlcm5pemF0aW9uIGZvciBwYXRpZW50LXV0aWxpemF0aW9uIGFuYWx5dGljcywgYXBwbHlpbmcgRGVsdGEgTGFrZSBhbmQgTWVkYWxsaW9uIEFyY2hpdGVjdHVyZSB0byBvcmdhbml6ZSBoZWFsdGhjYXJlIHJlY29yZHMgYWNyb3NzIGdvdmVybmVkIEJyb256ZSwgU2lsdmVyLCBhbmQgR29sZCBsYXllcnMuPC9saT4KICAgICAgICA8bGk+RGVwbG95ZWQgVW5pdHkgQ2F0YWxvZyB3aXRoIERlbHRhIExpdmUgVGFibGVzLCBzdHJlbmd0aGVuaW5nIGRhdGEgZ292ZXJuYW5jZSB3aGlsZSBpbmNyZWFzaW5nIHRydXN0ZWQgZGF0YXNldCBjb3ZlcmFnZSBmcm9tIDgyJSB0byA5NyUgdGhyb3VnaCBhdXRvbWF0ZWQgY29udHJvbHMgYW5kIHN0YW5kYXJkaXplZCBhY2Nlc3MuPC9saT4KICAgICAgICA8bGk+RGVzaWduZWQgU25vd2ZsYWtlIHdhcmVob3VzZSBzdHJ1Y3R1cmVzIHdpdGggU25vd3BhcmsgdHJhbnNmb3JtYXRpb25zLCBpbXByb3ZpbmcgY29ob3J0LXF1ZXJ5IHJlc3BvbnNlIHRpbWVzIGJ5IDM4JSB3aGlsZSBzdXBwb3J0aW5nIHNjYWxhYmxlIGhlYWx0aGNhcmUgcmVwb3J0aW5nIGFjcm9zcyBtdWx0aXBsZSBjbGluaWNhbCBwcm9ncmFtcy48L2xpPgogICAgICAgIDxsaT5BdXRvbWF0ZWQgRGF0YWJyaWNrcyBXb3JrZmxvd3Mgd2l0aCBKZW5raW5zIHJlbGVhc2VzLCByZWR1Y2luZyBkZXBsb3ltZW50IGVycm9ycyB0aHJvdWdoIHN0YW5kYXJkaXplZCB2YWxpZGF0aW9uLCBwcm9tb3Rpb24sIGFuZCByb2xsYmFjayBwcm9jZWR1cmVzIGFjcm9zcyBoZWFsdGhjYXJlIGFuYWx5dGljcyBzZXJ2aWNlcy48L2xpPgogICAgICAgIDxsaT5Qcm92aXNpb25lZCBUZXJyYWZvcm0gaW5mcmFzdHJ1Y3R1cmUgd2l0aCBLdWJlcm5ldGVzIFBvZHMgYW5kIERlcGxveW1lbnRzLCBpbXByb3ZpbmcgcmVzb3VyY2Ugc2NhbGFiaWxpdHkgd2hpbGUgc3RyZW5ndGhlbmluZyBMaW51eC1iYXNlZCByZWNvdmVyeSBwcm9jZWR1cmVzIGZvciByZXBlYXRhYmxlIHBsYXRmb3JtIG9wZXJhdGlvbnMuPC9saT4KICAgICAgICA8bGk+SW50ZWdyYXRlZCBBcGFjaGUgSWNlYmVyZyB3aXRoIFBhcnF1ZXQgYW5kIEF2cm8gZGF0YXNldHMsIGVzdGFibGlzaGluZyBHcmVhdCBFeHBlY3RhdGlvbnMgdmFsaWRhdGlvbiBhbmQgZGF0YSBsaW5lYWdlIG1vbml0b3Jpbmcgd2hpbGUgcmVkdWNpbmcgc2NoZW1hLXJlbGF0ZWQgaW5jaWRlbnRzIGJ5IDI5JSBhY3Jvc3Mgc2hhcmVkIGNsaW5pY2FsIGRhdGFzZXRzLjwvbGk+CiAgICAgIDwvdWw+CiAgICA8L2Rpdj4KCiAgICA8ZGl2IGNsYXNzPSJqb2IiPgogICAgICA8ZGl2IGNsYXNzPSJqb2ItaGVhZCI+CiAgICAgICAgPHNwYW4gY2xhc3M9ImpvYi10aXRsZSI+RGF0YSBFbmdpbmVlciwgPHNwYW4gY2xhc3M9ImNvbXBhbnkiPklCTTwvc3Bhbj48L3NwYW4+CiAgICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPlNlcHQgMjAxOSDigJMgSnVsIDIwMjIgwrcgUmVtb3RlLCBJbmRpYTwvc3Bhbj4KICAgICAgPC9kaXY+CiAgICAgIDx1bD4KICAgICAgICA8bGk+RW5naW5lZXJlZCBQeXRob24gRVRMIHBpcGVsaW5lcyBmb3IgYmFua2luZyB0cmFuc2FjdGlvbiByZWNvbmNpbGlhdGlvbiwgcHJvY2Vzc2luZyAxMiBtaWxsaW9uIG1vbnRobHkgcmVjb3JkcyBhbmQgaW1wcm92aW5nIHNldHRsZW1lbnQgdmFsaWRhdGlvbiBieSAyOCUgdGhyb3VnaCBzdGFuZGFyZGl6ZWQgdHJhbnNmb3JtYXRpb24gYW5kIGV4Y2VwdGlvbiBoYW5kbGluZy48L2xpPgogICAgICAgIDxsaT5EZXZlbG9wZWQgU1FMIGRhdGEgbW9kZWxzIGZvciBjcmVkaXQtcmlzayByZXBvcnRpbmcsIGFwcGx5aW5nIHdpbmRvdyBmdW5jdGlvbnMgYW5kIGRpbWVuc2lvbmFsIG1vZGVsaW5nIHRvIGNvbnNvbGlkYXRlIGN1c3RvbWVyIGV4cG9zdXJlcyB3aGlsZSByZWR1Y2luZyByZWN1cnJpbmcgcmVwb3J0IHByZXBhcmF0aW9uIHRpbWUgYnkgMzUlLjwvbGk+CiAgICAgICAgPGxpPkJ1aWx0IEphdmEgaW5nZXN0aW9uIHNlcnZpY2VzIGZvciBwYXltZW50IGV2ZW50cywgaW50ZWdyYXRpbmcgSlNPTiBwYXlsb2FkcyB3aXRoIFBvc3RncmVTUUwgc291cmNlcyBhbmQgYXV0b21hdGVkIHZhbGlkYXRpb24gdGhhdCBpbXByb3ZlZCBkb3duc3RyZWFtIGRhdGEgY29uc2lzdGVuY3kgYWNyb3NzIGRhaWx5IGZpbmFuY2lhbCByZXBvcnRpbmcuPC9saT4KICAgICAgICA8bGk+U3RyZWFtbGluZWQgQXBhY2hlIFNwYXJrIHByb2Nlc3Npbmcgd2l0aCBQeVNwYXJrIGFuZCBTcGFyayBTUUwgZm9yIHBvcnRmb2xpbyBhbmFseXRpY3MsIHJlZHVjaW5nIGJhdGNoIGV4ZWN1dGlvbiB0aW1lIGJ5IDI0JSB0aHJvdWdoIHBhcnRpdGlvbmluZywgY2FjaGluZywgYW5kIHRhcmdldGVkIHF1ZXJ5IG9wdGltaXphdGlvbi48L2xpPgogICAgICAgIDxsaT5Db25maWd1cmVkIEFwYWNoZSBLYWZrYSBwaXBlbGluZXMgZm9yIHRyYW5zYWN0aW9uLWV2ZW50IHN0cmVhbWluZywgZXN0YWJsaXNoaW5nIFNjaGVtYSBSZWdpc3RyeSBjb250cm9scyB0aGF0IGltcHJvdmVkIG1lc3NhZ2UgY29tcGF0aWJpbGl0eSBhbmQgc3VwcG9ydGVkIHJlbGlhYmxlIGRvd25zdHJlYW0gZnJhdWQtbW9uaXRvcmluZyB3b3JrZmxvd3MuPC9saT4KICAgICAgICA8bGk+T3JjaGVzdHJhdGVkIEFwYWNoZSBBaXJmbG93IHdvcmtmbG93cyBmb3IgcmVndWxhdG9yeS1kYXRhIHByZXBhcmF0aW9uLCBjb29yZGluYXRpbmcgdmFsaWRhdGlvbiBzdGVwcyBhbmQgc2NoZWR1bGVkIGRlcGVuZGVuY2llcyB3aGlsZSBpbXByb3ZpbmcgcGlwZWxpbmUgY29tcGxldGlvbiByZWxpYWJpbGl0eSB0byA5OS41JS48L2xpPgogICAgICAgIDxsaT5JbXBsZW1lbnRlZCBBV1MgUzMgaW5nZXN0aW9uIHdpdGggRU1SIGZvciBmaW5hbmNpYWwgZGF0YXNldHMsIGFwcGx5aW5nIEJhc2ggYXV0b21hdGlvbiBhbmQgQ0RDIHByb2Nlc3NpbmcgdG8gc2hvcnRlbiBzb3VyY2UtdG8tcmVwb3J0IGxhdGVuY3kgYnkgNDcgbWludXRlcyBhY3Jvc3MgZGFpbHkgb3BlcmF0aW9ucy48L2xpPgogICAgICA8L3VsPgogICAgPC9kaXY+CiAgPC9zZWN0aW9uPgoKICA8c2VjdGlvbj4KICAgIDxoMj5Qcm9qZWN0czwvaDI+CgogICAgPGRpdiBjbGFzcz0icHJvamVjdCI+CiAgICAgIDxkaXYgY2xhc3M9InByb2plY3QtdGl0bGUiPlJldGFpbCBEYXRhIEVuZ2luZWVyaW5nIFBsYXRmb3JtPC9kaXY+CiAgICAgIDxkaXYgY2xhc3M9InN0YWNrIj5QeXRob24gwrcgS2Fma2EgwrcgU3BhcmsgwrcgQWlyZmxvdyDCtyBNeVNRTCDCtyBUYWJsZWF1PC9kaXY+CiAgICAgIDx1bD4KICAgICAgICA8bGk+Q29uc3RydWN0ZWQgYSByZWFsLXRpbWUgcmV0YWlsIHBpcGVsaW5lIHVzaW5nIEthZmthIGFuZCBTcGFyayBTdHJ1Y3R1cmVkIFN0cmVhbWluZywgdHJhbnNmb3JtaW5nIHNhbGVzIGFuZCBpbnZlbnRvcnkgZXZlbnRzIHRocm91Z2ggQnJvbnplLCBTaWx2ZXIsIGFuZCBHb2xkIHByb2Nlc3NpbmcgbGF5ZXJzLjwvbGk+CiAgICAgICAgPGxpPkFycmFuZ2VkIHNjaGVkdWxlZCBBaXJmbG93IHdvcmtmbG93cyB0byBsb2FkIGN1cmF0ZWQgTXlTUUwgZGF0YXNldHMgYW5kIGRlbGl2ZXIgVGFibGVhdS1yZWFkeSByZXBvcnRpbmcgbW9kZWxzIHN1cHBvcnRpbmcgaW52ZW50b3J5IHZpc2liaWxpdHksIHNhbGVzIGFuYWx5c2lzLCBhbmQgcmVwbGVuaXNobWVudCBkZWNpc2lvbnMuPC9saT4KICAgICAgPC91bD4KICAgIDwvZGl2PgoKICAgIDxkaXYgY2xhc3M9InByb2plY3QiPgogICAgICA8ZGl2IGNsYXNzPSJwcm9qZWN0LXRpdGxlIj5TYWxlcyBQZXJmb3JtYW5jZSBBbmFseXRpY3M8L2Rpdj4KICAgICAgPGRpdiBjbGFzcz0ic3RhY2siPlB5dGhvbiDCtyBTUUwgwrcgVGFibGVhdSDCtyBHaXQ8L2Rpdj4KICAgICAgPHVsPgogICAgICAgIDxsaT5CdWlsdCBhIFB5dGhvbiBFVEwgcGlwZWxpbmUgYWNyb3NzIHRocmVlIENTViBkYXRhc2V0cywgaW5nZXN0aW5nIHNhbGVzLCBwcm9kdWN0LCBhbmQgY3VzdG9tZXIgZGF0YSBpbnRvIGNsZWFuZWQgcmVwb3J0aW5nIG91dHB1dHMgdGhyb3VnaCBtb2R1bGFyIGluZ2VzdGlvbiwgdHJhbnNmb3JtYXRpb24sIGFuZCBkYXRhLXF1YWxpdHkgc3RhZ2VzLjwvbGk+CiAgICAgICAgPGxpPkZlZCBTUUwgYW5hbHl0aWNzIGFuZCBpbnRlcmFjdGl2ZSBUYWJsZWF1IGRhc2hib2FyZHMgd2l0aCBmaWx0ZXJpbmcgYWNyb3NzIHByb2R1Y3QgbGluZXMsIHJlZ2lvbnMsIGFuZCB0aW1lIHBlcmlvZHMuPC9saT4KICAgICAgPC91bD4KICAgIDwvZGl2PgoKICAgIDxkaXYgY2xhc3M9InByb2plY3QiPgogICAgICA8ZGl2IGNsYXNzPSJwcm9qZWN0LXRpdGxlIj5NaWNyb3NvZnQgRmFicmljIFJldGFpbCBTYWxlcyBBbmFseXRpY3M8L2Rpdj4KICAgICAgPGRpdiBjbGFzcz0ic3RhY2siPk1pY3Jvc29mdCBGYWJyaWMgwrcgUHlTcGFyayDCtyBTUUwgwrcgUG93ZXIgQkk8L2Rpdj4KICAgICAgPHVsPgogICAgICAgIDxsaT5CdWlsdCBhIExha2Vob3VzZS1iYXNlZCByZXRhaWwgYW5hbHl0aWNzIHNvbHV0aW9uIGluIE1pY3Jvc29mdCBGYWJyaWMsIGFwcGx5aW5nIFB5U3BhcmsgdHJhbnNmb3JtYXRpb25zIHRvIGNsZWFuc2UsIHN0YW5kYXJkaXplLCBhbmQgb3JnYW5pemUgc2FsZXMgZGF0YSBhY3Jvc3MgQnJvbnplLCBTaWx2ZXIsIGFuZCBHb2xkIGxheWVycy48L2xpPgogICAgICAgIDxsaT5DcmVhdGVkIFNRTCBBbmFseXRpY3MgRW5kcG9pbnQgcXVlcmllcyBhbmQgUG93ZXIgQkkgZGFzaGJvYXJkcyBjb252ZXJ0aW5nIGN1cmF0ZWQgc2FsZXMgZGF0YXNldHMgaW50byBpbnRlcmFjdGl2ZSB2aWV3cyBvZiByZXZlbnVlIHRyZW5kcywgcHJvZHVjdCBwZXJmb3JtYW5jZSwgYW5kIHJlZ2lvbmFsIGFjdGl2aXR5LjwvbGk+CiAgICAgIDwvdWw+CiAgICA8L2Rpdj4KCiAgICA8ZGl2IGNsYXNzPSJtaW5vciI+CiAgICAgIDxwPjxzcGFuIGNsYXNzPSJwcm9qZWN0LXRpdGxlIj5FdmVudGlmeSDigJQgTWFzdGVyJ3MgQ2Fwc3RvbmUuPC9zcGFuPiBEZXNpZ25lZCB0aGUgcmVsYXRpb25hbCBkYXRhIG1vZGVsLCBSRVNUIEFQSXMsIGFuZCBhdXRoZW50aWNhdGlvbiBjb250cm9scyBmb3IgYW4gZXZlbnQtbWFuYWdlbWVudCBwbGF0Zm9ybSBjb3ZlcmluZyBldmVudCBjcmVhdGlvbiwgdGlja2V0IGludmVudG9yeSwgYXR0ZW5kZWUgcmVnaXN0cmF0aW9uLCBhbmQgdHJhbnNhY3Rpb24gcmVjb3Jkcy48L3A+CiAgICAgIDxwPjxzcGFuIGNsYXNzPSJwcm9qZWN0LXRpdGxlIj5Jb1QgVm9pY2UtQ29udHJvbGxlZCBTbWFydCBIb21lLjwvc3Bhbj4gUmFzcGJlcnJ5IFBpIGF1dG9tYXRpb24gdHJhbnNsYXRpbmcgR29vZ2xlIEhvbWUgdm9pY2UgY29tbWFuZHMgaW50byByZWFsLXRpbWUgYXBwbGlhbmNlIGNvbnRyb2wgdGhyb3VnaCBJRlRUVC10cmlnZ2VyZWQgd29ya2Zsb3dzLjwvcD4KICAgICAgPHA+PHNwYW4gY2xhc3M9InByb2plY3QtdGl0bGUiPlJlbnRhbCBQb3J0YWwuPC9zcGFuPiBTY2FsYWJsZSByZW50YWwgc2VhcmNoIGFwcGxpY2F0aW9uIGNvbm5lY3Rpbmcgb3duZXJzIGFuZCB0ZW5hbnRzLCB3aXRoIGJhY2tlbmQgc2VydmljZXMsIGludGVncmF0ZWQgZGF0YWJhc2VzLCBhbmQgZmlsdGVyZWQgc2VhcmNoLjwvcD4KICAgICAgPHA+PHNwYW4gY2xhc3M9InByb2plY3QtdGl0bGUiPkZydWl0IEJhc2tldCDigJQgSU5NQVIgVGVjaG5vbG9naWVzLjwvc3Bhbj4gT25saW5lIG1hcmtldHBsYWNlIHdpdGggc2VjdXJlIHBheW1lbnRzIGFuZCBhdXRvbWF0ZWQgb3JkZXIgbWFuYWdlbWVudCwgZGVkdWN0aW5nIHNvbGQgaW52ZW50b3J5IGFuZCBxdWV1aW5nIGZ1bGZpbGxtZW50IGluIHJlYWwgdGltZS48L3A+CiAgICA8L2Rpdj4KICA8L3NlY3Rpb24+CgogIDxzZWN0aW9uPgogICAgPGgyPkNlcnRpZmljYXRpb25zPC9oMj4KICAgIDx1bCBjbGFzcz0iY2VydHMiPgogICAgICA8bGk+QVdTIENlcnRpZmllZCBEYXRhIEVuZ2luZWVyIOKAlCBBc3NvY2lhdGUgKERFQS1DMDEpIDxzcGFuIGNsYXNzPSJpc3N1ZXIiPsK3IEFtYXpvbiBXZWIgU2VydmljZXM8L3NwYW4+IOKAlCA8YSBocmVmPSJodHRwczovL3d3dy5saW5rZWRpbi5jb20vaW4vYW5pdGhhLXJhai1iYWxlLWE4YmEzMTE3Yi9kZXRhaWxzL2NlcnRpZmljYXRpb25zLyI+VmVyaWZ5PC9hPjwvbGk+CiAgICAgIDxsaT5BV1MgQ2xvdWQgUHJhY3RpdGlvbmVyIEVzc2VudGlhbHMgPHNwYW4gY2xhc3M9Imlzc3VlciI+wrcgQW1hem9uIFdlYiBTZXJ2aWNlczwvc3Bhbj4g4oCUIDxhIGhyZWY9Imh0dHBzOi8vc2tpbGxidWlsZGVyLmF3cy9sZWFybi85NFQyQkVOODVBL2F3cy1jbG91ZC1wcmFjdGl0aW9uZXItZXNzZW50aWFscy84RDc5RjNBVlI3Ij5WZXJpZnk8L2E+PC9saT4KICAgICAgPGxpPkRhdGEgRW5naW5lZXJpbmcgUHJvZmVzc2lvbmFsIENlcnRpZmljYXRlIDxzcGFuIGNsYXNzPSJpc3N1ZXIiPsK3IFNub3dmbGFrZSDCtyBTZXAgMjAyNjwvc3Bhbj48L2xpPgogICAgICA8bGk+RGF0YSBFbmdpbmVlcmluZyBGb3VuZGF0aW9uIENlcnRpZmljYXRpb24gPHNwYW4gY2xhc3M9Imlzc3VlciI+wrcgSW5mb3JtYXRpY2EgwrcgQXVnIDIwMjY8L3NwYW4+PC9saT4KICAgICAgPGxpPkRhdGFicmlja3MgRnVuZGFtZW50YWxzIEFjY3JlZGl0YXRpb24gPHNwYW4gY2xhc3M9Imlzc3VlciI+wrcgRGF0YWJyaWNrczwvc3Bhbj48L2xpPgogICAgICA8bGk+RGF0YSBBbmFseXNpcyBVc2luZyBQeXRob24gPHNwYW4gY2xhc3M9Imlzc3VlciI+wrcgRGF0YSBBbmFseXRpY3MgSm9iIFNpbXVsYXRpb24gwrcgUiBFc3NlbnRpYWxzPC9zcGFuPjwvbGk+CiAgICA8L3VsPgogIDwvc2VjdGlvbj4KCiAgPHNlY3Rpb24+CiAgICA8aDI+RWR1Y2F0aW9uPC9oMj4KICAgIDxkaXYgY2xhc3M9ImVkdSI+CiAgICAgIDxzcGFuPjxzcGFuIGNsYXNzPSJkZWdyZWUiPk1hc3RlciBvZiBTY2llbmNlLCBDb21wdXRlciBTY2llbmNlPC9zcGFuPiDigJQgPHNwYW4gY2xhc3M9InNjaG9vbCI+UGFjZSBVbml2ZXJzaXR5PC9zcGFuPjwvc3Bhbj4KICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPkphbiAyMDI0IOKAkyBEZWMgMjAyNSDCtyBOWSwgVVNBPC9zcGFuPgogICAgPC9kaXY+CiAgICA8ZGl2IGNsYXNzPSJlZHUiPgogICAgICA8c3Bhbj48c3BhbiBjbGFzcz0iZGVncmVlIj5CYWNoZWxvciBvZiBUZWNobm9sb2d5LCBJbmZvcm1hdGlvbiBUZWNobm9sb2d5PC9zcGFuPiDigJQgPHNwYW4gY2xhc3M9InNjaG9vbCI+UFZQU0lUPC9zcGFuPjwvc3Bhbj4KICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPkp1biAyMDE1IOKAkyBNYXIgMjAxOSDCtyBBUCwgSW5kaWE8L3NwYW4+CiAgICA8L2Rpdj4KICA8L3NlY3Rpb24+Cgo8L2Rpdj4KPC9ib2R5Pgo8L2h0bWw+Cg==" download="Anitha_Raj_Bale_Resume.html" class="btn btn-ghost magnetic"><i class="fa-solid fa-download"></i> Download resume</a>
    </div>
  </div>
  <div class="scroll-cue"><span>Scroll</span><span class="stick"></span></div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="wrap">
    <div class="reveal">
      <div class="eyebrow">About</div>
      <h2 class="section-title">From core data engineering<br class="br-desktop"> to <span class="gradient-text">intelligent data infrastructure</span>.</h2>
    </div>

    <div class="about-grid reveal-stagger">
      <div class="bento-cell bio-cell tilt">
        <span class="quote-mark">&ldquo;</span>
        <p>I'm a Senior Data Engineer with 5+ years building scalable data platforms and production pipelines across financial, healthcare, and AI-driven environments.</p>
        <p>My work combines streaming ingestion and warehouse modeling — Kafka, Spark, Airflow, dbt, Snowflake, Redshift, Databricks, and AWS — with ML-ready pipelines, feature engineering, MLflow, GenAI and LLM data processing, RAG, and vector-based retrieval, backed by a consistent focus on schema governance, data quality, lineage, and performance tuning.</p>
      </div>
      <div class="bento-cell stat-cell tilt">
        <div class="num" data-count="5" data-suffix="+">0</div>
        <div class="label">Years of experience</div>
      </div>
      <div class="bento-cell stat-cell tilt">
        <div class="num" data-count="1.6" data-suffix="M">0</div>
        <div class="label">Documents processed monthly through LLM pipelines</div>
      </div>
      <div class="bento-cell stat-cell tilt">
        <div class="num" data-count="43" data-suffix="%">0</div>
        <div class="label">Better context retrieval via vector search</div>
      </div>
      <div class="bento-cell stat-cell tilt">
        <div class="num" data-count="97" data-suffix="%">0</div>
        <div class="label">Trusted dataset coverage at GE HealthCare</div>
      </div>
    </div>
  </div>
</section>

<!-- ARCHITECTURE -->
<section id="architecture">
  <div class="wrap">
    <div class="reveal">
      <div class="eyebrow">Architecture</div>
      <h2 class="section-title">How data moves from<br class="br-desktop"> raw events to AI answers.</h2>
      <p class="section-sub">A composite of the patterns I've shipped at Pinecone, GE HealthCare, and IBM — streaming and batch ingestion converging through governed transformation, then branching into analytics and ML/RAG retrieval.</p>
    </div>

    <div class="arch-frame reveal">
      <div class="arch-caption">
        <span class="tag-pill">End-to-end platform</span>
        <div class="legend">
          <span><i class="streaming-dot"></i> Ingestion &amp; processing</span>
          <span><i class="batch-dot"></i> AI / ML path</span>
          <span><i class="quality-dot"></i> Governance &amp; quality</span>
        </div>
      </div>

      <svg class="arch-svg" viewBox="0 0 1180 470" xmlns="http://www.w3.org/2000/svg">
        <path class="arch-flow-line" d="M180,110 H300" />
        <path class="arch-flow-line" d="M470,110 H560 Q590,110 590,145 V195" />
        <path class="arch-flow-line" d="M180,355 H300" />
        <path class="arch-flow-line" d="M470,355 H560 Q590,355 590,320 V245" />
        <path class="arch-flow-line" d="M740,220 H830" />
        <path class="arch-flow-line" d="M1000,195 V145 Q1000,115 970,115 H890" />
        <path class="arch-flow-line batch" d="M1000,245 V300 Q1000,330 970,330 H890" />
        <path class="arch-flow-line batch" d="M810,370 H720 Q690,370 690,335 V245" />
        <path class="arch-flow-line quality" d="M590,245 V300 Q590,330 560,330 H470" />

        <!-- Streaming sources -->
        <g class="arch-node">
          <rect x="20" y="70" width="160" height="80" rx="14"/>
          <text class="n-icon" x="40" y="100" font-size="16">&#9670;</text>
          <text class="n-title" x="40" y="122">Streaming Sources</text>
          <text class="n-sub" x="40" y="140">Transaction &amp; clinical events</text>
        </g>
        <!-- Batch sources -->
        <g class="arch-node">
          <rect x="20" y="315" width="160" height="80" rx="14"/>
          <text class="n-icon" x="40" y="345" font-size="16">&#9670;</text>
          <text class="n-title" x="40" y="367">Batch &amp; CDC Sources</text>
          <text class="n-sub" x="40" y="385">S3 · PostgreSQL · APIs</text>
        </g>

        <!-- Kafka -->
        <g class="arch-node">
          <rect x="300" y="70" width="170" height="80" rx="14"/>
          <text class="n-icon" x="320" y="100" font-size="16">&#8694;</text>
          <text class="n-title" x="320" y="122">Kafka</text>
          <text class="n-sub" x="320" y="140">Schema Registry · Connect</text>
        </g>
        <!-- Spark -->
        <g class="arch-node">
          <rect x="300" y="315" width="170" height="80" rx="14"/>
          <text class="n-icon" x="320" y="345" font-size="16">&#9650;</text>
          <text class="n-title" x="320" y="367">Spark</text>
          <text class="n-sub" x="320" y="385">PySpark · Structured Streaming</text>
        </g>

        <!-- Orchestration -->
        <g class="arch-node">
          <rect x="570" y="195" width="170" height="80" rx="14"/>
          <text class="n-icon" x="590" y="225" font-size="16">&#10039;</text>
          <text class="n-title" x="590" y="247">Airflow &amp; dbt</text>
          <text class="n-sub" x="590" y="265">Orchestration · modeling</text>
        </g>

        <!-- Lakehouse / warehouse -->
        <g class="arch-node">
          <rect x="830" y="180" width="170" height="80" rx="14"/>
          <text class="n-icon" x="850" y="210" font-size="16">&#9921;</text>
          <text class="n-title" x="850" y="232">Lakehouse</text>
          <text class="n-sub" x="850" y="250">Databricks · Snowflake</text>
        </g>

        <!-- Analytics -->
        <g class="arch-node">
          <rect x="1000" y="55" width="160" height="80" rx="14"/>
          <text class="n-icon" x="1020" y="85" font-size="16">&#9632;</text>
          <text class="n-title" x="1020" y="107">Analytics</text>
          <text class="n-sub" x="1020" y="125">Tableau · Power BI</text>
        </g>

        <!-- ML pipelines -->
        <g class="arch-node">
          <rect x="1000" y="290" width="160" height="80" rx="14"/>
          <text class="n-icon" x="1020" y="320" font-size="16">&#10022;</text>
          <text class="n-title" x="1020" y="342">ML Pipelines</text>
          <text class="n-sub" x="1020" y="360">Features · MLflow · serving</text>
        </g>

        <!-- Vector / RAG -->
        <g class="arch-node">
          <rect x="640" y="330" width="170" height="80" rx="14"/>
          <text class="n-icon" x="660" y="360" font-size="16">&#10098;&#10099;</text>
          <text class="n-title" x="660" y="382">Vector &amp; RAG</text>
          <text class="n-sub" x="660" y="400">Pinecone · pgvector · LLM APIs</text>
        </g>

        <circle class="arch-pulse" r="3.5">
          <animateMotion dur="3.4s" repeatCount="indefinite" path="M180,110 H470 Q590,110 590,145 V195 H740 H830 V195 H1000 V145 Q1000,115 970,115 H890" />
        </circle>
        <circle class="arch-pulse" r="3.5">
          <animateMotion dur="3.8s" begin="0.7s" repeatCount="indefinite" path="M180,355 H470 Q590,355 590,320 V245 H740 H830 V245 H1000 V300 Q1000,330 970,330 H890" />
        </circle>
      </svg>

      <div class="competency-strip">
        <div class="competency-chip"><i class="fa-solid fa-water"></i><div class="c-title">Streaming Ingestion</div><div class="c-sub">Kafka, Schema Registry, CDC</div></div>
        <div class="competency-chip"><i class="fa-solid fa-bolt"></i><div class="c-title">Distributed Processing</div><div class="c-sub">Spark, PySpark, Spark SQL</div></div>
        <div class="competency-chip"><i class="fa-solid fa-diagram-project"></i><div class="c-title">Orchestration</div><div class="c-sub">Airflow, dbt, Workflows</div></div>
        <div class="competency-chip"><i class="fa-solid fa-database"></i><div class="c-title">Lakehouse &amp; Warehouse</div><div class="c-sub">Databricks, Snowflake, Redshift</div></div>
        <div class="competency-chip"><i class="fa-solid fa-brain"></i><div class="c-title">ML &amp; GenAI Pipelines</div><div class="c-sub">MLflow, embeddings, RAG</div></div>
        <div class="competency-chip"><i class="fa-solid fa-shield-halved"></i><div class="c-title">Governance &amp; Quality</div><div class="c-sub">Unity Catalog, lineage, GE</div></div>
      </div>
    </div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-strip">
  <div class="marquee-track" id="marqueeTrack"></div>
</div>

<!-- SKILLS -->
<section id="skills">
  <div class="wrap">
    <div class="reveal">
      <div class="eyebrow">Skills</div>
      <h2 class="section-title">The stack behind<br class="br-desktop"> the platforms.</h2>
      <p class="section-sub">Tools I reach for across ingestion, transformation, storage, ML enablement, and governance.</p>
    </div>

    <div class="skills-grid reveal-stagger">
      <div class="bento-cell skill-cell tilt">
        <h4>Data Engineering</h4>
        <div class="tag-row">
          <span class="tag">ETL / ELT</span><span class="tag">Data Modeling</span><span class="tag">Dimensional Modeling</span><span class="tag">Apache Spark</span><span class="tag">PySpark</span><span class="tag">Spark SQL</span><span class="tag">Structured Streaming</span><span class="tag">Apache Kafka</span><span class="tag">Kafka Connect</span><span class="tag">Schema Registry</span><span class="tag">Apache Airflow</span><span class="tag">dbt</span><span class="tag">Change Data Capture</span>
        </div>
      </div>
      <div class="bento-cell skill-cell tilt">
        <h4>AI/ML &amp; Intelligent Data</h4>
        <div class="tag-row">
          <span class="tag">ML Pipelines</span><span class="tag">Feature Engineering</span><span class="tag">ML-Ready Pipelines</span><span class="tag">MLflow</span><span class="tag">Model Training</span><span class="tag">Inference &amp; Serving</span><span class="tag">GenAI Data Workflows</span><span class="tag">LLM Data Processing</span><span class="tag">LLM / API Integration</span><span class="tag">Embeddings</span><span class="tag">Pinecone</span><span class="tag">pgvector</span><span class="tag">Vector Search</span><span class="tag">RAG Pipelines</span>
        </div>
      </div>
      <div class="bento-cell skill-cell tilt">
        <h4>Cloud &amp; Platforms</h4>
        <div class="tag-row">
          <span class="tag">AWS S3</span><span class="tag">AWS EMR</span><span class="tag">AWS Glue</span><span class="tag">AWS Lambda</span><span class="tag">Databricks</span><span class="tag">Delta Lake</span><span class="tag">Unity Catalog</span><span class="tag">Delta Live Tables</span><span class="tag">Snowflake</span><span class="tag">Snowpark</span><span class="tag">Amazon Redshift</span><span class="tag">Microsoft Fabric</span><span class="tag">Apache Iceberg</span><span class="tag">Parquet</span><span class="tag">Avro</span>
        </div>
      </div>
      <div class="bento-cell skill-cell tilt">
        <h4>Data Quality &amp; Analytics</h4>
        <div class="tag-row">
          <span class="tag">Data Quality</span><span class="tag">Data Governance</span><span class="tag">Data Lineage</span><span class="tag">Great Expectations</span><span class="tag">Data Observability</span><span class="tag">Query Optimization</span><span class="tag">Performance Tuning</span><span class="tag">Partitioning</span><span class="tag">PostgreSQL</span><span class="tag">MySQL</span><span class="tag">MongoDB</span><span class="tag">Tableau</span><span class="tag">Power BI</span>
        </div>
      </div>
      <div class="bento-cell skill-cell tilt">
        <h4>Programming &amp; Querying</h4>
        <div class="tag-row">
          <span class="tag">Python</span><span class="tag">SQL</span><span class="tag">Window Functions</span><span class="tag">Java</span><span class="tag">Scala</span><span class="tag">Bash</span><span class="tag">JSON</span>
        </div>
      </div>
      <div class="bento-cell skill-cell tilt">
        <h4>DevOps &amp; Platform</h4>
        <div class="tag-row">
          <span class="tag">Git</span><span class="tag">GitHub Actions</span><span class="tag">Jenkins</span><span class="tag">CI/CD</span><span class="tag">Docker</span><span class="tag">Kubernetes</span><span class="tag">Terraform</span><span class="tag">Linux</span><span class="tag">REST APIs</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CERTIFICATIONS -->
<section id="certifications">
  <div class="wrap">
    <div class="reveal">
      <div class="eyebrow">Certifications</div>
      <h2 class="section-title">Credentials behind<br class="br-desktop"> the <span class="gradient-text">cloud &amp; data</span> work.</h2>
      <p class="section-sub">Cloud and platform certifications first, verified where a credential link is available.</p>
    </div>

    <div class="cert-stats reveal-stagger">
      <div class="cert-stat"><div class="num" data-count="8">0</div><div class="label">Total Certifications</div></div>
      <div class="cert-stat"><div class="num" data-count="5">0</div><div class="label">Cloud &amp; Platform</div></div>
      <div class="cert-stat"><div class="num" data-count="3">0</div><div class="label">Data Engineering</div></div>
    </div>

    <div class="cert-group-label">Cloud &amp; Platform Certifications</div>
    <div class="cert-grid reveal-stagger">
      <div class="cert-card tilt">
        <div class="cert-card-top">
          <div class="cert-icon aws"><i class="fa-brands fa-aws"></i></div>
          <span class="featured-badge"><i class="fa-solid fa-star"></i>Featured</span>
        </div>
        <h3>AWS Certified Data Engineer — Associate (DEA-C01)</h3>
        <div class="cert-org">Amazon Web Services</div>
        <div class="cert-meta-row"><span><i class="fa-solid fa-layer-group"></i>Cloud · Data Engineering</span></div>
        <a class="cert-verify" href="https://www.linkedin.com/in/anitha-raj-bale-a8ba3117b/details/certifications/" target="_blank" rel="noopener">Verify credential <i class="fa-solid fa-arrow-up-right-from-square"></i></a>
      </div>

      <div class="cert-card tilt">
        <div class="cert-card-top">
          <div class="cert-icon"><i class="fa-solid fa-snowflake"></i></div>
          <span class="featured-badge"><i class="fa-solid fa-star"></i>Featured</span>
        </div>
        <h3>Data Engineering Professional Certificate</h3>
        <div class="cert-org">Snowflake</div>
        <div class="cert-meta-row"><span><i class="fa-solid fa-calendar"></i>Sep 2026</span><span><i class="fa-solid fa-layer-group"></i>Data Engineering</span></div>
      </div>

      <div class="cert-card tilt">
        <div class="cert-card-top">
          <div class="cert-icon"><i class="fa-solid fa-diagram-project"></i></div>
          <span class="featured-badge"><i class="fa-solid fa-star"></i>Featured</span>
        </div>
        <h3>Data Engineering Foundation Certification</h3>
        <div class="cert-org">Informatica</div>
        <div class="cert-meta-row"><span><i class="fa-solid fa-calendar"></i>Aug 2026</span><span><i class="fa-solid fa-layer-group"></i>Data Engineering</span></div>
      </div>

      <div class="cert-card tilt">
        <div class="cert-card-top">
          <div class="cert-icon"><i class="fa-solid fa-fire"></i></div>
          <span class="featured-badge"><i class="fa-solid fa-star"></i>Featured</span>
        </div>
        <h3>Databricks Fundamentals Accreditation</h3>
        <div class="cert-org">Databricks</div>
        <div class="cert-meta-row"><span><i class="fa-solid fa-cloud"></i>Lakehouse Platform</span></div>
      </div>

      <div class="cert-card tilt">
        <div class="cert-card-top">
          <div class="cert-icon aws"><i class="fa-brands fa-aws"></i></div>
          <span class="featured-badge"><i class="fa-solid fa-star"></i>Featured</span>
        </div>
        <h3>AWS Cloud Practitioner Essentials</h3>
        <div class="cert-org">Amazon Web Services</div>
        <div class="cert-meta-row"><span><i class="fa-solid fa-cloud"></i>Cloud</span></div>
        <a class="cert-verify" href="https://skillbuilder.aws/learn/94T2BEN85A/aws-cloud-practitioner-essentials/8D79F3AVR7" target="_blank" rel="noopener">Verify credential <i class="fa-solid fa-arrow-up-right-from-square"></i></a>
      </div>
    </div>

    <div class="cert-group-label">Additional Certifications</div>
    <div class="cert-grid reveal-stagger">
      <div class="cert-card tilt">
        <div class="cert-card-top">
          <div class="cert-icon"><i class="fa-brands fa-python"></i></div>
          <span class="featured-badge"><i class="fa-solid fa-star"></i>Featured</span>
        </div>
        <h3>Data Analysis Using Python</h3>
        <div class="cert-meta-row"><span><i class="fa-solid fa-chart-line"></i>Data</span></div>
      </div>

      <div class="cert-card tilt">
        <div class="cert-card-top">
          <div class="cert-icon"><i class="fa-solid fa-briefcase"></i></div>
          <span class="featured-badge"><i class="fa-solid fa-star"></i>Featured</span>
        </div>
        <h3>Data Analytics Job Simulation</h3>
        <div class="cert-meta-row"><span><i class="fa-solid fa-chart-line"></i>Data</span></div>
      </div>

      <div class="cert-card tilt">
        <div class="cert-card-top">
          <div class="cert-icon"><i class="fa-brands fa-r-project"></i></div>
        </div>
        <h3>R Essentials</h3>
        <div class="cert-meta-row"><span><i class="fa-solid fa-code"></i>Programming</span></div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <div class="wrap">
    <div class="reveal">
      <div class="eyebrow">Projects</div>
      <h2 class="section-title">Data platforms,<br class="br-desktop"> built end to end.</h2>
      <p class="section-sub">Pipelines spanning streaming ingestion, orchestration, lakehouse modeling, and BI delivery.</p>
    </div>

    <div class="project-grid reveal-stagger">
      <div class="project-card tilt">
        <div class="project-index">01 <span class="de-badge">Streaming · ETL</span></div>
        <h3>Retail Data Engineering Platform</h3>
        <p>A real-time retail pipeline built with Kafka and Spark Structured Streaming, transforming sales and inventory events through Bronze, Silver, and Gold processing layers. Scheduled Airflow workflows load curated MySQL datasets and deliver Tableau-ready reporting models supporting inventory visibility, sales analysis, and replenishment decisions.</p>
        <div class="project-tags"><span>Python</span><span>Kafka</span><span>Spark</span><span>Airflow</span><span>MySQL</span><span>Tableau</span></div>
        <a class="project-github" href="https://github.com/Anitharaj31" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i> View on GitHub</a>
      </div>
      <div class="project-card tilt">
        <div class="project-index">02 <span class="de-badge">Lakehouse · BI</span></div>
        <h3>Microsoft Fabric Retail Sales Analytics</h3>
        <p>A Lakehouse-based retail analytics solution in Microsoft Fabric, applying PySpark transformations to cleanse, standardize, and organize sales data across Bronze, Silver, and Gold layers. SQL Analytics Endpoint queries and Power BI dashboards convert curated datasets into interactive views of revenue trends, product performance, and regional activity.</p>
        <div class="project-tags"><span>Microsoft Fabric</span><span>PySpark</span><span>SQL</span><span>Power BI</span></div>
        <a class="project-github" href="https://github.com/Anitharaj31" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i> View on GitHub</a>
      </div>
      <div class="project-card tilt" style="grid-column:1 / -1;">
        <div class="project-index">03 <span class="de-badge">ETL · Analytics</span></div>
        <h3>Sales Performance Analytics</h3>
        <p>A Python ETL pipeline across three CSV datasets, ingesting sales, product, and customer data into cleaned reporting outputs through modular ingestion, transformation, and data-quality stages. Feeds SQL analytics and interactive Tableau dashboards with filtering across product lines, regions, and time periods.</p>
        <div class="project-tags"><span>Python</span><span>SQL</span><span>Tableau</span><span>Git</span></div>
        <a class="project-github" href="https://github.com/Anitharaj31" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i> View on GitHub</a>
      </div>
    </div>

    <div class="other-projects reveal">
      <h4>Other Projects</h4>
      <div class="other-list">
        <div class="other-item">
          <h5>Eventify — Master's Capstone</h5>
          <p>Relational data model, REST APIs, and authentication controls for an event-management platform covering event creation, ticket inventory, attendee registration, and transaction records.</p>
          <a class="other-github" href="https://github.com/Anitharaj31" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i> GitHub</a>
        </div>
        <div class="other-item">
          <h5>IoT Voice-Controlled Smart Home</h5>
          <p>Raspberry Pi automation translating Google Home voice commands into real-time appliance control through IFTTT-triggered workflows.</p>
          <a class="other-github" href="https://github.com/Anitharaj31" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i> GitHub</a>
        </div>
        <div class="other-item">
          <h5>Rental Portal</h5>
          <p>Scalable rental search application connecting owners and tenants, with backend services, integrated databases, and filtered search.</p>
          <a class="other-github" href="https://github.com/Anitharaj31" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i> GitHub</a>
        </div>
        <div class="other-item">
          <h5>Fruit Basket — INMAR Technologies</h5>
          <p>Online marketplace with secure payments and automated order management, deducting sold inventory and queuing fulfillment in real time.</p>
          <a class="other-github" href="https://github.com/Anitharaj31" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i> GitHub</a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="wrap">
    <div class="reveal">
      <div class="eyebrow">Experience</div>
      <h2 class="section-title">Where I've<br class="br-desktop"> put it into practice.</h2>
    </div>

    <div class="timeline reveal">
      <div class="timeline-item">
        <div class="timeline-head">
          <h3>Senior AI/ML Data Engineer · <span>Pinecone</span></h3>
          <div class="timeline-meta">Jun 2025 — Present · Remote, USA</div>
        </div>
        <ul>
          <li>Architected machine learning pipelines for recommendation services, combining feature engineering with MLflow tracking and ML-ready datasets across 35 feature groups for production model preparation workflows.</li>
          <li>Launched generative AI data workflows for support-document intelligence, transforming LLM data processing into inference pipelines that handled 1.6 million documents monthly with systematized enrichment controls.</li>
          <li>Connected Pinecone and pgvector vector databases, generating embeddings and implementing vector search that improved relevant-context retrieval by 43% across indexed enterprise knowledge collections.</li>
        </ul>
      </div>
      <div class="timeline-item">
        <div class="timeline-head">
          <h3>Senior Data Engineer · <span>GE HealthCare</span></h3>
          <div class="timeline-meta">Aug 2022 — Nov 2023 · Remote, India</div>
        </div>
        <ul>
          <li>Led Databricks modernization for patient-utilization analytics, applying Delta Lake and Medallion Architecture to organize healthcare records across governed Bronze, Silver, and Gold layers.</li>
          <li>Deployed Unity Catalog with Delta Live Tables, strengthening data governance while increasing trusted dataset coverage from 82% to 97% through automated controls and standardized access.</li>
          <li>Designed Snowflake warehouse structures with Snowpark transformations, improving cohort-query response times by 38% while supporting scalable healthcare reporting across multiple clinical programs.</li>
        </ul>
      </div>
      <div class="timeline-item">
        <div class="timeline-head">
          <h3>Data Engineer · <span>IBM</span></h3>
          <div class="timeline-meta">Sept 2019 — Jul 2022 · Remote, India</div>
        </div>
        <ul>
          <li>Engineered Python ETL pipelines for banking transaction reconciliation, processing 12 million monthly records and improving settlement validation by 28% through standardized transformation and exception handling.</li>
          <li>Configured Apache Kafka pipelines for transaction-event streaming, establishing Schema Registry controls that improved message compatibility and supported reliable downstream fraud-monitoring workflows.</li>
          <li>Orchestrated Apache Airflow workflows for regulatory-data preparation, coordinating validation steps and scheduled dependencies while improving pipeline completion reliability to 99.5%.</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION -->
<section id="education">
  <div class="wrap">
    <div class="reveal">
      <div class="eyebrow">Education</div>
      <h2 class="section-title">Foundations.</h2>
    </div>

    <div class="edu-single reveal">
      <div class="edu-item">
        <div class="deg">Master of Science, Computer Science</div>
        <div class="school">Pace University</div>
        <div class="meta">Jan 2024 — Dec 2025 · NY, USA</div>
      </div>
      <div class="edu-item">
        <div class="deg">Bachelor of Technology, Information Technology</div>
        <div class="school">PVPSIT</div>
        <div class="meta">Jun 2015 — Mar 2019 · AP, India</div>
      </div>
    </div>
  </div>
</section>

<!-- CLOSER -->
<section class="closer" id="contact">
  <div class="closer-glow"></div>
  <div class="wrap reveal">
    <div class="eyebrow" style="justify-content:center;">Contact</div>
    <h2>Let's build data infrastructure<br> worth <span class="gradient-text">trusting</span>.</h2>
    <p>Open to senior data engineering and AI/ML platform roles, and conversations about streaming, lakehouse, and retrieval at scale.</p>
    <div class="hero-ctas">
      <a href="mailto:anitharajballe@gmail.com" class="btn btn-primary magnetic"><i class="fa-solid fa-paper-plane"></i> Say hello</a>
    </div>
    <div class="contact-links">
      <a href="mailto:anitharajballe@gmail.com"><i class="fa-solid fa-envelope"></i> anitharajballe@gmail.com</a>
      <a href="tel:+14759885865"><i class="fa-solid fa-phone"></i> +1 (475) 988-5865</a>
      <a href="https://www.linkedin.com/in/anitha-raj-bale-a8ba3117b/" target="_blank" rel="noopener"><i class="fa-brands fa-linkedin"></i> LinkedIn</a>
      <a href="https://github.com/Anitharaj31" target="_blank" rel="noopener"><i class="fa-brands fa-github"></i> GitHub</a>
      <a href="https://anitharajbale31.netlify.app/" target="_blank" rel="noopener"><i class="fa-solid fa-globe"></i> Portfolio</a>
      <a href="data:text/html;base64,PCFET0NUWVBFIGh0bWw+CjxodG1sIGxhbmc9ImVuIj4KPGhlYWQ+CjxtZXRhIGNoYXJzZXQ9InV0Zi04Ij4KPG1ldGEgbmFtZT0idmlld3BvcnQiIGNvbnRlbnQ9IndpZHRoPWRldmljZS13aWR0aCwgaW5pdGlhbC1zY2FsZT0xIj4KPHRpdGxlPkFuaXRoYSBSYWogQmFsZSDigJQgUmVzdW1lPC90aXRsZT4KPHN0eWxlPgogIDpyb290ewogICAgLS1pbms6IzFiMTczMDsKICAgIC0tYm9keTojM2EzNTUyOwogICAgLS1tdXRlZDojNmY2YTg2OwogICAgLS1hY2NlbnQ6IzViM2ZhNjsKICAgIC0tcnVsZTojZGRkOWU2OwogICAgLS1wYXBlcjojZmZmZmZmOwogICAgLS13YXNoOiNmNmY0ZmE7CiAgfQogICp7Ym94LXNpemluZzpib3JkZXItYm94O30KICBodG1sey13ZWJraXQtdGV4dC1zaXplLWFkanVzdDoxMDAlO30KICBib2R5ewogICAgbWFyZ2luOjA7CiAgICBiYWNrZ3JvdW5kOnZhcigtLXdhc2gpOwogICAgY29sb3I6dmFyKC0tYm9keSk7CiAgICBmb250LWZhbWlseToiSW50ZXIiLCJTZWdvZSBVSSIsSGVsdmV0aWNhLEFyaWFsLHNhbnMtc2VyaWY7CiAgICBmb250LXNpemU6MTAuNHB0OwogICAgbGluZS1oZWlnaHQ6MS41OwogIH0KICAuc2hlZXR7CiAgICBtYXgtd2lkdGg6OC41aW47CiAgICBtYXJnaW46MjhweCBhdXRvOwogICAgcGFkZGluZzowLjYyaW4gMC43aW4gMC43aW47CiAgICBiYWNrZ3JvdW5kOnZhcigtLXBhcGVyKTsKICAgIGJveC1zaGFkb3c6MCAycHggMThweCByZ2JhKDI3LDIzLDQ4LC4xMCk7CiAgfQoKICAvKiBIZWFkZXIgKi8KICBoZWFkZXJ7bWFyZ2luLWJvdHRvbToxOHB4O30KICBoMXsKICAgIGZvbnQtZmFtaWx5OiJJb3dhbiBPbGQgU3R5bGUiLCJQYWxhdGlubyBMaW5vdHlwZSIsUGFsYXRpbm8sR2VvcmdpYSxzZXJpZjsKICAgIGZvbnQtc2l6ZToyN3B0OwogICAgZm9udC13ZWlnaHQ6NjAwOwogICAgbGV0dGVyLXNwYWNpbmc6LS4wMWVtOwogICAgY29sb3I6dmFyKC0taW5rKTsKICAgIG1hcmdpbjowIDAgM3B4OwogIH0KICAucm9sZXsKICAgIGZvbnQtc2l6ZToxMXB0OwogICAgY29sb3I6dmFyKC0tYWNjZW50KTsKICAgIGZvbnQtd2VpZ2h0OjYwMDsKICAgIG1hcmdpbjowIDAgOXB4OwogIH0KICAuY29udGFjdHsKICAgIGZvbnQtc2l6ZTo5LjRwdDsKICAgIGNvbG9yOnZhcigtLW11dGVkKTsKICAgIGxpbmUtaGVpZ2h0OjEuNzsKICB9CiAgLmNvbnRhY3QgYXtjb2xvcjp2YXIoLS1ib2R5KTt0ZXh0LWRlY29yYXRpb246bm9uZTtib3JkZXItYm90dG9tOjFweCBzb2xpZCB2YXIoLS1ydWxlKTt9CiAgLmNvbnRhY3QgYTpob3ZlciwuY29udGFjdCBhOmZvY3Vze2NvbG9yOnZhcigtLWFjY2VudCk7Ym9yZGVyLWJvdHRvbS1jb2xvcjp2YXIoLS1hY2NlbnQpO30KICAuc2Vwe2NvbG9yOnZhcigtLXJ1bGUpO21hcmdpbjowIDdweDt9CgogIC8qIFNlY3Rpb25zICovCiAgc2VjdGlvbnttYXJnaW4tdG9wOjE5cHg7fQogIGgyewogICAgZm9udC1mYW1pbHk6Iklvd2FuIE9sZCBTdHlsZSIsIlBhbGF0aW5vIExpbm90eXBlIixQYWxhdGlubyxHZW9yZ2lhLHNlcmlmOwogICAgZm9udC1zaXplOjEyLjRwdDsKICAgIGZvbnQtd2VpZ2h0OjYwMDsKICAgIGNvbG9yOnZhcigtLWluayk7CiAgICBtYXJnaW46MCAwIDlweDsKICAgIHBhZGRpbmctYm90dG9tOjVweDsKICAgIGJvcmRlci1ib3R0b206MnB4IHNvbGlkIHZhcigtLWFjY2VudCk7CiAgfQogIHAuc3VtbWFyeXttYXJnaW46MDt9CgogIC8qIFNraWxscyAqLwogIC5za2lsbC1yb3d7CiAgICBkaXNwbGF5OmdyaWQ7CiAgICBncmlkLXRlbXBsYXRlLWNvbHVtbnM6MS40NWluIDFmcjsKICAgIGdhcDo0cHggMTRweDsKICAgIHBhZGRpbmc6NHB4IDA7CiAgICBib3JkZXItYm90dG9tOjFweCBzb2xpZCB2YXIoLS1ydWxlKTsKICB9CiAgLnNraWxsLXJvdzpsYXN0LWNoaWxke2JvcmRlci1ib3R0b206bm9uZTt9CiAgLnNraWxsLXJvdyBkdHtmb250LXdlaWdodDo2NTA7Y29sb3I6dmFyKC0taW5rKTt9CiAgLnNraWxsLXJvdyBkZHttYXJnaW46MDt9CiAgZGx7bWFyZ2luOjA7fQoKICAvKiBFeHBlcmllbmNlICovCiAgLmpvYnttYXJnaW4tYm90dG9tOjE0cHg7fQogIC5qb2I6bGFzdC1jaGlsZHttYXJnaW4tYm90dG9tOjA7fQogIC5qb2ItaGVhZHsKICAgIGRpc3BsYXk6ZmxleDsKICAgIGp1c3RpZnktY29udGVudDpzcGFjZS1iZXR3ZWVuOwogICAgYWxpZ24taXRlbXM6YmFzZWxpbmU7CiAgICBnYXA6MTRweDsKICAgIGZsZXgtd3JhcDp3cmFwOwogIH0KICAuam9iLXRpdGxle2ZvbnQtd2VpZ2h0OjcwMDtjb2xvcjp2YXIoLS1pbmspO2ZvbnQtc2l6ZToxMC45cHQ7fQogIC5jb21wYW55e2NvbG9yOnZhcigtLWFjY2VudCk7Zm9udC13ZWlnaHQ6NjAwO30KICAud2hlbntjb2xvcjp2YXIoLS1tdXRlZCk7Zm9udC1zaXplOjkuM3B0O3doaXRlLXNwYWNlOm5vd3JhcDt9CiAgdWx7bWFyZ2luOjVweCAwIDA7cGFkZGluZy1sZWZ0OjE3cHg7fQogIGxpe21hcmdpbi1ib3R0b206M3B4O30KICBsaTo6bWFya2Vye2NvbG9yOnZhcigtLWFjY2VudCk7fQoKICAvKiBQcm9qZWN0cyAqLwogIC5wcm9qZWN0e21hcmdpbi1ib3R0b206MTFweDt9CiAgLnByb2plY3Q6bGFzdC1jaGlsZHttYXJnaW4tYm90dG9tOjA7fQogIC5wcm9qZWN0LXRpdGxle2ZvbnQtd2VpZ2h0OjcwMDtjb2xvcjp2YXIoLS1pbmspO30KICAuc3RhY2t7Y29sb3I6dmFyKC0tbXV0ZWQpO2ZvbnQtc2l6ZTo5LjNwdDtmb250LXN0eWxlOml0YWxpYzt9CiAgLm1pbm9yewogICAgbWFyZ2luLXRvcDo5cHg7CiAgICBwYWRkaW5nOjlweCAxMnB4OwogICAgYmFja2dyb3VuZDp2YXIoLS13YXNoKTsKICB9CiAgLm1pbm9yIHB7bWFyZ2luOjAgMCA1cHg7fQogIC5taW5vciBwOmxhc3QtY2hpbGR7bWFyZ2luLWJvdHRvbTowO30KCiAgLyogQ2VydGlmaWNhdGlvbnMgKi8KICAuY2VydHN7bGlzdC1zdHlsZTpub25lO21hcmdpbjowO3BhZGRpbmc6MDt9CiAgLmNlcnRzIGxpewogICAgcGFkZGluZy1sZWZ0OjE1cHg7CiAgICBwb3NpdGlvbjpyZWxhdGl2ZTsKICAgIG1hcmdpbi1ib3R0b206NHB4OwogIH0KICAuY2VydHMgbGk6OmJlZm9yZXsKICAgIGNvbnRlbnQ6IiI7CiAgICBwb3NpdGlvbjphYnNvbHV0ZTsKICAgIGxlZnQ6MDt0b3A6LjU1ZW07CiAgICB3aWR0aDo2cHg7aGVpZ2h0OjZweDsKICAgIGJhY2tncm91bmQ6dmFyKC0tYWNjZW50KTsKICB9CiAgLmNlcnRzIGF7Y29sb3I6dmFyKC0tYWNjZW50KTt0ZXh0LWRlY29yYXRpb246bm9uZTtib3JkZXItYm90dG9tOjFweCBzb2xpZCB0cmFuc3BhcmVudDt9CiAgLmNlcnRzIGE6aG92ZXIsLmNlcnRzIGE6Zm9jdXN7Ym9yZGVyLWJvdHRvbS1jb2xvcjp2YXIoLS1hY2NlbnQpO30KICAuaXNzdWVye2NvbG9yOnZhcigtLW11dGVkKTt9CgogIC8qIEVkdWNhdGlvbiAqLwogIC5lZHV7CiAgICBkaXNwbGF5OmZsZXg7CiAgICBqdXN0aWZ5LWNvbnRlbnQ6c3BhY2UtYmV0d2VlbjsKICAgIGFsaWduLWl0ZW1zOmJhc2VsaW5lOwogICAgZ2FwOjE0cHg7CiAgICBmbGV4LXdyYXA6d3JhcDsKICAgIHBhZGRpbmc6NnB4IDA7CiAgICBib3JkZXItYm90dG9tOjFweCBzb2xpZCB2YXIoLS1ydWxlKTsKICB9CiAgLmVkdTpsYXN0LWNoaWxke2JvcmRlci1ib3R0b206bm9uZTt9CiAgLmRlZ3JlZXtmb250LXdlaWdodDo3MDA7Y29sb3I6dmFyKC0taW5rKTt9CiAgLnNjaG9vbHtjb2xvcjp2YXIoLS1ib2R5KTt9CgogIGE6Zm9jdXMtdmlzaWJsZXtvdXRsaW5lOjJweCBzb2xpZCB2YXIoLS1hY2NlbnQpO291dGxpbmUtb2Zmc2V0OjJweDt9CgogIEBtZWRpYSAobWF4LXdpZHRoOjY0MHB4KXsKICAgIC5zaGVldHttYXJnaW46MDtwYWRkaW5nOjIycHggMThweDtib3gtc2hhZG93Om5vbmU7fQogICAgaDF7Zm9udC1zaXplOjIycHQ7fQogICAgLnNraWxsLXJvd3tncmlkLXRlbXBsYXRlLWNvbHVtbnM6MWZyO2dhcDoxcHg7fQogIH0KCiAgQG1lZGlhIHByaW50ewogICAgQHBhZ2V7c2l6ZTpsZXR0ZXI7bWFyZ2luOjAuNWluO30KICAgIGJvZHl7YmFja2dyb3VuZDojZmZmO2ZvbnQtc2l6ZTo5LjlwdDt9CiAgICAuc2hlZXR7bWFyZ2luOjA7cGFkZGluZzowO21heC13aWR0aDpub25lO2JveC1zaGFkb3c6bm9uZTt9CiAgICBzZWN0aW9ue2JyZWFrLWluc2lkZTphdXRvO30KICAgIC5qb2IsLnByb2plY3QsLmVkdXticmVhay1pbnNpZGU6YXZvaWQ7fQogICAgaDJ7YnJlYWstYWZ0ZXI6YXZvaWQ7fQogICAgLmNvbnRhY3QgYXtib3JkZXItYm90dG9tOm5vbmU7fQogIH0KPC9zdHlsZT4KPC9oZWFkPgo8Ym9keT4KPGRpdiBjbGFzcz0ic2hlZXQiPgoKICA8aGVhZGVyPgogICAgPGgxPkFuaXRoYSBSYWogQmFsZTwvaDE+CiAgICA8cCBjbGFzcz0icm9sZSI+U2VuaW9yIERhdGEgRW5naW5lZXIg4oCUIEFJL01MICZhbXA7IFN0cmVhbWluZyBDbG91ZCBQbGF0Zm9ybXM8L3A+CiAgICA8ZGl2IGNsYXNzPSJjb250YWN0Ij4KICAgICAgPGEgaHJlZj0ibWFpbHRvOmFuaXRoYXJhamJhbGxlQGdtYWlsLmNvbSI+YW5pdGhhcmFqYmFsbGVAZ21haWwuY29tPC9hPjxzcGFuIGNsYXNzPSJzZXAiPnw8L3NwYW4+KzEgKDQ3NSkgOTg4LTU4NjU8c3BhbiBjbGFzcz0ic2VwIj58PC9zcGFuPk5KLCBVU0E8YnI+CiAgICAgIDxhIGhyZWY9Imh0dHBzOi8vd3d3LmxpbmtlZGluLmNvbS9pbi9hbml0aGEtcmFqLWJhbGUtYThiYTMxMTdiLyI+TGlua2VkSW48L2E+PHNwYW4gY2xhc3M9InNlcCI+fDwvc3Bhbj48YSBocmVmPSJodHRwczovL2dpdGh1Yi5jb20vQW5pdGhhcmFqMzEiPkdpdEh1YjwvYT48c3BhbiBjbGFzcz0ic2VwIj58PC9zcGFuPjxhIGhyZWY9Imh0dHBzOi8vYW5pdGhhcmFqYmFsZTMxLm5ldGxpZnkuYXBwLyI+UG9ydGZvbGlvPC9hPgogICAgPC9kaXY+CiAgPC9oZWFkZXI+CgogIDxzZWN0aW9uPgogICAgPGgyPlN1bW1hcnk8L2gyPgogICAgPHAgY2xhc3M9InN1bW1hcnkiPlNlbmlvciBEYXRhIEVuZ2luZWVyIHdpdGggNSsgeWVhcnMgYnVpbGRpbmcgc2NhbGFibGUgZGF0YSBwbGF0Zm9ybXMgYW5kIHByb2R1Y3Rpb24gcGlwZWxpbmVzIGFjcm9zcyBmaW5hbmNpYWwsIGhlYWx0aGNhcmUsIGFuZCBBSS1kcml2ZW4gZW52aXJvbm1lbnRzLCBwcm9ncmVzc2luZyBmcm9tIGNvcmUgZGF0YSBlbmdpbmVlcmluZyB0byBpbnRlbGxpZ2VudCBkYXRhIGluZnJhc3RydWN0dXJlLiBDb21iaW5lcyBzdHJlYW1pbmcgaW5nZXN0aW9uIGFuZCB3YXJlaG91c2UgbW9kZWxpbmcg4oCUIEthZmthLCBTcGFyaywgQWlyZmxvdywgZGJ0LCBTbm93Zmxha2UsIFJlZHNoaWZ0LCBEYXRhYnJpY2tzLCBhbmQgQVdTIOKAlCB3aXRoIE1MLXJlYWR5IHBpcGVsaW5lcywgZmVhdHVyZSBlbmdpbmVlcmluZywgTUxmbG93LCBHZW5BSSBhbmQgTExNIGRhdGEgcHJvY2Vzc2luZywgUkFHLCBhbmQgdmVjdG9yLWJhc2VkIHJldHJpZXZhbCwgYmFja2VkIGJ5IGEgY29uc2lzdGVudCBmb2N1cyBvbiBzY2hlbWEgZ292ZXJuYW5jZSwgZGF0YSBxdWFsaXR5LCBsaW5lYWdlLCBhbmQgcGVyZm9ybWFuY2UgdHVuaW5nLjwvcD4KICA8L3NlY3Rpb24+CgogIDxzZWN0aW9uPgogICAgPGgyPlRlY2huaWNhbCBTa2lsbHM8L2gyPgogICAgPGRsPgogICAgICA8ZGl2IGNsYXNzPSJza2lsbC1yb3ciPjxkdD5Qcm9ncmFtbWluZyAmYW1wOyBRdWVyeWluZzwvZHQ+PGRkPlB5dGhvbiwgU1FMIChBZHZhbmNlZCBPcHRpbWl6YXRpb24sIFdpbmRvdyBGdW5jdGlvbnMpLCBKYXZhLCBTY2FsYSwgQmFzaCwgSlNPTjwvZGQ+PC9kaXY+CiAgICAgIDxkaXYgY2xhc3M9InNraWxsLXJvdyI+PGR0PkRhdGEgRW5naW5lZXJpbmc8L2R0PjxkZD5FVEwvRUxULCBEYXRhIE1vZGVsaW5nLCBEaW1lbnNpb25hbCBNb2RlbGluZywgQXBhY2hlIFNwYXJrIChQeVNwYXJrLCBTcGFyayBTUUwsIFN0cnVjdHVyZWQgU3RyZWFtaW5nKSwgQXBhY2hlIEthZmthIChLYWZrYSBDb25uZWN0LCBTY2hlbWEgUmVnaXN0cnkpLCBBcGFjaGUgQWlyZmxvdywgZGJ0LCBDaGFuZ2UgRGF0YSBDYXB0dXJlIChDREMpPC9kZD48L2Rpdj4KICAgICAgPGRpdiBjbGFzcz0ic2tpbGwtcm93Ij48ZHQ+Q2xvdWQgJmFtcDsgUGxhdGZvcm1zPC9kdD48ZGQ+QVdTIChTMywgRU1SLCBHbHVlLCBMYW1iZGEpLCBEYXRhYnJpY2tzIChEZWx0YSBMYWtlLCBVbml0eSBDYXRhbG9nLCBEZWx0YSBMaXZlIFRhYmxlcywgV29ya2Zsb3dzKSwgU25vd2ZsYWtlIChTbm93cGFyayksIEFtYXpvbiBSZWRzaGlmdCwgTWljcm9zb2Z0IEZhYnJpYywgQXBhY2hlIEljZWJlcmcsIFBhcnF1ZXQsIEF2cm88L2RkPjwvZGl2PgogICAgICA8ZGl2IGNsYXNzPSJza2lsbC1yb3ciPjxkdD5BSS9NTCAmYW1wOyBJbnRlbGxpZ2VudCBEYXRhPC9kdD48ZGQ+TWFjaGluZSBMZWFybmluZyBQaXBlbGluZXMsIEZlYXR1cmUgRW5naW5lZXJpbmcsIE1MLVJlYWR5IERhdGEgUGlwZWxpbmVzLCBNTGZsb3csIE1vZGVsIFRyYWluaW5nLCBJbmZlcmVuY2UgJmFtcDsgTW9kZWwgU2VydmluZyBQaXBlbGluZXMsIEdlbmVyYXRpdmUgQUkgRGF0YSBXb3JrZmxvd3MsIExMTSBEYXRhIFByb2Nlc3NpbmcsIExMTS9BUEkgSW50ZWdyYXRpb24sIEVtYmVkZGluZ3MsIFZlY3RvciBEYXRhYmFzZXMgKFBpbmVjb25lLCBwZ3ZlY3RvciksIFZlY3RvciBTZWFyY2gsIFJBRyBQaXBlbGluZXM8L2RkPjwvZGl2PgogICAgICA8ZGl2IGNsYXNzPSJza2lsbC1yb3ciPjxkdD5EZXZPcHMgJmFtcDsgUGxhdGZvcm08L2R0PjxkZD5HaXQsIENJL0NEIChHaXRIdWIgQWN0aW9ucywgSmVua2lucyksIERvY2tlciAoQ29tcG9zZSwgTXVsdGktc3RhZ2UgQnVpbGRzKSwgS3ViZXJuZXRlcyAoUG9kcywgRGVwbG95bWVudHMpLCBUZXJyYWZvcm0gKElhQyksIExpbnV4LCBSRVNUIEFQSXM8L2RkPjwvZGl2PgogICAgICA8ZGl2IGNsYXNzPSJza2lsbC1yb3ciPjxkdD5EYXRhIFF1YWxpdHkgJmFtcDsgQW5hbHl0aWNzPC9kdD48ZGQ+RGF0YSBRdWFsaXR5LCBEYXRhIEdvdmVybmFuY2UsIERhdGEgTGluZWFnZSwgRGF0YSBPYnNlcnZhYmlsaXR5IChHcmVhdCBFeHBlY3RhdGlvbnMpLCBRdWVyeSBPcHRpbWl6YXRpb24sIFBlcmZvcm1hbmNlIFR1bmluZywgUGFydGl0aW9uaW5nLCBNb25pdG9yaW5nLCBQb3N0Z3JlU1FMLCBNeVNRTCwgTW9uZ29EQiwgVGFibGVhdSwgUG93ZXIgQkk8L2RkPjwvZGl2PgogICAgPC9kbD4KICA8L3NlY3Rpb24+CgogIDxzZWN0aW9uPgogICAgPGgyPlByb2Zlc3Npb25hbCBFeHBlcmllbmNlPC9oMj4KCiAgICA8ZGl2IGNsYXNzPSJqb2IiPgogICAgICA8ZGl2IGNsYXNzPSJqb2ItaGVhZCI+CiAgICAgICAgPHNwYW4gY2xhc3M9ImpvYi10aXRsZSI+U2VuaW9yIEFJL01MIERhdGEgRW5naW5lZXIsIDxzcGFuIGNsYXNzPSJjb21wYW55Ij5QaW5lY29uZTwvc3Bhbj48L3NwYW4+CiAgICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPkp1biAyMDI1IOKAkyBQcmVzZW50IMK3IFJlbW90ZSwgVVNBPC9zcGFuPgogICAgICA8L2Rpdj4KICAgICAgPHVsPgogICAgICAgIDxsaT5BcmNoaXRlY3RlZCBtYWNoaW5lIGxlYXJuaW5nIHBpcGVsaW5lcyBmb3IgcmVjb21tZW5kYXRpb24gc2VydmljZXMsIGNvbWJpbmluZyBmZWF0dXJlIGVuZ2luZWVyaW5nIHdpdGggTUxmbG93IHRyYWNraW5nIGFuZCBNTC1yZWFkeSBkYXRhc2V0cyBhY3Jvc3MgMzUgZmVhdHVyZSBncm91cHMgZm9yIHByb2R1Y3Rpb24gbW9kZWwgcHJlcGFyYXRpb24gd29ya2Zsb3dzLjwvbGk+CiAgICAgICAgPGxpPk9wZXJhdGlvbmFsaXplZCBtb2RlbCB0cmFpbmluZywgaW5mZXJlbmNlLCBhbmQgbW9kZWwgc2VydmluZyBwaXBlbGluZXMgZm9yIGludGVsbGlnZW50IHNlYXJjaCwgaW1wcm92aW5nIGRlcGxveW1lbnQgcmVhZGluZXNzIHRocm91Z2ggc3RhbmRhcmRpemVkIHZhbGlkYXRpb24sIGZlYXR1cmUgYXZhaWxhYmlsaXR5LCBhbmQgcmVwZWF0YWJsZSBzZXJ2aW5nIHdvcmtmbG93cy48L2xpPgogICAgICAgIDxsaT5MYXVuY2hlZCBnZW5lcmF0aXZlIEFJIGRhdGEgd29ya2Zsb3dzIGZvciBzdXBwb3J0LWRvY3VtZW50IGludGVsbGlnZW5jZSwgdHJhbnNmb3JtaW5nIExMTSBkYXRhIHByb2Nlc3NpbmcgaW50byBpbmZlcmVuY2UgcGlwZWxpbmVzIHRoYXQgaGFuZGxlZCAxLjYgbWlsbGlvbiBkb2N1bWVudHMgbW9udGhseSB3aXRoIHN5c3RlbWF0aXplZCBlbnJpY2htZW50IGNvbnRyb2xzLjwvbGk+CiAgICAgICAgPGxpPkNvbm5lY3RlZCBQaW5lY29uZSBhbmQgcGd2ZWN0b3IgdmVjdG9yIGRhdGFiYXNlcywgZ2VuZXJhdGluZyBlbWJlZGRpbmdzIGFuZCBpbXBsZW1lbnRpbmcgdmVjdG9yIHNlYXJjaCB0aGF0IGltcHJvdmVkIHJlbGV2YW50LWNvbnRleHQgcmV0cmlldmFsIGJ5IDQzJSBhY3Jvc3MgaW5kZXhlZCBlbnRlcnByaXNlIGtub3dsZWRnZSBjb2xsZWN0aW9ucy48L2xpPgogICAgICAgIDxsaT5Fc3RhYmxpc2hlZCBSQUcgcGlwZWxpbmVzIHdpdGggTExNL0FQSSBpbnRlZ3JhdGlvbiwgZXhwb3NpbmcgUkVTVCBBUElzIHRoYXQgY29ubmVjdGVkIGVudGVycHJpc2UgcmV0cmlldmFsIHdpdGggcHJvZHVjdGlvbiBBSSBhc3Npc3RhbnRzIHdoaWxlIHN1cHBvcnRpbmcgc2VjdXJlIG1vZGVsLXNlcnZpbmcgd29ya2Zsb3dzLjwvbGk+CiAgICAgICAgPGxpPkNvbnRhaW5lcml6ZWQgQUkgYXBwbGljYXRpb25zIHVzaW5nIERvY2tlciAoQ29tcG9zZSwgbXVsdGktc3RhZ2UgYnVpbGRzKSwgaW50ZWdyYXRpbmcgR2l0IGFuZCBHaXRIdWIgQWN0aW9ucyB3aGlsZSBzdHJlbmd0aGVuaW5nIGRhdGEgb2JzZXJ2YWJpbGl0eSBhbmQgcHJvZHVjdGlvbiBtb25pdG9yaW5nIGNhcGFiaWxpdGllcy48L2xpPgogICAgICA8L3VsPgogICAgPC9kaXY+CgogICAgPGRpdiBjbGFzcz0iam9iIj4KICAgICAgPGRpdiBjbGFzcz0iam9iLWhlYWQiPgogICAgICAgIDxzcGFuIGNsYXNzPSJqb2ItdGl0bGUiPlNlbmlvciBEYXRhIEVuZ2luZWVyLCA8c3BhbiBjbGFzcz0iY29tcGFueSI+R0UgSGVhbHRoQ2FyZTwvc3Bhbj48L3NwYW4+CiAgICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPkF1ZyAyMDIyIOKAkyBOb3YgMjAyMyDCtyBSZW1vdGUsIEluZGlhPC9zcGFuPgogICAgICA8L2Rpdj4KICAgICAgPHVsPgogICAgICAgIDxsaT5MZWQgRGF0YWJyaWNrcyBtb2Rlcm5pemF0aW9uIGZvciBwYXRpZW50LXV0aWxpemF0aW9uIGFuYWx5dGljcywgYXBwbHlpbmcgRGVsdGEgTGFrZSBhbmQgTWVkYWxsaW9uIEFyY2hpdGVjdHVyZSB0byBvcmdhbml6ZSBoZWFsdGhjYXJlIHJlY29yZHMgYWNyb3NzIGdvdmVybmVkIEJyb256ZSwgU2lsdmVyLCBhbmQgR29sZCBsYXllcnMuPC9saT4KICAgICAgICA8bGk+RGVwbG95ZWQgVW5pdHkgQ2F0YWxvZyB3aXRoIERlbHRhIExpdmUgVGFibGVzLCBzdHJlbmd0aGVuaW5nIGRhdGEgZ292ZXJuYW5jZSB3aGlsZSBpbmNyZWFzaW5nIHRydXN0ZWQgZGF0YXNldCBjb3ZlcmFnZSBmcm9tIDgyJSB0byA5NyUgdGhyb3VnaCBhdXRvbWF0ZWQgY29udHJvbHMgYW5kIHN0YW5kYXJkaXplZCBhY2Nlc3MuPC9saT4KICAgICAgICA8bGk+RGVzaWduZWQgU25vd2ZsYWtlIHdhcmVob3VzZSBzdHJ1Y3R1cmVzIHdpdGggU25vd3BhcmsgdHJhbnNmb3JtYXRpb25zLCBpbXByb3ZpbmcgY29ob3J0LXF1ZXJ5IHJlc3BvbnNlIHRpbWVzIGJ5IDM4JSB3aGlsZSBzdXBwb3J0aW5nIHNjYWxhYmxlIGhlYWx0aGNhcmUgcmVwb3J0aW5nIGFjcm9zcyBtdWx0aXBsZSBjbGluaWNhbCBwcm9ncmFtcy48L2xpPgogICAgICAgIDxsaT5BdXRvbWF0ZWQgRGF0YWJyaWNrcyBXb3JrZmxvd3Mgd2l0aCBKZW5raW5zIHJlbGVhc2VzLCByZWR1Y2luZyBkZXBsb3ltZW50IGVycm9ycyB0aHJvdWdoIHN0YW5kYXJkaXplZCB2YWxpZGF0aW9uLCBwcm9tb3Rpb24sIGFuZCByb2xsYmFjayBwcm9jZWR1cmVzIGFjcm9zcyBoZWFsdGhjYXJlIGFuYWx5dGljcyBzZXJ2aWNlcy48L2xpPgogICAgICAgIDxsaT5Qcm92aXNpb25lZCBUZXJyYWZvcm0gaW5mcmFzdHJ1Y3R1cmUgd2l0aCBLdWJlcm5ldGVzIFBvZHMgYW5kIERlcGxveW1lbnRzLCBpbXByb3ZpbmcgcmVzb3VyY2Ugc2NhbGFiaWxpdHkgd2hpbGUgc3RyZW5ndGhlbmluZyBMaW51eC1iYXNlZCByZWNvdmVyeSBwcm9jZWR1cmVzIGZvciByZXBlYXRhYmxlIHBsYXRmb3JtIG9wZXJhdGlvbnMuPC9saT4KICAgICAgICA8bGk+SW50ZWdyYXRlZCBBcGFjaGUgSWNlYmVyZyB3aXRoIFBhcnF1ZXQgYW5kIEF2cm8gZGF0YXNldHMsIGVzdGFibGlzaGluZyBHcmVhdCBFeHBlY3RhdGlvbnMgdmFsaWRhdGlvbiBhbmQgZGF0YSBsaW5lYWdlIG1vbml0b3Jpbmcgd2hpbGUgcmVkdWNpbmcgc2NoZW1hLXJlbGF0ZWQgaW5jaWRlbnRzIGJ5IDI5JSBhY3Jvc3Mgc2hhcmVkIGNsaW5pY2FsIGRhdGFzZXRzLjwvbGk+CiAgICAgIDwvdWw+CiAgICA8L2Rpdj4KCiAgICA8ZGl2IGNsYXNzPSJqb2IiPgogICAgICA8ZGl2IGNsYXNzPSJqb2ItaGVhZCI+CiAgICAgICAgPHNwYW4gY2xhc3M9ImpvYi10aXRsZSI+RGF0YSBFbmdpbmVlciwgPHNwYW4gY2xhc3M9ImNvbXBhbnkiPklCTTwvc3Bhbj48L3NwYW4+CiAgICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPlNlcHQgMjAxOSDigJMgSnVsIDIwMjIgwrcgUmVtb3RlLCBJbmRpYTwvc3Bhbj4KICAgICAgPC9kaXY+CiAgICAgIDx1bD4KICAgICAgICA8bGk+RW5naW5lZXJlZCBQeXRob24gRVRMIHBpcGVsaW5lcyBmb3IgYmFua2luZyB0cmFuc2FjdGlvbiByZWNvbmNpbGlhdGlvbiwgcHJvY2Vzc2luZyAxMiBtaWxsaW9uIG1vbnRobHkgcmVjb3JkcyBhbmQgaW1wcm92aW5nIHNldHRsZW1lbnQgdmFsaWRhdGlvbiBieSAyOCUgdGhyb3VnaCBzdGFuZGFyZGl6ZWQgdHJhbnNmb3JtYXRpb24gYW5kIGV4Y2VwdGlvbiBoYW5kbGluZy48L2xpPgogICAgICAgIDxsaT5EZXZlbG9wZWQgU1FMIGRhdGEgbW9kZWxzIGZvciBjcmVkaXQtcmlzayByZXBvcnRpbmcsIGFwcGx5aW5nIHdpbmRvdyBmdW5jdGlvbnMgYW5kIGRpbWVuc2lvbmFsIG1vZGVsaW5nIHRvIGNvbnNvbGlkYXRlIGN1c3RvbWVyIGV4cG9zdXJlcyB3aGlsZSByZWR1Y2luZyByZWN1cnJpbmcgcmVwb3J0IHByZXBhcmF0aW9uIHRpbWUgYnkgMzUlLjwvbGk+CiAgICAgICAgPGxpPkJ1aWx0IEphdmEgaW5nZXN0aW9uIHNlcnZpY2VzIGZvciBwYXltZW50IGV2ZW50cywgaW50ZWdyYXRpbmcgSlNPTiBwYXlsb2FkcyB3aXRoIFBvc3RncmVTUUwgc291cmNlcyBhbmQgYXV0b21hdGVkIHZhbGlkYXRpb24gdGhhdCBpbXByb3ZlZCBkb3duc3RyZWFtIGRhdGEgY29uc2lzdGVuY3kgYWNyb3NzIGRhaWx5IGZpbmFuY2lhbCByZXBvcnRpbmcuPC9saT4KICAgICAgICA8bGk+U3RyZWFtbGluZWQgQXBhY2hlIFNwYXJrIHByb2Nlc3Npbmcgd2l0aCBQeVNwYXJrIGFuZCBTcGFyayBTUUwgZm9yIHBvcnRmb2xpbyBhbmFseXRpY3MsIHJlZHVjaW5nIGJhdGNoIGV4ZWN1dGlvbiB0aW1lIGJ5IDI0JSB0aHJvdWdoIHBhcnRpdGlvbmluZywgY2FjaGluZywgYW5kIHRhcmdldGVkIHF1ZXJ5IG9wdGltaXphdGlvbi48L2xpPgogICAgICAgIDxsaT5Db25maWd1cmVkIEFwYWNoZSBLYWZrYSBwaXBlbGluZXMgZm9yIHRyYW5zYWN0aW9uLWV2ZW50IHN0cmVhbWluZywgZXN0YWJsaXNoaW5nIFNjaGVtYSBSZWdpc3RyeSBjb250cm9scyB0aGF0IGltcHJvdmVkIG1lc3NhZ2UgY29tcGF0aWJpbGl0eSBhbmQgc3VwcG9ydGVkIHJlbGlhYmxlIGRvd25zdHJlYW0gZnJhdWQtbW9uaXRvcmluZyB3b3JrZmxvd3MuPC9saT4KICAgICAgICA8bGk+T3JjaGVzdHJhdGVkIEFwYWNoZSBBaXJmbG93IHdvcmtmbG93cyBmb3IgcmVndWxhdG9yeS1kYXRhIHByZXBhcmF0aW9uLCBjb29yZGluYXRpbmcgdmFsaWRhdGlvbiBzdGVwcyBhbmQgc2NoZWR1bGVkIGRlcGVuZGVuY2llcyB3aGlsZSBpbXByb3ZpbmcgcGlwZWxpbmUgY29tcGxldGlvbiByZWxpYWJpbGl0eSB0byA5OS41JS48L2xpPgogICAgICAgIDxsaT5JbXBsZW1lbnRlZCBBV1MgUzMgaW5nZXN0aW9uIHdpdGggRU1SIGZvciBmaW5hbmNpYWwgZGF0YXNldHMsIGFwcGx5aW5nIEJhc2ggYXV0b21hdGlvbiBhbmQgQ0RDIHByb2Nlc3NpbmcgdG8gc2hvcnRlbiBzb3VyY2UtdG8tcmVwb3J0IGxhdGVuY3kgYnkgNDcgbWludXRlcyBhY3Jvc3MgZGFpbHkgb3BlcmF0aW9ucy48L2xpPgogICAgICA8L3VsPgogICAgPC9kaXY+CiAgPC9zZWN0aW9uPgoKICA8c2VjdGlvbj4KICAgIDxoMj5Qcm9qZWN0czwvaDI+CgogICAgPGRpdiBjbGFzcz0icHJvamVjdCI+CiAgICAgIDxkaXYgY2xhc3M9InByb2plY3QtdGl0bGUiPlJldGFpbCBEYXRhIEVuZ2luZWVyaW5nIFBsYXRmb3JtPC9kaXY+CiAgICAgIDxkaXYgY2xhc3M9InN0YWNrIj5QeXRob24gwrcgS2Fma2EgwrcgU3BhcmsgwrcgQWlyZmxvdyDCtyBNeVNRTCDCtyBUYWJsZWF1PC9kaXY+CiAgICAgIDx1bD4KICAgICAgICA8bGk+Q29uc3RydWN0ZWQgYSByZWFsLXRpbWUgcmV0YWlsIHBpcGVsaW5lIHVzaW5nIEthZmthIGFuZCBTcGFyayBTdHJ1Y3R1cmVkIFN0cmVhbWluZywgdHJhbnNmb3JtaW5nIHNhbGVzIGFuZCBpbnZlbnRvcnkgZXZlbnRzIHRocm91Z2ggQnJvbnplLCBTaWx2ZXIsIGFuZCBHb2xkIHByb2Nlc3NpbmcgbGF5ZXJzLjwvbGk+CiAgICAgICAgPGxpPkFycmFuZ2VkIHNjaGVkdWxlZCBBaXJmbG93IHdvcmtmbG93cyB0byBsb2FkIGN1cmF0ZWQgTXlTUUwgZGF0YXNldHMgYW5kIGRlbGl2ZXIgVGFibGVhdS1yZWFkeSByZXBvcnRpbmcgbW9kZWxzIHN1cHBvcnRpbmcgaW52ZW50b3J5IHZpc2liaWxpdHksIHNhbGVzIGFuYWx5c2lzLCBhbmQgcmVwbGVuaXNobWVudCBkZWNpc2lvbnMuPC9saT4KICAgICAgPC91bD4KICAgIDwvZGl2PgoKICAgIDxkaXYgY2xhc3M9InByb2plY3QiPgogICAgICA8ZGl2IGNsYXNzPSJwcm9qZWN0LXRpdGxlIj5TYWxlcyBQZXJmb3JtYW5jZSBBbmFseXRpY3M8L2Rpdj4KICAgICAgPGRpdiBjbGFzcz0ic3RhY2siPlB5dGhvbiDCtyBTUUwgwrcgVGFibGVhdSDCtyBHaXQ8L2Rpdj4KICAgICAgPHVsPgogICAgICAgIDxsaT5CdWlsdCBhIFB5dGhvbiBFVEwgcGlwZWxpbmUgYWNyb3NzIHRocmVlIENTViBkYXRhc2V0cywgaW5nZXN0aW5nIHNhbGVzLCBwcm9kdWN0LCBhbmQgY3VzdG9tZXIgZGF0YSBpbnRvIGNsZWFuZWQgcmVwb3J0aW5nIG91dHB1dHMgdGhyb3VnaCBtb2R1bGFyIGluZ2VzdGlvbiwgdHJhbnNmb3JtYXRpb24sIGFuZCBkYXRhLXF1YWxpdHkgc3RhZ2VzLjwvbGk+CiAgICAgICAgPGxpPkZlZCBTUUwgYW5hbHl0aWNzIGFuZCBpbnRlcmFjdGl2ZSBUYWJsZWF1IGRhc2hib2FyZHMgd2l0aCBmaWx0ZXJpbmcgYWNyb3NzIHByb2R1Y3QgbGluZXMsIHJlZ2lvbnMsIGFuZCB0aW1lIHBlcmlvZHMuPC9saT4KICAgICAgPC91bD4KICAgIDwvZGl2PgoKICAgIDxkaXYgY2xhc3M9InByb2plY3QiPgogICAgICA8ZGl2IGNsYXNzPSJwcm9qZWN0LXRpdGxlIj5NaWNyb3NvZnQgRmFicmljIFJldGFpbCBTYWxlcyBBbmFseXRpY3M8L2Rpdj4KICAgICAgPGRpdiBjbGFzcz0ic3RhY2siPk1pY3Jvc29mdCBGYWJyaWMgwrcgUHlTcGFyayDCtyBTUUwgwrcgUG93ZXIgQkk8L2Rpdj4KICAgICAgPHVsPgogICAgICAgIDxsaT5CdWlsdCBhIExha2Vob3VzZS1iYXNlZCByZXRhaWwgYW5hbHl0aWNzIHNvbHV0aW9uIGluIE1pY3Jvc29mdCBGYWJyaWMsIGFwcGx5aW5nIFB5U3BhcmsgdHJhbnNmb3JtYXRpb25zIHRvIGNsZWFuc2UsIHN0YW5kYXJkaXplLCBhbmQgb3JnYW5pemUgc2FsZXMgZGF0YSBhY3Jvc3MgQnJvbnplLCBTaWx2ZXIsIGFuZCBHb2xkIGxheWVycy48L2xpPgogICAgICAgIDxsaT5DcmVhdGVkIFNRTCBBbmFseXRpY3MgRW5kcG9pbnQgcXVlcmllcyBhbmQgUG93ZXIgQkkgZGFzaGJvYXJkcyBjb252ZXJ0aW5nIGN1cmF0ZWQgc2FsZXMgZGF0YXNldHMgaW50byBpbnRlcmFjdGl2ZSB2aWV3cyBvZiByZXZlbnVlIHRyZW5kcywgcHJvZHVjdCBwZXJmb3JtYW5jZSwgYW5kIHJlZ2lvbmFsIGFjdGl2aXR5LjwvbGk+CiAgICAgIDwvdWw+CiAgICA8L2Rpdj4KCiAgICA8ZGl2IGNsYXNzPSJtaW5vciI+CiAgICAgIDxwPjxzcGFuIGNsYXNzPSJwcm9qZWN0LXRpdGxlIj5FdmVudGlmeSDigJQgTWFzdGVyJ3MgQ2Fwc3RvbmUuPC9zcGFuPiBEZXNpZ25lZCB0aGUgcmVsYXRpb25hbCBkYXRhIG1vZGVsLCBSRVNUIEFQSXMsIGFuZCBhdXRoZW50aWNhdGlvbiBjb250cm9scyBmb3IgYW4gZXZlbnQtbWFuYWdlbWVudCBwbGF0Zm9ybSBjb3ZlcmluZyBldmVudCBjcmVhdGlvbiwgdGlja2V0IGludmVudG9yeSwgYXR0ZW5kZWUgcmVnaXN0cmF0aW9uLCBhbmQgdHJhbnNhY3Rpb24gcmVjb3Jkcy48L3A+CiAgICAgIDxwPjxzcGFuIGNsYXNzPSJwcm9qZWN0LXRpdGxlIj5Jb1QgVm9pY2UtQ29udHJvbGxlZCBTbWFydCBIb21lLjwvc3Bhbj4gUmFzcGJlcnJ5IFBpIGF1dG9tYXRpb24gdHJhbnNsYXRpbmcgR29vZ2xlIEhvbWUgdm9pY2UgY29tbWFuZHMgaW50byByZWFsLXRpbWUgYXBwbGlhbmNlIGNvbnRyb2wgdGhyb3VnaCBJRlRUVC10cmlnZ2VyZWQgd29ya2Zsb3dzLjwvcD4KICAgICAgPHA+PHNwYW4gY2xhc3M9InByb2plY3QtdGl0bGUiPlJlbnRhbCBQb3J0YWwuPC9zcGFuPiBTY2FsYWJsZSByZW50YWwgc2VhcmNoIGFwcGxpY2F0aW9uIGNvbm5lY3Rpbmcgb3duZXJzIGFuZCB0ZW5hbnRzLCB3aXRoIGJhY2tlbmQgc2VydmljZXMsIGludGVncmF0ZWQgZGF0YWJhc2VzLCBhbmQgZmlsdGVyZWQgc2VhcmNoLjwvcD4KICAgICAgPHA+PHNwYW4gY2xhc3M9InByb2plY3QtdGl0bGUiPkZydWl0IEJhc2tldCDigJQgSU5NQVIgVGVjaG5vbG9naWVzLjwvc3Bhbj4gT25saW5lIG1hcmtldHBsYWNlIHdpdGggc2VjdXJlIHBheW1lbnRzIGFuZCBhdXRvbWF0ZWQgb3JkZXIgbWFuYWdlbWVudCwgZGVkdWN0aW5nIHNvbGQgaW52ZW50b3J5IGFuZCBxdWV1aW5nIGZ1bGZpbGxtZW50IGluIHJlYWwgdGltZS48L3A+CiAgICA8L2Rpdj4KICA8L3NlY3Rpb24+CgogIDxzZWN0aW9uPgogICAgPGgyPkNlcnRpZmljYXRpb25zPC9oMj4KICAgIDx1bCBjbGFzcz0iY2VydHMiPgogICAgICA8bGk+QVdTIENlcnRpZmllZCBEYXRhIEVuZ2luZWVyIOKAlCBBc3NvY2lhdGUgKERFQS1DMDEpIDxzcGFuIGNsYXNzPSJpc3N1ZXIiPsK3IEFtYXpvbiBXZWIgU2VydmljZXM8L3NwYW4+IOKAlCA8YSBocmVmPSJodHRwczovL3d3dy5saW5rZWRpbi5jb20vaW4vYW5pdGhhLXJhai1iYWxlLWE4YmEzMTE3Yi9kZXRhaWxzL2NlcnRpZmljYXRpb25zLyI+VmVyaWZ5PC9hPjwvbGk+CiAgICAgIDxsaT5BV1MgQ2xvdWQgUHJhY3RpdGlvbmVyIEVzc2VudGlhbHMgPHNwYW4gY2xhc3M9Imlzc3VlciI+wrcgQW1hem9uIFdlYiBTZXJ2aWNlczwvc3Bhbj4g4oCUIDxhIGhyZWY9Imh0dHBzOi8vc2tpbGxidWlsZGVyLmF3cy9sZWFybi85NFQyQkVOODVBL2F3cy1jbG91ZC1wcmFjdGl0aW9uZXItZXNzZW50aWFscy84RDc5RjNBVlI3Ij5WZXJpZnk8L2E+PC9saT4KICAgICAgPGxpPkRhdGEgRW5naW5lZXJpbmcgUHJvZmVzc2lvbmFsIENlcnRpZmljYXRlIDxzcGFuIGNsYXNzPSJpc3N1ZXIiPsK3IFNub3dmbGFrZSDCtyBTZXAgMjAyNjwvc3Bhbj48L2xpPgogICAgICA8bGk+RGF0YSBFbmdpbmVlcmluZyBGb3VuZGF0aW9uIENlcnRpZmljYXRpb24gPHNwYW4gY2xhc3M9Imlzc3VlciI+wrcgSW5mb3JtYXRpY2EgwrcgQXVnIDIwMjY8L3NwYW4+PC9saT4KICAgICAgPGxpPkRhdGFicmlja3MgRnVuZGFtZW50YWxzIEFjY3JlZGl0YXRpb24gPHNwYW4gY2xhc3M9Imlzc3VlciI+wrcgRGF0YWJyaWNrczwvc3Bhbj48L2xpPgogICAgICA8bGk+RGF0YSBBbmFseXNpcyBVc2luZyBQeXRob24gPHNwYW4gY2xhc3M9Imlzc3VlciI+wrcgRGF0YSBBbmFseXRpY3MgSm9iIFNpbXVsYXRpb24gwrcgUiBFc3NlbnRpYWxzPC9zcGFuPjwvbGk+CiAgICA8L3VsPgogIDwvc2VjdGlvbj4KCiAgPHNlY3Rpb24+CiAgICA8aDI+RWR1Y2F0aW9uPC9oMj4KICAgIDxkaXYgY2xhc3M9ImVkdSI+CiAgICAgIDxzcGFuPjxzcGFuIGNsYXNzPSJkZWdyZWUiPk1hc3RlciBvZiBTY2llbmNlLCBDb21wdXRlciBTY2llbmNlPC9zcGFuPiDigJQgPHNwYW4gY2xhc3M9InNjaG9vbCI+UGFjZSBVbml2ZXJzaXR5PC9zcGFuPjwvc3Bhbj4KICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPkphbiAyMDI0IOKAkyBEZWMgMjAyNSDCtyBOWSwgVVNBPC9zcGFuPgogICAgPC9kaXY+CiAgICA8ZGl2IGNsYXNzPSJlZHUiPgogICAgICA8c3Bhbj48c3BhbiBjbGFzcz0iZGVncmVlIj5CYWNoZWxvciBvZiBUZWNobm9sb2d5LCBJbmZvcm1hdGlvbiBUZWNobm9sb2d5PC9zcGFuPiDigJQgPHNwYW4gY2xhc3M9InNjaG9vbCI+UFZQU0lUPC9zcGFuPjwvc3Bhbj4KICAgICAgPHNwYW4gY2xhc3M9IndoZW4iPkp1biAyMDE1IOKAkyBNYXIgMjAxOSDCtyBBUCwgSW5kaWE8L3NwYW4+CiAgICA8L2Rpdj4KICA8L3NlY3Rpb24+Cgo8L2Rpdj4KPC9ib2R5Pgo8L2h0bWw+Cg==" download="Anitha_Raj_Bale_Resume.html"><i class="fa-solid fa-file-arrow-down"></i> Resume</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap">
    <div>&copy; <span id="year"></span> Anitha Raj Bale. Built with data in mind.</div>
    <div class="hint">psst &mdash; the logo up top isn't just decoration</div>
  </div>
</footer>
<script>
document.getElementById('year').textContent = new Date().getFullYear();

/* ---------- device detection ---------- */
const isTouch = window.matchMedia('(pointer: coarse)').matches || 'ontouchstart' in window;
if(isTouch){ document.body.classList.add('touch'); }

/* ---------- header scroll state ---------- */
const header = document.getElementById('siteHeader');
function onScrollHeader(){
  if(window.scrollY > 40) header.classList.add('scrolled');
  else header.classList.remove('scrolled');
}
document.addEventListener('scroll', onScrollHeader, {passive:true});
onScrollHeader();

/* ---------- mobile nav ---------- */
const navToggle = document.getElementById('navToggle');
const navLinks = document.getElementById('navLinks');
navToggle.addEventListener('click', ()=>{
  navLinks.classList.toggle('open');
  navToggle.innerHTML = navLinks.classList.contains('open') ? '<i class="fa-solid fa-xmark"></i>' : '<i class="fa-solid fa-bars"></i>';
});
document.querySelectorAll('.nav-link').forEach(l=>{
  l.addEventListener('click', ()=>{
    navLinks.classList.remove('open');
    navToggle.innerHTML = '<i class="fa-solid fa-bars"></i>';
  });
});

/* ---------- active section highlighting ---------- */
const sections = document.querySelectorAll('section[id]');
const navA = document.querySelectorAll('.nav-link');
const navObserver = new IntersectionObserver((entries)=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      navA.forEach(a=>a.classList.remove('active'));
      const match = document.querySelector('.nav-link[href="#'+entry.target.id+'"]');
      if(match) match.classList.add('active');
    }
  });
}, {rootMargin:'-45% 0px -50% 0px'});
sections.forEach(s=>navObserver.observe(s));

/* ---------- scroll progress bars ---------- */
const progressH = document.getElementById('progressH');
const progressVFill = document.getElementById('progressVFill');
const progressVDot = document.getElementById('progressVDot');
function onScrollProgress(){
  const h = document.documentElement;
  const scrolled = h.scrollTop;
  const max = h.scrollHeight - h.clientHeight;
  const pct = max > 0 ? (scrolled/max)*100 : 0;
  progressH.style.width = pct + '%';
  progressVFill.style.height = pct + '%';
  progressVDot.style.bottom = pct + '%';
}
document.addEventListener('scroll', onScrollProgress, {passive:true});
onScrollProgress();

/* ---------- reveal on scroll ---------- */
const revealEls = document.querySelectorAll('.reveal, .reveal-stagger');
const revealObserver = new IntersectionObserver((entries)=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      entry.target.classList.add('in');
      revealObserver.unobserve(entry.target);
    }
  });
}, {threshold:0.15});
revealEls.forEach(el=>revealObserver.observe(el));

/* ---------- count-up stats ---------- */
const countEls = document.querySelectorAll('.num[data-count]');
function animateCount(el){
  const target = parseFloat(el.getAttribute('data-count'));
  const suffix = el.getAttribute('data-suffix') || '';
  const dur = 1400;
  const start = performance.now();
  function step(now){
    const p = Math.min((now-start)/dur, 1);
    const eased = 1 - Math.pow(1-p, 3);
    const dec = (String(target).split('.')[1] || '').length;
    const val = (target * eased).toFixed(dec);
    el.textContent = val + suffix;
    if(p < 1) requestAnimationFrame(step);
  }
  requestAnimationFrame(step);
}
const countObserver = new IntersectionObserver((entries)=>{
  entries.forEach(entry=>{
    if(entry.isIntersecting){
      animateCount(entry.target);
      countObserver.unobserve(entry.target);
    }
  });
}, {threshold:0.6});
countEls.forEach(el=>countObserver.observe(el));

/* ---------- scramble reveal on hero word ---------- */
const scrambleEl = document.getElementById('scrambleWord');
const scrambleChars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
function scrambleTo(el, finalText, duration){
  let frame = 0;
  const totalFrames = Math.floor(duration/30);
  const iv = setInterval(()=>{
    let out = '';
    for(let i=0;i<finalText.length;i++){
      if(i < (frame/totalFrames)*finalText.length){
        out += finalText[i];
      } else {
        out += scrambleChars[Math.floor(Math.random()*scrambleChars.length)];
      }
    }
    el.textContent = out;
    frame++;
    if(frame > totalFrames){
      el.textContent = finalText;
      clearInterval(iv);
    }
  }, 30);
}
window.addEventListener('load', ()=>{
  setTimeout(()=>scrambleTo(scrambleEl, 'trust', 900), 1400);
});

/* ---------- custom cursor (desktop only) ---------- */
if(!isTouch){
  const dot = document.getElementById('cursorDot');
  const ring = document.getElementById('cursorRing');
  let mx=0,my=0, rx=0, ry=0;
  window.addEventListener('mousemove', e=>{
    mx = e.clientX; my = e.clientY;
    dot.style.transform = 'translate('+mx+'px,'+my+'px) translate(-50%,-50%)';
  });
  function ringLoop(){
    rx += (mx-rx)*0.16;
    ry += (my-ry)*0.16;
    ring.style.transform = 'translate('+rx+'px,'+ry+'px) translate(-50%,-50%)';
    requestAnimationFrame(ringLoop);
  }
  ringLoop();
  const interactive = 'a, button, .btn, .tag, .bento-cell, .project-card, .nav-link, input, textarea';
  document.addEventListener('mouseover', e=>{
    if(e.target.closest(interactive)) ring.classList.add('swell');
  });
  document.addEventListener('mouseout', e=>{
    if(e.target.closest(interactive)) ring.classList.remove('swell');
  });
}

/* ---------- bento / project card cursor glow + tilt (desktop only) ---------- */
if(!isTouch){
  document.querySelectorAll('.tilt').forEach(card=>{
    card.addEventListener('mousemove', e=>{
      const r = card.getBoundingClientRect();
      const px = e.clientX - r.left;
      const py = e.clientY - r.top;
      card.style.setProperty('--x', px+'px');
      card.style.setProperty('--y', py+'px');
      const cx = (px/r.width) - 0.5;
      const cy = (py/r.height) - 0.5;
      card.style.transform = 'perspective(700px) rotateX('+(-cy*6)+'deg) rotateY('+(cx*6)+'deg) translateY(-2px)';
    });
    card.addEventListener('mouseleave', ()=>{
      card.style.transform = 'perspective(700px) rotateX(0) rotateY(0) translateY(0)';
    });
  });
}

/* ---------- magnetic buttons (desktop only) ---------- */
if(!isTouch){
  document.querySelectorAll('.magnetic').forEach(btn=>{
    btn.addEventListener('mousemove', e=>{
      const r = btn.getBoundingClientRect();
      const cx = e.clientX - r.left - r.width/2;
      const cy = e.clientY - r.top - r.height/2;
      btn.style.transform = 'translate('+(cx*0.25)+'px,'+(cy*0.35)+'px)';
    });
    btn.addEventListener('mouseleave', ()=>{
      btn.style.transform = 'translate(0,0)';
    });
  });
}

/* ---------- marquee content ---------- */
const marqueeSkills = ['Python','SQL','Apache Spark','Apache Kafka','Apache Airflow','dbt','Snowflake','Databricks','Delta Lake','Amazon Redshift','AWS','MLflow','Embeddings','Vector Search','RAG Pipelines','Terraform','Kubernetes','Great Expectations'];
const track = document.getElementById('marqueeTrack');
const fullSet = marqueeSkills.concat(marqueeSkills);
track.innerHTML = fullSet.map(s=>'<span>'+s+' <i class="fa-solid fa-circle"></i></span>').join('');

/* ---------- hero canvas: mouse-reactive abstract motion graphic ---------- */
(function(){
  const canvas = document.getElementById('heroCanvas');
  const ctx = canvas.getContext('2d');
  let w,h, dpr = Math.min(window.devicePixelRatio||1, 2);
  const hero = document.getElementById('hero');
  function resize(){
    w = hero.clientWidth; h = hero.clientHeight;
    canvas.width = w*dpr; canvas.height = h*dpr;
    canvas.style.width = w+'px'; canvas.style.height = h+'px';
    ctx.setTransform(dpr,0,0,dpr,0,0);
  }
  resize();
  window.addEventListener('resize', resize);

  let mouseX = w/2, mouseY = h/2, targetX = w/2, targetY = h/2;
  hero.addEventListener('mousemove', e=>{
    const r = hero.getBoundingClientRect();
    targetX = e.clientX - r.left;
    targetY = e.clientY - r.top;
  });

  const nodeCount = isTouch ? 5 : 9;
  const nodes = Array.from({length:nodeCount}, (_,i)=>({
    baseX: Math.random()*1,
    baseY: Math.random()*1,
    r: 90 + Math.random()*160,
    speed: 0.15 + Math.random()*0.2,
    offset: Math.random()*1000,
    hueShift: i%2===0 ? 1 : 0.6
  }));

  function draw(t){
    ctx.clearRect(0,0,w,h);
    mouseX += (targetX-mouseX)*0.04;
    mouseY += (targetY-mouseY)*0.04;

    nodes.forEach((n, i)=>{
      const angle = t*0.00005*n.speed*60 + n.offset;
      const px = (n.baseX*w) + Math.sin(angle)*60 + (mouseX-w/2)*0.06;
      const py = (n.baseY*h) + Math.cos(angle*0.8)*60 + (mouseY-h/2)*0.06;
      const grad = ctx.createRadialGradient(px,py,0,px,py,n.r);
      grad.addColorStop(0, 'rgba(155,77,255,'+(0.20*n.hueShift)+')');
      grad.addColorStop(1, 'rgba(155,77,255,0)');
      ctx.fillStyle = grad;
      ctx.beginPath();
      ctx.arc(px,py,n.r,0,Math.PI*2);
      ctx.fill();
    });

    requestAnimationFrame(draw);
  }
  requestAnimationFrame(draw);
})();

/* ---------- theme cycling easter egg ---------- */
const themes = [
  {name:'Violet Dusk', violet:'#9b4dff', bright:'#c69bff', deep:'#5b1fb0'},
  {name:'Ultraviolet', violet:'#7c3aed', bright:'#a78bfa', deep:'#4c1d95'},
  {name:'Neon Orchid', violet:'#c026d3', bright:'#e879f9', deep:'#701a75'},
  {name:'Deep Indigo', violet:'#6366f1', bright:'#a5b4fc', deep:'#312e81'},
  {name:'Electric Grape', violet:'#8b2fff', bright:'#d4b3ff', deep:'#3d0a91'}
];
let themeIdx = 0;
const logoBtn = document.getElementById('logoBtn');
const toast = document.getElementById('themeToast');
const toastLabel = document.getElementById('themeLabel');
const toastSwatch = document.getElementById('themeSwatch');
let toastTimer;
logoBtn.addEventListener('click', (e)=>{
  e.preventDefault();
  themeIdx = (themeIdx+1) % themes.length;
  const th = themes[themeIdx];
  const root = document.documentElement.style;
  root.setProperty('--violet', th.violet);
  root.setProperty('--violet-bright', th.bright);
  root.setProperty('--violet-deep', th.deep);
  root.setProperty('--violet-glow', th.violet+'73');
  toastLabel.textContent = th.name;
  toastSwatch.style.background = th.violet;
  toast.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer = setTimeout(()=>toast.classList.remove('show'), 1800);
});
</script>
</body>
</html>
