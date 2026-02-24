[index.html](https://github.com/user-attachments/files/25532737/index.html)
<!doctype html>
<html lang="es-MX">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Tapo by TP-Link | Programa para ISPs</title>
  <meta name="description" content="Página para ISPs: vende y distribuye TP-Link Tapo a tus clientes cautivos con bundles, instalación y monitoreo desde app." />
  <style>
    :root{
      --bg:#0b1220;
      --card:#101a30;
      --muted:#8ea0c6;
      --text:#eaf0ff;
      --brand:#35c7ff;
      --brand2:#7cffc4;
      --border:rgba(255,255,255,.10);
      --shadow: 0 18px 50px rgba(0,0,0,.35);
      --radius:18px;
    }
    *{box-sizing:border-box}
    body{
      margin:0; font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Noto Sans", "Apple Color Emoji","Segoe UI Emoji";
      background: radial-gradient(1200px 700px at 10% 10%, rgba(53,199,255,.20), transparent 55%),
                  radial-gradient(1200px 700px at 80% 30%, rgba(124,255,196,.12), transparent 60%),
                  linear-gradient(180deg, #070c16, var(--bg));
      color:var(--text);
    }
    a{color:inherit; text-decoration:none}
    .wrap{max-width:1180px; margin:0 auto; padding:0 18px}
    header{
      position:sticky; top:0; z-index:10;
      backdrop-filter: blur(10px);
      background: rgba(7,12,22,.55);
      border-bottom:1px solid var(--border);
    }
    .nav{
      display:flex; align-items:center; justify-content:space-between;
      padding:14px 0;
    }
    .brand{
      display:flex; gap:10px; align-items:center; font-weight:700; letter-spacing:.2px;
    }
    .logo{
      width:36px; height:36px; border-radius:12px;
      background: linear-gradient(135deg, var(--brand), var(--brand2));
      box-shadow: 0 12px 30px rgba(53,199,255,.15);
    }
    .navlinks{display:flex; gap:14px; flex-wrap:wrap; align-items:center}
    .navlinks a{
      padding:8px 10px; border-radius:12px; color:var(--muted);
      border:1px solid transparent;
    }
    .navlinks a:hover{color:var(--text); border-color:var(--border); background:rgba(255,255,255,.03)}
    .btn{
      display:inline-flex; align-items:center; gap:10px;
      padding:11px 14px;
      border-radius:14px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.04);
      color:var(--text);
      box-shadow:none;
      cursor:pointer;
      transition: transform .12s ease, background .12s ease, border-color .12s ease;
      white-space:nowrap;
    }
    .btn:hover{transform: translateY(-1px); background: rgba(255,255,255,.07); border-color: rgba(53,199,255,.35)}
    .btn.primary{
      border-color: rgba(53,199,255,.55);
      background: linear-gradient(135deg, rgba(53,199,255,.18), rgba(124,255,196,.10));
    }

    /* HERO */
    .hero{padding:34px 0 10px}
    .heroGrid{
      display:grid; gap:18px;
      grid-template-columns: 1.25fr .75fr;
      align-items:stretch;
    }
    @media (max-width: 980px){
      .heroGrid{grid-template-columns:1fr}
    }
    .heroCard{
      border:1px solid var(--border);
      background: linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02));
      border-radius: var(--radius);
      padding:24px;
      box-shadow: var(--shadow);
      position:relative;
      overflow:hidden;
    }
    .kicker{
      display:inline-flex; gap:10px; align-items:center;
      padding:7px 10px; border-radius:999px;
      border:1px solid rgba(53,199,255,.35);
      color: #cfefff;
      background: rgba(53,199,255,.08);
      font-size:13px;
    }
    h1{margin:14px 0 10px; font-size:42px; line-height:1.05}
    @media (max-width: 560px){ h1{font-size:34px} }
    .sub{
      margin:0; color:var(--muted); font-size:16px; line-height:1.6; max-width:70ch;
    }
    .heroActions{display:flex; gap:10px; flex-wrap:wrap; margin-top:16px}
    .badges{display:flex; gap:10px; flex-wrap:wrap; margin-top:16px}
    .badge{
      font-size:13px; color:var(--muted);
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      padding:8px 10px; border-radius:999px;
    }
    .sideCard{
      border:1px solid var(--border);
      background: rgba(16,26,48,.55);
      border-radius: var(--radius);
      padding:18px;
      box-shadow: var(--shadow);
      display:flex; flex-direction:column; gap:12px;
    }
    .sideTitle{font-weight:700}
    .sideList{margin:0; padding-left:18px; color:var(--muted); line-height:1.6}
    .sideList li{margin:6px 0}

    /* SECTIONS */
    section{padding:22px 0}
    .sectionHead{
      display:flex; align-items:flex-end; justify-content:space-between; gap:12px; flex-wrap:wrap;
      margin-bottom:12px;
    }
    .sectionHead h2{margin:0; font-size:22px}
    .sectionHead p{margin:0; color:var(--muted)}
    .grid{
      display:grid; gap:14px;
      grid-template-columns: repeat(12, 1fr);
    }
    .col-4{grid-column: span 4}
    .col-6{grid-column: span 6}
    .col-12{grid-column: span 12}
    @media (max-width: 980px){
      .col-4,.col-6{grid-column: span 12}
    }
    .card{
      border:1px solid var(--border);
      background: rgba(16,26,48,.55);
      border-radius: var(--radius);
      padding:16px;
      box-shadow: var(--shadow);
    }
    .card h3{margin:0 0 6px; font-size:16px}
    .card p{margin:0; color:var(--muted); line-height:1.55}
    .mini{font-size:13px; color:var(--muted)}
    .chipRow{display:flex; gap:8px; flex-wrap:wrap; margin-top:10px}
    .chip{
      font-size:12px; padding:6px 8px; border-radius:999px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      color:var(--muted);
    }

    /* CATALOG */
    .toolbar{
      display:flex; gap:10px; flex-wrap:wrap; align-items:center; justify-content:space-between;
      margin: 10px 0 12px;
    }
    .filters{display:flex; gap:8px; flex-wrap:wrap; align-items:center}
    .pill{
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      padding:8px 10px; border-radius:999px;
      color:var(--muted);
      cursor:pointer;
      user-select:none;
    }
    .pill.active{
      color:var(--text);
      border-color: rgba(53,199,255,.45);
      background: rgba(53,199,255,.10);
    }
    .search{
      display:flex; align-items:center; gap:8px;
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      padding:10px 12px; border-radius:14px;
      min-width: 260px;
    }
    .search input{
      width:100%;
      background:transparent; border:0; outline:0;
      color:var(--text); font-size:14px;
    }
    .catalog{
      display:grid; gap:14px;
      grid-template-columns: repeat(12, 1fr);
    }
    .product{
      grid-column: span 4;
      border:1px solid var(--border);
      background: rgba(16,26,48,.55);
      border-radius: var(--radius);
      padding:14px;
      box-shadow: var(--shadow);
      display:flex; flex-direction:column; gap:10px;
      min-height: 210px;
    }
    @media (max-width: 980px){ .product{grid-column: span 6} }
    @media (max-width: 560px){ .product{grid-column: span 12} }
    .productTop{
      display:flex; align-items:flex-start; justify-content:space-between; gap:10px;
    }
    .tag{
      font-size:12px; padding:6px 8px; border-radius:999px;
      border:1px solid rgba(53,199,255,.35);
      background: rgba(53,199,255,.08);
      color:#cfefff;
      white-space:nowrap;
    }
    .prodName{margin:0; font-weight:700}
    .prodDesc{margin:0; color:var(--muted); line-height:1.55; font-size:14px}
    .prodBullets{margin:0; padding-left:18px; color:var(--muted); line-height:1.5; font-size:13px}
    .prodActions{margin-top:auto; display:flex; gap:10px; flex-wrap:wrap}
    .link{
      display:inline-flex; align-items:center; gap:8px;
      color:#cfefff;
      padding:10px 12px;
      border-radius:14px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(255,255,255,.03);
    }
    .link:hover{border-color: rgba(53,199,255,.35); background: rgba(255,255,255,.06)}
    .mutedLink{color:var(--muted)}

    /* BUNDLES */
    .bundle{
      border:1px solid rgba(124,255,196,.25);
      background: linear-gradient(180deg, rgba(124,255,196,.10), rgba(16,26,48,.55));
    }

    /* FOOTER */
    footer{
      border-top:1px solid var(--border);
      padding:24px 0 34px;
      color:var(--muted);
    }
    .footerGrid{
      display:grid; gap:14px;
      grid-template-columns: 1.1fr .9fr;
      align-items:start;
    }
    @media (max-width: 980px){ .footerGrid{grid-template-columns:1fr} }
    .form{
      display:grid; gap:10px;
      grid-template-columns: repeat(12, 1fr);
    }
    .field{grid-column: span 6}
    .field.full{grid-column: span 12}
    .form input, .form textarea, .form select{
      width:100%;
      border:1px solid var(--border);
      background: rgba(255,255,255,.03);
      color:var(--text);
      border-radius: 14px;
      padding: 11px 12px;
      outline:0;
      font-size:14px;
    }
    .form textarea{min-height:100px; resize:vertical}
    .note{font-size:12px; color:var(--muted); line-height:1.5}
    .smallCaps{font-size:12px; letter-spacing:.12em; text-transform:uppercase; color:var(--muted)}
  </style>
