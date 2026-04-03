# good-night
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Good Night Tashuuuuu 🌙</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,400&family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Dancing+Script:wght@400;600;700&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: 'Cormorant Garamond', Georgia, serif;
    background: #0a0515;
    color: #f9f0ff;
    min-height: 100vh;
    overflow-x: hidden;
  }
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: #0a0515; }
  ::-webkit-scrollbar-thumb { background: #7c3aed55; border-radius: 4px; }
  @keyframes twinkle {
    0%,100% { opacity:.15; transform:scale(.7); }
    50%     { opacity:1;   transform:scale(1.3); }
  }
  @keyframes shoot {
    0%   { transform:translateX(0) translateY(0) rotate(-35deg); opacity:1; }
    100% { transform:translateX(600px) translateY(280px) rotate(-35deg); opacity:0; }
  }
  @keyframes float {
    0%,100% { transform:translateY(0) rotate(0deg); }
    33%     { transform:translateY(-18px) rotate(2deg); }
    66%     { transform:translateY(-8px) rotate(-2deg); }
  }
  @keyframes moonGlow {
    0%,100% { filter:drop-shadow(0 0 25px #f9c74f88) drop-shadow(0 0 60px #f9c74f44); transform:translateY(0) rotate(-6deg); }
    50%     { filter:drop-shadow(0 0 55px #f9c74fcc) drop-shadow(0 0 100px #f9c74f66); transform:translateY(-14px) rotate(6deg); }
  }
  @keyframes glowPulse {
    0%,100% { text-shadow:0 0 20px #f4a0c488,0 0 50px #c77dff55; }
    50%     { text-shadow:0 0 40px #f4a0c4cc,0 0 80px #c77dff99,0 0 120px #f4a0c466; }
  }
  @keyframes shimmer {
    0%   { background-position:-300% center; }
    100% { background-position:300% center; }
  }
  @keyframes heartbeat {
    0%,100% { transform:scale(1); }
    20%     { transform:scale(1.2); }
    40%     { transform:scale(1); }
    60%     { transform:scale(1.15); }
  }
  @keyframes petalFall {
    0%   { transform:translateY(-20px) rotate(0deg) translateX(0); opacity:0; }
    10%  { opacity:.9; }
    90%  { opacity:.6; }
    100% { transform:translateY(110vh) rotate(720deg) translateX(70px); opacity:0; }
  }
  @keyframes orbPulse {
    0%,100% { transform:scale(1) translate(0,0); opacity:.12; }
    33%     { transform:scale(1.15) translate(10px,-10px); opacity:.18; }
    66%     { transform:scale(.9) translate(-8px,8px); opacity:.08; }
  }
  @keyframes borderGlow {
    0%,100% { border-color:rgba(196,81,122,.3); box-shadow:0 8px 32px rgba(0,0,0,.4),0 0 20px rgba(196,81,122,.1); }
    50%     { border-color:rgba(199,125,255,.5); box-shadow:0 8px 32px rgba(0,0,0,.4),0 0 50px rgba(199,125,255,.2); }
  }
  @keyframes riseUp {
    from { opacity:0; transform:translateY(40px) scale(.96); }
    to   { opacity:1; transform:translateY(0) scale(1); }
  }
  @keyframes fadeMsg {
    0%  { opacity:0; transform:translateY(6px); }
    15% { opacity:1; transform:translateY(0); }
    85% { opacity:1; }
    100%{ opacity:0; }
  }
  @keyframes pageFade {
    from { opacity:0; }
    to   { opacity:1; }
  }
  @keyframes cardReveal {
    from { opacity:0; transform:translateY(24px) scale(.97); }
    to   { opacity:1; transform:translateY(0) scale(1); }
  }
  .star { position:fixed; border-radius:50%; background:#fff; pointer-events:none; animation:twinkle var(--dur,3s) ease-in-out infinite var(--del,0s); }
  .shoot-star { position:fixed; width:120px; height:2px; border-radius:2px; background:linear-gradient(90deg,#fff,transparent); pointer-events:none; opacity:0; animation:shoot var(--dur,2s) ease-in var(--del,0s) infinite; }
  .petal { position:fixed; pointer-events:none; opacity:0; font-size:var(--sz,18px); left:var(--x,50%); top:-30px; animation:petalFall var(--dur,9s) ease-in var(--del,0s) infinite; }
  .orb { position:absolute; border-radius:50%; pointer-events:none; animation:orbPulse var(--dur,10s) ease-in-out infinite var(--del,0s); }
  .glass {
    background:linear-gradient(135deg,rgba(91,33,182,.18),rgba(139,92,246,.12),rgba(196,81,122,.15));
    backdrop-filter:blur(20px) saturate(150%);
    -webkit-backdrop-filter:blur(20px) saturate(150%);
    border:1px solid rgba(196,81,122,.25);
    border-radius:24px;
    animation:borderGlow 4s ease-in-out infinite;
  }
  .shimmer {
    background:linear-gradient(90deg,#f4a0c4,#e879f9,#fbbf24,#f4a0c4,#c77dff,#fbbf24,#f4a0c4);
    background-size:300% auto;
    -webkit-background-clip:text; background-clip:text;
    -webkit-text-fill-color:transparent;
    animation:shimmer 4s linear infinite;
  }
  .btn-main {
    display:inline-block; padding:.9rem 2.8rem; border-radius:9999px;
    border:1px solid rgba(244,160,196,.3);
    background:linear-gradient(135deg,#be185d,#7c3aed);
    color:#fff; font-family:'Cormorant Garamond',serif; font-size:1.1rem;
    letter-spacing:.05em; cursor:pointer;
    transition:transform .2s,box-shadow .3s;
    box-shadow:0 0 30px rgba(190,24,93,.4),0 0 60px rgba(124,58,237,.2);
  }
  .btn-main:hover { transform:scale(1.06) translateY(-2px); box-shadow:0 0 55px rgba(190,24,93,.6),0 0 80px rgba(124,58,237,.3); }
  .btn-back {
    display:inline-block; padding:.75rem 2rem; border-radius:9999px;
    border:1px solid rgba(199,125,255,.3); background:rgba(124,58,237,.15);
    color:#c77dff; font-family:'Cormorant Garamond',serif; font-size:1rem;
    cursor:pointer; transition:all .3s;
  }
  .btn-back:hover { background:rgba(124,58,237,.3); border-color:rgba(199,125,255,.6); transform:scale(1.03); }
  #page1, #page2 { min-height:100vh; position:relative; overflow:hidden; }
  #page1 { background:radial-gradient(ellipse 80% 60% at 50% 0%,#1a0533,#0d0122 40%,#060010); }
  #page2 { background:linear-gradient(170deg,#0e0120,#150730 35%,#1a083c 65%,#200a44); }
  .page-wrap { position:relative; z-index:10; max-width:680px; margin:0 auto; padding:3rem 1.5rem 4rem; text-align:center; animation:pageFade 1.2s ease both; }
  .script  { font-family:'Dancing Script',cursive; }
  .display { font-family:'Playfair Display',Georgia,serif; }
  .glow    { animation:glowPulse 3s ease-in-out infinite; }
  .hb      { display:inline-block; animation:heartbeat 2s ease-in-out infinite; }
  .fl      { animation:float 5s ease-in-out infinite; }
  .moon    { animation:moonGlow 6s ease-in-out infinite; }
  .divider { display:flex; align-items:center; gap:12px; justify-content:center; margin:1.2rem auto; }
  .divider-line { height:1px; width:70px; }
  #rot-msg { height:2.4rem; display:flex; align-items:center; justify-content:center; margin-bottom:2rem; }
  #rot-msg span { animation:fadeMsg 3.2s ease both; font-size:1.2rem; color:#c4b5fd; font-style:italic; }
  .cards-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(260px,1fr)); gap:1.2rem; margin-bottom:2.5rem; }
  .sweet-card { border-radius:18px; padding:1.5rem; animation:cardReveal .6s cubic-bezier(.34,1.56,.64,1) both; }
  .grad-border { position:relative; }
  .grad-border::before { content:''; position:absolute; inset:-1px; border-radius:inherit; background:linear-gradient(135deg,#f4a0c4,#c77dff,#fbbf24,#f4a0c4); background-size:300% 300%; animation:shimmer 3s linear infinite; z-index:-1; opacity:.6; }
  .emoji-row { display:flex; justify-content:center; flex-wrap:wrap; gap:1rem; margin:1.5rem 0; }
  .emoji-row span { font-size:1.5rem; }
  .quote { font-family:Georgia,serif; font-size:3.5rem; line-height:1; opacity:.35; color:#f4a0c4; }
</style>
</head>
<body>
<!-- PAGE 1 — GOOD NIGHT -->
<div id="page1">
  <div id="p1-bg"></div>
  <div class="page-wrap">
    <div class="moon" style="font-size:clamp(75px,14vw,105px);display:inline-block;margin-bottom:1.5rem;">🌙</div>
    <h1 class="display shimmer" style="font-size:clamp(2.8rem,10vw,5.5rem);font-weight:700;line-height:1.1;margin-bottom:.5rem;">Tashuuuuu</h1>
    <p class="script" style="font-size:clamp(1.2rem,3.5vw,1.7rem);color:#f0abfc;margin-bottom:1.8rem;">✨ my rasmalai ✨</p>
    <div class="divider">
      <div class="divider-line" style="background:linear-gradient(90deg,transparent,#c77dff);"></div>
      <span style="color:#fbbf24;font-size:1.2rem;">❧</span>
      <div class="divider-line" style="background:linear-gradient(90deg,#c77dff,transparent);"></div>
    </div>
    <h2 class="display glow" style="font-size:clamp(1.9rem,6vw,3.4rem);color:#f9a8d4;margin:1rem 0 .8rem;">Good Night, Sweetheart</h2>
    <div id="rot-msg"><span id="rot-text"></span></div>
    <div class="glass" style="padding:2rem 2.2rem;margin-bottom:2rem;animation:riseUp .8s .2s cubic-bezier(.34,1.56,.64,1) both;">
      <div class="quote" style="text-align:left;">"</div>
      <p class="display" style="font-size:1.1rem;color:#f9a8d4;line-height:1.8;margin-bottom:.8rem;">Hey there, my sweetest Tashuuuuu</p>
      <p style="font-size:1.02rem;line-height:1.95;color:#e9d5ff;margin-bottom:.9rem;">
        As the stars come out one by one tonight, and the moon rises just to light your way — I want you to know how incredibly special you are. You brighten every corner of this world simply by being in it.
      </p>
      <p style="font-size:1.02rem;line-height:1.95;color:#ddd6fe;margin-bottom:1.1rem;">
        Let tonight's gentle breeze carry away every worry. Let the moonlight wrap around you like the warmest hug. Let the stars keep tender watch over you as you drift into the most beautiful, peaceful dreams.
      </p>
      <p class="script" style="font-size:1.4rem;color:#fde68a;">Sweet dreams, my rasmalai 🍮 💛</p>
      <div class="quote" style="text-align:right;">"</div>
    </div>
    <div class="emoji-row" id="emoji-row1"></div>
    <button class="btn-main" onclick="goTo2()">See Your Sweet Dreams Message 🌟</button>
    <p style="margin-top:1.8rem;color:#9f7aea;font-size:.88rem;letter-spacing:.1em;opacity:.8;">Made with all the love in the universe 💫</p>
  </div>
</div>
<!-- PAGE 2 — SWEET DREAMS -->
<div id="page2" style="display:none;">
  <div id="p2-bg"></div>
  <div class="page-wrap" style="max-width:780px;">
    <div class="fl" style="font-size:clamp(70px,13vw,100px);display:inline-block;margin-bottom:1rem;">🌠</div>
    <h1 class="display shimmer" style="font-size:clamp(2.6rem,9vw,4.8rem);font-weight:700;line-height:1.1;margin-bottom:.6rem;">Sweet Dreams</h1>
    <p class="script" style="font-size:clamp(1.2rem,3.5vw,1.6rem);color:#f0abfc;margin-bottom:1.2rem;">for my darling Tashuuuuu</p>
    <div class="divider">
      <div class="divider-line" style="background:linear-gradient(90deg,transparent,#c77dff);"></div>
      <span class="hb" style="color:#fbbf24;font-size:1.3rem;">💛</span>
      <div class="divider-line" style="background:linear-gradient(90deg,#c77dff,transparent);"></div>
    </div>
    <div class="glass" style="padding:2rem 2.4rem;margin:1.8rem 0;animation:riseUp .8s .1s both;">
      <div style="font-size:3.2rem;margin-bottom:.6rem;">💌</div>
      <p class="display glow" style="font-size:clamp(1.3rem,4vw,1.9rem);color:#f9a8d4;font-weight:700;margin-bottom:1rem;">"Good Night, Sweetheart"</p>
      <div style="height:1px;background:linear-gradient(90deg,transparent,rgba(199,125,255,.4),transparent);margin:.8rem 0;"></div>
      <p style="font-size:1.02rem;line-height:1.95;color:#e9d5ff;max-width:520px;margin:0 auto;">
        May the night hold you gently in its arms, may the moon sing you the softest lullabies, and may your dreams be as sweet, warm, and beautiful as your smile. Sleep peacefully, my rasmalai — tomorrow brings a new day just as wonderful as you. 💛
      </p>
      <div style="height:1px;background:linear-gradient(90deg,transparent,rgba(199,125,255,.4),transparent);margin:.8rem 0;"></div>
      <div class="emoji-row" id="emoji-row2"></div>
    </div>
    <div class="cards-grid" id="cards-grid"></div>
    <div style="margin-bottom:2.5rem;">
      <div class="grad-border glass" style="display:inline-block;max-width:480px;padding:2rem 2.2rem;border-radius:24px;">
        <div class="hb" style="font-size:2.8rem;margin-bottom:.6rem;display:block;">💗</div>
        <p class="display glow" style="font-size:clamp(1.1rem,3.5vw,1.5rem);color:#fde68a;font-weight:700;margin-bottom:.8rem;">You are my rasmalai</p>
        <p style="color:#c4b5fd;font-style:italic;font-size:.95rem;line-height:1.8;">
          Sweet, warm, and the reason everything feels better.<br>Good night and sweet dreams, always and always. 🌙✨
        </p>
        <div class="emoji-row" id="emoji-row3" style="margin-top:1rem;"></div>
      </div>
    </div>
    <button class="btn-back" onclick="goTo1()">← Back to Good Night</button>
    <p style="margin-top:1.2rem;color:#7c3aed;font-size:.85rem;letter-spacing:.12em;opacity:.7;">Made with 💜 just for Tashuuuuu</p>
  </div>
</div>
<script>
function rand(min,max){ return Math.random()*(max-min)+min; }
function makeStars(container,count){
  for(let i=0;i<count;i++){
    const d=document.createElement('div');
    d.className='star';
    const sz=rand(.7,3);
    Object.assign(d.style,{ left:rand(0,100)+'%', top:rand(0,100)+'%', width:sz+'px', height:sz+'px', '--dur':rand(2,5)+'s', '--del':rand(0,5)+'s' });
    container.appendChild(d);
  }
}
function makeShoots(container,count){
  for(let i=0;i<count;i++){
    const d=document.createElement('div');
    d.className='shoot-star';
    Object.assign(d.style,{ left:rand(0,60)+'%', top:rand(0,25)+'%', '--dur':rand(1.5,3)+'s', '--del':rand(0,18)+'s' });
    container.appendChild(d);
  }
}
const PETALS=['🌸','🌺','✿','❀','🌷'];
function makePetals(container,count){
  for(let i=0;i<count;i++){
    const d=document.createElement('div');
    d.className='petal';
    Object.assign(d.style,{ '--x':rand(0,100)+'%', '--dur':rand(7,14)+'s', '--del':rand(0,14)+'s', '--sz':rand(14,23)+'px' });
    d.textContent=PETALS[i%PETALS.length];
    container.appendChild(d);
  }
}
function makeOrbs(container,list){
  list.forEach(o=>{
    const d=document.createElement('div');
    d.className='orb';
    Object.assign(d.style,{ width:o.w+'px', height:o.w+'px', background:o.bg, top:o.top||'', left:o.left||'', right:o.right||'', bottom:o.bottom||'', '--dur':o.dur+'s', '--del':(o.del||0)+'s' });
    container.appendChild(d);
  });
}
function makeEmoji(id,list){
  const el=document.getElementById(id);
  list.forEach((e,i)=>{
    const s=document.createElement('span');
    s.textContent=e; s.className='hb';
    s.style.animationDelay=(i*.18)+'s';
    el.appendChild(s);
  });
}
// Rotating messages
const MSGS=['Close your eyes, my rasmalai… 🌙','Let the moonlight kiss your cheeks ✨','Dream of all the sweetest things 💛','You are so precious to this world 💜','Sleep now, my sweetheart 🌸'];
let msgIdx=0;
const rotEl=document.getElementById('rot-text');
function nextMsg(){
  rotEl.style.animation='none';
  rotEl.offsetHeight;
  rotEl.textContent=MSGS[msgIdx];
  rotEl.style.animation='fadeMsg 3.2s ease both';
  msgIdx=(msgIdx+1)%MSGS.length;
}
nextMsg();
setInterval(nextMsg,3200);
// Sweet cards
const CARDS=[
  { emoji:'🌸', title:'You Are Beautiful', color:'#f9a8d4', body:'In a world full of ordinary moments, you are the extraordinary one. The way you smile, the warmth in your eyes — it makes every moment better, every room brighter.' },
  { emoji:'💛', title:'Sweet as Rasmalai',  color:'#fde68a', body:'Just like the sweetest rasmalai, you melt every heart you touch. Soft, warm, sweet, and absolutely irresistible — that is you, always and forever.' },
  { emoji:'🌙', title:'Dream Beautiful',    color:'#c4b5fd', body:'Tonight, may your dreams be filled with soft clouds, golden light, and all the things that make your heart sing. You deserve the most peaceful rest.' },
  { emoji:'💜', title:'You Are Loved',      color:'#e879f9', body:'More than every star in the night sky, more than every wave in the ocean — that is how deeply and endlessly you are loved, my sweetheart.' },
];
const grid=document.getElementById('cards-grid');
CARDS.forEach((c,i)=>{
  const d=document.createElement('div');
  d.className='sweet-card glass';
  d.style.cssText+=`border-color:${c.color}33;box-shadow:0 8px 32px rgba(0,0,0,.4),0 0 40px ${c.color}11;animation-delay:${.1+i*.18}s;`;
  d.innerHTML=`<div style="font-size:2.4rem;margin-bottom:.5rem;">${c.emoji}</div>
    <h3 style="font-family:'Playfair Display',serif;font-size:1.1rem;color:${c.color};margin-bottom:.6rem;font-weight:700;">${c.title}</h3>
    <p style="font-size:.92rem;line-height:1.8;color:#ddd6fe;opacity:.9;">${c.body}</p>`;
  grid.appendChild(d);
});
makeEmoji('emoji-row1',['💖','🌟','💜','🌙','💗','✨','💕','🌸','💛']);
makeEmoji('emoji-row2',['🌸','✨','💜','🌙','💖','⭐','🌺']);
makeEmoji('emoji-row3',['💜','🌸','💛','🌙','💗']);
// Build backgrounds
function buildBg(id,orbs){
  const bg=document.getElementById(id);
  Object.assign(bg.style,{ position:'fixed', inset:'0', pointerEvents:'none' });
  makeStars(bg,150); makeShoots(bg,6); makePetals(bg,20); makeOrbs(bg,orbs);
}
buildBg('p1-bg',[
  {w:600,bg:'radial-gradient(circle,rgba(196,81,255,.12),transparent 70%)',top:'-200px',left:'50%',dur:12},
  {w:400,bg:'radial-gradient(circle,rgba(244,114,182,.1),transparent 70%)',bottom:'0',right:'-100px',dur:9,del:3},
  {w:350,bg:'radial-gradient(circle,rgba(124,58,237,.1),transparent 70%)',bottom:'20%',left:'-80px',dur:11,del:1},
]);
buildBg('p2-bg',[
  {w:700,bg:'radial-gradient(circle,rgba(139,92,246,.1),transparent 70%)',top:'-200px',left:'50%',dur:14},
  {w:450,bg:'radial-gradient(circle,rgba(236,72,153,.08),transparent 70%)',bottom:'0',right:'-100px',dur:10,del:2},
  {w:380,bg:'radial-gradient(circle,rgba(99,102,241,.09),transparent 70%)',bottom:'25%',left:'-80px',dur:12,del:4},
]);
document.getElementById('p2-bg').style.display='none';
function goTo2(){
  document.getElementById('page1').style.display='none';
  document.getElementById('p1-bg').style.display='none';
  document.getElementById('page2').style.display='block';
  document.getElementById('p2-bg').style.display='block';
  window.scrollTo(0,0);
}
function goTo1(){
  document.getElementById('page2').style.display='none';
  document.getElementById('p2-bg').style.display='none';
  document.getElementById('page1').style.display='block';
  document.getElementById('p1-bg').style.display='block';
  window.scrollTo(0,0);
}
</script>
</body>
</html>
