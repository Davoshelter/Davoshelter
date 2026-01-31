<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#0b0f1a" />
  <title>Portafolio | Davoshelter</title>
  <meta name="description" content="Portafolio de estudiante de Ingeniería de Sistemas: Frontend (React/Next.js), Backend (ASP.NET) y Bases de Datos (SQL Server/PostgreSQL/MySQL)." />
  <style>
    :root{
      --bg: #0b0f1a;
      --panel: rgba(255,255,255,.06);
      --panel2: rgba(255,255,255,.09);
      --text: rgba(255,255,255,.92);
      --muted: rgba(255,255,255,.70);
      --border: rgba(255,255,255,.12);
      --shadow: 0 20px 60px rgba(0,0,0,.35);
      --brand: #7c5cff;
      --brand2:#22c55e;
      --warn:#f59e0b;
      --radius: 18px;
      --radius2: 26px;
      --max: 1120px;
    }
    [data-theme="light"]{
      --bg: #f6f7fb;
      --panel: rgba(10,20,40,.06);
      --panel2: rgba(10,20,40,.10);
      --text: rgba(10,15,25,.92);
      --muted: rgba(10,15,25,.70);
      --border: rgba(10,20,40,.14);
      --shadow: 0 18px 50px rgba(0,0,0,.12);
    }

    *{ box-sizing:border-box; }
    html{ scroll-behavior:smooth; }
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Cantarell, "Helvetica Neue", Arial;
      color:var(--text);
      background:
        radial-gradient(1200px 600px at 10% 10%, rgba(124,92,255,.22), transparent 60%),
        radial-gradient(900px 500px at 90% 20%, rgba(34,197,94,.14), transparent 55%),
        radial-gradient(900px 600px at 50% 100%, rgba(245,158,11,.10), transparent 60%),
        var(--bg);
      min-height:100dvh;
    }
    a{ color:inherit; text-decoration:none; }
    .wrap{ width:min(var(--max), calc(100% - 40px)); margin:0 auto; }

    /* Nav */
    .nav{
      position:sticky; top:0; z-index:50;
      backdrop-filter: blur(12px);
      background: linear-gradient(to bottom, rgba(0,0,0,.25), rgba(0,0,0,0));
      border-bottom: 1px solid rgba(255,255,255,.06);
    }
    [data-theme="light"] .nav{
      background: linear-gradient(to bottom, rgba(255,255,255,.70), rgba(255,255,255,0));
      border-bottom: 1px solid rgba(10,20,40,.08);
    }
    .navin{
      display:flex; align-items:center; justify-content:space-between;
      padding: 14px 0;
    }
    .brand{
      display:flex; align-items:center; gap:10px; font-weight:700; letter-spacing:.2px;
    }
    .logo{
      width:34px; height:34px; border-radius:12px;
      background: linear-gradient(135deg, var(--brand), rgba(34,197,94,.9));
      box-shadow: var(--shadow);
    }
    .links{ display:flex; gap:16px; align-items:center; }
    .links a{
      padding: 10px 12px; border-radius:12px; color:var(--muted);
      border: 1px solid transparent;
    }
    .links a:hover{ color:var(--text); border-color:var(--border); background:var(--panel); }
    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      gap:10px;
      padding: 12px 14px;
      border-radius: 14px;
      border: 1px solid var(--border);
      background: var(--panel);
      box-shadow: none;
      cursor:pointer;
      color:var(--text);
    }
    .btn:hover{ background: var(--panel2); }
    .btn.primary{
      border-color: rgba(124,92,255,.45);
      background: linear-gradient(135deg, rgba(124,92,255,.22), rgba(124,92,255,.10));
    }
    .btn.primary:hover{ border-color: rgba(124,92,255,.75); }

    /* Hero */
    .hero{ padding: 52px 0 22px; }
    .grid{
      display:grid;
      grid-template-columns: 1.25fr .75fr;
      gap: 18px;
      align-items: stretch;
    }
    @media (max-width: 920px){
      .grid{ grid-template-columns: 1fr; }
      .links{ display:none; }
    }
    .card{
      border:1px solid var(--border);
      background: var(--panel);
      border-radius: var(--radius2);
      box-shadow: var(--shadow);
      overflow:hidden;
      position:relative;
    }
    .card .inner{ padding: 22px; }
    .kicker{
      display:inline-flex; align-items:center; gap:8px;
      font-size: 13px; color: var(--muted);
      padding: 8px 10px; border-radius:999px;
      border:1px solid var(--border);
      background: rgba(0,0,0,.06);
    }
    [data-theme="light"] .kicker{ background: rgba(255,255,255,.55); }
    h1{
      margin: 14px 0 10px;
      font-size: clamp(28px, 3.2vw, 46px);
      line-height: 1.05;
      letter-spacing: -.6px;
    }
    .subtitle{ color: var(--muted); font-size: 16px; line-height: 1.6; }
    .cta{ display:flex; gap:12px; flex-wrap:wrap; margin-top:16px; }
    .meta{
      display:flex; flex-wrap:wrap; gap:10px;
      margin-top: 16px;
    }
    .chip{
      display:inline-flex; gap:8px; align-items:center;
      padding: 9px 10px; border-radius: 999px;
      border: 1px solid var(--border);
      background: rgba(255,255,255,.04);
      color: var(--muted);
      font-size: 13px;
    }

    /* Side card */
    .side{
      display:flex; flex-direction:column; justify-content:space-between;
      min-height: 100%;
    }
    .statgrid{
      display:grid; grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-top: 10px;
    }
    .stat{
      border: 1px solid var(--border);
      background: rgba(255,255,255,.04);
      border-radius: var(--radius);
      padding: 14px;
    }
    .stat b{ font-size: 18px; display:block; }
    .stat span{ color: var(--muted); font-size: 13px; }
    .divider{ height:1px; background: var(--border); margin: 14px 0; }

    /* Sections */
    section{ padding: 26px 0; }
    .sectionTitle{
      display:flex; align-items:flex-end; justify-content:space-between;
      gap: 12px;
      margin-bottom: 12px;
    }
    .sectionTitle h2{
      margin:0;
      font-size: 22px;
      letter-spacing: -.2px;
    }
    .sectionTitle p{ margin:0; color: var(--muted); }

    /* Skills */
    .skills{
      display:grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 12px;
    }
    .skill{
      grid-column: span 4;
      border:1px solid var(--border);
      background: var(--panel);
      border-radius: var(--radius2);
      padding: 16px;
    }
    @media (max-width: 920px){ .skill{ grid-column: span 6; } }
    @media (max-width: 600px){ .skill{ grid-column: span 12; } }
    .skill h3{ margin:0 0 8px; font-size: 16px; }
    .skill ul{ margin:0; padding-left: 18px; color: var(--muted); line-height: 1.8; }

    /* Projects */
    .projects{
      display:grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 12px;
    }
    .proj{
      grid-column: span 6;
      border:1px solid var(--border);
      background: var(--panel);
      border-radius: var(--radius2);
      padding: 16px;
      display:flex; flex-direction:column; gap: 10px;
      position:relative;
      overflow:hidden;
    }
    @media (max-width: 900px){ .proj{ grid-column: span 12; } }
    .proj:hover{ background: var(--panel2); transform: translateY(-1px); transition: .18s ease; }
    .projTop{ display:flex; align-items:flex-start; justify-content:space-between; gap:12px; }
    .proj h3{ margin:0; font-size: 16px; letter-spacing: -.2px; }
    .proj p{ margin:0; color: var(--muted); line-height: 1.6; }
    .tags{ display:flex; flex-wrap:wrap; gap:8px; }
    .tag{
      font-size: 12px; color: var(--muted);
      border: 1px solid var(--border);
      border-radius: 999px;
      padding: 7px 9px;
      background: rgba(255,255,255,.04);
    }
    .proj a.open{
      margin-top: 4px;
      display:inline-flex; align-items:center; gap:8px;
      color: var(--text);
      font-weight: 600;
      width: fit-content;
      padding: 10px 12px;
      border-radius: 14px;
      border: 1px solid var(--border);
      background: rgba(255,255,255,.04);
    }
    .proj a.open:hover{ background: rgba(124,92,255,.15); border-color: rgba(124,92,255,.35); }

    /* Footer */
    footer{ padding: 30px 0 44px; color: var(--muted); }
    .foot{
      display:flex; align-items:center; justify-content:space-between; gap: 12px;
      border-top: 1px solid var(--border);
      padding-top: 18px;
      flex-wrap:wrap;
    }
    .tiny{ font-size: 13px; }
  </style>
