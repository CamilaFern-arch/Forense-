<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CV Administración — Camila F. Azola Garaventa</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --cream: #F7F4EF;
    --warm-white: #FDFBF8;
    --ink: #1A1714;
    --muted: #6B6560;
    --accent: #8B6F47;
    --accent-light: #C4A882;
    --rule: #D9D0C4;
    --sidebar-bg: #1A1714;
    --sidebar-text: #F7F4EF;
    --sidebar-muted: #A09890;
    --tag-bg: #EDE8E0;
  }

  @media print {
    body { -webkit-print-color-adjust: exact; print-color-adjust: exact; }
    .page { box-shadow: none; margin: 0; max-width: 100%; }
  }

  body {
    font-family: 'DM Sans', sans-serif;
    background: #E8E2D9;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding: 40px 20px;
  }

  .page {
    display: grid;
    grid-template-columns: 260px 1fr;
    max-width: 900px;
    width: 100%;
    background: var(--warm-white);
    box-shadow: 0 20px 60px rgba(0,0,0,0.18), 0 4px 16px rgba(0,0,0,0.1);
    min-height: 1100px;
  }

  /* ── SIDEBAR ── */
  .sidebar {
    background: var(--sidebar-bg);
    padding: 44px 28px;
    display: flex;
    flex-direction: column;
    gap: 36px;
  }

  .photo-wrap {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    overflow: hidden;
    border: 3px solid var(--accent-light);
    margin: 0 auto 4px;
  }
  .photo-wrap img { width: 100%; height: 100%; object-fit: cover; }

  .name-block { text-align: center; }
  .name-first {
    font-family: 'Cormorant Garamond', serif;
    font-weight: 300;
    font-size: 22px;
    color: var(--sidebar-text);
    letter-spacing: 0.08em;
    line-height: 1.2;
  }
  .name-last {
    font-family: 'Cormorant Garamond', serif;
    font-weight: 600;
    font-size: 22px;
    color: var(--accent-light);
    letter-spacing: 0.08em;
    line-height: 1.2;
  }
  .role-tag {
    margin-top: 10px;
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--sidebar-muted);
    border-top: 1px solid #333;
    padding-top: 10px;
  }

  .s-section { display: flex; flex-direction: column; gap: 10px; }
  .s-label {
    font-size: 9px;
    font-weight: 500;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--accent-light);
    border-bottom: 1px solid #333;
    padding-bottom: 6px;
    margin-bottom: 2px;
  }

  .contact-item {
    display: flex;
    align-items: flex-start;
    gap: 8px;
    font-size: 11.5px;
    color: var(--sidebar-muted);
    line-height: 1.5;
  }
  .contact-icon { color: var(--accent-light); flex-shrink: 0; margin-top: 2px; font-size: 12px; }

  .skill-item {
    font-size: 11px;
    color: var(--sidebar-text);
    padding: 5px 10px;
    background: rgba(255,255,255,0.06);
    border-left: 2px solid var(--accent);
    line-height: 1.4;
  }

  .edu-item { margin-bottom: 10px; }
  .edu-title { font-size: 11.5px; color: var(--sidebar-text); font-weight: 500; line-height: 1.4; }
  .edu-place { font-size: 10.5px; color: var(--sidebar-muted); line-height: 1.4; }

  .lang-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 11px;
    color: var(--sidebar-text);
    margin-bottom: 4px;
  }
  .lang-dots { display: flex; gap: 3px; }
  .dot { width: 7px; height: 7px; border-radius: 50%; background: #333; }
  .dot.on { background: var(--accent-light); }

  /* ── MAIN ── */
  .main {
    padding: 44px 40px;
    display: flex;
    flex-direction: column;
    gap: 28px;
  }

  .main-header {
    border-bottom: 2px solid var(--ink);
    padding-bottom: 16px;
  }
  .main-role {
    font-family: 'Cormorant Garamond', serif;
    font-size: 11px;
    font-weight: 400;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 6px;
  }
  .main-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 32px;
    font-weight: 300;
    color: var(--ink);
    line-height: 1.1;
    letter-spacing: -0.01em;
  }
  .main-title span { font-weight: 600; }

  .profile-text {
    font-size: 12.5px;
    color: var(--muted);
    line-height: 1.75;
    font-weight: 300;
    border-left: 3px solid var(--accent-light);
    padding-left: 14px;
  }

  .section-title {
    font-size: 9px;
    font-weight: 500;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--rule);
  }

  .exp-item { margin-bottom: 20px; }
  .exp-header { display: flex; justify-content: space-between; align-items: flex-start; margin-bottom: 3px; }
  .exp-company {
    font-family: 'Cormorant Garamond', serif;
    font-size: 16px;
    font-weight: 600;
    color: var(--ink);
    line-height: 1.2;
  }
  .exp-date {
    font-size: 10px;
    color: var(--muted);
    font-weight: 400;
    letter-spacing: 0.05em;
    white-space: nowrap;
    margin-left: 10px;
    margin-top: 3px;
  }
  .exp-role {
    font-size: 10.5px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 8px;
  }
  .exp-bullets { list-style: none; padding: 0; }
  .exp-bullets li {
    font-size: 12px;
    color: var(--muted);
    line-height: 1.65;
    padding-left: 14px;
    position: relative;
    margin-bottom: 2px;
  }
  .exp-bullets li::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--accent-light);
    font-size: 10px;
    top: 3px;
  }

  .tags-row { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 6px; }
  .tag {
    font-size: 9.5px;
    font-weight: 500;
    letter-spacing: 0.08em;
    padding: 3px 9px;
    background: var(--tag-bg);
    color: var(--accent);
    border-radius: 2px;
  }

  .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }

  .mini-exp { padding: 12px 14px; border: 1px solid var(--rule); border-left: 3px solid var(--accent-light); }
  .mini-company { font-size: 12.5px; font-weight: 500; color: var(--ink); }
  .mini-role-text { font-size: 10px; color: var(--accent); text-transform: uppercase; letter-spacing: 0.08em; }
  .mini-date { font-size: 10px; color: var(--muted); margin-bottom: 4px; }
  .mini-bullets { list-style: none; }
  .mini-bullets li { font-size: 11px; color: var(--muted); padding-left: 10px; position: relative; line-height: 1.55; }
  .mini-bullets li::before { content: '·'; position: absolute; left: 2px; color: var(--accent); font-weight: 700; }
