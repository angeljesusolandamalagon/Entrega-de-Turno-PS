<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>ICQA — Entrega de Turno | Mercado Libre</title>
<!--
  =====================================================
  APP: Entrega de Turno ICQA — Mercado Libre
  ÁREA: ICQA (Inventory Control & Quality Assurance)
  VERSIÓN: 1.0
  FECHA: Mayo 2026
  
  HISTORIAL DE CAMBIOS:
  v1.0 - Estructura base: 4 pasos, 4 áreas, 5 turnos
       - Producción con líneas NTB1, L1-L25, NTB2
       - Análisis IA con Claude API
       - Horarios: T1=6:00-15:30, T2=12:40-21:40,
                   T3=21:40-6:00, T4=9:00-19:00, T5=21:30-6:00

  ÁREAS DE OPORTUNIDAD / MEJORAS PENDIENTES:
  - [ ] Agregar aquí futuras mejoras identificadas
  =====================================================
-->
<style>
  :root {
    --yellow: #FFE600;
    --dark: #2C2C2A;
    --purple-bg: #EEEDFE;
    --purple-text: #3C3489;
    --purple-border: #AFA9EC;
    --purple-strong: #534AB7;
    --blue-bg: #E6F1FB;
    --blue-text: #0C447C;
    --blue-border: #85B7EB;
    --blue-strong: #185FA5;
    --pink-bg: #FBEAF0;
    --pink-text: #72243E;
    --pink-border: #ED93B1;
    --green-bg: #EAF3DE;
    --green-text: #3B6D11;
    --green-border: #97C459;
    --green-strong: #27500A;
    --teal-bg: #E1F5EE;
    --teal-text: #085041;
    --red-bg: #FCEBEB;
    --red-text: #A32D2D;
    --red-border: #F09595;
    --amber-bg: #FAEEDA;
    --amber-text: #854F0B;
    --amber-border: #EF9F27;
    --gray-bg: #F1EFE8;
    --gray-text: #444441;
    --border: #e0ddd6;
    --border-strong: #c8c5be;
    --bg: #ffffff;
    --bg-secondary: #f7f6f2;
    --text: #1a1a18;
    --text-secondary: #5f5e5a;
    --text-tertiary: #888780;
    --radius-md: 8px;
    --radius-lg: 12px;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif; font-size: 14px; background: var(--bg-secondary); color: var(--text); }
  .app { max-width: 680px; margin: 24px auto; background: var(--bg); border-radius: var(--radius-lg); border: 0.5px solid var(--border); overflow: hidden; }
  .topbar { background: var(--yellow); padding: 12px 18px; display: flex; align-items: center; justify-content: space-between; }
  .topbar-logo { font-size: 15px; font-weight: 600; color: var(--dark); }
  .topbar-sub { font-size: 11px; color: #444441; margin-top: 2px; }
  .topbar-badge { background: var(--dark); color: var(--yellow); font-size: 11px; padding: 4px 12px; border-radius: 20px; font-weight: 600; }
  .topbar-fecha { font-size: 11px; color: #444441; margin-top: 3px; text-align: right; }
  .container { padding: 18px; }
  .stepper { display: flex; margin-bottom: 20px; border: 0.5px solid var(--border); border-radius: var(--radius-md); overflow: hidden; }
  .step { flex: 1; padding: 9px 6px; text-align: center; font-size: 12px; color: var(--text-secondary); cursor: pointer; border-right: 0.5px solid var(--border); background: var(--bg); transition: all 0.15s; }
  .step:last-child { border-right: none; }
  .step.active { background: var(--yellow); color: var(--dark); font-weight: 600; }
  .step.done { background: var(--green-bg); color: var(--green-strong); }
  .section { display: none; }
  .section.visible { display: block; }
  label, .field-label { display: block; font-size: 12px; color: var(--text-secondary); margin-bottom: 5px; margin-top: 14px; }
  label:first-child, .field-label:first-child { margin-top: 0; }
  input[type=text], textarea, select {
    width: 100%; padding: 9px 12px; font-size: 13px; border: 0.5px solid var(--border-strong);
    border-radius: var(--radius-md); background: var(--bg); color: var(--text);
    font-family: inherit; outline: none; transition: border 0.15s;
  }
  input[type=text]:focus, textarea:focus { border-color: var(--blue-strong); }
  textarea { min-height: 72px; resize: vertical; }
  .turno-selector { display: grid; grid-template-columns: repeat(5, 1fr); gap: 6px; margin-top: 8px; }
  .turno-btn { padding: 8px 4px; text-align: center; font-size: 12px; line-height: 1.4; border: 0.5px solid var(--border); border-radius: var(--radius-md); cursor: pointer; background: var(--bg); color: var(--text-secondary); transition: all 0.15s; }
  .turno-btn:hover { background: var(--bg-secondary); }
  .turno-btn.sel { background: var(--purple-bg); color: var(--purple-text); border-color: var(--purple-border); font-weight: 600; }
  .area-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(140px, 1fr)); gap: 8px; margin-top: 8px; }
  .area-card { border: 0.5px solid var(--border); border-radius: var(--radius-md); padding: 10px 12px; cursor: pointer; background: var(--bg); transition: all 0.15s; }
  .area-card:hover { border-color: var(--border-strong); }
  .area-card.sel { border: 2px solid var(--blue-strong); background: var(--blue-bg); }
  .ac-name { font-size: 13px; font-weight: 600; color: var(--text); }
  .ac-sub { font-size: 11px; color: var(--text-secondary); margin-top: 2px; }
  .subarea-panel { border: 0.5px solid var(--border); border-radius: var(--radius-md); padding: 12px; margin-top: 10px; background: var(--bg-secondary); }
  .subarea-title { font-size: 12px; font-weight: 600; color: var(--text-secondary); margin-bottom: 8px; }
  .lineas-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(72px, 1fr)); gap: 5px; }
  .linea-btn { padding: 7px 4px; text-align: center; font-size: 12px; line-height: 1.3; border-radius: var(--radius-md); border: 0.5px solid var(--border); cursor: pointer; background: var(--bg); color: var(--text-secondary); transition: all 0.15s; }
  .linea-btn:hover { background: var(--bg-secondary); border-color: var(--border-strong); }
  .linea-btn.sel { background: var(--pink-bg); color: var(--pink-text); border-color: var(--pink-border); font-weight: 600; }
  .linea-btn.ntb { background: var(--purple-bg); color: var(--purple-text); border-color: var(--purple-border); }
  .linea-btn.ntb.sel { background: var(--purple-strong); color: #EEEDFE; border-color: var(--purple-text); }
  .prio-row { display: flex; gap: 6px; margin-top: 8px; }
  .prio-btn { flex: 1; padding: 8px 4px; text-align: center; font-size: 12px; border-radius: var(--radius-md); cursor: pointer; border: 0.5px solid var(--border); background: transparent; color: var(--text-secondary); transition: all 0.15s; }
  .prio-btn.p-alta.sel { background: var(--red-bg); color: var(--red-text); border-color: var(--red-border); }
  .prio-btn.p-media.sel { background: var(--amber-bg); color: var(--amber-text); border-color: var(--amber-border); }
  .prio-btn.p-baja.sel { background: var(--green-bg); color: var(--green-text); border-color: var(--green-border); }
  .add-btn { margin-top: 10px; width: 100%; padding: 9px; font-size: 13px; border-radius: var(--radius-md); border: 0.5px dashed var(--border-strong); background: transparent; color: var(--text-secondary); cursor: pointer; font-family: inherit; transition: background 0.15s; }
  .add-btn:hover { background: var(--bg-secondary); }
  .pending-list { margin-top: 12px; display: flex; flex-direction: column; gap: 6px; }
  .pending-item { border: 0.5px solid var(--border); border-radius: var(--radius-md); padding: 10px 12px; display: flex; align-items: flex-start; justify-content: space-between; gap: 8px; }
  .pi-content { flex: 1; }
  .pi-title { font-size: 13px; font-weight: 600; color: var(--text); }
  .pi-meta { font-size: 11px; color: var(--text-secondary); margin-top: 3px; }
  .pi-badge { font-size: 11px; padding: 2px 8px; border-radius: 20px; white-space: nowrap; display: inline-block; }
  .badge-row { display: flex; gap: 5px; flex-wrap: wrap; margin-bottom: 5px; }
  .del-btn { font-size: 12px; color: var(--text-tertiary); cursor: pointer; padding: 2px 7px; border-radius: 4px; border: none; background: transparent; transition: all 0.15s; }
  .del-btn:hover { color: var(--red-text); background: var(--red-bg); }
  .nav-row { display: flex; justify-content: space-between; margin-top: 20px; gap: 8px; }
  .btn { padding: 9px 20px; font-size: 13px; border-radius: var(--radius-md); cursor: pointer; border: 0.5px solid var(--border-strong); background: transparent; color: var(--text); font-family: inherit; transition: all 0.15s; }
  .btn:hover { background: var(--bg-secondary); }
  .btn.primary { background: var(--yellow); color: var(--dark); border-color: var(--yellow); font-weight: 600; }
  .btn.primary:hover { filter: brightness(0.95); }
  .btn.full { width: 100%; }
  .btn.outline-grid { flex: 1; }
  .metrics-row { display: grid; grid-template-columns: repeat(4, 1fr); gap: 8px; margin-bottom: 16px; }
  .metric { background: var(--bg-secondary); border-radius: var(--radius-md); padding: 10px; text-align: center; }
  .metric-n { font-size: 22px; font-weight: 600; color: var(--text); }
  .metric-l { font-size: 11px; color: var(--text-secondary); margin-top: 2px; }
  .ai-box { border: 0.5px solid var(--border); border-radius: var(--radius-lg); padding: 14px; margin-top: 0; background: var(--bg-secondary); }
  .ai-header { display: flex; align-items: center; gap: 8px; margin-bottom: 10px; }
  .ai-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--purple-strong); }
  .ai-label { font-size: 13px; font-weight: 600; color: var(--purple-text); }
  .ai-text { font-size: 13px; color: var(--text); line-height: 1.65; }
  .ai-loading { display: flex; gap: 4px; align-items: center; padding: 4px 0; }
  .dot { width: 6px; height: 6px; border-radius: 50%; background: var(--purple-border); animation: pulse 1s infinite; }
  .dot:nth-child(2) { animation-delay: 0.2s; }
  .dot:nth-child(3) { animation-delay: 0.4s; }
  @keyframes pulse { 0%,100%{opacity:0.3;} 50%{opacity:1;} }
  .success-icon { width: 52px; height: 52px; border-radius: 50%; background: var(--green-bg); margin: 0 auto 12px; display: flex; align-items: center; justify-content: center; }
  .summary-card { border: 0.5px solid var(--border); border-radius: var(--radius-md); padding: 14px; margin-bottom: 10px; background: var(--bg); }
  .summary-label { font-size: 11px; font-weight: 600; color: var(--text-secondary); margin-bottom: 8px; text-transform: uppercase; letter-spacing: 0.05em; }
  .summary-row { font-size: 13px; color: var(--text); line-height: 1.8; }
  .btn-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-top: 12px; }
  .empty-msg { font-size: 13px; color: var(--text-tertiary); text-align: center; padding: 14px; }
  .error-highlight { border-color: #E24B4A !important; }
</style>
</head>
<body>
<div class="app">
  <div class="topbar">
    <div>
      <div class="topbar-logo">ICQA — Entrega de turno</div>
      <div class="topbar-sub">Problem Solver · Mercado Libre</div>
    </div>
    <div style="text-align:right;">
      <div id="turno-display" class="topbar-badge">T1 — 6:00–15:30</div>
      <div class="topbar-fecha" id="fecha-display"></div>
    </div>
  </div>

  <div class="container">
    <div class="stepper">
      <div class="step active" onclick="goStep(0)">1. Identificación</div>
      <div class="step" onclick="goStep(1)">2. Pendientes</div>
      <div class="step" onclick="goStep(2)">3. Revisión IA</div>
      <div class="step" onclick="goStep(3)">4. Cierre</div>
    </div>

    <!-- PASO 1: IDENTIFICACIÓN -->
    <div class="section visible" id="s0">
      <label>Problem Solver (nombre)</label>
      <input type="text" id="ps-nombre" placeholder="Ej. Carlos Mendoza" />
      <label>Turno que entrega</label>
      <div class="turno-selector">
        <div class="turno-btn sel" onclick="selTurno(this,'T1 — 6:00–15:30')">T1<br><span style="font-size:10px;">6:00–15:30</span></div>
        <div class="turno-btn" onclick="selTurno(this,'T2 — 12:40–21:40')">T2<br><span style="font-size:10px;">12:40–21:40</span></div>
        <div class="turno-btn" onclick="selTurno(this,'T3 — 21:40–6:00')">T3<br><span style="font-size:10px;">21:40–6:00</span></div>
        <div class="turno-btn" onclick="selTurno(this,'T4 — 9:00–19:00')">T4<br><span style="font-size:10px;">9:00–19:00</span></div>
        <div class="turno-btn" onclick="selTurno(this,'T5 — 21:30–6:00')">T5<br><span style="font-size:10px;">21:30–6:00</span></div>
      </div>
      <label>Problem Solver que recibe</label>
      <input type="text" id="ps-recibe" placeholder="Ej. Ana Torres" />
      <label>Observación general del turno</label>
      <textarea id="obs-general" placeholder="Describe brevemente cómo estuvo el turno en general..."></textarea>
      <div class="nav-row">
        <div></div>
        <button class="btn primary" onclick="goStep(1)">Siguiente →</button>
      </div>
    </div>

    <!-- PASO 2: PENDIENTES -->
    <div class="section" id="s1">
      <label>Área del pendiente</label>
      <div class="area-grid">
        <div class="area-card sel" id="area-recibo" onclick="selArea(this,'Recibo')">
          <div class="ac-name">Recibo</div><div class="ac-sub">Logística entrada</div>
        </div>
        <div class="area-card" id="area-despacho" onclick="selArea(this,'Despacho')">
          <div class="ac-name">Despacho</div><div class="ac-sub">Logística salida</div>
        </div>
        <div class="area-card" id="area-check" onclick="selArea(this,'Check')">
          <div class="ac-name">Check</div><div class="ac-sub">Producción</div>
        </div>
        <div class="area-card" id="area-pick" onclick="selArea(this,'Pick')">
          <div class="ac-name">Pick</div><div class="ac-sub">Producción</div>
        </div>
      </div>

      <div id="prod-panel" style="display:none;">
        <div class="subarea-panel" id="subarea-panel">
          <div class="subarea-title" id="prod-panel-title">Selecciona la línea</div>
          <div class="lineas-grid" id="lineas-grid"></div>
        </div>
      </div>

      <label style="margin-top:16px;">Descripción del pendiente</label>
      <input type="text" id="pend-desc" placeholder="Describe el problema o tarea pendiente..." />
      <label>Prioridad</label>
      <div class="prio-row">
        <div class="prio-btn p-alta" onclick="selPrio(this,'Alta')">Alta</div>
        <div class="prio-btn p-media sel" onclick="selPrio(this,'Media')">Media</div>
        <div class="prio-btn p-baja" onclick="selPrio(this,'Baja')">Baja</div>
      </div>
      <label>Acción requerida por el siguiente turno</label>
      <textarea id="pend-accion" placeholder="Ej: Verificar discrepancia en SKU 4892-X, escalar con supervisor si persiste..." style="min-height:56px;"></textarea>
      <button class="add-btn" onclick="addPendiente()">+ Agregar pendiente a la lista</button>
      <div class="pending-list" id="pending-list"></div>
      <div class="nav-row">
        <button class="btn" onclick="goStep(0)">← Atrás</button>
        <button class="btn primary" onclick="goStep(2)">Analizar con IA →</button>
      </div>
    </div>

    <!-- PASO 3: REVISIÓN IA -->
    <div class="section" id="s2">
      <div class="metrics-row">
        <div class="metric"><div class="metric-n" id="m-total">0</div><div class="metric-l">Pendientes</div></div>
        <div class="metric"><div class="metric-n" id="m-alta" style="color:#A32D2D;">0</div><div class="metric-l">Alta prioridad</div></div>
        <div class="metric"><div class="metric-n" id="m-areas">0</div><div class="metric-l">Áreas/Líneas</div></div>
        <div class="metric"><div class="metric-n" id="m-acciones">0</div><div class="metric-l">Con acción</div></div>
      </div>
      <div class="ai-box">
        <div class="ai-header">
          <div class="ai-dot"></div>
          <div class="ai-label">Análisis IA — Asistente ICQA</div>
        </div>
        <div id="ai-content">
          <div class="ai-loading"><div class="dot"></div><div class="dot"></div><div class="dot"></div></div>
        </div>
      </div>
      <div class="nav-row">
        <button class="btn" onclick="goStep(1)">← Atrás</button>
        <button class="btn primary" onclick="goStep(3)">Confirmar y cerrar turno →</button>
      </div>
    </div>

    <!-- PASO 4: CIERRE -->
    <div class="section" id="s3">
      <div style="text-align:center;padding:20px 0 12px;">
        <div class="success-icon">
          <svg width="26" height="26" viewBox="0 0 24 24" fill="none">
            <path d="M5 13l4 4L19 7" stroke="#3B6D11" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
        <div style="font-size:16px;font-weight:600;color:var(--text);">Turno registrado correctamente</div>
        <div style="font-size:13px;color:var(--text-secondary);margin-top:4px;" id="cierre-sub"></div>
      </div>
      <div class="summary-card">
        <div class="summary-label">Resumen del registro</div>
        <div class="summary-row" id="resumen-final"></div>
      </div>
      <div class="btn-grid">
        <button class="btn outline-grid" onclick="imprimirResumen()">Imprimir resumen</button>
        <button class="btn outline-grid" onclick="copiarResumen()">Copiar para Sheets</button>
      </div>
      <div style="margin-top:8px;">
        <button class="btn primary full" onclick="resetApp()">Registrar nuevo turno</button>
      </div>
    </div>

  </div><!-- /container -->
</div><!-- /app -->

<script>
const TURNOS = [
  { label: 'T1 — 6:00–15:30',   hora: '6:00–15:30'   },
  { label: 'T2 — 12:40–21:40',  hora: '12:40–21:40'  },
  { label: 'T3 — 21:40–6:00',   hora: '21:40–6:00'   },
  { label: 'T4 — 9:00–19:00',   hora: '9:00–19:00'   },
  { label: 'T5 — 21:30–6:00',   hora: '21:30–6:00'   },
];

const PROD_AREAS = ['Check', 'Pick'];

let selectedArea  = 'Recibo';
let selectedLinea = null;
let selectedPrio  = 'Media';
let selectedTurno = TURNOS[0].label;
let pendientes    = [];

// Fecha actual
document.getElementById('fecha-display').textContent =
  new Date().toLocaleDateString('es-MX', { weekday:'long', day:'2-digit', month:'long', year:'numeric' });

// Build líneas grid
(function buildLineasGrid() {
  const grid  = document.getElementById('lineas-grid');
  const items = ['NTB 1', ...Array.from({length:25}, (_,i) => 'Línea '+(i+1)), 'NTB 2'];
  grid.innerHTML = items.map(item => {
    const isNtb = item.startsWith('NTB');
    return `<div class="linea-btn${isNtb?' ntb':''}" onclick="selLinea(this,'${item}')">${item}</div>`;
  }).join('');
})();

function goStep(n) {
  if (n === 2) buildAI();
  if (n === 3) buildCierre();
  document.querySelectorAll('.section').forEach((s,i) => s.classList.toggle('visible', i===n));
  document.querySelectorAll('.step').forEach((s,i) => {
    s.classList.remove('active','done');
    if (i===n)     s.classList.add('active');
    else if (i<n)  s.classList.add('done');
  });
}

function selTurno(el, label) {
  document.querySelectorAll('.turno-btn').forEach(b => b.classList.remove('sel'));
  el.classList.add('sel');
  selectedTurno = label;
  document.getElementById('turno-display').textContent = label;
}

function selArea(el, name) {
  document.querySelectorAll('.area-card').forEach(c => c.classList.remove('sel'));
  el.classList.add('sel');
  selectedArea  = name;
  selectedLinea = null;
  const panel = document.getElementById('prod-panel');
  if (PROD_AREAS.includes(name)) {
    panel.style.display = 'block';
    document.getElementById('prod-panel-title').textContent = `Línea de ${name}`;
    document.querySelectorAll('.linea-btn').forEach(b => b.classList.remove('sel'));
  } else {
    panel.style.display = 'none';
  }
}

function selLinea(el, linea) {
  document.querySelectorAll('.linea-btn').forEach(b => b.classList.remove('sel'));
  el.classList.add('sel');
  selectedLinea = linea;
}

function selPrio(el, p) {
  document.querySelectorAll('.prio-btn').forEach(b => b.classList.remove('sel'));
  el.classList.add('sel');
  selectedPrio = p;
}

function getAreaLabel() {
  return (PROD_AREAS.includes(selectedArea) && selectedLinea)
    ? `${selectedArea} — ${selectedLinea}`
    : selectedArea;
}

function addPendiente() {
  const desc = document.getElementById('pend-desc').value.trim();
  if (!desc) {
    document.getElementById('pend-desc').classList.add('error-highlight');
    setTimeout(() => document.getElementById('pend-desc').classList.remove('error-highlight'), 2000);
    return;
  }
  if (PROD_AREAS.includes(selectedArea) && !selectedLinea) {
    const sp = document.getElementById('subarea-panel');
    sp.classList.add('error-highlight');
    setTimeout(() => sp.classList.remove('error-highlight'), 2000);
    return;
  }
  document.getElementById('pend-desc').classList.remove('error-highlight');
  const accion = document.getElementById('pend-accion').value.trim();
  pendientes.push({
    area: selectedArea, linea: selectedLinea, label: getAreaLabel(),
    desc, prio: selectedPrio, accion, id: Date.now(),
    timestamp: new Date().toLocaleTimeString('es-MX', {hour:'2-digit', minute:'2-digit'})
  });
  document.getElementById('pend-desc').value  = '';
  document.getElementById('pend-accion').value = '';
  renderPendientes();
}

const colorArea = {
  Recibo:   'background:#E6F1FB;color:#0C447C;',
  Despacho: 'background:#EEEDFE;color:#3C3489;',
  Check:    'background:#FBEAF0;color:#72243E;',
  Pick:     'background:#E1F5EE;color:#085041;',
};
const colorPrio = {
  Alta:  'background:#FCEBEB;color:#A32D2D;',
  Media: 'background:#FAEEDA;color:#854F0B;',
  Baja:  'background:#EAF3DE;color:#3B6D11;',
};

function renderPendientes() {
  const el = document.getElementById('pending-list');
  if (!pendientes.length) {
    el.innerHTML = '<div class="empty-msg">Sin pendientes agregados aún</div>';
    return;
  }
  el.innerHTML = pendientes.map(p => `
    <div class="pending-item">
      <div class="pi-content">
        <div class="badge-row">
          <span class="pi-badge" style="${colorArea[p.area]||''}">${p.label}</span>
          <span class="pi-badge" style="${colorPrio[p.prio]||''}">${p.prio}</span>
          <span class="pi-badge" style="background:#F1EFE8;color:#5F5E5A;">${p.timestamp}</span>
        </div>
        <div class="pi-title">${p.desc}</div>
        ${p.accion ? `<div class="pi-meta">Acción: ${p.accion}</div>` : ''}
      </div>
      <button class="del-btn" onclick="removePendiente(${p.id})">✕</button>
    </div>`).join('');
}

function removePendiente(id) {
  pendientes = pendientes.filter(p => p.id !== id);
  renderPendientes();
}

function buildAI() {
  const total     = pendientes.length;
  const alta      = pendientes.filter(p => p.prio === 'Alta').length;
  const areas     = [...new Set(pendientes.map(p => p.label))];
  const conAccion = pendientes.filter(p => p.accion).length;
  document.getElementById('m-total').textContent    = total;
  document.getElementById('m-alta').textContent     = alta;
  document.getElementById('m-areas').textContent    = areas.length;
  document.getElementById('m-acciones').textContent = conAccion;

  const ps     = document.getElementById('ps-nombre').value || 'el PS';
  const recibe = document.getElementById('ps-recibe').value || 'el siguiente turno';

  if (!total) {
    document.getElementById('ai-content').innerHTML =
      `<div class="ai-text">No se registraron pendientes para este turno. Se recomienda confirmar verbalmente con ${recibe} antes de retirarse.</div>`;
    return;
  }

  document.getElementById('ai-content').innerHTML =
    '<div class="ai-loading"><div class="dot"></div><div class="dot"></div><div class="dot"></div></div>';

  const prompt = `Eres el asistente de entrega de turno del área ICQA (Inventory Control and Quality Assurance) de Mercado Libre México.
El PS "${ps}" del turno "${selectedTurno}" entrega a "${recibe}".

Pendientes registrados:
${pendientes.map((p,i) => `${i+1}. [${p.label}] [Prioridad ${p.prio}] ${p.desc}${p.accion ? ' — Acción requerida: '+p.accion : ''}`).join('\n')}

Genera un análisis conciso (máximo 4 oraciones) con: estado general del turno, qué debe atender PRIMERO el turno entrante, y qué riesgo operativo existe si algún pendiente no se atiende a tiempo. Usa lenguaje operativo, directo y profesional. Sin títulos ni bullets, solo párrafo fluido.`;

  fetch('https://api.anthropic.com/v1/messages', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({
      model: 'claude-sonnet-4-20250514',
      max_tokens: 1000,
      messages: [{ role: 'user', content: prompt }]
    })
  })
  .then(r => r.json())
  .then(data => {
    const text = data.content?.filter(b => b.type==='text').map(b => b.text).join('') || 'Análisis no disponible.';
    document.getElementById('ai-content').innerHTML = `<div class="ai-text">${text}</div>`;
  })
  .catch(() => {
    const fb = alta > 0
      ? `Se detectaron ${alta} pendiente(s) de alta prioridad en ${areas.slice(0,3).join(', ')}. El turno entrante debe atenderlos de inmediato para evitar bloqueos operativos. Se recomienda escalar a supervisor si no se resuelven en los primeros 30 minutos.`
      : `Turno con ${total} pendiente(s) de prioridad media/baja distribuidos en ${areas.join(', ')}. Sin riesgos críticos inmediatos — revisar y dar seguimiento ordenado por área.`;
    document.getElementById('ai-content').innerHTML = `<div class="ai-text">${fb}</div>`;
  });
}

