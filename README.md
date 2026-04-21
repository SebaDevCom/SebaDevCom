<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SebaDevCom - Java Backend Developer</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=JetBrains+Mono:wght@400;600&display=swap');
        * { box-sizing: border-box; margin: 0; padding: 0; }
        .readme-wrap { font-family: 'Space Grotesk', sans-serif; background: #0a0e1a; color: #e2e8f0; max-width: 860px; margin: 0 auto; padding: 0 0 60px; overflow: hidden; }
        .hero { position: relative; padding: 60px 40px 50px; text-align: center; background: linear-gradient(135deg, #0d1117 0%, #1a1a2e 50%, #16213e 100%); overflow: hidden; }
        .hero::before { content: ''; position: absolute; top: -80px; left: -80px; width: 320px; height: 320px; background: radial-gradient(circle, rgba(56,139,253,0.15) 0%, transparent 70%); animation: pulse 4s ease-in-out infinite; }
        .hero::after { content: ''; position: absolute; bottom: -60px; right: -60px; width: 280px; height: 280px; background: radial-gradient(circle, rgba(56,189,248,0.1) 0%, transparent 70%); animation: pulse 4s ease-in-out infinite 2s; }
        @keyframes pulse { 0%,100%{opacity:.6;transform:scale(1)}50%{opacity:1;transform:scale(1.05)} }
        .hero-name { font-size: 52px; font-weight: 700; letter-spacing: -1px; background: linear-gradient(135deg,#58a6ff 0%,#79c0ff 50%,#a5d6ff 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; position: relative; z-index: 1; animation: fadeSlideDown 0.8s ease; }
        .hero-sub { font-family: 'JetBrains Mono', monospace; font-size: 15px; color: #8b949e; margin-top: 10px; letter-spacing: 1px; position: relative; z-index: 1; animation: fadeSlideDown 0.8s ease 0.1s both; }
        .typing-line { display: inline-block; font-family: 'JetBrains Mono', monospace; font-size: 14px; color: #58a6ff; margin-top: 20px; padding: 8px 20px; border: 1px solid rgba(88,166,255,0.3); border-radius: 100px; background: rgba(88,166,255,0.07); position: relative; z-index: 1; animation: fadeSlideDown 0.8s ease 0.2s both; }
        .typing-cursor { display: inline-block; width: 2px; height: 14px; background: #58a6ff; margin-left: 2px; vertical-align: middle; animation: blink 1s step-end infinite; }
        @keyframes blink { 0%,100%{opacity:1}50%{opacity:0} }
        .badges { display: flex; justify-content: center; gap: 10px; flex-wrap: wrap; margin-top: 24px; position: relative; z-index: 1; animation: fadeSlideDown 0.8s ease 0.3s both; }
        .badge { display: inline-flex; align-items: center; gap: 6px; font-size: 12px; font-weight: 500; padding: 5px 14px; border-radius: 100px; border: 1px solid; letter-spacing: 0.3px; }
        .badge-blue { background: rgba(88,166,255,0.1); border-color: rgba(88,166,255,0.3); color: #79c0ff; }
        .badge-green { background: rgba(63,185,80,0.1); border-color: rgba(63,185,80,0.3); color: #56d364; }
        .badge-purple { background: rgba(188,140,255,0.1); border-color: rgba(188,140,255,0.3); color: #c9a0ff; }
        @keyframes fadeSlideDown { from{opacity:0;transform:translateY(-16px)}to{opacity:1;transform:translateY(0)} }
        .section { padding: 40px 40px 0; }
        .section-title { font-size: 13px; font-weight: 600; text-transform: uppercase; letter-spacing: 2px; color: #58a6ff; margin-bottom: 20px; display: flex; align-items: center; gap: 10px; }
        .section-title::after { content: ''; flex: 1; height: 1px; background: linear-gradient(to right, rgba(88,166,255,0.3), transparent); }
        .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
        @media (max-width: 768px) { .about-grid { grid-template-columns: 1fr; } }
        .code-block { background: #0d1117; border: 1px solid rgba(88,166,255,0.15); border-radius: 12px; padding: 20px; font-family: 'JetBrains Mono', monospace; font-size: 13px; line-height: 1.9; }
        .code-block::before { content: '● ● ●'; display: block; color: #484f58; font-size: 10px; letter-spacing: 4px; margin-bottom: 14px; }
        .code-key{color:#79c0ff}.code-str{color:#a5d6ff}.code-arr{color:#ff7b72}.code-comment{color:#484f58}
        .stat-mini { background: linear-gradient(135deg,#0d1117 0%,#161b22 100%); border: 1px solid rgba(88,166,255,0.15); border-radius: 12px; padding: 20px; display: flex; flex-direction: column; gap: 12px; }
        .stat-row { display: flex; justify-content: space-between; align-items: center; padding: 10px 14px; background: rgba(255,255,255,0.03); border-radius: 8px; font-size: 13px; border: 1px solid rgba(255,255,255,0.05); transition: border-color 0.2s; }
        .stat-row:hover { border-color: rgba(88,166,255,0.2); }
        .stat-label{color:#8b949e}.stat-val{color:#e2e8f0;font-weight:600;font-family:'JetBrains Mono',monospace;font-size:12px}
        .divider { height: 1px; background: linear-gradient(to right,transparent,rgba(88,166,255,0.15),transparent); margin: 36px 40px 0; }
        .tech-section { background: #0d1117; border: 1px solid rgba(88,166,255,0.12); border-radius: 14px; padding: 24px 28px; }
        .tech-group { margin-bottom: 20px; }
        .tech-group:last-child { margin-bottom: 0; }
        .tech-group-label { font-size: 11px; font-family: 'JetBrains Mono', monospace; color: #484f58; text-transform: uppercase; letter-spacing: 1.5px; margin-bottom: 12px; }
        .icon-row { display: flex; align-items: center; gap: 10px; flex-wrap: wrap; }
        .icon-item { display: flex; flex-direction: column; align-items: center; gap: 6px; padding: 10px 14px; background: rgba(255,255,255,0.03); border: 1px solid rgba(88,166,255,0.08); border-radius: 10px; transition: all 0.2s; cursor: default; }
        .icon-item:hover { border-color: rgba(88,166,255,0.3); background: rgba(88,166,255,0.06); transform: translateY(-2px); }
        .icon-item img { width: 32px; height: 32px; display: block; }
        .icon-label { font-size: 11px; color: #8b949e; font-family: 'JetBrains Mono', monospace; white-space: nowrap; }
        .project-card { background: #0d1117; border: 1px solid rgba(88,166,255,0.12); border-radius: 14px; padding: 22px; margin-bottom: 12px; display: flex; justify-content: space-between; align-items: flex-start; gap: 20px; transition: all 0.25s; }
        .project-card:hover { border-color: rgba(88,166,255,0.3); transform: translateX(4px); }
        .project-title{font-size:15px;font-weight:600;color:#58a6ff;margin-bottom:6px}
        .project-desc{font-size:13px;color:#8b949e;line-height:1.6}
        .project-tags{display:flex;gap:6px;margin-top:10px;flex-wrap:wrap}
        .tag{font-size:11px;font-family:'JetBrains Mono',monospace;padding:3px 10px;border-radius:100px;border:1px solid rgba(88,166,255,0.25);color:#79c0ff;background:rgba(88,166,255,0.08)}
        .project-status{font-size:11px;font-family:'JetBrains Mono',monospace;padding:4px 12px;border-radius:100px;white-space:nowrap;flex-shrink:0}
        .status-active{background:rgba(63,185,80,0.1);border:1px solid rgba(63,185,80,0.3);color:#56d364}
        .status-wip{background:rgba(255,183,77,0.1);border:1px solid rgba(255,183,77,0.3);color:#ffb74d}
        .goal-list{display:flex;flex-direction:column;gap:10px}
        .goal-item{display:flex;align-items:center;gap:14px;padding:14px 18px;background:#0d1117;border:1px solid rgba(88,166,255,0.1);border-radius:10px;font-size:14px;transition:all 0.2s}
        .goal-item:hover{border-color:rgba(88,166,255,0.25);background:#111827}
        .goal-dot{width:8px;height:8px;border-radius:50%;flex-shrink:0}
        .dot-done{background:#56d364;box-shadow:0 0 6px rgba(86,211,100,0.5)}
        .dot-active{background:#58a6ff;box-shadow:0 0 6px rgba(88,166,255,0.5);animation:pulse 2s infinite}
        .dot-next{background:#484f58}
        .goal-text{color:#c9d1d9}
        .goal-label{margin-left:auto;font-size:11px;font-family:'JetBrains Mono',monospace;color:#484f58}
        .footer{margin-top:50px;padding:30px 40px;background:#0d1117;border-top:1px solid rgba(88,166,255,0.1);display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:16px}
        .footer-text{font-size:13px;color:#484f58;font-family:'JetBrains Mono',monospace}
        .footer-link{font-size:13px;color:#58a6ff;text-decoration:none;padding:7px 16px;border:1px solid rgba(88,166,255,0.3);border-radius:8px;background:rgba(88,166,255,0.07);transition:all 0.2s;cursor:pointer}
        .footer-link:hover{background:rgba(88,166,255,0.15)}
    </style>
</head>
<body>

<div class="readme-wrap">
  <div class="hero">
    <div class="hero-name">SebaDevCom</div>
    <div class="hero-sub">// Java Backend Developer · Building Real Solutions</div>
    <div class="typing-line">
      <span id="typing-text">Building REST APIs with Spark Java</span><span class="typing-cursor"></span>
    </div>
    <div class="badges">
      <span class="badge badge-blue">Java Developer</span>
      <span class="badge badge-green">● Open to work</span>
      <span class="badge badge-purple">Backend Focus</span>
    </div>
  </div>

  <div class="section" style="margin-top:36px">
    <div class="section-title">About Me</div>
    <div class="about-grid">
      <div class="code-block">
        <div><span class="code-key">name</span>: <span class="code-str">"Sebastián"</span></div>
        <div><span class="code-key">role</span>: <span class="code-str">"Java Backend Dev"</span></div>
        <div><span class="code-key">database</span>: <span class="code-str">"MongoDB"</span></div>
        <div><span class="code-key">framework</span>: <span class="code-str">"Spark Java"</span></div>
        <div><span class="code-key">goal</span>: <span class="code-str">"Full Stack Dev"</span></div>
        <div style="margin-top:8px"><span class="code-arr">building</span>: [</div>
        <div style="padding-left:16px"><span class="code-str">"Inventory System"</span>,</div>
        <div style="padding-left:16px"><span class="code-str">"Mobile Backend"</span>,</div>
        <div style="padding-left:16px"><span class="code-str">"Sales Analytics"</span></div>
        <div>]</div>
        <div style="margin-top:8px"><span class="code-comment">// always: learning & shipping</span></div>
      </div>
      <div class="stat-mini">
        <div class="stat-row"><span class="stat-label">Location</span><span class="stat-val">México</span></div>
        <div class="stat-row"><span class="stat-label">Specialty</span><span class="stat-val">REST APIs</span></div>
        <div class="stat-row"><span class="stat-label">Database</span><span class="stat-val">MongoDB</span></div>
        <div class="stat-row"><span class="stat-label">Status</span><span class="stat-val" style="color:#56d364;">● Active</span></div>
        <div class="stat-row"><span class="stat-label">Goal</span><span class="stat-val">Backend → Full Stack</span></div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section">
    <div class="section-title">Tech Stack</div>
    <div class="tech-section">
      <div class="tech-group">
        <div class="tech-group-label">Backend</div>
        <div class="icon-row">
          <div class="icon-item">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" alt="Java"/>
            <span class="icon-label">Java</span>
          </div>
          <div class="icon-item" title="Spark Java">
            <svg width="32" height="32" viewBox="0 0 32 32" fill="none">
              <circle cx="16" cy="16" r="14" fill="#E74C3C" opacity="0.15"/>
              <text x="16" y="21" text-anchor="middle" font-size="13" font-weight="700" fill="#E74C3C" font-family="JetBrains Mono,monospace">SP</text>
            </svg>
            <span class="icon-label">Spark Java</span>
          </div>
          <div class="icon-item">
            <svg width="32" height="32" viewBox="0 0 32 32" fill="none">
              <rect width="32" height="32" rx="6" fill="rgba(88,166,255,0.1)"/>
              <text x="16" y="22" text-anchor="middle" font-size="11" font-weight="700" fill="#58a6ff" font-family="JetBrains Mono,monospace">REST</text>
            </svg>
            <span class="icon-label">REST APIs</span>
          </div>
        </div>
      </div>
      <div class="tech-group">
        <div class="tech-group-label">Database</div>
        <div class="icon-row">
          <div class="icon-item">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg" alt="MongoDB"/>
            <span class="icon-label">MongoDB</span>
          </div>
        </div>
      </div>
      <div class="tech-group">
        <div class="tech-group-label">Tools</div>
        <div class="icon-row">
          <div class="icon-item">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" alt="Git"/>
            <span class="icon-label">Git</span>
          </div>
          <div class="icon-item">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" alt="GitHub" style="filter: invert(1) brightness(0.8)"/>
            <span class="icon-label">GitHub</span>
          </div>
          <div class="icon-item">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" alt="VS Code"/>
            <span class="icon-label">VS Code</span>
          </div>
          <div class="icon-item">
            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postman/postman-original.svg" alt="Postman"/>
            <span class="icon-label">Postman</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section">
    <div class="section-title">Current Projects</div>
    <div class="project-card">
      <div>
        <div class="project-title">Inventory Management System</div>
        <div class="project-desc">Sistema completo con MongoDB, control de stock, entradas/salidas y reportes en tiempo real.</div>
        <div class="project-tags"><span class="tag">Java</span><span class="tag">Spark Java</span><span class="tag">MongoDB</span><span class="tag">REST API</span></div>
      </div>
      <span class="project-status status-active">● Active</span>
    </div>
    <div class="project-card">
      <div>
        <div class="project-title">Mobile App Backend</div>
        <div class="project-desc">Backend API con autenticación y gestión de datos de usuarios.</div>
        <div class="project-tags"><span class="tag">Java</span><span class="tag">REST</span><span class="tag">Auth</span></div>
      </div>
      <span class="project-status status-wip">⚡ WIP</span>
    </div>
    <div class="project-card">
      <div>
        <div class="project-title">Sales Analytics Module</div>
        <div class="project-desc">Módulo de análisis de ventas con métricas, dashboards y exportación de reportes.</div>
        <div class="project-tags"><span class="tag">Java</span><span class="tag">MongoDB</span><span class="tag">Analytics</span></div>
      </div>
      <span class="project-status status-wip">⚡ WIP</span>
    </div>
  </div>

  <div class="divider"></div>

  <div class="section">
    <div class="section-title">Roadmap</div>
    <div class="goal-list">
      <div class="goal-item"><div class="goal-dot dot-done"></div><div class="goal-text">Java Backend — REST APIs con Spark Java</div><div class="goal-label">done</div></div>
      <div class="goal-item"><div class="goal-dot dot-done"></div><div class="goal-text">MongoDB — Diseño y consultas NoSQL</div><div class="goal-label">done</div></div>
      <div class="goal-item"><div class="goal-dot dot-active"></div><div class="goal-text">Sistema de inventario completo en producción</div><div class="goal-label">now</div></div>
      <div class="goal-item"><div class="goal-dot dot-next"></div><div class="goal-text">Spring Boot — Migración y ecosistema</div><div class="goal-label">next</div></div>
      <div class="goal-item"><div class="goal-dot dot-next"></div><div class="goal-text">Full Stack — React / Vue frontend</div><div class="goal-label">future</div></div>
    </div>
  </div>

  <div class="footer">
    <div class="footer-text">// Sebastián · Java Backend Developer · 2026</div>
    <div class="footer-link" onclick="window.location.href='https://github.com/SebaDevCom'">→ github.com/SebaDevCom</div>
  </div>

</div>

<script>
  const lines = ['Building REST APIs with Spark Java','MongoDB & Inventory Systems','Future Full Stack Developer','Always learning, always shipping'];
  let idx = 0;
  const el = document.getElementById('typing-text');
  function nextLine() {
    el.style.opacity='0'; el.style.transform='translateY(6px)'; el.style.transition='all 0.4s ease';
    setTimeout(()=>{ idx=(idx+1)%lines.length; el.textContent=lines[idx]; el.style.opacity='1'; el.style.transform='translateY(0)'; },400);
  }
  setInterval(nextLine,3000);
</script>

</body>
</html>
