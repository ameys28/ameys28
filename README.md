
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap');

  * { box-sizing: border-box; margin: 0; padding: 0; }

  .profile {
    font-family: 'Space Grotesk', sans-serif;
    background: #0d1117;
    color: #e6edf3;
    min-height: 100vh;
    padding: 2rem 1.5rem;
    line-height: 1.6;
  }

  .header {
    display: flex;
    align-items: center;
    gap: 2rem;
    margin-bottom: 2.5rem;
    padding-bottom: 2rem;
    border-bottom: 1px solid #21262d;
  }

  .avatar {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    background: linear-gradient(135deg, #1f6feb, #388bfd);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    font-weight: 700;
    color: #fff;
    flex-shrink: 0;
    border: 2px solid #30363d;
  }

  .header-info h1 {
    font-size: 1.6rem;
    font-weight: 700;
    color: #e6edf3;
    margin-bottom: 0.25rem;
  }

  .header-info .tagline {
    color: #8b949e;
    font-size: 0.95rem;
    font-weight: 400;
  }

  .badges {
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
    margin-top: 0.75rem;
  }

  .badge {
    background: #161b22;
    border: 1px solid #30363d;
    border-radius: 20px;
    padding: 3px 12px;
    font-size: 0.75rem;
    color: #8b949e;
    font-family: 'Fira Code', monospace;
  }

  .badge.active {
    border-color: #1f6feb;
    color: #388bfd;
    background: #0d1f36;
  }

  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-bottom: 1.5rem;
  }

  .card {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 10px;
    padding: 1.25rem;
    transition: border-color 0.2s;
  }

  .card:hover {
    border-color: #388bfd;
  }

  .card-label {
    font-size: 0.7rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: #8b949e;
    margin-bottom: 0.5rem;
    font-family: 'Fira Code', monospace;
  }

  .card-content {
    color: #e6edf3;
    font-size: 0.9rem;
    font-weight: 500;
  }

  .card-content a {
    color: #388bfd;
    text-decoration: none;
  }

  .card-content a:hover {
    text-decoration: underline;
  }

  .section-title {
    font-size: 0.75rem;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    color: #8b949e;
    font-family: 'Fira Code', monospace;
    margin-bottom: 1rem;
    padding-bottom: 0.5rem;
    border-bottom: 1px solid #21262d;
  }

  .skills-section {
    margin-bottom: 1.5rem;
  }

  .skill-category {
    margin-bottom: 1rem;
  }

  .skill-category-label {
    font-size: 0.78rem;
    color: #8b949e;
    margin-bottom: 0.5rem;
    font-family: 'Fira Code', monospace;
  }

  .skill-pills {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }

  .pill {
    padding: 4px 12px;
    border-radius: 6px;
    font-size: 0.8rem;
    font-weight: 500;
    font-family: 'Fira Code', monospace;
  }

  .pill.frontend { background: #0d2137; color: #58a6ff; border: 1px solid #1f4778; }
  .pill.backend  { background: #0d2b1a; color: #56d364; border: 1px solid #176024; }
  .pill.tools    { background: #2b1d0d; color: #e3b341; border: 1px solid #693f0a; }
  .pill.lang     { background: #2b0d1b; color: #f78166; border: 1px solid #6e1c36; }

  .connect-section {
    margin-bottom: 1.5rem;
  }

  .connect-links {
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 8px 16px;
    border-radius: 8px;
    font-size: 0.85rem;
    font-weight: 500;
    text-decoration: none;
    border: 1px solid #30363d;
    background: #161b22;
    color: #e6edf3;
    cursor: pointer;
    transition: all 0.2s;
  }

  .connect-btn:hover { border-color: #388bfd; color: #388bfd; background: #0d1f36; }
  .connect-btn.linkedin:hover { border-color: #0a66c2; color: #0a66c2; background: #061524; }
  .connect-btn.insta:hover { border-color: #e1306c; color: #e1306c; background: #250a12; }
  .connect-btn.mail:hover { border-color: #56d364; color: #56d364; background: #0a2010; }

  .stats-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-bottom: 1rem;
  }

  .stat-card {
    background: #161b22;
    border: 1px solid #21262d;
    border-radius: 10px;
    overflow: hidden;
  }

  .stat-card img {
    width: 100%;
    display: block;
  }

  .currently-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: #0d2b1a;
    border: 1px solid #176024;
    border-radius: 6px;
    padding: 4px 12px;
    font-size: 0.8rem;
    color: #56d364;
    font-family: 'Fira Code', monospace;
  }

  .dot-blink {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: #56d364;
    animation: blink 1.4s infinite;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.2; }
  }
</style>

<div class="profile">

  <!-- Header -->
  <div class="header">
    <div class="avatar">AS</div>
    <div class="header-info">
      <h1>Amey Sawant</h1>
      <div class="tagline">Software Developer · Full-Stack · MERN</div>
      <div class="badges">
        <span class="badge">📍 India</span>
        <span class="badge active">🌱 learning web dev</span>
        <span class="badge">Open to work</span>
      </div>
    </div>
  </div>

  <!-- Quick info grid -->
  <div class="grid" style="margin-bottom:1.5rem;">
    <div class="card">
      <div class="card-label">Portfolio</div>
      <div class="card-content">
        <a href="https://portfolio-website-psi-jet.vercel.app/" target="_blank">portfolio-website-psi-jet.vercel.app</a>
      </div>
    </div>
    <div class="card">
      <div class="card-label">Contact</div>
      <div class="card-content">
        <a href="mailto:ameysawant2806@gmail.com">ameysawant2806@gmail.com</a>
      </div>
    </div>
    <div class="card">
      <div class="card-label">Resume</div>
      <div class="card-content">
        <a href="https://drive.google.com/file/d/1arv8yyJ-0s6lkmhBYMHg2XbQwC_jt8c8/view?usp=sharing" target="_blank">View on Google Drive ↗</a>
      </div>
    </div>
    <div class="card">
      <div class="card-label">Status</div>
      <div class="card-content">
        <span class="currently-badge"><span class="dot-blink"></span>Building in public</span>
      </div>
    </div>
  </div>

  <!-- Skills -->
  <div class="skills-section">
    <div class="section-title">// tech stack</div>

    <div class="skill-category">
      <div class="skill-category-label">languages</div>
      <div class="skill-pills">
        <span class="pill lang">JavaScript</span>
        <span class="pill lang">Python</span>
        <span class="pill lang">Java</span>
        <span class="pill lang">C</span>
      </div>
    </div>

    <div class="skill-category" style="margin-top:0.75rem;">
      <div class="skill-category-label">frontend</div>
      <div class="skill-pills">
        <span class="pill frontend">React</span>
        <span class="pill frontend">Redux</span>
        <span class="pill frontend">HTML5</span>
        <span class="pill frontend">CSS3</span>
      </div>
    </div>

    <div class="skill-category" style="margin-top:0.75rem;">
      <div class="skill-category-label">backend & db</div>
      <div class="skill-pills">
        <span class="pill backend">Node.js</span>
        <span class="pill backend">Express.js</span>
        <span class="pill backend">MongoDB</span>
      </div>
    </div>

    <div class="skill-category" style="margin-top:0.75rem;">
      <div class="skill-category-label">tools & design</div>
      <div class="skill-pills">
        <span class="pill tools">Git</span>
        <span class="pill tools">Figma</span>
      </div>
    </div>
  </div>

  <!-- Connect -->
  <div class="connect-section">
    <div class="section-title">// connect</div>
    <div class="connect-links">
      <a class="connect-btn linkedin" href="https://linkedin.com/in/ameys28" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"/><circle cx="4" cy="4" r="2"/></svg>
        LinkedIn
      </a>
      <a class="connect-btn insta" href="https://instagram.com/amey_s_28" target="_blank">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="0.5" fill="currentColor" stroke="none"/></svg>
        Instagram
      </a>
      <a class="connect-btn mail" href="mailto:ameysawant2806@gmail.com">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><polyline points="2,4 12,13 22,4"/></svg>
        Email me
      </a>
    </div>
  </div>

  <!-- GitHub Stats -->
  <div class="section-title">// github stats</div>
  <div class="stats-row">
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api/top-langs?username=ameys28&show_icons=true&locale=en&layout=compact&theme=github_dark&hide_border=true&bg_color=161b22" alt="Top Languages" />
    </div>
    <div class="stat-card">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=ameys28&theme=github-dark-blue&hide_border=true&background=161b22" alt="GitHub Streak" />
    </div>
  </div>

</div>