</head>

<body>
<header>
  <div class="wrap">
    <div class="nav">
      <div class="brand">
        <div class="logo" aria-hidden="true"></div>
        <div>
          <div style="line-height:1.1">Tapo <span class="mutedLink">by TP-Link</span></div>
          <div class="mini">Programa para ISPs</div>
        </div>
      </div>

      <nav class="navlinks" aria-label="Navegación">
        <a href="#beneficios">Beneficios</a>
        <a href="#catalogo">Catálogo</a>
        <a href="#bundles">Bundles</a>
        <a href="#implementacion">Implementación</a>
        <a class="btn primary" href="#contacto">Quiero ser distribuidor</a>
      </nav>
    </div>
  </div>
</header>

<main>
  <div class="wrap hero">
    <div class="heroGrid">
      <div class="heroCard">
        <div class="kicker">✅ Incrementa ARPU • Reduce churn • Upsell inmediato</div>
        <h1>Vende Tapo a tus <span style="color:var(--brand)">clientes cautivos</span> como un servicio.</h1>
        <p class="sub">
          Con Tapo puedes ofrecer seguridad y hogar inteligente (cámaras, timbres, sensores, enchufes, focos, etc.)
          como venta directa o como <b>add-on mensual</b>. Ideal para ISPs con FTTH/WISP y PyME.
        </p>
        <div class="heroActions">
          <a class="btn primary" href="#catalogo">Ver productos Tapo</a>
          <a class="btn" href="#bundles">Ver bundles para ISP</a>
          <a class="btn" href="#contacto">Cotizar / Kit demo</a>
        </div>
        <div class="badges">
          <div class="badge">📦 Entrega e instalación opcional</div>
          <div class="badge">📱 App Tapo (control local/remoto)</div>
          <div class="badge">🏠 Hogar / Negocio / Oficinas</div>
        </div>
      </div>

      <aside class="sideCard">
        <div class="sideTitle">Cómo gana el ISP</div>
        <ul class="sideList">
          <li><b>Upsell</b> a base instalada (0 CAC)</li>
          <li><b>Bundles</b> por nivel de plan (Silver/Gold/Pro)</li>
          <li><b>Instalación</b> como servicio (margen adicional)</li>
          <li><b>Menos churn</b> al amarrar ecosistema en el hogar</li>
          <li><b>Soporte</b> estandarizado con guías y kits</li>
        </ul>
        <div class="card" style="margin-top:6px">
          <div class="smallCaps">Tip</div>
          <p class="mini" style="margin:6px 0 0">
            Ofrece Tapo en 2 modalidades: <b>Venta</b> (pago único) o <b>Renta</b> (18–24 meses) + instalación.
          </p>
        </div>
      </aside>
    </div>
  </div>