</style>
</head>
<body>
<div class="page">

  <!-- SIDEBAR -->
  <aside class="sidebar">

    <div>
      <div class="name-block">
        <div class="name-first">Camila Fernanda</div>
        <div class="name-last">Azola Garaventa</div>
        <div class="role-tag">Asistente Administrativa &amp; Coordinadora</div>
      </div>
    </div>

    <div class="s-section">
      <div class="s-label">Contacto</div>
      <div class="contact-item"><span class="contact-icon">✉</span> camilafern.ag@gmail.com</div>
      <div class="contact-item"><span class="contact-icon">✆</span> +34 662 467 425</div>
      <div class="contact-item"><span class="contact-icon">◎</span> Barcelona, España</div>
    </div>

    <div class="s-section">
      <div class="s-label">Habilidades Clave</div>
      <div class="skill-item">Gestión de agenda y documentación</div>
      <div class="skill-item">Apoyo administrativo general</div>
      <div class="skill-item">Control de inventario y stock</div>
      <div class="skill-item">Atención al cliente y recepción</div>
      <div class="skill-item">Coordinación de equipos</div>
      <div class="skill-item">Resolución de incidencias</div>
      <div class="skill-item">Excel básico / medio</div>
      <div class="skill-item">Entornos de alta exigencia</div>
    </div>

    <div class="s-section">
      <div class="s-label">Herramientas</div>
      <div class="skill-item">Microsoft Office (Word, Excel)</div>
      <div class="skill-item">Google Workspace</div>
      <div class="skill-item">Gestión de caja y TPV</div>
    </div>

    <div class="s-section">
      <div class="s-label">Formación</div>
      <div class="edu-item">
        <div class="edu-title">Marketing & Publicidad + Gestión de Proyectos</div>
        <div class="edu-place">En curso · 2025–2026</div>
      </div>
      <div class="edu-item">
        <div class="edu-title">Turismo y Hotelería</div>
        <div class="edu-place">CFT PUCV · Chile</div>
      </div>
      <div class="edu-item">
        <div class="edu-title">Bachillerato</div>
        <div class="edu-place">Liceo N°1 de Niñas · Valparaíso</div>
      </div>
    </div>

    <div class="s-section">
      <div class="s-label">Idiomas</div>
      <div class="lang-item">
        <span>Español</span>
        <div class="lang-dots">
          <div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div><div class="dot on"></div>
        </div>
      </div>
      <div class="lang-item">
        <span>Inglés básico</span>
        <div class="lang-dots">
          <div class="dot on"></div><div class="dot on"></div><div class="dot"></div><div class="dot"></div><div class="dot"></div>
        </div>
      </div>
    </div>

  </aside>

  <!-- MAIN -->
  <main class="main">

    <div class="main-header">
      <div class="main-role">Asistente Administrativa · Coordinadora de Operaciones</div>
      <div class="main-title">Organización.<br><span>Precisión. Resultado.</span></div>
    </div>

    <div>
      <p class="profile-text">
        Profesional con más de 8 años de experiencia real en coordinación operativa, control administrativo y atención al cliente en entornos de alta exigencia. He gestionado agendas, inventarios, documentación y flujos de trabajo en proyectos de gran escala, desarrollando un perfil metódico, orientado al detalle y con alta capacidad de adaptación. Actualmente en formación en Marketing y Gestión de Proyectos, en búsqueda de incorporarme a un equipo administrativo en Barcelona donde aportar rigor, autonomía y compromiso desde el primer día.
      </p>
    </div>

    <!-- EXPERIENCIA PRINCIPAL -->
    <div>
      <div class="section-title">Experiencia Relevante</div>

      <div class="exp-item">
        <div class="exp-header">
          <div class="exp-company">LDZ Constructora</div>
          <div class="exp-date">2017 – 2019 · Chile</div>
        </div>
        <div class="exp-role">Responsable de Control de Calidad y Post Venta</div>
        <ul class="exp-bullets">
          <li>Coordinación de equipos multidisciplinares en 3 proyectos de alto estándar (Mandarin Oriental, Hotel Pullman, 45 By Director), asegurando el cumplimiento de deadlines críticos de entrega.</li>
          <li>Control y gestión del inventario de bodega: registro de entradas/salidas de materiales, control de stock y optimización del espacio operativo.</li>
          <li>Supervisión de calidad en fases finales de obra: detección, documentación y seguimiento de incidencias hasta su resolución.</li>
          <li>Coordinación de la fase de post-venta con clientes: atención de requerimientos, gestión de agenda de visitas y resolución de incidencias en plazo.</li>
        </ul>
        <div class="tags-row">
          <span class="tag">Gestión documental</span>
          <span class="tag">Control de inventario</span>
          <span class="tag">Coordinación de agenda</span>
          <span class="tag">Seguimiento de incidencias</span>
          <span class="tag">Atención al cliente</span>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-header">
          <div class="exp-company">Clínica Médica Sermeda</div>
          <div class="exp-date">2017 · Chile</div>
        </div>
        <div class="exp-role">Recepcionista / Apoyo Administrativo</div>
        <ul class="exp-bullets">
          <li>Gestión de agenda médica: coordinación de citas, priorización de pacientes y comunicación con el equipo clínico.</li>
          <li>Atención presencial y telefónica al público, resolución de dudas y orientación de usuarios.</li>
          <li>Soporte administrativo general: archivo documental, facturación básica y mantenimiento del orden operativo del área de recepción.</li>
        </ul>
        <div class="tags-row">
          <span class="tag">Recepción</span>
          <span class="tag">Gestión de agenda</span>
          <span class="tag">Archivo documental</span>
          <span class="tag">Apoyo administrativo</span>
        </div>
      </div>

      <div class="exp-item">
        <div class="exp-header">
          <div class="exp-company">Walmart Líder Chile</div>
          <div class="exp-date">2020 · Chile</div>
        </div>
        <div class="exp-role">Cajera / Atención al Cliente / Apoyo a Jefatura</div>
        <ul class="exp-bullets">
          <li>Manejo de caja, medios de pago y cuadre diario de efectivo con responsabilidad directa.</li>
          <li>Apoyo a jefatura en tareas administrativas: control de inventario, reposición de stock y reporte de incidencias.</li>
          <li>Resolución de dudas y reclamaciones de clientes, manteniendo estándares de servicio en entorno de alta afluencia.</li>
        </ul>
        <div class="tags-row">
          <span class="tag">Control de stock</span>
          <span class="tag">Apoyo a dirección</span>
          <span class="tag">Gestión de caja</span>
          <span class="tag">Atención al cliente</span>
        </div>
      </div>
    </div>

    <!-- EXPERIENCIA ADICIONAL -->
    <div>
      <div class="section-title">Experiencia Complementaria</div>
      <div class="two-col">
        <div class="mini-exp">
          <div class="mini-company">Constructora Paz</div>
          <div class="mini-role-text">Control de Calidad</div>
          <div class="mini-date">2015 – 2016 · Chile</div>
          <ul class="mini-bullets">
            <li>Control de calidad y revisión de terminaciones en proyectos residenciales (Reñaca y Concón).</li>
            <li>Organización administrativa del área operativa y contribución al cumplimiento de plazos.</li>
          </ul>
        </div>
        <div class="mini-exp">
          <div class="mini-company">Tabaquería Wolff</div>
          <div class="mini-role-text">Vendedora / Control de Inventario</div>
          <div class="mini-date">2021 – 2022 · Chile</div>
          <ul class="mini-bullets">
            <li>Gestión de stock, reposición y control de inventario en punto de venta.</li>
            <li>Atención personalizada y asesoramiento de producto.</li>
          </ul>
        </div>
        <div class="mini-exp">
          <div class="mini-company">Atención Adulto Mayor – España</div>
          <div class="mini-role-text">Cuidadora / Coordinación de Rutinas</div>
          <div class="mini-date">2024 – 2026 · Barcelona</div>
          <ul class="mini-bullets">
            <li>Organización del hogar, gestión de rutinas y acompañamiento diario.</li>
            <li>Alta responsabilidad autónoma y desarrollo de empatía interpersonal.</li>
          </ul>
        </div>
        <div class="mini-exp">
          <div class="mini-company">Adidas Outlet Placilla</div>
          <div class="mini-role-text">Cajera / Apoyo en Ventas</div>
          <div class="mini-date">2023 · Chile</div>
          <ul class="mini-bullets">
            <li>Atención al cliente, gestión de caja y presentación visual del punto de venta.</li>
          </ul>
        </div>
      </div>
    </div>

  </main>
</div>
</body>
</html>
