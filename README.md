<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Anchor</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Newsreader:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#F4F6FB; --card:#FFFFFF; --panel:#EEF1F6; --ink:#14213D; --muted:#5B6B8C; --edge:#DDE2EC; --accent:#14213D; --onaccent:#FFFFFF; --focus:#2F5FD0;
  --yellow:#F2B705; --hero:#14213D;
  --s0:#F6D55C; --s1:#A9CBFF; --s2:#FFC46B; --s3:#8DB4F2; --s4:#E8DC9A; --s5:#C5D8F7;
  --sans:Calibri,Carlito,"Segoe UI",Arial,sans-serif; --serif:"Newsreader",Cambria,Georgia,serif;
  box-sizing:border-box; padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){--bg:#0A101E;--card:#111B31;--panel:#1A2745;--ink:#E8ECF4;--muted:#9AA8C4;--edge:#26355A;--accent:#F2B705;--onaccent:#14213D;--focus:#F2B705;--hero:#1B2B52}
}
:root[data-theme="dark"]{--bg:#0A101E;--card:#111B31;--panel:#1A2745;--ink:#E8ECF4;--muted:#9AA8C4;--edge:#26355A;--accent:#F2B705;--onaccent:#14213D;--focus:#F2B705;--hero:#1B2B52}
*,*::before,*::after{box-sizing:inherit}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--ink);font-family:var(--sans);font-size:16px;line-height:1.45}
button,input,textarea{font:inherit;color:inherit}
button{cursor:pointer}
:is(button,input,textarea,summary,label.drop):focus-visible,mark:focus-visible{outline:3px solid var(--focus);outline-offset:2px}
.page{max-width:1160px;margin:0 auto;padding:22px 16px 48px}
.top{display:flex;align-items:center;justify-content:space-between;gap:14px;flex-wrap:wrap;margin-bottom:20px}
.brand{display:flex;align-items:center;gap:14px}
.brand .lg{width:48px;height:48px;border-radius:50%;background:var(--yellow);color:#14213D;display:grid;place-items:center}
.brand svg{width:26px;height:26px}
h1{margin:0;font-family:var(--serif);font-size:32px;line-height:1;font-weight:600;letter-spacing:.02em}
.tag{margin:4px 0 0;color:var(--muted);font-size:15px}
.acts{display:flex;gap:8px;flex-wrap:wrap}
.btn{background:var(--card);border:1px solid var(--edge);border-radius:8px;padding:6px 13px;font-weight:700;font-size:14px}
.btn:hover{border-color:var(--muted)}
.btn.pri{background:var(--accent);color:var(--onaccent);border-color:var(--accent)}
.btn.hl{background:var(--yellow);color:#14213D;border-color:var(--yellow);font-size:15px;padding:8px 20px;animation:pulse 2.2s ease-out infinite}
.btn.hl:hover{background:#FFC929;border-color:#FFC929}
@keyframes pulse{0%{box-shadow:0 0 0 0 rgba(242,183,5,.55)}70%,100%{box-shadow:0 0 0 12px rgba(242,183,5,0)}}
.setup,.pair{display:grid;grid-template-columns:1fr 1fr;gap:16px;align-items:start}
.box{background:var(--card);border:1px solid var(--edge);border-radius:14px;padding:16px 18px;margin-bottom:16px;min-width:0}
.box h2{margin:0 0 4px;font-size:17px}
.step{display:inline-grid;place-items:center;width:24px;height:24px;border-radius:50%;background:var(--accent);color:var(--onaccent);font-size:13px;margin-right:8px}
.hint{margin:0 0 12px;color:var(--muted);font-size:14px}
.drop{display:block;position:relative;border:2px dashed var(--edge);border-radius:12px;padding:14px 12px;text-align:center;cursor:pointer;background:var(--panel)}
.drop:hover,.drop.over{border-color:var(--yellow);background:color-mix(in srgb,var(--yellow) 14%,var(--panel))}
.drop b{display:block;font-size:15px}
.drop span{font-size:13px;color:var(--muted)}
.drop input{position:absolute;opacity:0;width:1px;height:1px}
details.paste{margin-top:10px}
details.paste summary{cursor:pointer;font-weight:700;font-size:14px;color:var(--muted)}
details.paste input,details.paste textarea{display:block;width:100%;margin-top:8px;background:var(--panel);border:1px solid var(--edge);border-radius:8px;padding:8px 10px;font-size:14px}
details.paste textarea{min-height:100px;resize:vertical}
details.paste .btn{margin-top:8px}
ul.list{list-style:none;margin:12px 0 0;padding:0;display:flex;flex-direction:column;gap:8px}
.item{display:flex;align-items:center;gap:10px;background:var(--panel);border-radius:10px;padding:7px 10px}
.chip{flex:none;display:inline-grid;place-items:center;min-width:24px;height:24px;border-radius:12px;font-size:13px;font-weight:700;color:#14213D;background:var(--c,var(--s0))}
.item .nm{flex:1;min-width:0;background:none;border:0;text-align:left;padding:0}
.item .nm b{display:block;font-size:14px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.item .nm small{color:var(--muted);font-size:12px}
.x{flex:none;background:transparent;border:0;color:var(--muted);font-size:18px;line-height:1;padding:4px 6px;border-radius:6px}
.x:hover{color:var(--ink);background:var(--edge)}
.tabs{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}
.tab{display:flex;align-items:center;gap:8px;background:var(--panel);border:2px solid transparent;border-radius:10px;padding:5px 12px;font-size:14px;font-weight:700;max-width:240px}
.tab[aria-pressed="true"]{border-color:var(--accent)}
.tab span{overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.tab em{font-style:normal;color:var(--muted)}
.hero{display:grid;grid-template-columns:auto 1fr;gap:26px;align-items:center;background:var(--hero);color:#fff;border-radius:16px;padding:22px 26px;margin-bottom:16px}
.tank{position:relative;width:128px;height:172px;border:4px solid rgba(255,255,255,.6);border-top-width:3px;border-radius:12px 12px 30px 30px;overflow:hidden;background:rgba(255,255,255,.07);box-shadow:inset 0 0 14px rgba(0,0,0,.35)}
.water{position:absolute;left:0;right:0;bottom:0;height:0;background:linear-gradient(#4C8DF5,#1F55C9);transition:height 1.3s cubic-bezier(.3,.7,.2,1)}
.water::before,.water::after{content:"";position:absolute;left:0;right:0;top:-12px;height:12px;background:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 50 12'%3E%3Cpath d='M0 6Q12.5 0 25 6T50 6V12H0Z' fill='%234C8DF5'/%3E%3C/svg%3E") repeat-x;background-size:50px 12px;animation:wave 2.6s linear infinite}
.water::after{top:-9px;opacity:.5;filter:brightness(1.35);animation-duration:4s;animation-direction:reverse}
@keyframes wave{to{background-position-x:50px}}
.tank.dry .water::before,.tank.dry .water::after{display:none}
.tick{position:absolute;right:0;width:14px;height:2px;background:rgba(255,255,255,.55)}
.tank .n{position:absolute;inset:0;display:grid;place-content:center;text-align:center;font-family:var(--serif);font-size:40px;font-weight:600;line-height:1;color:#fff;text-shadow:0 1px 8px rgba(0,0,0,.55)}
.tank .n small{font-family:var(--sans);font-size:12px;font-weight:400;margin-top:4px}
.hero h3{margin:0;font-family:var(--serif);font-size:28px;font-weight:600;color:var(--yellow)}
.hero p{margin:4px 0 14px;opacity:.85;font-size:14px;max-width:56ch}
.stats{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}
.stats div{background:rgba(255,255,255,.09);border-radius:10px;padding:8px 10px}
.stats b{display:block;font-size:20px}
.stats span{font-size:12px;opacity:.8}
.ph{display:flex;align-items:center;justify-content:space-between;gap:8px;flex-wrap:wrap;margin-bottom:8px}
.ph h2{margin:0}
.stabs{display:flex;gap:6px;flex-wrap:wrap;margin-bottom:10px}
.stab{display:flex;align-items:center;gap:6px;background:var(--panel);border:2px solid transparent;border-radius:10px;padding:3px 10px 3px 4px;font-size:13px;font-weight:700;max-width:200px}
.stab[aria-pressed="true"]{border-color:var(--accent)}
.stab span.t{overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.stab em{font-style:normal;color:var(--muted);font-weight:400}
.scroll{max-height:540px;overflow:auto;border-radius:12px;background:var(--panel)}
.txt{font-family:var(--serif);font-size:18px;line-height:1.75;white-space:pre-wrap;padding:16px 18px;margin:0}
mark{background:var(--c,var(--s0));color:#14213D;border-radius:3px;padding:1px 2px;cursor:pointer}
mark sup{font-family:var(--sans);font-size:11px;font-weight:700;margin-left:2px}
mark.flash{animation:fl 1.8s ease-out}
@keyframes fl{0%,65%{outline:4px solid var(--focus);outline-offset:2px}100%{outline:4px solid transparent;outline-offset:2px}}
textarea.ed{width:100%;min-height:300px;background:var(--panel);border:1px solid var(--edge);border-radius:12px;padding:16px;font-family:var(--serif);font-size:18px;line-height:1.6;resize:vertical}
.note{color:var(--muted);font-size:14px;margin:0 0 8px}
.quotes{list-style:none;margin:10px 0 0;padding:0;display:flex;flex-direction:column;gap:6px}
.qrow{display:flex;gap:10px;align-items:baseline;width:100%;text-align:left;background:var(--panel);border:0;border-radius:10px;padding:8px 12px;font-size:15px}
.qrow:hover{outline:2px solid var(--edge)}
.qrow q{font-family:var(--serif);font-size:17px;quotes:"“" "”"}
.qrow small{color:var(--muted)}
.empty{color:var(--muted);padding:18px 4px}
.toast{position:fixed;left:50%;bottom:calc(18px + env(safe-area-inset-bottom,0px));transform:translateX(-50%);background:var(--accent);color:var(--onaccent);padding:10px 16px;border-radius:10px;font-weight:700;font-size:14px;max-width:90vw;opacity:0;pointer-events:none;transition:opacity .2s}
.toast.on{opacity:1}
.foot{color:var(--muted);font-size:13px;margin-top:6px;max-width:80ch}
[hidden]{display:none!important}
.shelf{list-style:none;margin:10px 0 0;padding:0;display:flex;flex-direction:column;gap:8px}
.srow{display:grid;grid-template-columns:34px 1fr auto;gap:4px 12px;align-items:center;width:100%;text-align:left;background:var(--panel);border:2px solid transparent;border-radius:12px;padding:10px 14px}
.srow[aria-current="true"]{border-color:var(--accent)}
.srow:hover{outline:2px solid var(--edge)}
.rk{width:30px;height:30px;border-radius:50%;display:grid;place-items:center;font-weight:700;background:var(--edge);color:var(--ink)}
li:first-child>.srow .rk{background:var(--yellow);color:#14213D}
.srow .nm{font-weight:700;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.srow small{display:block;color:var(--muted);font-weight:400;font-size:13px}
.srow .pc{font-family:var(--serif);font-size:28px;font-weight:600}
.srow .meter{grid-column:2/4;height:6px;border-radius:3px;background:var(--edge);overflow:hidden}
.srow .meter i{display:block;height:100%;background:#3E86F0;border-radius:3px}
#tourOv{position:fixed;inset:0;z-index:998}
#tourHole{position:fixed;z-index:999;border-radius:14px;box-shadow:0 0 0 9999px rgba(8,13,26,.74),0 0 0 3px var(--yellow);pointer-events:none;transition:top .25s ease,left .25s ease,width .25s ease,height .25s ease}
#tourPop{position:fixed;left:50%;transform:translateX(-50%);z-index:1000;width:min(440px,calc(100vw - 24px));background:var(--card);color:var(--ink);border:2px solid var(--yellow);border-radius:14px;padding:16px 18px;box-shadow:0 10px 30px rgba(0,0,0,.45)}
#tourPop.atTop{top:calc(12px + env(safe-area-inset-top,0px))}
#tourPop.atBottom{bottom:calc(12px + env(safe-area-inset-bottom,0px))}
#tourPop .ts{font-size:12px;font-weight:700;color:var(--muted)}
#tourPop h3{margin:2px 0 6px;font-family:var(--serif);font-size:22px;font-weight:600}
#tourPop p{margin:0 0 14px;font-size:15px}
.tact{display:flex;gap:8px;align-items:center}
.tact .sp{flex:1}
@media (prefers-reduced-motion:reduce){#tourHole{transition:none}.btn.hl{animation:none}}
html{--cur:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='32' height='32' viewBox='0 0 24 24' fill='none' stroke-linecap='round' stroke-linejoin='round'%3E%3Cg stroke='%23fff' stroke-width='5.2'%3E%3Ccircle cx='12' cy='5' r='2.4'/%3E%3Cpath d='M12 7.5V21M8 11h8M4 14c0 4 3.6 7 8 7s8-3 8-7M4 14l-1.5 2.2M20 14l1.5 2.2'/%3E%3C/g%3E%3Cg stroke='%2314213D' stroke-width='2.4'%3E%3Ccircle cx='12' cy='5' r='2.4'/%3E%3Cpath d='M12 7.5V21M8 11h8M4 14c0 4 3.6 7 8 7s8-3 8-7M4 14l-1.5 2.2M20 14l1.5 2.2'/%3E%3C/g%3E%3C/svg%3E") 16 16,auto;
  --hand:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='32' height='32' viewBox='0 0 24 24' fill='none' stroke-linecap='round' stroke-linejoin='round'%3E%3Cg stroke='%23F2B705' stroke-width='6'%3E%3Ccircle cx='12' cy='5' r='2.4'/%3E%3Cpath d='M12 7.5V21M8 11h8M4 14c0 4 3.6 7 8 7s8-3 8-7M4 14l-1.5 2.2M20 14l1.5 2.2'/%3E%3C/g%3E%3Cg stroke='%2314213D' stroke-width='2.4'%3E%3Ccircle cx='12' cy='5' r='2.4'/%3E%3Cpath d='M12 7.5V21M8 11h8M4 14c0 4 3.6 7 8 7s8-3 8-7M4 14l-1.5 2.2M20 14l1.5 2.2'/%3E%3C/g%3E%3C/svg%3E") 16 16,pointer}
body,body *{cursor:var(--cur)!important}
body :is(button,[role=button],mark,label.drop,summary,a,input[type=range]),body :is(button,[role=button],mark,label.drop,summary) *{cursor:var(--hand)!important}
body :is(textarea,input:not([type=file]):not([type=range])){cursor:text!important}
@media (max-width:880px){.setup,.pair{grid-template-columns:1fr}.hero{grid-template-columns:1fr;justify-items:center;text-align:center}.stats{grid-template-columns:repeat(2,1fr);width:100%;text-align:left}}
@media (prefers-reduced-motion:reduce){.water,.toast{transition:none}.water::before,.water::after{animation:none}mark.flash{animation:none;outline:4px solid var(--focus)}}
</style>
</head>
<body>
<div class="page">
  <header class="top">
    <div class="brand">
      <div class="lg"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="12" cy="5" r="2.4"/><path d="M12 7.5V21M8 11h8M4 14c0 4 3.6 7 8 7s8-3 8-7M4 14l-1.5 2.2M20 14l1.5 2.2"/></svg></div>
      <div><h1>Anchor</h1><p class="tag">How well is a reading grounded in the texts it talks about?</p></div>
    </div>
    <div class="acts">
      <button class="btn hl" id="sample">Load sample</button>
      <button class="btn" id="tourBtn">Take the tour</button>
      <button class="btn" id="theme">Dark mode</button>
      <button class="btn" id="clear">Clear all</button>
    </div>
  </header>

  <div class="setup">
    <section class="box">
      <h2><span class="step">1</span>Source texts</h2>
      <p class="hint">Poems, stories, essays, articles: anything the reading should rest on. Add as many as you like.</p>
      <label class="drop" data-kind="src"><input type="file" multiple accept=".txt,.md,.markdown,.csv,.html,.htm,.json,.docx,.pdf,text/*"><b>Upload source files</b><span>or drop them here · .pdf .docx .txt .md .html</span></label>
      <details class="paste" data-kind="src"><summary>Paste text instead</summary><input class="pn" placeholder="Name (optional)" aria-label="Source name"><textarea class="pt" placeholder="Paste a source text here" aria-label="Source text"></textarea><button class="btn pa">Add source</button></details>
      <ul class="list" id="srcList"></ul>
    </section>
    <section class="box">
      <h2><span class="step">2</span>Reading to check</h2>
      <p class="hint">An essay, review, critique, or AI-written analysis. Add several to compare them.</p>
      <label class="drop" data-kind="read"><input type="file" multiple accept=".txt,.md,.markdown,.csv,.html,.htm,.json,.docx,.pdf,text/*"><b>Upload reading files</b><span>or drop them here · .pdf .docx .txt .md .html</span></label>
      <details class="paste" data-kind="read"><summary>Paste text instead</summary><input class="pn" placeholder="Name (optional)" aria-label="Reading name"><textarea class="pt" placeholder="Paste a reading here" aria-label="Reading text"></textarea><button class="btn pa">Add reading</button></details>
      <div class="tabs" id="tabs" role="group" aria-label="Readings"></div>
    </section>
  </div>

  <div id="hero"></div>
  <div class="pair" id="pair" hidden>
    <section class="box"><div class="ph"><h2>Source text</h2></div><div class="stabs" id="stabs" role="group" aria-label="Source texts"></div><p class="note" id="srcNote"></p><div class="scroll" id="srcScroll"><pre class="txt" id="srcBody"></pre></div></section>
    <section class="box"><div class="ph"><h2>Reading</h2><span id="rdTools"></span></div><p class="note" id="rdNote"></p><div id="rdBody"></div></section>
  </div>
  <section class="box" id="quotesBox" hidden><h2>Quotations found</h2><p class="note">Click one to see where it sits in both the source and the reading.</p><ul class="quotes" id="quotes"></ul></section>
  <section class="box" id="shelfBox" hidden><h2>Reading shelf</h2><p class="note">All your readings ranked by anchor density. Click one to open it.</p><ol class="shelf" id="shelf"></ol></section>
  <p class="foot">Anchor measures grounding, not quality: it finds direct quotations of 4 or more words in a row, not paraphrases. Anchor density is the share of a reading’s sentences that contain a quotation from your sources. Sample texts are original, written for this demo.</p>
</div>
<div class="toast" id="toast" role="status"></div>
<div id="tour" hidden><div id="tourOv"></div><div id="tourHole"></div>
  <div id="tourPop" class="atBottom" role="dialog" aria-modal="true" aria-labelledby="tourT"><div class="ts" id="tourN"></div><h3 id="tourT"></h3><p id="tourD"></p>
    <div class="tact"><button class="btn" id="tourSkip">Skip tour</button><span class="sp"></span><button class="btn" id="tourBack">Back</button><button class="btn pri" id="tourNext">Next</button></div></div></div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script>
<script>
const SAMPLE = {
  sources: [
    { name: "rain-over-jaro.txt", text: "The bell tower counts the rain\nand market women fold blue tarps.\nMy lola hums a half-sung song,\neach line a stone across the flood.\nNothing the river takes is lost.\nWe wake to mud and sweet rice." },
    { name: "market-day.txt", text: "On Saturdays the market opened before the roosters had finished arguing. Aling Ising stacked her mangoes in careful pyramids, each one turned so the blush faced the road. She had learned long ago that people buy with their eyes first and their hands second. By noon the heat pressed the whole street flat, and even the dogs lay still, as if the day had been ironed." }
  ],
  readings: [
    { name: "student-essay.txt", text: "Both texts treat ordinary routines as acts of memory. In the poem, the grandmother’s song becomes each line a stone across the flood, an image of survival through repetition. The story echoes this when it says people buy with their eyes first and their hands second, a habit passed down like a song. Yet the opening, The bell tower counts the rain, frames time as something heard rather than seen. Memory here is not grand but domestic. The writers seem to care about community." },
    { name: "ai-analysis.txt", text: "This collection is a profound meditation on memory, resilience, and community. Through rich imagery of rain, markets, and floods, the writers explore how culture survives hardship. The universal themes of loss and renewal resonate deeply, inviting readers to reflect on their own heritage." }
  ]
};
const MIN = 4;
const S = { sources: [], readings: [], active: null, src: 0, editing: false, id: 0, cur: null };
const $ = id => document.getElementById(id);
const esc = s => s.replace(/&/g,"&amp;").replace(/</g,"&lt;").replace(/>/g,"&gt;");
const WORD = /[\p{L}\p{N}]+(?:['’][\p{L}]+)?/gu;
const norm = w => w.toLowerCase().replace(/’/g,"'");
const STOP = new Set("a an the and or but of in on at to for with by from as is are was were be been it its this that these those i you he she we they my your his her our their not no so if then than there here have has had do does did".split(" "));
const col = i => `var(--s${i % 6})`;

function lev(a,b){ const m=a.length,n=b.length; if(Math.abs(m-n)>1) return 2; let p=Array.from({length:n+1},(_,j)=>j);
  for(let i=1;i<=m;i++){ const c=[i]; for(let j=1;j<=n;j++) c[j]=Math.min(p[j]+1,c[j-1]+1,p[j-1]+(a[i-1]===b[j-1]?0:1)); p=c; } return p[n]; }
const same = (a,b) => a===b || (a.length>=5 && b.length>=5 && lev(a,b)<=1);
const words = t => { const r=[], re=new RegExp(WORD.source,"gu"); let m; while((m=re.exec(t))) r.push({n:norm(m[0]),s:m.index,e:m.index+m[0].length}); return r; };

function prep(src){ const ws = words(src.text), map = new Map(); src.w = ws.map(x=>x.n); src.off = ws;
  for(let i=0;i<src.w.length-1;i++){ const k=src.w[i]+" "+src.w[i+1]; (map.get(k)||map.set(k,[]).get(k)).push(i); }
  src.map = map; return src; }

function analyse(text){
  const R = words(text), matches = []; let last = 0, j = 0;
  while(j < R.length-1){
    const key = R[j].n+" "+R[j+1].n; let best = null;
    S.sources.forEach((src, si) => { const pos = src.map.get(key); if(!pos) return;
      for(const k of pos.slice(0,2000)){
        let f=2; while(j+f<R.length && k+f<src.w.length && same(R[j+f].n, src.w[k+f])) f++;
        let b=0; while(j-b-1>=last && k-b-1>=0 && same(R[j-b-1].n, src.w[k-b-1])) b++;
        if(!best || f+b>best.len) best = { si, from:j-b, to:j+f-1, len:f+b, k:k-b };
      } });
    if(best && best.len >= MIN && R.slice(best.from,best.to+1).filter(x=>!STOP.has(x.n)).length >= 2){
      const so = S.sources[best.si].off;
      best.s = R[best.from].s; best.e = R[best.to].e; best.ss = so[best.k].s; best.se = so[best.k+best.len-1].e;
      matches.push(best); last = j = best.to+1;
    } else j++;
  }
  const sents = []; const re = /[^.!?\n]+(?:[.!?]+["'”’)]*)?/g; let m;
  while((m = re.exec(text))) if((m[0].match(WORD)||[]).length >= 3) sents.push({s:m.index, e:m.index+m[0].length});
  const anchored = sents.filter(x => matches.some(q => q.s < x.e && q.e > x.s)).length;
  const qw = matches.reduce((t,q)=>t+q.len,0);
  const pct = sents.length ? Math.round(100*anchored/sents.length) : 0;
  const per = S.sources.map(() => ({ n:0, w:0 })); matches.forEach(q => { per[q.si].n++; per[q.si].w += q.len; });
  const verdict = !sents.length ? "Nothing to score" : pct===0 ? "Not anchored" : pct<34 ? "Thinly anchored" : pct<67 ? "Partly anchored" : "Well anchored";
  return { matches, sents:sents.length, anchored, qw, tw:R.length, pct, per, verdict };
}

function toast(msg){ const t=$("toast"); t.textContent=msg; t.classList.add("on"); clearTimeout(toast.h); toast.h=setTimeout(()=>t.classList.remove("on"),3200); }
const loadScript = u => new Promise((ok,no) => { const s = document.createElement("script"); s.src = u; s.onload = ok; s.onerror = () => no(new Error("couldn’t load the PDF reader (check your connection)")); document.head.appendChild(s); });
async function loadPdf(){ if(window.pdfjsLib && window.pdfjsWorker) return; const B = "https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/";
  await loadScript(B+"pdf.min.js"); await loadScript(B+"pdf.worker.min.js"); pdfjsLib.GlobalWorkerOptions.workerSrc = B+"pdf.worker.min.js"; }
async function readFile(f){
  const ext = (f.name.split(".").pop()||"").toLowerCase();
  if(f.size > 5e6) throw new Error("too large (5 MB max)");
  if(ext==="pdf"){ toast("Reading "+f.name+"…"); await loadPdf();
    const pdf = await pdfjsLib.getDocument({ data: new Uint8Array(await f.arrayBuffer()) }).promise, pages = [];
    for(let p=1;p<=pdf.numPages;p++){ const c = await (await pdf.getPage(p)).getTextContent(); let s = ""; c.items.forEach(it => { s += it.str + (it.hasEOL ? "\n" : " "); }); pages.push(s); }
    const t = pages.join("\n\n").replace(/-\n(?=[a-z])/g,"").replace(/[ \t]+/g," ").trim();
    if(t.length < 20) throw new Error("no readable text (maybe a scanned PDF); paste the text instead");
    return t; }
  if(ext==="docx"){ if(!window.JSZip) throw new Error("Word support didn’t load; paste the text instead");
    const z = await JSZip.loadAsync(await f.arrayBuffer()); const x = await z.file("word/document.xml").async("string");
    return x.replace(/<\/w:p>/g,"\n").replace(/<w:tab\/>/g,"\t").replace(/<[^>]+>/g,"").replace(/&quot;/g,'"').replace(/&apos;/g,"'").replace(/&lt;/g,"<").replace(/&gt;/g,">").replace(/&amp;/g,"&"); }
  const t = await f.text();
  return (ext==="html"||ext==="htm") ? new DOMParser().parseFromString(t,"text/html").body.textContent : t;
}
function add(kind, name, text){
  if(!text.trim()) return toast(name+" is empty");
  const item = { id: ++S.id, name, text };
  if(kind==="src") S.sources.push(prep(item)); else { S.readings.push(item); S.active = item.id; }
  render();
}
async function ingest(kind, files){ for(const f of files){ try{ add(kind, f.name, await readFile(f)); } catch(e){ toast(f.name+": "+e.message); } } }
const activeReading = () => S.readings.find(r => r.id===S.active) || null;

function render(){
  $("srcList").innerHTML = S.sources.map((s,i) => `<li class="item"><span class="chip" style="--c:${col(i)}">${i+1}</span><button class="nm" data-src="${i}" title="Show in the side-by-side view"><b>${esc(s.name)}</b><small>${s.w.length.toLocaleString()} words</small></button><button class="x" data-rm="src" data-id="${s.id}" aria-label="Remove ${esc(s.name)}">×</button></li>`).join("");
  $("tabs").innerHTML = S.readings.map(r => `<button class="tab" data-tab="${r.id}" aria-pressed="${r.id===S.active}"><span title="${esc(r.name)}">${esc(r.name)}</span>${S.sources.length?`<em>${analyse(r.text).pct}%</em>`:""}</button>`).join("");
  if(S.src >= S.sources.length) S.src = 0;
  results();
}

function results(){
  const rd = activeReading(), ready = S.sources.length && rd;
  $("pair").hidden = $("quotesBox").hidden = !ready; $("shelfBox").hidden = true;
  if(!ready){ S.cur = null; S.lastPct = 0; $("hero").innerHTML = `<p class="empty">${!S.sources.length?"Add at least one source text":"Add a reading"} to see its anchor density. Not sure where to start? Press <b>Load sample</b>.</p>`; return; }
  S.cur = analyse(rd.text); heroHTML(rd); renderSrc(); renderRd(rd); renderQuotes(rd); renderShelf();
}

function heroHTML(rd){
  const a = S.cur, used = a.per.filter(p=>p.n).length;
  $("hero").innerHTML = `<section class="hero">
    <div class="tank" id="tank" role="img" aria-label="Anchor density ${a.pct} percent"><div class="water" id="water" style="height:${S.lastPct||0}%"></div><i class="tick" style="bottom:25%"></i><i class="tick" style="bottom:50%"></i><i class="tick" style="bottom:75%"></i><div class="n"><div>${a.pct}%<br><small>anchor density</small></div></div></div>
    <div><h3>${a.verdict}</h3><p>${a.anchored} of ${a.sents} sentences in <b>${esc(rd.name)}</b> contain a quotation from your sources.</p>
    <div class="stats"><div><b>${a.anchored}/${a.sents}</b><span>sentences anchored</span></div><div><b>${a.matches.length}</b><span>quotations found</span></div><div><b>${a.tw?Math.round(100*a.qw/a.tw):0}%</b><span>of words quoted</span></div><div><b>${used}/${S.sources.length}</b><span>sources used</span></div></div></div></section>`;
  const w = $("water"), tk = $("tank"); tk.classList.toggle("dry", a.pct===0);
  requestAnimationFrame(() => requestAnimationFrame(() => { w.style.height = a.pct + "%"; })); S.lastPct = a.pct;
}

function renderSrc(){
  const a = S.cur, si = S.src, src = S.sources[si];
  $("stabs").innerHTML = S.sources.map((s,i) => `<button class="stab" data-src="${i}" aria-pressed="${i===si}"><span class="chip" style="--c:${col(i)}">${i+1}</span><span class="t" title="${esc(s.name)}">${esc(s.name)}</span><em>${a.per[i].n}</em></button>`).join("");
  const qs = a.matches.map((q,i)=>({ss:q.ss,se:q.se,i,si:q.si})).filter(q=>q.si===si).sort((x,y)=>x.ss-y.ss), groups = [];
  qs.forEach(q => { const g = groups[groups.length-1]; if(g && q.ss <= g.e){ g.e = Math.max(g.e,q.se); g.ids.push(q.i); } else groups.push({ s:q.ss, e:q.se, ids:[q.i] }); });
  let out = "", pos = 0;
  groups.forEach(g => { out += esc(src.text.slice(pos,g.s)) + `<mark style="--c:${col(si)}" data-qs="${g.ids.join(" ")}" tabindex="0" role="button" title="Quoted in the reading. Click to jump there.">${esc(src.text.slice(g.s,g.e))}</mark>`; pos = g.e; });
  $("srcBody").innerHTML = out + esc(src.text.slice(pos));
  $("srcNote").textContent = a.per[si].n ? `Highlighted passages are quoted in the reading. Click one to jump to where.` : "The current reading doesn’t quote this source.";
}

function renderRd(rd){
  const a = S.cur;
  $("rdTools").innerHTML = `<button class="btn" id="edit">${S.editing?"Done editing":"Edit text"}</button> <button class="btn" data-rm="read" data-id="${rd.id}">Remove</button>`;
  if(S.editing){
    $("rdNote").textContent = "Edit freely: the score and highlights update as you type.";
    $("rdBody").innerHTML = `<textarea class="ed" id="edTxt" aria-label="Edit reading">${esc(rd.text)}</textarea>`;
    $("edTxt").oninput = e => { rd.text = e.target.value; S.cur = analyse(rd.text); heroHTML(rd); renderSrc(); renderQuotes(rd); renderShelf();
      const em = document.querySelector('.tab[aria-pressed="true"] em'); if(em) em.textContent = S.cur.pct+"%"; };
    return; }
  $("rdNote").textContent = "Highlights are quoted from your sources; the number shows which file. Click one to jump to its source.";
  let out = "", pos = 0;
  a.matches.forEach((q,i) => { out += esc(rd.text.slice(pos,q.s)) + `<mark id="rq${i}" style="--c:${col(q.si)}" data-q="${i}" tabindex="0" role="button" title="From ${esc(S.sources[q.si].name)}. Click to see it in the source.">${esc(rd.text.slice(q.s,q.e))}<sup>${q.si+1}</sup></mark>`; pos = q.e; });
  $("rdBody").innerHTML = `<div class="scroll"><div class="txt">${out+esc(rd.text.slice(pos))}</div></div>`;
}

function renderQuotes(rd){
  $("quotes").innerHTML = S.cur.matches.length ? S.cur.matches.slice(0,20).map((q,i) => `<li><button class="qrow" data-qrow="${i}"><span class="chip" style="--c:${col(q.si)}">${q.si+1}</span><span><q>${esc(rd.text.slice(q.s,q.e))}</q> <small>from ${esc(S.sources[q.si].name)}</small></span></button></li>`).join("") : `<li class="empty">No quotations found in this reading.</li>`;
}

function flash(el){ if(!el) return; el.classList.remove("flash"); void el.offsetWidth; el.classList.add("flash"); setTimeout(()=>el.classList.remove("flash"),1900); }
function jump(i, to){
  const q = S.cur.matches[i]; if(!q) return;
  if(S.src !== q.si){ S.src = q.si; renderSrc(); }
  const sm = $("srcBody").querySelector(`mark[data-qs~="${i}"]`), rm = $("rq"+i);
  const target = to==="read" ? rm : sm;
  if(target) target.scrollIntoView({ block:"center", behavior: matchMedia("(prefers-reduced-motion: reduce)").matches ? "auto" : "smooth" });
  flash(sm); flash(rm);
}

document.addEventListener("click", e => {
  const m = e.target.closest("mark[data-q]"); if(m) return jump(+m.dataset.q, "src");
  const ms = e.target.closest("mark[data-qs]"); if(ms) return jump(+ms.dataset.qs.split(" ")[0], "read");
  const qr = e.target.closest("[data-qrow]"); if(qr) return jump(+qr.dataset.qrow, "src");
  const st = e.target.closest("[data-src]"); if(st && S.cur){ S.src = +st.dataset.src; renderSrc(); return $("pair").scrollIntoView({block:"nearest",behavior:"smooth"}); }
  const sh = e.target.closest("[data-shelf]"); if(sh){ S.active = +sh.dataset.shelf; S.editing = false; render(); return $("hero").scrollIntoView({ block:"start", behavior:"smooth" }); }
  const t = e.target.closest("[data-tab]"); if(t){ S.active = +t.dataset.tab; S.editing = false; return render(); }
  const r = e.target.closest("[data-rm]"); if(r){ const id=+r.dataset.id;
    if(r.dataset.rm==="src") S.sources = S.sources.filter(s=>s.id!==id);
    else { S.readings = S.readings.filter(x=>x.id!==id); S.active = S.readings.length ? S.readings[0].id : null; S.editing = false; }
    return render(); }
  if(e.target.id==="edit"){ S.editing = !S.editing; return results(); }
  const p = e.target.closest(".pa"); if(p){ const d = p.closest("details"), nm = d.querySelector(".pn"), tx = d.querySelector(".pt"), kind = d.dataset.kind;
    add(kind, nm.value.trim() || (kind==="src"?"Pasted source ":"Pasted reading ")+(S.id+1), tx.value); nm.value = tx.value = ""; d.open = false; }
});
document.addEventListener("keydown", e => { if((e.key==="Enter"||e.key===" ") && e.target.matches("mark[role=button]")){ e.preventDefault(); e.target.click(); } });
document.querySelectorAll(".drop").forEach(z => {
  z.querySelector("input").addEventListener("change", e => { ingest(z.dataset.kind, [...e.target.files]); e.target.value = ""; });
  ["dragenter","dragover"].forEach(t => z.addEventListener(t, e => { e.preventDefault(); z.classList.add("over"); }));
  ["dragleave","drop"].forEach(t => z.addEventListener(t, e => { e.preventDefault(); z.classList.remove("over"); }));
  z.addEventListener("drop", e => ingest(z.dataset.kind, [...e.dataTransfer.files]));
});
function loadSample(){ S.sources = []; S.readings = []; S.editing = false; S.src = 0;
  SAMPLE.sources.forEach(s => S.sources.push(prep({ id:++S.id, ...s })));
  SAMPLE.readings.forEach(r => S.readings.push({ id:++S.id, ...r })); S.active = S.readings[0].id; render(); }
$("sample").onclick = loadSample;
$("clear").onclick = () => { S.sources = []; S.readings = []; S.active = null; S.editing = false; S.src = 0; render(); };
function renderShelf(){
  const box = $("shelfBox"); if(S.readings.length < 2 || !S.sources.length){ box.hidden = true; return; }
  const rows = S.readings.map(r => ({ r, a: analyse(r.text) })).sort((x,y) => y.a.pct - x.a.pct || y.a.matches.length - x.a.matches.length);
  $("shelf").innerHTML = rows.map(({r,a},i) => `<li><button class="srow" data-shelf="${r.id}" aria-current="${r.id===S.active}"><span class="rk">${i+1}</span><span class="nm" title="${esc(r.name)}">${esc(r.name)}<small>${a.verdict} · ${a.anchored} of ${a.sents} sentences · ${a.matches.length} quotation${a.matches.length===1?"":"s"}${r.id===S.active?" · viewing":""}</small></span><span class="pc">${a.pct}%</span><span class="meter"><i style="width:${a.pct}%"></i></span></button></li>`).join("");
  box.hidden = false;
}

const TOUR = [
  { sel: ".setup > section:nth-child(1)", t: "Add your source texts", d: "Upload poems, stories, essays or articles (PDF, Word or text files), or paste them in. The reading will be checked against these." },
  { sel: ".setup > section:nth-child(2)", t: "Add a reading", d: "This is the essay, review or AI analysis you want to check. Upload several to compare them." },
  { sel: "#hero", t: "The anchor beaker", d: "The water level is the anchor density: the share of the reading’s sentences that contain a quotation from your sources." },
  { sel: "#pair > section:nth-child(1)", t: "Source text", d: "Quoted passages are highlighted. Tabs switch between your source files. Click a highlight to jump to where the reading uses it." },
  { sel: "#pair > section:nth-child(2)", t: "The reading", d: "Each highlight carries the number of the file it came from. Click one to jump to its source, or use Edit text and watch the water move." },
  { sel: "#quotesBox", t: "Quotations found", d: "Every quotation with its file name. Click a row to see it in both places." },
  { sel: "#shelfBox", t: "Reading shelf", d: "With several readings, they are ranked here by anchor density. Click one to open it." },
  { sel: ".top .acts", t: "Handy tools", d: "Load the sample, replay this tour, switch between light and dark mode, or clear everything." }
];
const T = { i: 0, steps: [], on: false };
function tourPlace(){
  if(!T.on) return; const el = document.querySelector(T.steps[T.i].sel); if(!el) return;
  const r = el.getBoundingClientRect(), p = 8, h = $("tourHole"), pop = $("tourPop"), low = r.top + r.height/2 > innerHeight*0.5;
  h.style.top = (r.top-p)+"px"; h.style.left = (r.left-p)+"px"; h.style.width = (r.width+2*p)+"px"; h.style.height = (r.height+2*p)+"px";
  pop.classList.toggle("atTop", low); pop.classList.toggle("atBottom", !low);
}
function tourShow(i){
  T.i = i; const st = T.steps[i], el = document.querySelector(st.sel);
  el.scrollIntoView({ block: el.getBoundingClientRect().height > innerHeight*0.6 ? "start" : "center", behavior: "auto" });
  $("tourN").textContent = `Step ${i+1} of ${T.steps.length}`; $("tourT").textContent = st.t; $("tourD").textContent = st.d;
  $("tourBack").hidden = i===0; $("tourNext").textContent = i===T.steps.length-1 ? "Done" : "Next";
  tourPlace(); requestAnimationFrame(tourPlace); setTimeout(tourPlace,150); $("tourNext").focus({ preventScroll:true });
}
function tourStart(){
  if(T.on) return; if(!S.cur) loadSample();
  T.steps = TOUR.filter(s => { const e = document.querySelector(s.sel); return e && e.getClientRects().length; });
  if(!T.steps.length) return; T.on = true; $("tour").hidden = false; tourShow(0);
}
function tourEnd(){ T.on = false; $("tour").hidden = true; try{ localStorage.setItem("anchor-tour","1"); }catch(_){} $("tourBtn").focus({ preventScroll:true }); window.scrollTo({ top:0, behavior:"auto" }); }
$("tourBtn").onclick = tourStart;
$("tourSkip").onclick = tourEnd;
$("tourBack").onclick = () => tourShow(T.i-1);
$("tourNext").onclick = () => T.i < T.steps.length-1 ? tourShow(T.i+1) : tourEnd();
["scroll","resize"].forEach(ev => window.addEventListener(ev, tourPlace, { passive:true }));
document.addEventListener("keydown", e => {
  if(!T.on) return;
  if(e.key==="Escape") return tourEnd();
  if(e.key==="ArrowRight") return $("tourNext").click();
  if(e.key==="ArrowLeft" && T.i>0) return $("tourBack").click();
  if(e.key==="Tab"){ const f = [...$("tourPop").querySelectorAll("button")].filter(b => !b.hidden), a = document.activeElement, k = f.indexOf(a);
    e.preventDefault(); f[(k + (e.shiftKey ? -1 : 1) + f.length) % f.length].focus(); }
});

const root = document.documentElement;
function setTheme(t, save){ root.dataset.theme = t; root.style.colorScheme = t; const b = $("theme");
  b.textContent = t==="dark" ? "☀ Light mode" : "☾ Dark mode"; b.setAttribute("aria-label", t==="dark" ? "Switch to light mode" : "Switch to dark mode");
  if(save){ try{ localStorage.setItem("anchor-theme", t); }catch(_){} } }
let savedTheme = null; try{ savedTheme = localStorage.getItem("anchor-theme"); }catch(_){}
setTheme(savedTheme || (matchMedia("(prefers-color-scheme: dark)").matches ? "dark" : "light"));
$("theme").onclick = () => setTheme(root.dataset.theme==="dark" ? "light" : "dark", true);
loadSample();
let seenTour = null; try{ seenTour = localStorage.getItem("anchor-tour"); }catch(_){}
if(!seenTour) setTimeout(tourStart, 800);
</script>
</body>
</html>
