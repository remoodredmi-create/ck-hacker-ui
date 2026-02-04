<!doctype html>
<html lang="my">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>CK • EXTREME HACKER UI</title>
  <style>
    :root{
      --txt:#d9ffe9;
      --muted: rgba(120,255,180,.75);
      --good:#00ff88;
      --line: rgba(0,255,140,.26);
      --radius: 16px;
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", monospace;
      --glow:
        0 0 10px rgba(0,255,140,.75),
        0 0 22px rgba(0,255,140,.45),
        0 0 50px rgba(0,255,140,.28);
    }
    html,body{height:100%; margin:0; background:#000; color:var(--txt);}

    /* ===== MAIN WEBSITE ===== */
    .content{position:fixed; inset:0; background:#000; z-index:1;}
    iframe{position:absolute; inset:0; width:100%; height:100%; border:0; background:#000;}

    /* ===== FLOATING WIDGET ===== */
    .widget{
      position: fixed;
      z-index: 2147483000;
      right: 12px;
      top: calc(12px + env(safe-area-inset-top, 0px));
      width: min(320px, calc(100vw - 24px));
      border-radius: var(--radius);
      border: 1px solid var(--line);
      background: rgba(0,18,9,.72);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      box-shadow: var(--glow);
      overflow:hidden;
      user-select:none;
      display:none; /* show after hacker gate */
    }
    .header{
      display:flex; align-items:center; justify-content:space-between;
      gap:10px;
      padding: 10px 10px 8px;
      border-bottom: 1px solid rgba(0,255,140,.18);
      background: linear-gradient(180deg, rgba(0,26,12,.92), rgba(0,12,6,.86));
    }
    .title{display:flex; flex-direction:column; line-height:1.1;}
    .title b{font-family: var(--mono); font-size: 12px; letter-spacing:.3px; text-shadow:0 0 10px rgba(0,255,140,.35);}
    .title span{font-family: var(--mono); font-size: 11px; color: var(--muted);}

    .btn{
      border: 1px solid rgba(0,255,140,.22);
      background: rgba(0,255,140,.07);
      color: var(--txt);
      padding: 6px 10px;
      border-radius: 12px;
      font-weight: 800;
      cursor:pointer;
      font-family: var(--mono);
      font-size: 12px;
    }
    .btn.primary{
      background: rgba(0,255,140,.12);
      box-shadow: 0 0 14px rgba(0,255,140,.22);
      border-color: rgba(0,255,140,.36);
    }
    .btn:active{ transform: translateY(1px); }

    .body{
      padding: 10px;
      display:grid;
      grid-template-columns: 1fr 92px;
      gap:10px;
      align-items:center;
    }
    .stats{
      font-family: var(--mono);
      font-size: 12px;
      border: 1px solid rgba(0,255,140,.20);
      border-radius: 14px;
      padding: 10px 10px;
      background: rgba(0,0,0,.16);
      line-height: 1.35;
    }
    .stats b{ color: var(--good); text-shadow: 0 0 10px rgba(0,255,140,.35); }
    .small{ font-size: 11px; color: var(--muted); margin-top:6px; display:block; }

    .controls{display:flex; flex-wrap:wrap; gap:8px; padding: 0 10px 10px;}
    .controls .btn{ flex: 1 1 auto; text-align:center; }

    /* Dice */
    .stage{ width: 92px; height: 92px; perspective: 900px; display:grid; place-items:center; }
    .cubeWrap{
      width: 68px; height: 68px;
      filter: drop-shadow(0 0 10px rgba(0,255,140,.65))
              drop-shadow(0 0 26px rgba(0,255,140,.30))
              drop-shadow(0 14px 18px rgba(0,0,0,.55));
    }
    .cube{
      width: 62px; height: 62px;
      position: relative;
      transform-style: preserve-3d;
      transform: rotateX(-18deg) rotateY(22deg);
      transition: transform .35s ease;
    }
    .face{
      position:absolute; inset:0;
      border-radius: 12px;
      border:1px solid rgba(0,255,140,.22);
      background: radial-gradient(circle at 30% 30%, rgba(0,255,140,.18), rgba(0,0,0,.86));
      overflow:hidden;
      box-shadow: inset 0 0 12px rgba(0,255,140,.18);
      backface-visibility:hidden;
    }
    .tex{
      width:100%; height:100%;
      background-image: url("dice.jpg");
      background-size: cover;
      background-position:center;
      filter: saturate(1.08) contrast(1.10);
      opacity:.98;
    }
    .f1{ transform: translateZ(31px); }
    .f2{ transform: rotateY(90deg) translateZ(31px); }
    .f3{ transform: rotateY(180deg) translateZ(31px); }
    .f4{ transform: rotateY(-90deg) translateZ(31px); }
    .f5{ transform: rotateX(90deg) translateZ(31px); }
    .f6{ transform: rotateX(-90deg) translateZ(31px); }

    @keyframes spin {
      0%{ transform: rotateX(0deg) rotateY(0deg) rotateZ(0deg); }
      100%{ transform: rotateX(980deg) rotateY(1160deg) rotateZ(760deg); }
    }
    .spinning{ animation: spin .9s cubic-bezier(.2,.82,.2,1) both; }

    /* ===== EXTREME HACKER OVERLAY ===== */
    .gate{
      position: fixed;
      inset: 0;
      z-index: 2147483647;
      background: #000;
      color: var(--good);
      font-family: var(--mono);
      overflow:hidden;
      display:flex;
      align-items:center;
      justify-content:center;
    }
    .gateFx{position:absolute; inset:0; pointer-events:none;}
    .gateFx .noise{
      position:absolute; inset:-20px;
      background-image:
        url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='140' height='140'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='140' height='140' filter='url(%23n)' opacity='.55'/%3E%3C/svg%3E");
      opacity:.08;
      mix-blend-mode: overlay;
      animation: jitter 1.2s infinite steps(2);
    }
    .gateFx .scan{
      position:absolute; left:0; right:0;
      height: 220px;
      background: linear-gradient(180deg, transparent, rgba(0,255,140,.16), transparent);
      filter: blur(1px);
      animation: scan 3.6s linear infinite;
      opacity:.9;
      mix-blend-mode: screen;
    }
    @keyframes scan{ 0%{ top:-240px } 100%{ top: calc(100% + 240px) } }
    @keyframes jitter{
      0%{ transform: translate(0,0); }
      25%{ transform: translate(1px,-1px); }
      50%{ transform: translate(-1px,1px); }
      75%{ transform: translate(1px,1px); }
      100%{ transform: translate(0,0); }
    }

    #m2{position:absolute; inset:0; opacity:.28; mix-blend-mode: screen;}

    .panel2{
      position: relative;
      width: min(560px, calc(100vw - 28px));
      border: 1px solid rgba(0,255,140,.25);
      border-radius: 18px;
      background: rgba(0,16,8,.72);
      box-shadow: var(--glow);
      overflow:hidden;
    }
    .panel2::before{
      content:"";
      position:absolute; inset:-2px;
      background: linear-gradient(90deg, transparent, rgba(0,255,140,.35), rgba(0,255,220,.20), rgba(0,255,140,.35), transparent);
      filter: blur(12px);
      opacity:.6;
      animation: borderflow 2.8s linear infinite;
      pointer-events:none;
    }
    @keyframes borderflow{ 0%{ transform: translateX(-35%);} 100%{ transform: translateX(35%);} }

    .panel2Head{
      padding: 14px 14px 10px;
      border-bottom: 1px solid rgba(0,255,140,.18);
      background: linear-gradient(180deg, rgba(0,26,12,.92), rgba(0,12,6,.86));
      display:flex; align-items:center; justify-content:space-between; gap:10px;
    }
    .logo{
      display:flex; flex-direction:column; gap:2px;
    }
    .logo b{font-size: 13px; letter-spacing:.4px; text-shadow: 0 0 12px rgba(0,255,140,.35);}
    .logo span{font-size: 11px; color: rgba(160,255,210,.8);}
    .badge{
      font-size: 11px;
      padding: 6px 10px;
      border: 1px solid rgba(0,255,140,.22);
      border-radius: 999px;
      background: rgba(0,255,140,.08);
      color: rgba(200,255,230,.95);
    }

    .terminal2{
      padding: 12px 14px 0;
      font-size: 12px;
      line-height: 1.35rem;
      min-height: 170px;
      white-space: pre-wrap;
    }
    .glitch{
      position: relative;
      display:inline-block;
      text-shadow: 0 0 10px rgba(0,255,140,.45);
      animation: glitch 1.4s infinite;
    }
    @keyframes glitch{
      0%{ transform: translate(0,0); filter: hue-rotate(0deg); }
      20%{ transform: translate(1px,-1px); }
      40%{ transform: translate(-1px,1px); }
      60%{ transform: translate(2px,0); filter: hue-rotate(10deg); }
      80%{ transform: translate(-2px,0); }
      100%{ transform: translate(0,0); }
    }

    .formRow{
      padding: 12px 14px 16px;
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:10px;
    }
    .field{
      border: 1px solid rgba(0,255,140,.22);
      border-radius: 14px;
      background: rgba(0,0,0,.25);
      padding: 10px 10px;
    }
    .label{font-size: 11px; color: rgba(160,255,210,.8); margin-bottom:6px;}
    .inp{
      width:100%;
      border:0;
      outline:0;
      background: transparent;
      color: var(--good);
      font-family: var(--mono);
      font-size: 14px;
      caret-color: var(--good);
    }
    .actions{
      grid-column: 1 / -1;
      display:flex;
      gap:10px;
      flex-wrap:wrap;
      align-items:center;
      justify-content:space-between;
      margin-top:2px;
    }
    .progress{
      flex: 1 1 220px;
      height: 10px;
      border-radius: 999px;
      border: 1px solid rgba(0,255,140,.22);
      background: rgba(0,0,0,.25);
      overflow:hidden;
    }
    .bar{
      height:100%;
      width: 0%;
      background: linear-gradient(90deg, rgba(0,255,140,.0), rgba(0,255,140,.85), rgba(0,255,220,.55));
      box-shadow: 0 0 16px rgba(0,255,140,.35);
      transition: width .18s linear;
    }
    .hint{
      font-size: 11px;
      color: rgba(160,255,210,.85);
    }

    .btn2{
      border: 1px solid rgba(0,255,140,.25);
      background: rgba(0,255,140,.10);
      color: rgba(220,255,240,.98);
      padding: 10px 12px;
      border-radius: 14px;
      cursor:pointer;
      font-weight: 900;
      letter-spacing: .2px;
      font-family: var(--mono);
      min-width: 140px;
    }
    .btn2:active{ transform: translateY(1px); }
    .btn2.alt{ background: rgba(255,77,109,.08); border-color: rgba(255,77,109,.26); }

    /* Mobile: stack fields */
    @media (max-width: 520px){
      .formRow{ grid-template-columns: 1fr; }
      .btn2{ width: 100%; }
      .actions{ gap:12px; }
    }
  </style>
</head>
<body>

  <!-- MAIN WEBSITE -->
  <div class="content">
    <iframe
      src="http://www.cklottery.tv/#/register?invitationCode=87836425711"
      referrerpolicy="no-referrer"
      allow="clipboard-read; clipboard-write; fullscreen"
    ></iframe>
  </div>

  <!-- FLOATING DICE WIDGET -->
  <div class="widget" id="widget">
    <div class="header">
      <div class="title">
        <b>ULTRA DICE</b>
        <span id="miniLine">auto / 13s</span>
      </div>
      <div style="display:flex; gap:8px;">
        <button class="btn primary" id="rollBtn">Roll</button>
      </div>
    </div>

    <div class="body">
      <div class="stats">
        Bet: <b id="bet">—</b> MMK<br/>
        Dice: <b id="num">—</b><br/>
        Next: <b id="next">13</b>s<br/>
        <span class="small" id="status">status: ready</span>
      </div>

      <div class="stage">
        <div class="cubeWrap">
          <div class="cube" id="cube">
            <div class="face f1"><div class="tex"></div></div>
            <div class="face f2"><div class="tex"></div></div>
            <div class="face f3"><div class="tex"></div></div>
            <div class="face f4"><div class="tex"></div></div>
            <div class="face f5"><div class="tex"></div></div>
            <div class="face f6"><div class="tex"></div></div>
          </div>
        </div>
      </div>
    </div>

    <div class="controls">
      <button class="btn" id="autoBtn">Auto: ON</button>
      <button class="btn" id="soundBtn">Sound: ON</button>
    </div>
  </div>

  <!-- EXTREME HACKER GATE (SIMULATION) -->
  <div class="gate" id="gate">
    <div class="gateFx" aria-hidden="true">
      <canvas id="m2"></canvas>
      <div class="scan"></div>
      <div class="noise"></div>
    </div>

    <div class="panel2">
      <div class="panel2Head">
        <div class="logo">
          <b>SECURE ACCESS NODE</b>
          <span id="nodeLine">NODE: — • ENCRYPTION: AES-256</span>
        </div>
        <div class="badge" id="badge">LOCKED</div>
      </div>

      <div class="terminal2" id="term"></div>

      <div class="formRow">
        <div class="field">
          <div class="label">PHONE / ID (demo only)</div>
          <input class="inp" id="phone" inputmode="numeric" placeholder="e.g. 978174829" />
        </div>

        <div class="field">
          <div class="label">PASSWORD (demo only)</div>
          <input class="inp" id="pass" type="password" placeholder="••••••••" />
        </div>

        <div class="actions">
          <div class="progress"><div class="bar" id="bar"></div></div>
          <div class="hint" id="hint">Press ENTER or tap “ACCESS”</div>
        </div>

        <button class="btn2" id="accessBtn">ACCESS</button>
        <button class="btn2 alt" id="denyBtn">DENY (glitch)</button>
      </div>
    </div>
  </div>

  <script>
    // =================== SAFE NOTICE ===================
    // This gate is a MOVIE-STYLE simulation only.
    // It does NOT send/store phone/password anywhere.

    // ===== Matrix on gate =====
    const c = document.getElementById("m2");
    const ctx = c.getContext("2d");
    let W,H,cols,drops,fontSize;
    const chars = "01#$%&@*+=<>[]{}()アイウエオカキクケコサシスセソタチツテト";
    function resize(){
      W = c.width = innerWidth;
      H = c.height = innerHeight;
      fontSize = Math.max(12, Math.min(18, Math.floor(W/90)));
      cols = Math.floor(W / fontSize);
      drops = new Array(cols).fill(0).map(()=> Math.random()*H/fontSize);
      ctx.font = `${fontSize}px ui-monospace, monospace`;
    }
    addEventListener("resize", resize); resize();
    (function draw(){
      ctx.fillStyle = "rgba(0,0,0,0.08)";
      ctx.fillRect(0,0,W,H);
      for(let i=0;i<cols;i++){
        const t = chars[Math.floor(Math.random()*chars.length)];
        const x = i*fontSize;
        const y = drops[i]*fontSize;
        ctx.fillStyle = "rgba(0,255,140,0.95)";
        ctx.fillText(t,x,y);
        if(y>H && Math.random()>0.975) drops[i]=0;
        drops[i]+=0.6+Math.random()*0.9;
      }
      requestAnimationFrame(draw);
    })();

    // ===== Tiny sounds (WebAudio) =====
    let soundOn = true;
    let audioCtx = null;
    function beep(freq=680, dur=0.06, type="sine", gain=0.03){
      if(!soundOn) return;
      try{
        if(!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)();
        const o = audioCtx.createOscillator();
        const g = audioCtx.createGain();
        o.type = type; o.frequency.value = freq;
        g.gain.value = gain;
        o.connect(g); g.connect(audioCtx.destination);
        o.start(); o.stop(audioCtx.currentTime + dur);
      }catch(e){}
    }
    function keyClick(){ beep(880,0.012,"square",0.015); }
    function whoosh(){
      beep(320,0.05,"sine",0.02);
      setTimeout(()=>beep(520,0.06,"triangle",0.03),60);
      setTimeout(()=>beep(820,0.08,"sine",0.03),130);
    }
    function alarm(){
      beep(220,0.09,"sawtooth",0.03);
      setTimeout(()=>beep(180,0.09,"sawtooth",0.03),90);
      setTimeout(()=>beep(140,0.10,"sawtooth",0.03),180);
    }

    // ===== Gate typing + logic =====
    const gate = document.getElementById("gate");
    const widget = document.getElementById("widget");
    const term = document.getElementById("term");
    const bar = document.getElementById("bar");
    const badge = document.getElementById("badge");
    const nodeLine = document.getElementById("nodeLine");
    const hint = document.getElementById("hint");

    const phone = document.getElementById("phone");
    const pass  = document.getElementById("pass");
    const accessBtn = document.getElementById("accessBtn");
    const denyBtn   = document.getElementById("denyBtn");

    function rndNode(){ return Math.floor(100000000 + Math.random()*899999999); }
    nodeLine.textContent = `NODE: ${rndNode()} • ENCRYPTION: AES-256`;

    const scriptLines = [
      "[INIT] establishing uplink...",
      "[SCAN] probing open ports: 22 80 443 8080",
      "[BYPASS] injecting handshake token...",
      "[CRYPT] generating session key...",
      "[LOCK] secure gate requires credentials (demo only)",
      "",
      "TYPE PHONE + PASSWORD THEN PRESS ENTER"
    ];
    async function typeAll(){
      term.textContent = "";
      for(const line of scriptLines){
        await typeLine(line);
        await sleep(120);
      }
    }
    function sleep(ms){ return new Promise(r=>setTimeout(r,ms)); }
    async function typeLine(line){
      for(let i=0;i<line.length;i++){
        term.textContent += line[i];
        if(line[i] !== " ") keyClick();
        await sleep(12 + Math.random()*18);
      }
      term.textContent += "\n";
    }

    function glitchText(s){
      return s.split("").map(ch=>{
        if(Math.random()<0.08) return "█";
        if(Math.random()<0.06) return "▓";
        if(Math.random()<0.06) return "░";
        return ch;
      }).join("");
    }

    async function deny(){
      badge.textContent = "DENIED";
      badge.style.borderColor = "rgba(255,77,109,.35)";
      badge.style.background = "rgba(255,77,109,.10)";
      alarm();
      const msg = "\n> ACCESS <DENIED> :: " + glitchText("INTRUSION DETECTED") + "\n";
      await typeLine(msg);
      hint.textContent = "Try again (demo only) — press ENTER";
      bar.style.width = "0%";
    }

    async function grant(){
      badge.textContent = "GRANTED";
      badge.style.borderColor = "rgba(0,255,140,.45)";
      badge.style.background = "rgba(0,255,140,.10)";
      whoosh();
      hint.textContent = "Decrypting…";
      // progress
      for(let p=0;p<=100;p+=4){
        bar.style.width = p+"%";
        await sleep(35);
      }
      await typeLine("\n> ACCESS <GRANTED> :: SESSION UNLOCKED ✅\n");
      await sleep(450);
      gate.style.display = "none";
      widget.style.display = "block";
    }

    function maskedLen(s){
      return Math.max(0, s.replace(/\s+/g,"").length);
    }

    // Important: DO NOT store/send credentials.
    function onInput(){
      // just UI progress effect
      const a = Math.min(8, maskedLen(phone.value));
      const b = Math.min(10, maskedLen(pass.value));
      const pct = Math.min(100, (a/8*50) + (b/10*50));
      bar.style.width = pct.toFixed(0) + "%";
    }
    phone.addEventListener("input", onInput);
    pass.addEventListener("input", onInput);
    phone.addEventListener("keydown", (e)=>{ if(e.key.length===1) keyClick(); if(e.key==="Enter") accessBtn.click(); });
    pass.addEventListener("keydown", (e)=>{ if(e.key.length===1) keyClick(); if(e.key==="Enter") accessBtn.click(); });

    accessBtn.addEventListener("click", async ()=>{
      // Always safe demo: no validation, no sending.
      await grant();
    });
    denyBtn.addEventListener("click", deny);

    // start typing script
    typeAll();

    // ===== Widget Dice auto =====
    const cube = document.getElementById("cube");
    const betEl = document.getElementById("bet");
    const numEl = document.getElementById("num");
    const nextEl = document.getElementById("next");
    const statusEl = document.getElementById("status");
    const miniLine = document.getElementById("miniLine");

    const rollBtn = document.getElementById("rollBtn");
    const autoBtn = document.getElementById("autoBtn");
    const soundBtn = document.getElementById("soundBtn");

    let autoOn = true;
    let countdown = 13;
    let ticker = null;
    let rolling = false;

    function randDice(){ return Math.floor(Math.random()*6)+1; }
    function randBet(){
      const bets=[1000,2000,3000,4000,5000];
      return bets[Math.floor(Math.random()*bets.length)];
    }
    function fmt(n){ return n.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ","); }

    function setCubeToFace(n){
      const map = {
        1:{x:-18,y:22}, 2:{x:-18,y:-68}, 3:{x:-18,y:-158},
        4:{x:-18,y:112}, 5:{x:-108,y:22}, 6:{x:72,y:22}
      };
      const t=map[n];
      cube.style.transform=`rotateX(${t.x}deg) rotateY(${t.y}deg)`;
    }

    function rollSound2(){
      beep(420,0.05,"square",0.02);
      setTimeout(()=>beep(620,0.05,"sine",0.03), 60);
      setTimeout(()=>beep(860,0.06,"triangle",0.03), 120);
    }

    async function rollOnce(){
      if(rolling) return;
      rolling=true;
      const bet=randBet();
      const dice=randDice();

      betEl.textContent=fmt(bet);
      numEl.textContent="…";
      statusEl.textContent="status: spinning";
      miniLine.textContent="spinning...";
      cube.classList.add("spinning");
      rollSound2();

      const jitter=setInterval(()=>setCubeToFace(randDice()), 90);
      await new Promise(r=>setTimeout(r, 900));
      clearInterval(jitter);

      cube.classList.remove("spinning");
      setCubeToFace(dice);
      numEl.textContent=String(dice);
      statusEl.textContent="status: done";
      miniLine.textContent=`bet ${fmt(bet)} • dice ${dice}`;
      rolling=false;
    }

    function resetCountdown(){ countdown=13; nextEl.textContent=countdown; }

    function startAuto(){
      if(ticker) clearInterval(ticker);
      autoOn=true;
      autoBtn.textContent="Auto: ON";
      resetCountdown();
      rollOnce();
      ticker=setInterval(()=>{
        if(!autoOn) return;
        countdown--;
        if(countdown<=0){
          resetCountdown();
          rollOnce();
        }
        nextEl.textContent=countdown;
      },1000);
    }
    function stopAuto(){
      if(ticker) clearInterval(ticker);
      ticker=null;
      autoOn=false;
      autoBtn.textContent="Auto: OFF";
    }

    rollBtn.addEventListener("click", ()=>{ resetCountdown(); rollOnce(); });
    autoBtn.addEventListener("click", ()=>{ autoOn ? stopAuto() : startAuto(); });
    soundBtn.addEventListener("click", ()=>{
      soundOn = !soundOn;
      soundBtn.textContent = soundOn ? "Sound: ON" : "Sound: OFF";
      if(soundOn) beep(520,0.05,"sine",0.02);
    });

    // init dice
    setCubeToFace(1);
    startAuto();
  </script>
</body>
</html>
