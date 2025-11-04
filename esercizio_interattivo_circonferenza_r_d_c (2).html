<!DOCTYPE html>
<html lang="it">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Esercizio interattivo – Circonferenza</title>
  <style>
    :root{
      --bg:#fff;
      --card:#f7f7fb;
      --ink:#0f172a;
      --muted:#475569;
      --accent:#2563eb; /* blu raggio */
      --accent2:#dc2626; /* rosso diametro */
      --accent3:#16a34a; /* verde circonferenza */
      --ok:#16a34a; --warn:#dc2626;
    }
    *{box-sizing:border-box}
    body{margin:0; font-family:system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,"Helvetica Neue",Arial,sans-serif; color:var(--ink); background:var(--bg)}
    header{position:sticky; top:0; background:#ffffffee; backdrop-filter:saturate(1.2) blur(6px); border-bottom:1px solid #e5e7eb}
    .wrap{max-width:1000px; margin:0 auto; padding:1rem}
    h1{font-size:1.15rem; margin:0.25rem 0 0.5rem 0}
    .grid{display:grid; grid-template-columns:1.2fr 1fr; gap:1rem; align-items:stretch}
    @media (max-width:900px){.grid{grid-template-columns:1fr}}
    .card{background:var(--card); border:1px solid #e5e7eb; border-radius:16px; padding:1rem; box-shadow:0 1px 2px rgba(0,0,0,.04)}
    .viz{display:grid; place-items:center; min-height:360px}
    .controls label{font-size:.9rem; color:var(--muted)}
    .row{display:flex; gap:.75rem; align-items:center; margin:.5rem 0}
    input[type=number]{width:110px; padding:.55rem .6rem; border-radius:12px; border:1px solid #cbd5e1; font-size:1rem}
    input[readonly]{background:#f1f5f9}
    button{border:0; border-radius:999px; padding:.6rem 1rem; font-weight:600; cursor:pointer}
    .primary{background:var(--ink); color:#fff}
    .ghost{background:#e2e8f0}
    .link{border:0; background:transparent; color:var(--accent); text-decoration:underline; cursor:pointer}
    .legend{display:flex; gap:1rem; flex-wrap:wrap; justify-content:center; margin-top:.5rem; font-size:.9rem}
    .dot{width:12px; height:12px; border-radius:999px; display:inline-block; vertical-align:middle; margin-right:.4rem}
    .hint{font-size:.9rem; color:var(--muted)}
    .result{font-size:1.1rem; font-weight:700}
    .status{font-size:.9rem}
    .status.ok{color:var(--ok)}
    .status.warn{color:var(--warn)}
  </style>
</head>
<body>
  <header>
    <div class="wrap">
      <div class="row" style="justify-content:space-between; gap:.5rem; flex-wrap:wrap">
        <div>
          <div class="hint">Testo del problema</div>
          <h1 id="problem">Calcola la misura della circonferenza sapendo che il raggio misura <span id="r-problem">5</span> cm.</h1>
        </div>
        <div class="row">
          <button id="new" class="ghost" title="Genera un nuovo problema">Nuovo problema</button>
          <button id="reset" class="ghost">Reset</button>
        </div>
      </div>
    </div>
  </header>

  <main class="wrap grid" aria-live="polite">
    <!-- VISTA / DISEGNO -->
    <section class="card viz" aria-label="Disegno della circonferenza">
      <svg id="svg" width="100%" height="100%" viewBox="0 0 500 400" role="img" aria-label="Cerchio con raggio e diametro">
        <!-- Circonferenza -->
        <circle id="circle" cx="250" cy="200" r="80" fill="none" stroke="var(--accent3)" stroke-width="4" />
        <!-- Centro -->
        <circle cx="250" cy="200" r="4" fill="#111" />
        <!-- Linea raggio -->
        <line id="r-line" x1="250" y1="200" x2="330" y2="200" stroke="var(--accent)" stroke-width="4" />
        <!-- Linea diametro -->
        <line id="d-line" x1="170" y1="200" x2="330" y2="200" stroke="var(--accent2)" stroke-width="3" stroke-dasharray="6 6" />
        <!-- Etichette -->
        <text id="r-label" x="292" y="190" font-size="14" fill="var(--accent)">r</text>
        <text id="d-label" x="246" y="217" font-size="14" fill="var(--accent2)">d</text>
      </svg>
      <div class="legend">
        <span><span class="dot" style="background:var(--accent)"></span>Raggio (blu)</span>
        <span><span class="dot" style="background:var(--accent2)"></span>Diametro (rosso)</span>
        <span><span class="dot" style="background:var(--accent3)"></span>Circonferenza (verde)</span>
      </div>
    </section>

    <!-- CONTROLLI / DATI -->
    <section class="card controls" aria-label="Dati del problema">
      <div class="row"><strong>Dati</strong></div>

      <div class="row">
        <label for="r">r =</label>
        <input id="r" type="number" min="0" step="0.1" inputmode="decimal" aria-label="Valore del raggio in centimetri" />
        <span class="hint">cm</span>
      </div>
      <div class="row">
        <label for="d">d =</label>
        <input id="d" type="number" min="0" step="0.1" inputmode="decimal" aria-label="Valore del diametro in centimetri" />
        <span class="hint">cm</span>
      </div>

      <div class="row" style="margin-top:.25rem"><strong>Calcola C in due modi</strong></div>
      <div class="row">
        <label for="cpi">C =</label>
        <input id="cpi" type="text" aria-label="Circonferenza espressa come multiplo di pi greco" placeholder="es. 10π" />
        <button id="insert-pi" type="button" class="ghost" title="Inserisci il simbolo π nel box">π</button>
        <span class="hint">(in π, es. 10π)</span>
      </div>
      <div class="row">
        <label for="ccm">C =</label>
        <input id="ccm" type="number" step="0.01" inputmode="decimal" aria-label="Circonferenza in centimetri" placeholder="?" />
        <span class="hint">cm</span>
      </div>

      <div class="row" style="margin-top:.5rem">
        <button id="verify" class="primary">Verifica</button>
        <button id="show-steps" class="link" aria-expanded="false" aria-controls="steps">Mostra passaggi</button>
      </div>

      <div id="steps" hidden>
        <table style="width:100%; border-collapse:collapse; margin-bottom:0.5rem; font-size:1rem; width:100%;">
          <tr>
            <td style="border:1px solid #ccc; padding:4px; text-align:center; font-weight:600;">Circonferenza (espressa in π)</td>
            <td style="border:1px solid #ccc; padding:4px; text-align:center; font-weight:600;">Circonferenza (espressa in cm)</td>
          </tr>
          <tr>
            <td style="border:1px solid #ccc; padding:4px; text-align:center; font-size:1.15rem;"><strong>C = r·2·π</strong></td>
            <td style="border:1px solid #ccc; padding:4px; text-align:center; font-size:1.15rem;"><strong>C = r&nbsp;&nbsp;·&nbsp;&nbsp;6.28</strong></td>
          </tr>
          <tr>
            <td style="border:1px solid #ccc; padding:4px; text-align:center; font-size:1.15rem;"><strong>C = d·π</strong></td>
            <td style="border:1px solid #ccc; padding:4px; text-align:center; font-size:1.15rem;"><strong>C = d&nbsp;&nbsp;·&nbsp;&nbsp;3.14</strong></td>
          </tr>
        </table>
        <ol class="hint" style="padding-left:1rem">
          <li>Scrivi <em>prima</em> C in π (es. 10π).</li>
          <li>Poi calcola C in centimetri usando π ≈ valore scelto.</li>
          <li>Ricorda l'unità di misura (cm).</li>
        </ol>
      </div>

      <div class="row" style="justify-content:space-between; margin-top:.5rem">
        <span id="status" class="status" role="status"></span>
        <span class="result" id="result"></span>
      </div>

      <hr style="margin:1rem 0; border:none; border-top:1px solid #e5e7eb" />

      <div class="row">
        <label for="pi">π ≈</label>
        <input id="pi" type="number" step="0.0001" value="3.14" style="width:120px" aria-label="Valore approssimato di pi greco" />
      </div>

      <div class="row hint">Suggerimento: digita <kbd>Invio</kbd> nei campi per verificare subito.</div>
    </section>
  </main>

  <script>
    const svg = document.getElementById('svg');
    const circle = document.getElementById('circle');
    const rLine = document.getElementById('r-line');
    const dLine = document.getElementById('d-line');
    const rLabel = document.getElementById('r-label');
    const dLabel = document.getElementById('d-label');

    const inR = document.getElementById('r');
    const inD = document.getElementById('d');
    const inCpi = document.getElementById('cpi');
    const inCcm = document.getElementById('ccm');
    const inPi = document.getElementById('pi');

    const result = document.getElementById('result');
    const status = document.getElementById('status');
    const rProblem = document.getElementById('r-problem');

    const btnVerify = document.getElementById('verify');
    const btnReset = document.getElementById('reset');
    const btnNew = document.getElementById('new');
    const btnSteps = document.getElementById('show-steps');
    const steps = document.getElementById('steps');
    const btnPi = document.getElementById('insert-pi');

    // mapping: 1 cm -> k px (auto-scales but clamped)
    function radiusToPixels(r){
      // keep visual within SVG area: min 20, max 160 px
      const k = 12; // base scale px per cm
      const px = r * k;
      return Math.max(20, Math.min(160, px));
    }

    function updateDrawingFromR(r){
      const Rpx = radiusToPixels(r);
      // circle
      circle.setAttribute('r', Rpx);
      // radius line from center to right
      const cx = 250, cy = 200;
      rLine.setAttribute('x1', cx); rLine.setAttribute('y1', cy);
      rLine.setAttribute('x2', cx + Rpx); rLine.setAttribute('y2', cy);
      rLabel.setAttribute('x', cx + Rpx - 18);
      rLabel.setAttribute('y', cy - 10);
      // diameter line, left-right
      dLine.setAttribute('x1', cx - Rpx);
      dLine.setAttribute('y1', cy);
      dLine.setAttribute('x2', cx + Rpx);
      dLine.setAttribute('y2', cy);
      dLabel.setAttribute('x', cx - 6);
      dLabel.setAttribute('y', cy + 17);
    }

    function parsePiInput(txt){
      if(!txt) return NaN;
      const s = txt.toString().trim().toLowerCase().replace(',', '.');
      const norm = s.replaceAll('pi','π').split(' ').join('');
      if (norm === 'π') return 1;
      const idx = norm.indexOf('π');
      if (idx === -1) return NaN;
      const left = norm.slice(0, idx).replace('*','');
      const right = norm.slice(idx+1).replace('*','');
      let coeff = 1;
      if (left) { const n = parseFloat(left); if (isNaN(n)) return NaN; coeff *= n; }
      if (right) { const n = parseFloat(right); if (isNaN(n)) return NaN; coeff *= n; }
      return coeff;
    }

    function insertPi(){
      // inserisce π nel punto-cursore del campo C in π
      inCpi.focus();
      const start = inCpi.selectionStart ?? inCpi.value.length;
      const end = inCpi.selectionEnd ?? inCpi.value.length;
      const before = inCpi.value.substring(0, start);
      const after = inCpi.value.substring(end);
      inCpi.value = before + 'π' + after;
      const pos = start + 1;
      inCpi.setSelectionRange(pos, pos);
    }

    function verify(){
      const pi = parseFloat(inPi.value) || 3.14;
      const r = parseFloat(inR.value);
      const d = parseFloat(inD.value);

      let used = null; let R = null; let D = null; let C_pi_coeff = null; let C_cm_expected = null;
      if (!isNaN(r) && r > 0){ used = 'r'; R = r; D = 2*r; C_pi_coeff = 2*r; C_cm_expected = 2*pi*r; }
      else if (!isNaN(d) && d > 0){ used = 'd'; D = d; R = d/2; C_pi_coeff = d; C_cm_expected = pi*d; }
      else {
        status.textContent = 'Inserisci r oppure d (> 0).';
        status.className = 'status warn';
        result.textContent = '';
        return;
      }

      updateDrawingFromR(R);
      rProblem.textContent = (R).toLocaleString('it-IT', {maximumFractionDigits:2});

      const coeff_entered = parsePiInput(inCpi.value);
      const ok_pi = Math.abs(coeff_entered - C_pi_coeff) < 1e-2;

      const Ccm = parseFloat((inCcm.value||'').toString().replace(',','.'));
      const ok_cm = !isNaN(Ccm) && Math.abs(Ccm - C_cm_expected) <= Math.max(0.01, 0.005*C_cm_expected);

      const parts = [];
      parts.push(used === 'r' ? 'Usa C = 2·r·π (C=2rpigreco).' : 'Usa C = d·π (C=dpigreco).');
      parts.push(ok_pi ? '✔️ forma in π corretta' : `❌ forma in π: coefficiente atteso ${C_pi_coeff.toLocaleString('it-IT',{maximumFractionDigits:2})}`);
      parts.push(ok_cm ? '✔️ valore in cm corretto' : `❌ valore in cm atteso ≈ ${C_cm_expected.toLocaleString('it-IT',{maximumFractionDigits:2})}`);
      status.textContent = parts.join(' · ');
      status.className = (ok_pi && ok_cm) ? 'status ok' : 'status warn';

      result.textContent = (ok_pi && ok_cm) ? 'Ottimo!' : '';
    }

    function reset(){
      inR.value = '';
      inD.value = '';
      inCpi.value = '';
      inCcm.value = '';
      result.textContent = '';
      status.textContent = '';
      updateDrawingFromR(5);
      rProblem.textContent = '5';
    }

    function newProblem(){
      const base = Math.floor(Math.random()*15)+1;
      const half = Math.random()<0.3 ? 0.5 : 0;
      const r = base + half;
      inR.value = r.toString().replace('.', ',');
      inD.value = '';
      inCpi.value = '';
      inCcm.value = '';
      result.textContent = '';
      status.textContent = 'Nuovo r generato: completa i box e premi Verifica.';
      status.className = 'status';
      updateDrawingFromR(r);
      rProblem.textContent = r.toLocaleString('it-IT');
    }

    // Toggle steps
    btnSteps.addEventListener('click', () => {
      const open = steps.hasAttribute('hidden');
      if (open) { steps.removeAttribute('hidden'); btnSteps.setAttribute('aria-expanded','true'); btnSteps.textContent='Nascondi passaggi'; }
      else { steps.setAttribute('hidden',''); btnSteps.setAttribute('aria-expanded','false'); btnSteps.textContent='Mostra passaggi'; }
    });

    // Bottone π
    btnPi.addEventListener('click', () => { insertPi(); });

    // Events
    btnVerify.addEventListener('click', verify);
    btnReset.addEventListener('click', reset);
    btnNew.addEventListener('click', newProblem);

    inR.addEventListener('keydown', e=>{ if(e.key==='Enter') verify(); });
    inD.addEventListener('keydown', e=>{ if(e.key==='Enter') verify(); });

    inCpi.addEventListener('keydown', e=>{ if(e.key==='Enter') verify(); });
    inCcm.addEventListener('keydown', e=>{ if(e.key==='Enter') verify(); });

    inR.addEventListener('input', ()=>{ // live update drawing when r typed
      const r = parseFloat(inR.value.toString().replace(',','.'));
      if (!isNaN(r) && r>0) updateDrawingFromR(r);
    });

    // Init default state: r=5 cm, campi vuoti
    updateDrawingFromR(5);
    inR.value = '5';
    inCpi.value = '';
    inCcm.value = '';
    status.textContent = 'Scrivi C prima in π (es. 10π), poi in cm e premi Verifica.';
    status.className = 'status';
  </script>
</body>
</html>