</head>

<body>
  <header class="nav">
    <div class="wrap navin">
      <a class="brand" href="#top" aria-label="Inicio">
        <span class="logo" aria-hidden="true"></span>
        <span>Davoshelter</span>
      </a>

      <nav class="links" aria-label="Secciones">
        <a href="#about">Sobre mí</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Proyectos</a>
        <a href="#contact">Contacto</a>
      </nav>

      <div style="display:flex; gap:10px; align-items:center;">
        <button class="btn" id="themeBtn" type="button" aria-label="Cambiar tema">🌓 Tema</button>
        <a class="btn primary" href="https://github.com/Davoshelter" target="_blank" rel="noreferrer">GitHub ↗</a>
      </div>
    </div>
  </header>

  <main id="top" class="wrap">
    <!-- HERO -->
    <section class="hero">
      <div class="grid">
        <div class="card">
          <div class="inner">
            <span class="kicker">🚀 Portafolio • Ingeniería de Sistemas</span>
            <h1>Frontend & Backend en construcción, con foco en productos limpios y funcionales.</h1>
            <p class="subtitle">
              Tengo entendimiento en <b>C#</b>, <b>HTML/CSS/JS</b>, <b>React</b>, <b>Next.js</b>,
              backend con <b>ASP.NET</b> y bases de datos <b>SQL Server</b>, <b>PostgreSQL</b>, <b>MySQL</b>.
            </p>

            <div class="cta">
              <a class="btn primary" href="#projects">Ver proyectos</a>
              <a class="btn" href="#contact">Contactar</a>
            </div>

            <div class="meta">
              <span class="chip">⚡ UI moderna</span>
              <span class="chip">🧠 Estudiante Ing. Sistemas</span>
              <span class="chip">🧩 Full-stack (ASP.NET + DB)</span>
              <span class="chip">🎯 React / Next.js</span>
            </div>
          </div>
        </div>

        <div class="card side">
          <div class="inner">
            <div class="sectionTitle" style="margin-bottom:6px;">
              <h2>Resumen</h2>
              <p class="tiny">Actualiza estos datos</p>
            </div>
            <div class="statgrid">
              <div class="stat"><b>Frontend</b><span>HTML • CSS • JS • React</span></div>
              <div class="stat"><b>Backend</b><span>ASP.NET • C#</span></div>
              <div class="stat"><b>DB</b><span>SQL Server • PostgreSQL • MySQL</span></div>
              <div class="stat"><b>Aprendiendo</b><span>Arquitectura • Buenas prácticas</span></div>
            </div>

            <div class="divider"></div>

            <div class="tiny" style="line-height:1.8;">
              <b>Tip:</b> cambia tu nombre, links y un texto corto de “sobre mí”.
              Si tienes LinkedIn/Correo, ponlos en “Contacto”.
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <div class="sectionTitle">
        <h2>Sobre mí</h2>
        <p>Una presentación corta que se lee rápido</p>
      </div>

      <div class="card">
        <div class="inner">
          <p class="subtitle" style="margin:0;">
            Soy estudiante de Ingeniería de Sistemas. Me gusta construir interfaces limpias y proyectos donde
            el frontend y el backend se conecten con bases de datos reales. Me interesa mejorar en arquitectura,
            calidad de código, y despliegue.
            <br><br>
            <b>Actualmente:</b> fortaleciendo proyectos con React/Next.js y backend con ASP.NET.
          </p>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills">
      <div class="sectionTitle">
        <h2>Skills</h2>
        <p>Lo que ya manejas + lo que estás reforzando</p>
      </div>

      <div class="skills">
        <div class="skill">
          <h3>Frontend</h3>
          <ul>
            <li>HTML, CSS, JavaScript</li>
            <li>React</li>
            <li>Next.js</li>
            <li>UI responsive y componentes</li>
          </ul>
        </div>

        <div class="skill">
          <h3>Backend</h3>
          <ul>
            <li>C#</li>
            <li>ASP.NET (APIs / backend)</li>
            <li>Autenticación / lógica de negocio</li>
          </ul>
        </div>

        <div class="skill">
          <h3>Bases de datos</h3>
          <ul>
            <li>SQL Server</li>
            <li>PostgreSQL</li>
            <li>MySQL</li>
            <li>Modelado y consultas</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects">
      <div class="sectionTitle">
        <h2>Proyectos</h2>
        <p>Cards con links directos a tus repos</p>
      </div>

      <div class="projects">
        <article class="proj">
          <div class="projTop">
            <div>
              <h3>Proyecto Arcane</h3>
              <p>Proyecto Arcane Sistemas de Informacion.</p>
            </div>
            <span class="tag">JS/HTML/CSS</span>
          </div>
          <div class="tags">
            <span class="tag">UI</span>
            <span class="tag">Web</span>
            <span class="tag">Proyecto</span>
          </div>
          <a class="open" href="https://github.com/Davoshelter/ProyectoArcane.1" target="_blank" rel="noreferrer">
            Ver repo ↗
          </a>
        </article>

        <article class="proj">
          <div class="projTop">
            <div>
              <h3>Stopwatch with Music</h3>
              <p>Cronómetro con música (HTML, CSS, JS) usando Tailwind.</p>
            </div>
            <span class="tag">JS</span>
          </div>
          <div class="tags">
            <span class="tag">Tailwind</span>
            <span class="tag">UI</span>
            <span class="tag">Frontend</span>
          </div>
          <a class="open" href="https://github.com/Davoshelter/Stopwatch_with_music" target="_blank" rel="noreferrer">
            Ver repo ↗
          </a>
        </article>

        <article class="proj">
          <div class="projTop">
            <div>
              <h3>Proyecto OnlyThree</h3>
              <p>HTML, CSS y JS consumiendo base de datos en la nube con Supabase.</p>
            </div>
            <span class="tag">Supabase</span>
          </div>
          <div class="tags">
            <span class="tag">DB</span>
            <span class="tag">Fetch/API</span>
            <span class="tag">Web</span>
          </div>
          <a class="open" href="https://github.com/Davoshelter/DesignWeb2ProyectoOnlyThree" target="_blank" rel="noreferrer">
            Ver repo ↗
          </a>
        </article>

        <article class="proj">
          <div class="projTop">
            <div>
              <h3>Actividad 2 (Mod6)</h3>
              <p>Repositorio de ejercicios del módulo 6 / Actividad 2.</p>
            </div>
            <span class="tag">Práctica</span>
          </div>
          <div class="tags">
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
            <span class="tag">JS</span>
          </div>
          <a class="open" href="https://github.com/Davoshelter/DesignWeb2Actividad2" target="_blank" rel="noreferrer">
            Ver repo ↗
          </a>
        </article>

        <article class="proj">
          <div class="projTop">
            <div>
              <h3>DesignWeb2 Practicos</h3>
              <p>GitHub Pages centralizado con prácticas de Diseño Web 2.</p>
            </div>
            <span class="tag">Pages</span>
          </div>
          <div class="tags">
            <span class="tag">Colección</span>
            <span class="tag">Web</span>
            <span class="tag">Prácticas</span>
          </div>
          <a class="open" href="https://github.com/Davoshelter/DesignWeb2Practicos" target="_blank" rel="noreferrer">
            Ver repo ↗
          </a>
        </article>

        <article class="proj">
          <div class="projTop">
            <div>
              <h3>Tu próximo proyecto</h3>
              <p>Reserva este espacio para un proyecto full-stack (ASP.NET + DB + React).</p>
            </div>
            <span class="tag">Full-stack</span>
          </div>
          <div class="tags">
            <span class="tag">ASP.NET</span>
            <span class="tag">SQL</span>
            <span class="tag">React</span>
          </div>
          <a class="open" href="#contact">
            Hablemos ↗
          </a>
        </article>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="sectionTitle">
        <h2>Contacto</h2>
        <p>Deja 1–2 formas simples de encontrarte</p>
      </div>

      <div class="card">
        <div class="inner">
          <p class="subtitle" style="margin-top:0;">
            Edita estas líneas con tus datos reales:
          </p>
          <div class="cta">
            <a class="btn" href="mailto:TU_CORREO@correo.com">📩 Email</a>
            <a class="btn" href="https://www.linkedin.com/in/TU_USUARIO" target="_blank" rel="noreferrer">💼 LinkedIn</a>
            <a class="btn" href="https://github.com/Davoshelter" target="_blank" rel="noreferrer">🐙 GitHub</a>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div class="foot">
        <div class="tiny">© <span id="year"></span> Davoshelter • Hecho con HTML/CSS/JS</div>
        <div class="tiny">Modo: <span id="modeLabel">Oscuro</span></div>
      </div>
    </footer>
  </main>

  <script>
    // Año automático
    document.getElementById("year").textContent = new Date().getFullYear();

    // Tema (dark/light) con persistencia
    const root = document.documentElement;
    const themeBtn = document.getElementById("themeBtn");
    const modeLabel = document.getElementById("modeLabel");
    const saved = localStorage.getItem("theme");

    function applyTheme(t){
      if(t === "light"){
        root.setAttribute("data-theme","light");
        modeLabel.textContent = "Claro";
      }else{
        root.removeAttribute("data-theme");
        modeLabel.textContent = "Oscuro";
      }
      localStorage.setItem("theme", t);
    }

    // Preferencia inicial
    if(saved){
      applyTheme(saved);
    } else {
      // si el sistema está en claro, arranca en claro
      const prefersLight = window.matchMedia && window.matchMedia("(prefers-color-scheme: light)").matches;
      applyTheme(prefersLight ? "light" : "dark");
    }

    themeBtn.addEventListener("click", () => {
      const isLight = root.getAttribute("data-theme") === "light";
      applyTheme(isLight ? "dark" : "light");
    });
  </script>
</body>
</html>