function buildCierre() {
  const ps     = document.getElementById('ps-nombre').value  || '—';
  const recibe = document.getElementById('ps-recibe').value  || '—';
  const obs    = document.getElementById('obs-general').value || 'Sin observaciones generales.';
  const fecha  = new Date().toLocaleString('es-MX', { day:'2-digit', month:'short', year:'numeric', hour:'2-digit', minute:'2-digit' });
  document.getElementById('cierre-sub').textContent = `${selectedTurno} · ${fecha}`;
  const lineas  = [...new Set(pendientes.filter(p => p.linea).map(p => p.label))];
  const logistica = [...new Set(pendientes.filter(p => !PROD_AREAS.includes(p.area)).map(p => p.area))];
  document.getElementById('resumen-final').innerHTML = `
    <b>Turno:</b> ${selectedTurno}<br>
    <b>PS entrega:</b> ${ps}<br>
    <b>PS recibe:</b> ${recibe}<br>
    <b>Fecha/hora:</b> ${fecha}<br>
    <b>Total pendientes:</b> ${pendientes.length}<br>
    <b>Alta prioridad:</b> ${pendientes.filter(p=>p.prio==='Alta').length}<br>
    <b>Líneas afectadas:</b> ${lineas.length ? lineas.join(', ') : 'Ninguna'}<br>
    <b>Áreas logística:</b> ${logistica.length ? logistica.join(', ') : 'Ninguna'}<br>
    <b>Observación:</b> ${obs}
  `;
}