<section>
  <div class="wrap">
    <div class="card" style="border-color: rgba(53,199,255,.35); background: rgba(53,199,255,.06)">
      <div class="smallCaps">Canal TP-Link</div>
      <h3 style="margin:8px 0 6px">Distribución TP-Link Tapo para ISPs</h3>
      <p class="mini" style="margin:0">
        Somos vendedores de la marca TP-Link y ofrecemos un esquema de distribución para ISPs: bundles, kits demo, capacitación e instalación opcional.
      </p>
    </div>
  </div>
</section>
  <!-- BENEFICIOS -->
  <section id="beneficios">
    <div class="wrap">
      <div class="sectionHead">
        <div>
          <h2>Beneficios clave para ISP</h2>
          <p>Enfocado en distribución masiva a clientes residenciales y PyME.</p>
        </div>
      </div>

      <div class="grid">
        <div class="card col-4">
          <h3>📈 ARPU y paquetes</h3>
          <p>Agrega “Seguridad Tapo” como extra mensual o integra equipos en paquetes por velocidad.</p>
          <div class="chipRow">
            <span class="chip">Add-on</span><span class="chip">Bundling</span><span class="chip">Renta/venta</span>
          </div>
        </div>
        <div class="card col-4">
          <h3>🛡️ Seguridad lista para instalar</h3>
          <p>Productos fáciles de colocar y aprovisionar: cámaras Wi-Fi, timbres, sensores y hubs.</p>
          <div class="chipRow">
            <span class="chip">Residencial</span><span class="chip">Negocio</span><span class="chip">DIY/Pro</span>
          </div>
        </div>
        <div class="card col-4">
          <h3>📞 Soporte estandarizado</h3>
          <p>Flujos de soporte simples: checklist de Wi-Fi, ubicación, app, alertas y almacenamiento.</p>
          <div class="chipRow">
            <span class="chip">Guías</span><span class="chip">Scripts</span><span class="chip">FAQs</span>
          </div>
        </div>

        <div class="card col-6">
          <h3>🏠 Ecosistema completo</h3>
          <p>Desde seguridad (cámaras/timbres) hasta automatización (enchufes/focos/sensores). Crece por etapas con el cliente.</p>
        </div>
        <div class="card col-6">
          <h3>⚙️ Compatible con tu red actual</h3>
          <p>Funciona sobre tu Wi-Fi/Router existente. Recomendación: vender “Wi-Fi mejorado” + Tapo para mejores resultados.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CATALOGO -->
  <section id="catalogo">
    <div class="wrap">
      <div class="sectionHead">
        <div>
          <h2>Catálogo Tapo (para distribución)</h2>
          <p>Filtra por categoría y arma tu portafolio ISP.</p>
        </div>
      </div>

      <div class="toolbar">
        <div class="filters" id="filters"></div>

        <div class="search" role="search" aria-label="Buscar productos">
          <span aria-hidden="true">🔎</span>
          <input id="search" type="search" placeholder="Buscar: cámara, timbre, sensor, enchufe..." />
        </div>
      </div>

      <div class="catalog" id="catalog"></div>

      <p class="note" style="margin-top:12px">
        *Nota: Este catálogo es editable. Cambia nombres, descripciones y links en el arreglo <b>PRODUCTS</b> del script.
      </p>
    </div>
  </section>

  <!-- BUNDLES -->
  <section id="bundles">
    <div class="wrap">
      <div class="sectionHead">
        <div>
          <h2>Bundles recomendados para ISPs</h2>
          <p>Listos para “add-on” mensual o venta con instalación.</p>
        </div>
      </div>

      <div class="grid">
        <div class="card col-4 bundle">
          <h3>Starter Seguridad</h3>
          <p class="mini">Entrada para clientes residenciales.</p>
          <ul class="prodBullets">
            <li>1 cámara interior Wi-Fi</li>
            <li>1 enchufe inteligente (automatización básica)</li>
            <li>Instalación opcional + checklist Wi-Fi</li>
          </ul>
        </div>

        <div class="card col-4 bundle">
          <h3>Hogar Protegido</h3>
          <p class="mini">Paquete más vendido (puertas + interiores).</p>
          <ul class="prodBullets">
            <li>1 timbre/cámara exterior</li>
            <li>1–2 cámaras interior/exterior</li>
            <li>Notificaciones y escenas</li>
          </ul>
        </div>

        <div class="card col-4 bundle">
          <h3>Negocio / PyME</h3>
          <p class="mini">Para tiendas, oficinas y bodegas.</p>
          <ul class="prodBullets">
            <li>2–4 cámaras (según sitio)</li>
            <li>1 sensor / hub (opcional)</li>
            <li>Visitas de instalación y ajuste</li>
          </ul>
        </div>

        <div class="card col-12">
          <h3>Modelo comercial sugerido</h3>
          <p>
            <b>Opción A:</b> Venta de equipo + instalación (margen inmediato). &nbsp;•&nbsp;
            <b>Opción B:</b> Renta 18–24 meses + instalación (ingreso recurrente). &nbsp;•&nbsp;
            <b>Opción C:</b> Bundle “Wi-Fi mejorado” + Tapo (mejor experiencia y menos tickets).
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- IMPLEMENTACION -->
  <section id="implementacion">
    <div class="wrap">
      <div class="sectionHead">
        <div>
          <h2>Implementación rápida (ISP ready)</h2>
          <p>Checklist simple para vender, instalar y soportar.</p>
        </div>
      </div>

      <div class="grid">
        <div class="card col-6">
          <h3>1) Preparación</h3>
          <ul class="prodBullets">
            <li>Define 3 bundles y su precio/mes o pago único.</li>
            <li>Capacita 1 técnico con guía de instalación (30–60 min).</li>
            <li>Lista de verificación Wi-Fi: ubicación, señal, canal, backhaul.</li>
          </ul>
        </div>
        <div class="card col-6">
          <h3>2) Instalación</h3>
          <ul class="prodBullets">
            <li>Alta en app Tapo, emparejamiento y pruebas de notificación.</li>
            <li>Configura escenas (ej. “Noche”, “Fuera de casa”).</li>
            <li>Entrega mini manual al cliente (QR a tutoriales).</li>
          </ul>
        </div>

        <div class="card col-12">
          <h3>3) Soporte (baja fricción)</h3>
          <p class="mini">
            Estructura tus tickets con 4 preguntas: (1) ¿Hay internet? (2) ¿Señal Wi-Fi en el punto? (3) ¿App inicia sesión? (4) ¿Notificaciones activas?
            Con esto se resuelve la mayoría sin visita.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACTO -->
  <section id="contacto">
    <div class="wrap">
      <div class="sectionHead">
        <div>
          <h2>Quiero distribuir Tapo</h2>
          <p>Deja tus datos para cotización, kit demo y programa de distribución.</p>
        </div>
      </div>

      <div class="grid">
        <div class="card col-6">
          <h3>Contacto</h3>
          <form class="form" onsubmit="return handleSubmit(event)">
            <div class="field">
              <input required name="isp" placeholder="Nombre del ISP / Empresa" />
            </div>
            <div class="field">
              <input required name="nombre" placeholder="Nombre de contacto" />
            </div>
            <div class="field">
              <input required type="email" name="email" placeholder="Correo" />
            </div>
            <div class="field">
              <input name="telefono" placeholder="Teléfono / WhatsApp" />
            </div>
            <div class="field">
              <select name="interes">
                <option value="Distribucion">Distribución (mayoreo)</option>
                <option value="Bundles">Bundles para base instalada</option>
                <option value="Kit demo">Kit demo para pruebas</option>
                <option value="Instalacion">Instalación y soporte</option>
              </select>
            </div>
            <div class="field">
              <input name="ciudad" placeholder="Ciudad / Estado" />
            </div>
            <div class="field full">
              <textarea name="mensaje" placeholder="Cuéntame: # de clientes, tipo de red (FTTH/WISP), y qué bundle te interesa."></textarea>
            </div>

            <div class="field full" style="display:flex; gap:10px; flex-wrap:wrap">
              <button class="btn primary" type="submit">Enviar solicitud</button>
              <a class="btn" id="whatsBtn" href="#" target="_blank" rel="noopener">WhatsApp (opcional)</a>
            </div>

            <div class="field full note">
              Este formulario no envía por sí solo (es plantilla). Puedes:
              (1) conectarlo a tu CRM, (2) usar mailto:, o (3) integrarlo con un endpoint (Zapier/Make/Forms).
            </div>
          </form>
        </div>

        <div class="card col-6">
          <h3>Contenido listo para tu web</h3>
          <p class="mini">Incluye esto en tu propuesta comercial:</p>
          <ul class="prodBullets">
            <li><b>“Seguridad en casa”</b> con monitoreo desde app</li>
            <li><b>Automatización</b> (escenas, horarios, rutinas)</li>
            <li><b>Instalación certificada</b> por tu ISP (opcional)</li>
            <li><b>Soporte</b> de primer nivel (Wi-Fi + app)</li>
          </ul>
          <div class="card" style="margin-top:12px">
            <div class="smallCaps">Personaliza</div>
            <p class="mini" style="margin:6px 0 0">
              Cambia “Tu ISP” por tu marca, agrega tus bundles y pega tus links de compra/WhatsApp.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap">
    <div class="footerGrid">
      <div>
        <div class="brand" style="margin-bottom:8px">
          <div class="logo" aria-hidden="true"></div>
          <div>
            <div style="line-height:1.1">Tapo <span class="mutedLink">by TP-Link</span></div>
            <div class="mini">Plantilla para ISPs</div>
          </div>
        </div>
        <div class="note">
          Esta página es un template comercial para distribución. Puedes alojarla en tu hosting, landing builder o integrarla a tu sitio actual.
        </div>
      </div>

      <div>
        <div class="smallCaps">Quick links</div>
        <div style="display:flex; gap:10px; flex-wrap:wrap; margin-top:10px">
          <a class="link" href="#catalogo">Catálogo</a>
          <a class="link" href="#bundles">Bundles</a>
          <a class="link" href="#contacto">Contacto</a>
        </div>
      </div>
    </div>
  </div>
