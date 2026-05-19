<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap');

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
    color: #e6edf3;
    line-height: 1.6;
  }

  /* ===================== KEYFRAME ANIMATIONS ===================== */
  @keyframes slideInDown {
    from {
      opacity: 0;
      transform: translateY(-40px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(30px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
    }
    to {
      opacity: 1;
    }
  }

  @keyframes slideInLeft {
    from {
      opacity: 0;
      transform: translateX(-40px);
    }
    to {
      opacity: 1;
      transform: translateX(0);
    }
  }

  @keyframes slideInRight {
    from {
      opacity: 0;
      transform: translateX(40px);
    }
    to {
      opacity: 1;
      transform: translateX(0);
    }
  }

  @keyframes glow {
    0%, 100% {
      text-shadow: 0 0 20px rgba(88, 166, 255, 0.5), 0 0 40px rgba(88, 166, 255, 0.2);
    }
    50% {
      text-shadow: 0 0 30px rgba(88, 166, 255, 0.8), 0 0 60px rgba(88, 166, 255, 0.4);
    }
  }

  @keyframes float {
    0%, 100% {
      transform: translateY(0px);
    }
    50% {
      transform: translateY(-15px);
    }
  }

  @keyframes bounce {
    0%, 100% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(-12px);
    }
  }

  @keyframes pulse {
    0%, 100% {
      opacity: 1;
    }
    50% {
      opacity: 0.6;
    }
  }

  @keyframes shimmer {
    0% {
      background-position: -1000px 0;
    }
    100% {
      background-position: 1000px 0;
    }
  }

  @keyframes scaleIn {
    from {
      opacity: 0;
      transform: scale(0.95);
    }
    to {
      opacity: 1;
      transform: scale(1);
    }
  }

  @keyframes underlineGrow {
    from {
      width: 0;
    }
    to {
      width: 100%;
    }
  }

  /* ===================== HEADER & INTRO ===================== */
  .header-section {
    animation: slideInDown 0.8s ease-out;
    padding: 60px 20px 40px;
    text-align: center;
    background: linear-gradient(180deg, rgba(88, 166, 255, 0.1) 0%, transparent 100%);
    border-bottom: 1px solid rgba(88, 166, 255, 0.2);
    position: relative;
    overflow: hidden;
  }

  .header-section::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -10%;
    width: 300px;
    height: 300px;
    background: radial-gradient(circle, rgba(88, 166, 255, 0.15) 0%, transparent 70%);
    border-radius: 50%;
    animation: float 6s ease-in-out infinite;
  }

  .header-section::after {
    content: '';
    position: absolute;
    bottom: -50%;
    left: -10%;
    width: 300px;
    height: 300px;
    background: radial-gradient(circle, rgba(88, 166, 255, 0.1) 0%, transparent 70%);
    border-radius: 50%;
    animation: float 8s ease-in-out infinite reverse;
  }

  .header-content {
    position: relative;
    z-index: 1;
    max-width: 900px;
    margin: 0 auto;
  }

  .title {
    font-size: 3.5em;
    font-weight: 800;
    letter-spacing: -1px;
    margin: 20px 0;
    background: linear-gradient(135deg, #58a6ff 0%, #79c0ff 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: slideInDown 0.8s ease-out 0.1s backwards;
  }

  .subtitle {
    font-size: 1.3em;
    color: #79c0ff;
    font-weight: 600;
    margin-bottom: 10px;
    animation: slideInDown 0.8s ease-out 0.2s backwards;
  }

  .description {
    font-size: 1em;
    color: #8b949e;
    margin: 15px 0 25px;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.8;
    animation: fadeInUp 0.8s ease-out 0.3s backwards;
  }

  /* ===================== TYPING ANIMATION ===================== */
  .typing-container {
    margin: 30px 0;
    animation: fadeInUp 0.8s ease-out 0.4s backwards;
  }

  .typing-text {
    font-family: 'JetBrains Mono', monospace;
    font-size: 1.1em;
    color: #58a6ff;
    font-weight: 500;
    letter-spacing: 1px;
  }

  /* ===================== CTA BUTTONS ===================== */
  .cta-buttons {
    display: flex;
    gap: 15px;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 30px;
    animation: fadeInUp 0.8s ease-out 0.5s backwards;
  }

  .btn {
    padding: 12px 28px;
    border-radius: 6px;
    border: 2px solid;
    font-weight: 600;
    font-size: 0.95em;
    cursor: pointer;
    transition: all 0.3s ease;
    text-decoration: none;
    display: inline-block;
    font-family: 'Inter', sans-serif;
  }

  .btn-primary {
    background: linear-gradient(135deg, #58a6ff 0%, #79c0ff 100%);
    color: #0d1117;
    border-color: #58a6ff;
  }

  .btn-primary:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(88, 166, 255, 0.4);
  }

  .btn-secondary {
    background: transparent;
    color: #58a6ff;
    border-color: #58a6ff;
  }

  .btn-secondary:hover {
    background: rgba(88, 166, 255, 0.1);
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(88, 166, 255, 0.2);
  }

  /* ===================== SECTIONS ===================== */
  .section {
    padding: 60px 20px;
    max-width: 1200px;
    margin: 0 auto;
    animation: fadeInUp 1s ease-out both;
  }

  .section:nth-child(2) { animation-delay: 0.1s; }
  .section:nth-child(3) { animation-delay: 0.2s; }
  .section:nth-child(4) { animation-delay: 0.3s; }
  .section:nth-child(5) { animation-delay: 0.4s; }
  .section:nth-child(6) { animation-delay: 0.5s; }

  .section-title {
    font-size: 2em;
    font-weight: 700;
    margin-bottom: 35px;
    color: #c9d1d9;
    display: flex;
    align-items: center;
    gap: 12px;
    position: relative;
  }

  .section-title::after {
    content: '';
    flex: 1;
    height: 3px;
    background: linear-gradient(90deg, #58a6ff 0%, transparent 100%);
    border-radius: 2px;
    max-width: 150px;
  }

  /* ===================== ABOUT SECTION ===================== */
  .about-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
    margin: 30px 0;
  }

  .about-card {
    background: rgba(22, 27, 34, 0.5);
    border: 1px solid rgba(88, 166, 255, 0.2);
    border-radius: 8px;
    padding: 25px;
    transition: all 0.3s ease;
    animation: scaleIn 0.6s ease-out backwards;
  }

  .about-card:nth-child(1) { animation-delay: 0.1s; }
  .about-card:nth-child(2) { animation-delay: 0.2s; }
  .about-card:nth-child(3) { animation-delay: 0.3s; }
  .about-card:nth-child(4) { animation-delay: 0.4s; }

  .about-card:hover {
    background: rgba(22, 27, 34, 0.8);
    border-color: #58a6ff;
    transform: translateY(-5px);
    box-shadow: 0 12px 32px rgba(88, 166, 255, 0.15);
  }

  .card-icon {
    font-size: 2.5em;
    margin-bottom: 12px;
    animation: float 3s ease-in-out infinite;
  }

  .about-card h3 {
    color: #58a6ff;
    margin-bottom: 8px;
    font-weight: 600;
  }

  .about-card p {
    color: #8b949e;
    font-size: 0.95em;
    line-height: 1.6;
  }

  /* ===================== TECH STACK SECTION ===================== */
  .tech-categories {
    display: grid;
    gap: 40px;
  }

  .tech-category {
    animation: slideInLeft 0.8s ease-out backwards;
  }

  .tech-category:nth-child(2) { animation-delay: 0.1s; animation-name: slideInRight; }
  .tech-category:nth-child(3) { animation-delay: 0.2s; animation-name: slideInLeft; }
  .tech-category:nth-child(4) { animation-delay: 0.3s; animation-name: slideInRight; }

  .tech-category h3 {
    color: #79c0ff;
    font-size: 1.2em;
    margin-bottom: 20px;
    font-weight: 600;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .tech-list {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .tech-badge {
    background: rgba(88, 166, 255, 0.15);
    border: 1px solid rgba(88, 166, 255, 0.3);
    color: #79c0ff;
    padding: 8px 16px;
    border-radius: 20px;
    font-size: 0.85em;
    font-weight: 500;
    cursor: pointer;
    transition: all 0.3s ease;
    animation: scaleIn 0.6s ease-out backwards;
    font-family: 'JetBrains Mono', monospace;
  }

  .tech-badge:hover {
    background: rgba(88, 166, 255, 0.3);
    border-color: #58a6ff;
    transform: translateY(-3px);
    box-shadow: 0 8px 16px rgba(88, 166, 255, 0.2);
  }

  .tech-badge:nth-child(1) { animation-delay: 0s; }
  .tech-badge:nth-child(2) { animation-delay: 0.05s; }
  .tech-badge:nth-child(3) { animation-delay: 0.1s; }
  .tech-badge:nth-child(4) { animation-delay: 0.15s; }
  .tech-badge:nth-child(5) { animation-delay: 0.2s; }
  .tech-badge:nth-child(6) { animation-delay: 0.25s; }
  .tech-badge:nth-child(7) { animation-delay: 0.3s; }
  .tech-badge:nth-child(8) { animation-delay: 0.35s; }

  /* ===================== STATS SECTION ===================== */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 25px;
    margin: 30px 0;
  }

  .stat-card {
    background: rgba(22, 27, 34, 0.6);
    border: 1px solid rgba(88, 166, 255, 0.2);
    border-radius: 8px;
    padding: 25px;
    text-align: center;
    transition: all 0.3s ease;
    animation: fadeInUp 0.8s ease-out backwards;
    position: relative;
    overflow: hidden;
  }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: linear-gradient(90deg, #58a6ff 0%, transparent 100%);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }

  .stat-card:hover::before {
    transform: scaleX(1);
  }

  .stat-card:nth-child(1) { animation-delay: 0.1s; }
  .stat-card:nth-child(2) { animation-delay: 0.2s; }
  .stat-card:nth-child(3) { animation-delay: 0.3s; }

  .stat-card:hover {
    background: rgba(22, 27, 34, 0.9);
    border-color: #58a6ff;
    transform: translateY(-5px);
    box-shadow: 0 12px 32px rgba(88, 166, 255, 0.15);
  }

  .stat-image {
    margin-bottom: 15px;
    border-radius: 6px;
    transition: transform 0.3s ease;
  }

  .stat-card:hover .stat-image {
    transform: scale(1.02);
  }

  /* ===================== FOOTER ===================== */
  .footer {
    background: rgba(13, 17, 23, 0.8);
    border-top: 1px solid rgba(88, 166, 255, 0.2);
    padding: 40px 20px;
    text-align: center;
    animation: fadeIn 1s ease-out 1s backwards;
  }

  .social-links {
    display: flex;
    gap: 20px;
    justify-content: center;
    margin: 20px 0;
    flex-wrap: wrap;
  }

  .social-link {
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(88, 166, 255, 0.1);
    border: 2px solid rgba(88, 166, 255, 0.3);
    border-radius: 50%;
    color: #79c0ff;
    text-decoration: none;
    transition: all 0.3s ease;
    font-size: 1.3em;
    animation: scaleIn 0.6s ease-out backwards;
  }

  .social-link:nth-child(1) { animation-delay: 0.1s; }
  .social-link:nth-child(2) { animation-delay: 0.2s; }
  .social-link:nth-child(3) { animation-delay: 0.3s; }
  .social-link:nth-child(4) { animation-delay: 0.4s; }

  .social-link:hover {
    background: #58a6ff;
    color: #0d1117;
    transform: translateY(-5px) scale(1.1);
    box-shadow: 0 8px 20px rgba(88, 166, 255, 0.4);
  }

  .footer-text {
    color: #8b949e;
    margin-top: 30px;
    font-size: 0.95em;
  }

  .footer-text strong {
    color: #58a6ff;
  }

  /* ===================== RESPONSIVE ===================== */
  @media (max-width: 768px) {
    .title {
      font-size: 2.2em;
    }

    .subtitle {
      font-size: 1.1em;
    }

    .section {
      padding: 40px 15px;
    }

    .section-title {
      font-size: 1.5em;
    }

    .cta-buttons {
      flex-direction: column;
    }

    .btn {
      width: 100%;
    }
  }
</style>

<!-- ==================== HEADER & INTRO ==================== -->
<div class="header-section">
  <div class="header-content">
    <div class="subtitle">👋 Welcome to my Profile!</div>
    <h1 class="title">Quamar Mehboob</h1>
    <p class="description">
      Senior Developer | Full-Stack Engineer | Tech Innovator
    </p>
    <div class="typing-container">
      <span class="typing-text">// Crafting scalable solutions that make an impact ⚡</span>
    </div>
    <div class="cta-buttons">
      <a href="https://thecodeforge.in" class="btn btn-primary">🌐 Visit Website</a>
      <a href="https://www.linkedin.com/in/quamar-mehboob-ab10831b3/" class="btn btn-secondary">💼 LinkedIn</a>
    </div>
  </div>
</div>

<!-- ==================== ABOUT SECTION ==================== -->
<div class="section">
  <h2 class="section-title">📌 About Me</h2>
  <div class="about-grid">
    <div class="about-card">
      <div class="card-icon">🚀</div>
      <h3>Current Role</h3>
      <p>Sr Developer at <strong>Codeforge Solutions</strong>, building enterprise-scale applications and innovative solutions.</p>
    </div>
    <div class="about-card">
      <div class="card-icon">🎯</div>
      <h3>Focus Areas</h3>
      <p>Full-stack development, system design, cloud architecture, and scalable enterprise solutions.</p>
    </div>
    <div class="about-card">
      <div class="card-icon">📚</div>
      <h3>Learning</h3>
      <p>Currently expanding expertise in Node.js, Advanced System Design, and Cloud Architecture.</p>
    </div>
    <div class="about-card">
      <div class="card-icon">✨</div>
      <h3>Passion</h3>
      <p>Love creating content and building solutions that solve real problems and create impact.</p>
    </div>
  </div>
</div>

<!-- ==================== EXPERTISE SECTION ==================== -->
<div class="section">
  <h2 class="section-title">🛠️ Tech Stack</h2>
  
  <div class="tech-categories">
    <div class="tech-category">
      <h3>💻 Languages</h3>
      <div class="tech-list">
        <span class="tech-badge">JavaScript</span>
        <span class="tech-badge">TypeScript</span>
        <span class="tech-badge">PHP</span>
        <span class="tech-badge">Python</span>
        <span class="tech-badge">HTML5</span>
        <span class="tech-badge">CSS3</span>
        <span class="tech-badge">GraphQL</span>
        <span class="tech-badge">Solidity</span>
      </div>
    </div>

    <div class="tech-category">
      <h3>⚛️ Frontend</h3>
      <div class="tech-list">
        <span class="tech-badge">React</span>
        <span class="tech-badge">Next.js</span>
        <span class="tech-badge">TypeScript</span>
        <span class="tech-badge">Tailwind CSS</span>
        <span class="tech-badge">Chakra UI</span>
        <span class="tech-badge">Material-UI</span>
        <span class="tech-badge">Bootstrap</span>
      </div>
    </div>

    <div class="tech-category">
      <h3>🔧 Backend & Databases</h3>
      <div class="tech-list">
        <span class="tech-badge">Node.js</span>
        <span class="tech-badge">Express.js</span>
        <span class="tech-badge">MySQL</span>
        <span class="tech-badge">PostgreSQL</span>
        <span class="tech-badge">MongoDB</span>
        <span class="tech-badge">Apollo GraphQL</span>
        <span class="tech-badge">Socket.io</span>
      </div>
    </div>

    <div class="tech-category">
      <h3>🚀 DevOps & Tools</h3>
      <div class="tech-list">
        <span class="tech-badge">Vercel</span>
        <span class="tech-badge">Docker</span>
        <span class="tech-badge">Git</span>
        <span class="tech-badge">JWT</span>
        <span class="tech-badge">Redux</span>
        <span class="tech-badge">Chart.js</span>
        <span class="tech-badge">Electron.js</span>
      </div>
    </div>
  </div>
</div>

<!-- ==================== STATS SECTION ==================== -->
<div class="section">
  <h2 class="section-title">📊 GitHub Statistics</h2>
  <div class="stats-grid">
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api?username=kingSPARROW&theme=dark&hide_border=true&include_all_commits=false&count_private=false&bg_color=0d1117&text_color=79c0ff" alt="GitHub Stats" class="stat-image" style="width: 100%; border-radius: 6px;">
    </div>
    <div class="stat-card">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=kingSPARROW&theme=dark&hide_border=true&background=0d1117" alt="GitHub Streak" class="stat-image" style="width: 100%; border-radius: 6px;">
    </div>
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kingSPARROW&theme=dark&hide_border=true&include_all_commits=false&count_private=false&layout=compact&bg_color=0d1117&text_color=79c0ff" alt="Top Languages" class="stat-image" style="width: 100%; border-radius: 6px;">
    </div>
  </div>
</div>

<!-- ==================== PROJECTS SECTION ==================== -->
<div class="section">
  <h2 class="section-title">🏆 Top Repositories</h2>
  <div class="stats-grid" style="margin-top: 30px;">
    <div class="stat-card">
      <img src="https://github-contributor-stats.vercel.app/api?username=kingSPARROW&limit=5&theme=tokyonight&combine_all_yearly_contributions=true" alt="Top Contributed Repos" style="width: 100%; border-radius: 6px;">
    </div>
  </div>
</div>

<!-- ==================== CTA SECTION ==================== -->
<div class="section" style="text-align: center; background: rgba(88, 166, 255, 0.05); border-radius: 8px; border: 1px solid rgba(88, 166, 255, 0.2);">
  <h2 class="section-title" style="justify-content: center; margin-bottom: 20px;">🚀 What's Next?</h2>
  <p style="color: #8b949e; font-size: 1.1em; margin: 20px 0;">
    Building enterprise-scale solutions • Exploring emerging technologies • Open to collaboration
  </p>
  <div class="cta-buttons" style="margin-top: 25px;">
    <a href="https://thecodeforge.in" class="btn btn-primary">📧 Get in Touch</a>
    <a href="https://twitter.com/im_quamar001" class="btn btn-secondary">🐦 Follow on Twitter</a>
  </div>
</div>

<!-- ==================== FOOTER ==================== -->
<div class="footer">
  <div class="social-links">
    <a href="https://github.com/kingSPARROW" class="social-link" title="GitHub">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v 3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/></svg>
    </a>
    <a href="https://www.linkedin.com/in/quamar-mehboob-ab10831b3/" class="social-link" title="LinkedIn">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.475-2.236-1.986-2.236-1.081 0-1.722.731-2.004 1.437-.103.25-.129.599-.129.949v5.419h-3.554s.043-8.789 0-9.714h3.554v1.375c.428-.659 1.191-1.597 2.897-1.597 2.117 0 3.704 1.384 3.704 4.357v5.579zM5.337 8.855c-1.144 0-1.915-.759-1.915-1.71 0-.955.768-1.71 1.959-1.71 1.19 0 1.916.755 1.938 1.71 0 .951-.748 1.71-1.982 1.71zm1.614 11.597H3.615V9.638h3.336v10.814zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.225 0z"/></svg>
    </a>
    <a href="https://twitter.com/im_quamar001" class="social-link" title="Twitter">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor"><path d="M23.953 4.57a10 10 0 002.856-3.215 9.954 9.954 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/></svg>
    </a>
    <a href="https://thecodeforge.in" class="social-link" title="Website">
      <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"></circle><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"></path><path d="M2 12h20"></path></svg>
    </a>
  </div>
  
  <div class="footer-text">
    <p>🌟 Let's build something <strong>amazing</strong> together!</p>
    <p style="margin-top: 15px; font-size: 0.85em; color: #6e7681;">
      © 2025 Quamar Mehboob | Sr Developer at Codeforge Solutions<br>
      <em>Crafting scalable solutions with passion 💻✨</em>
    </p>
  </div>
</div>