function imprimirResumen() { window.print(); }

function copiarResumen() {
  const ps     = document.getElementById('ps-nombre').value  || '—';
  const recibe = document.getElementById('ps-recibe').value  || '—';
  const fecha  = new Date().toLocaleString('es-MX', { day:'2-digit', month:'short', year:'numeric', hour:'2-digit', minute:'2-digit' });
  let txt = `ENTREGA DE TURNO ICQA — ${selectedTurno}\nFecha: ${fecha}\nPS entrega: ${ps} → PS recibe: ${recibe}\n\nPENDIENTES:\n`;
  pendientes.forEach((p,i) => {
    txt += `${i+1}. [${p.label}] [${p.prio}] ${p.desc}`;
    if (p.accion) txt += `\n   Acción: ${p.accion}`;
    txt += '\n';
  });
  navigator.clipboard?.writeText(txt).then(() => alert('Copiado al portapapeles. Pega directamente en Google Sheets.'));
}

function resetApp() {
  pendientes = [];
  ['ps-nombre','ps-recibe','obs-general','pend-desc','pend-accion'].forEach(id => document.getElementById(id).value = '');
  selectedLinea = null;
  document.getElementById('prod-panel').style.display = 'none';
  document.querySelectorAll('.linea-btn').forEach(b => b.classList.remove('sel'));
  document.querySelectorAll('.area-card').forEach(c => c.classList.remove('sel'));
  document.getElementById('area-recibo').classList.add('sel');
  selectedArea = 'Recibo';
  renderPendientes();
  goStep(0);
}

renderPendientes();
</script>
</body>
</html>