</footer>

<script>
  // =========================
  //  EDITA TU CATÁLOGO AQUÍ
  // =========================
  const PRODUCTS = [
    {
      name: "Cámaras Wi-Fi Interior",
      category: "Cámaras",
      tag: "Seguridad",
      desc: "Para recámaras, salas, oficinas. Ideal para starter bundle.",
      bullets: ["Detección de movimiento", "Notificaciones en app", "Visión nocturna (según modelo)"],
      ctaText: "Solicitar kit",
      ctaHref: "#contacto"
    },
    {
      name: "Cámaras Wi-Fi Exterior",
      category: "Cámaras",
      tag: "Exterior",
      desc: "Protección perimetral para casa o negocio.",
      bullets: ["Resistencia intemperie (según modelo)", "Alertas en tiempo real", "Montaje simple"],
      ctaText: "Armar bundle",
      ctaHref: "#bundles"
    },
    {
      name: "Timbres / Video Doorbells",
      category: "Timbres",
      tag: "Accesos",
      desc: "Control de accesos y visitas desde el teléfono.",
      bullets: ["Notificación al timbrar", "Audio bidireccional (según modelo)", "Ideal para ‘Hogar Protegido’"],
      ctaText: "Ver bundles",
      ctaHref: "#bundles"
    },
    {
      name: "Enchufes Inteligentes",
      category: "Energía",
      tag: "Smart",
      desc: "Automatización sencilla: horarios, escenas y control remoto.",
      bullets: ["Programación por horario", "Escenas en app", "Upsell fácil"],
      ctaText: "Cotizar",
      ctaHref: "#contacto"
    },
    {
      name: "Focos / Iluminación",
      category: "Iluminación",
      tag: "Automatización",
      desc: "Iluminación inteligente para hogares y pequeños negocios.",
      bullets: ["Escenas (noche/lectura)", "Control desde app", "Bundle con enchufes"],
      ctaText: "Solicitar catálogo",
      ctaHref: "#contacto"
    },
    {
      name: "Sensores (puerta/movimiento)",
      category: "Sensores",
      tag: "Alarmas",
      desc: "Complemento ideal para seguridad y automatización.",
      bullets: ["Alertas por apertura/movimiento", "Escenas con cámaras/luces", "Expansión por habitación"],
      ctaText: "Armar bundle",
      ctaHref: "#bundles"
    },
    {
      name: "Hubs (para sensores)",
      category: "Sensores",
      tag: "Ecosistema",
      desc: "Centraliza sensores y automatizaciones (según línea/modelo).",
      bullets: ["Ecosistema unificado", "Mejor escalabilidad", "Menos fricción de soporte"],
      ctaText: "Hablar con ventas",
      ctaHref: "#contacto"
    },
    {
      name: "Robot Aspiradora",
      category: "Hogar",
      tag: "Premium",
      desc: "Producto premium para aumentar ticket promedio.",
      bullets: ["Upsell premium", "Ideal para clientes ‘Gold/Pro’", "Venta directa o financiamiento"],
      ctaText: "Solicitar propuesta",
      ctaHref: "#contacto"
    }
  ];

  // Categorías (se autogeneran)
  const categories = ["Todos", ...Array.from(new Set(PRODUCTS.map(p => p.category)))];

  const els = {
    filters: document.getElementById("filters"),
    catalog: document.getElementById("catalog"),
    search: document.getElementById("search"),
    whatsBtn: document.getElementById("whatsBtn"),
  };

  let state = { category: "Todos", q: "" };

  function renderFilters(){
    els.filters.innerHTML = "";
    categories.forEach(cat => {
      const el = document.createElement("div");
      el.className = "pill" + (state.category === cat ? " active" : "");
      el.textContent = cat;
      el.onclick = () => { state.category = cat; render(); };
      els.filters.appendChild(el);
    });
  }

  function renderCatalog(){
    const q = state.q.trim().toLowerCase();
    const filtered = PRODUCTS.filter(p => {
      const matchCategory = state.category === "Todos" ? true : p.category === state.category;
      const blob = (p.name + " " + p.category + " " + p.tag + " " + p.desc + " " + (p.bullets||[]).join(" ")).toLowerCase();
      const matchQ = q ? blob.includes(q) : true;
      return matchCategory && matchQ;
    });

    els.catalog.innerHTML = "";
    filtered.forEach(p => {
      const card = document.createElement("article");
      card.className = "product";
      card.innerHTML = `
        <div class="productTop">
          <div>
            <p class="prodName">${escapeHtml(p.name)}</p>
            <p class="mini">${escapeHtml(p.category)} • <span style="color:#cfefff">${escapeHtml(p.tag)}</span></p>
          </div>
          <div class="tag">${escapeHtml(p.tag)}</div>
        </div>
        <p class="prodDesc">${escapeHtml(p.desc)}</p>
        <ul class="prodBullets">
          ${(p.bullets || []).map(b => `<li>${escapeHtml(b)}</li>`).join("")}
        </ul>
        <div class="prodActions">
          <a class="link" href="${p.ctaHref}">👉 ${escapeHtml(p.ctaText)}</a>
          <a class="link mutedLink" href="#contacto">Agregar a propuesta</a>
        </div>
      `;
      els.catalog.appendChild(card);
    });

    if(!filtered.length){
      const empty = document.createElement("div");
      empty.className = "card col-12";
      empty.innerHTML = `<h3>Sin resultados</h3><p>Prueba con otra categoría o búsqueda.</p>`;
      els.catalog.appendChild(empty);
    }
  }

  function render(){
    renderFilters();
    renderCatalog();
  }

  els.search.addEventListener("input", (e) => {
    state.q = e.target.value || "";
    renderCatalog();
  });

  // WhatsApp link (opcional): pon tu número aquí (formato internacional sin + ni espacios)
  const WHATS_NUMBER = "5210000000000"; // <-- CAMBIA ESTO (ej. 5213312345678)
  const WHATS_MSG = encodeURIComponent("Hola, soy un ISP. Quiero distribuir TP-Link Tapo a mi base de clientes. ¿Me compartes precios, bundles y kit demo?");
  els.whatsBtn.href = `https://wa.me/${WHATS_NUMBER}?text=${WHATS_MSG}`;

  function handleSubmit(e){
    e.preventDefault();
    const form = e.target;
    const data = Object.fromEntries(new FormData(form).entries());

    // Plantilla: aquí integra tu envío real (CRM / endpoint / email).
    // Por ahora solo muestra un resumen y copia un texto listo para pegar.
    const summary =
`Solicitud Tapo para ISP
- ISP: ${data.isp || "-"}
- Contacto: ${data.nombre || "-"}
- Email: ${data.email || "-"}
- Tel/Whats: ${data.telefono || "-"}
- Interés: ${data.interes || "-"}
- Ciudad: ${data.ciudad || "-"}
- Mensaje: ${data.mensaje || "-"}`;

    alert("Listo ✅ (plantilla)\n\nCopia este texto y envíalo a tu equipo comercial:\n\n" + summary);
    form.reset();
    state.q = "";
    els.search.value = "";
    renderCatalog();
    return false;
  }

  function escapeHtml(str){
    return String(str)
      .replaceAll("&","&amp;")
      .replaceAll("<","&lt;")
      .replaceAll(">","&gt;")
      .replaceAll('"',"&quot;")
      .replaceAll("'","&#039;");
  }

  render();
</script>
</body>
</html>
