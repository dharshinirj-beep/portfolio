<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dharshini R J — Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;1,500;1,600&family=Manrope:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink: #392f4d;
    --ink-dim: #7a6e93;
    --ink-faint: #a89dc0;
    --glass: rgba(255,255,255,0.5);
    --glass-strong: rgba(255,255,255,0.72);
    --border: rgba(255,255,255,0.65);
    --rose: #ff9bb3;
    --gold: #ffc971;
    --lilac: #b6a3e8;
    --sky: #a3c9f1;
    --display: 'Cormorant Garamond', serif;
    --body: 'Manrope', sans-serif;
  }

  *{ margin:0; padding:0; box-sizing:border-box; }
  html{ scroll-behavior:smooth; }
  body{
    color:var(--ink); font-family:var(--body); font-weight:500; line-height:1.7; -webkit-font-smoothing:antialiased;
    background:
      radial-gradient(circle at 12% 8%, #ffe3c4 0%, transparent 42%),
      radial-gradient(circle at 88% 15%, #ffcfe0 0%, transparent 45%),
      radial-gradient(circle at 25% 85%, #cfe0ff 0%, transparent 45%),
      radial-gradient(circle at 85% 90%, #d9caf5 0%, transparent 48%),
      #fbf8ff;
    background-attachment:fixed;
    overflow-x:hidden;
  }
  a{ color:inherit; }
  ::selection{ background:var(--lilac); color:#fff; }
  :focus-visible{ outline:2px solid var(--lilac); outline-offset:3px; }
  .wrap{ max-width:1180px; margin:0 auto; padding:0 48px; position:relative; }
  @media (max-width:700px){ .wrap{ padding:0 24px; } }

  /* ---------- nav ---------- */
  .navbar{ position:sticky; top:16px; z-index:60; margin:0 auto; max-width:600px; padding:0 20px; }
  .navbar-inner{
    background:var(--glass-strong); backdrop-filter:blur(18px); -webkit-backdrop-filter:blur(18px);
    border:1px solid var(--border); border-radius:999px; padding:8px; display:flex; gap:4px; justify-content:center;
    box-shadow:0 8px 32px rgba(140,120,200,0.18);
  }
  .navbar-inner a{
    font-family:var(--body); font-weight:600; font-size:12px; color:var(--ink-dim); text-decoration:none;
    padding:9px 16px; border-radius:999px; white-space:nowrap; transition:background .25s, color .25s;
  }
  .navbar-inner a:hover{ color:var(--ink); }
  .navbar-inner a.active{ background:var(--ink); color:#fff; }
  @media (max-width:480px){ .navbar-inner a{ padding:9px 11px; font-size:11px; } }

  /* ---------- section scaffolding ---------- */
  section, header.hero{ padding:76px 0 20px; position:relative; z-index:1; }
  section{ padding-bottom:70px; }
  .section-head{ text-align:center; margin-bottom:46px; }
  .section-eyebrow{ font-family:var(--body); font-weight:700; font-size:11px; letter-spacing:0.16em; text-transform:uppercase; color:var(--lilac); }
  .section-title{ font-family:var(--display); font-style:italic; font-weight:600; font-size:2.3rem; letter-spacing:-0.01em; color:var(--ink); margin-top:6px; }

  /* ---------- glass panel base ---------- */
  .glass{ background:var(--glass); backdrop-filter:blur(20px); -webkit-backdrop-filter:blur(20px); border:1px solid var(--border); border-radius:28px; box-shadow:0 12px 40px rgba(140,120,200,0.16); }

  /* ---------- hero ---------- */
  header.hero{ padding-top:56px; text-align:center; }
  .eyebrow{ display:inline-block; font-family:var(--body); font-weight:700; font-size:11.5px; letter-spacing:0.08em; text-transform:uppercase; color:var(--ink-dim); background:var(--glass-strong); border:1px solid var(--border); padding:9px 20px; border-radius:999px; backdrop-filter:blur(12px); }
  h1{ font-family:var(--display); font-style:italic; font-weight:600; font-size:clamp(3rem, 8.5vw, 5.2rem); line-height:1.04; letter-spacing:-0.01em; color:var(--ink); margin-top:24px; }
  .role{ font-family:var(--body); font-weight:700; font-size:0.9rem; letter-spacing:0.14em; text-transform:uppercase; color:var(--ink-dim); margin-top:16px; }
  .role::before, .role::after{ content:'·'; color:var(--gold); margin:0 10px; }
  .objective{ max-width:50ch; margin:26px auto 0; color:var(--ink-dim); font-size:1.02rem; }
  .cta-row{ display:flex; flex-wrap:wrap; gap:14px; margin-top:36px; justify-content:center; }
  .btn{ font-family:var(--body); font-weight:700; font-size:13.5px; padding:15px 28px; text-decoration:none; transition:all .25s; border-radius:999px; }
  .btn.primary{ background:linear-gradient(135deg, var(--rose), var(--gold)); color:#3a2418; box-shadow:0 10px 26px rgba(255,155,179,0.4); }
  .btn.primary:hover{ transform:translateY(-2px); box-shadow:0 16px 32px rgba(255,155,179,0.5); }
  .btn.ghost{ color:var(--ink); background:var(--glass-strong); border:1px solid var(--border); backdrop-filter:blur(12px); }
  .btn.ghost:hover{ transform:translateY(-2px); background:#fff; }

  /* ---------- about ---------- */
  .about-grid{ display:grid; grid-template-columns:1.1fr 0.9fr; gap:26px; align-items:stretch; margin-top:10px; }
  @media (max-width:700px){ .about-grid{ grid-template-columns:1fr; } }
  .about-card{ padding:36px 32px; }
  .about-card p{ color:var(--ink-dim); margin-bottom:15px; }
  .about-card p:last-child{ margin-bottom:0; }
  .about-card strong{ color:var(--ink); font-weight:700; }
  .stat-card{ padding:30px 28px; display:flex; flex-direction:column; justify-content:center; }
  .stat-row{ display:flex; justify-content:space-between; gap:14px; align-items:baseline; padding:13px 0; border-bottom:1px solid rgba(122,110,147,0.18); font-size:13.5px; }
  .stat-row:last-child{ border-bottom:none; }
  .stat-label{ color:var(--ink-faint); font-weight:600; text-transform:uppercase; letter-spacing:0.04em; font-size:11px; }
  .stat-value{ color:var(--ink); font-weight:700; text-align:right; font-family:var(--display); font-size:1.05rem; }

  /* ---------- skills ---------- */
  .skills-grid{ display:grid; grid-template-columns:repeat(3,1fr); gap:18px; margin-top:10px; }
  @media (max-width:700px){ .skills-grid{ grid-template-columns:1fr 1fr; } }
  @media (max-width:480px){ .skills-grid{ grid-template-columns:1fr; } }
  .skill-card{ padding:24px 20px; transition:transform .3s, box-shadow .3s; }
  .skill-card:hover{ transform:translateY(-6px); box-shadow:0 20px 44px rgba(140,120,200,0.24); }
  .skill-icon{ font-size:1.7rem; display:block; margin-bottom:12px; }
  .skill-card h4{ font-family:var(--display); font-style:italic; font-weight:600; font-size:1.15rem; color:var(--ink); }
  .skill-card p{ font-size:0.85rem; color:var(--ink-dim); margin-top:7px; }
  .skill-tags{ margin-top:13px; display:flex; flex-wrap:wrap; gap:6px; }
  .mini-tag{ font-family:var(--body); font-weight:700; font-size:10px; color:var(--ink); background:rgba(182,163,232,0.22); padding:4px 10px; border-radius:999px; }

  /* ---------- projects ---------- */
  .cards{ display:grid; grid-template-columns:repeat(3,1fr); gap:18px; margin-top:10px; }
  @media (max-width:700px){ .cards{ grid-template-columns:1fr; } }
  .card{ padding:26px 22px 26px; display:flex; flex-direction:column; transition:transform .3s, box-shadow .3s; }
  .card:hover{ transform:translateY(-6px); box-shadow:0 22px 46px rgba(140,120,200,0.26); }
  .card .tag-top{ font-family:var(--body); font-weight:700; font-size:10px; letter-spacing:0.06em; text-transform:uppercase; color:var(--ink-dim); }
  .card h3{ font-family:var(--display); font-style:italic; font-weight:600; font-size:1.3rem; margin:14px 0 10px; color:var(--ink); }
  .card p{ font-size:0.88rem; color:var(--ink-dim); flex-grow:1; }
  .card a.link{ margin-top:18px; font-family:var(--body); font-weight:700; font-size:12.5px; color:var(--ink); text-decoration:none; display:inline-flex; align-items:center; gap:5px; align-self:flex-start; border-bottom:2px solid var(--gold); padding-bottom:2px; }
  .card a.link:hover{ border-color:var(--rose); }

  /* ---------- footer ---------- */
  footer{ padding:76px 0 90px; text-align:center; }
  .footer-card{ padding:52px 40px; position:relative; overflow:hidden; }
  @media (max-width:640px){ .footer-card{ padding:34px 22px; } }
  footer h2{ font-family:var(--display); font-style:italic; font-weight:600; font-size:clamp(2rem,5vw,2.8rem); color:var(--ink); }
  footer .sub{ color:var(--ink-dim); margin:16px auto 0; max-width:46ch; }
  .connect-row{ margin-top:34px; display:flex; flex-wrap:wrap; gap:12px; justify-content:center; }
  .connect-row a{ font-family:var(--body); font-weight:700; font-size:13px; color:var(--ink); text-decoration:none; background:var(--glass-strong); border:1px solid var(--border); padding:13px 22px; border-radius:999px; transition:all .25s; backdrop-filter:blur(10px); }
  .connect-row a:hover{ background:#fff; transform:translateY(-2px); box-shadow:0 10px 24px rgba(140,120,200,0.2); }
  .fine{ margin-top:30px; font-size:11.5px; color:var(--ink-faint); font-family:var(--body); font-weight:600; }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    .card, .skill-card, .navbar-inner a, .btn, .connect-row a{ transition:none; }
  }
</style>
</head>
<body>

<div class="navbar">
  <div class="navbar-inner" id="navlinks">
    <a href="#home" class="active" data-file="home">Home</a>
    <a href="#about" data-file="about">About</a>
    <a href="#skills" data-file="skills">Skills</a>
    <a href="#project" data-file="project">Project</a>
    <a href="#contact" data-file="contact">Contact</a>
  </div>
</div>

<header class="hero" id="home">
  <div class="wrap">
    <p class="eyebrow">Open to Software Developer roles</p>
    <h1>Hi, I'm Dharshini</h1>
    <p class="role">3rd Year IT Student</p>
    <p class="objective">3rd-year B.Tech IT student who builds things end to end — front to back, and increasingly cloud to secure. I'm looking for an entry-level Software Developer / Full-Stack Engineer role where I can build scalable applications and keep growing into cloud infrastructure and secure software design.</p>
    <div class="cta-row">
      <a class="btn primary" href="#skills">Explore my skills</a>
      <a class="btn ghost" href="#contact">Contact me</a>
    </div>
  </div>
</header>

<section id="about">
  <div class="wrap">
    <div class="section-head">
      <div class="section-eyebrow">Get to know me</div>
      <h2 class="section-title">About</h2>
    </div>
    <div class="about-grid">
      <div class="about-card glass">
        <p><strong>Hello 👋</strong> — I'm Dharshini R J, an IT Student who likes building real, working software more than just studying it.</p>
        <p>My internship experience spans <strong>full-stack development</strong>, <strong>Python AI/ML</strong>, and <strong>cloud &amp; cybersecurity fundamentals</strong> — I try to understand a system from the interface all the way down to how it's secured and deployed.</p>
        <p>I like following an idea past the classroom — turning coursework into projects I actually finish and can show.</p>
      </div>
      <div class="stat-card glass">
        <div class="stat-row"><span class="stat-label">Name</span><span class="stat-value">Dharshini R J</span></div>
        <div class="stat-row"><span class="stat-label">Role</span><span class="stat-value">B.Tech IT</span></div>
        <div class="stat-row"><span class="stat-label">Focus</span><span class="stat-value">Full-Stack + Cloud</span></div>
      </div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="wrap">
    <div class="section-head">
      <div class="section-eyebrow">What I bring</div>
      <h2 class="section-title">My Skills</h2>
    </div>
    <div class="skills-grid">
      <div class="skill-card glass">
        <span class="skill-icon">🐍</span>
        <h4>Python</h4>
        <p>Core language for scripting, AI/ML work, and application logic.</p>
        <div class="skill-tags"><span class="mini-tag">AI/ML</span><span class="mini-tag">CLI tools</span></div>
      </div>
      <div class="skill-card glass">
        <span class="skill-icon">☕</span>
        <h4>Java</h4>
        <p>Used for algorithmic problem-solving, including constraint-based logic.</p>
        <div class="skill-tags"><span class="mini-tag">Algorithms</span></div>
      </div>
      <div class="skill-card glass">
        <span class="skill-icon">🌐</span>
        <h4>HTML &amp; CSS</h4>
        <p>Building structured, clean front-end interfaces.</p>
        <div class="skill-tags"><span class="mini-tag">Frontend</span></div>
      </div>
      <div class="skill-card glass">
        <span class="skill-icon">☁️</span>
        <h4>AWS &amp; Cloud</h4>
        <p>Solutions-architecture fundamentals — explaining and costing cloud designs.</p>
        <div class="skill-tags"><span class="mini-tag">AWS basics</span></div>
      </div>
      <div class="skill-card glass">
        <span class="skill-icon">🗄️</span>
        <h4>SQL &amp; Git</h4>
        <p>Basic SQL for data work, Git/GitHub for version control.</p>
        <div class="skill-tags"><span class="mini-tag">SQL (basic)</span><span class="mini-tag">Git</span></div>
      </div>
    </div>
  </div>
</section>

<section id="project">
  <div class="wrap">
    <div class="section-head">
      <div class="section-eyebrow">Things I've made</div>
      <h2 class="section-title">Project</h2>
    </div>
    <div class="cards">
      <div class="card glass">
        <span class="tag-top">Python · CLI</span>
        <h3>Smart Task Manager</h3>
        <p>A Python CLI task manager built on dictionaries and JSON, handling storage, sorting, and task priority without a database.</p>
      </div>
      <div class="card glass">
        <span class="tag-top">Java · Algorithms</span>
        <h3>Java Sudoku Solver</h3>
        <p>A Java program that solves Sudoku puzzles algorithmically — constraint logic applied to a familiar grid.</p>
        <a class="link" href="https://github.com/dharshinirj-beep/Sudoku-solver" target="_blank" rel="noopener">View on GitHub →</a>
      </div>
      <div class="card glass">
        <span class="tag-top">Python · AI/ML</span>
        <h3>AI-Driven Sales Forecasting</h3>
        <p>A predictive analytics project applying AI/ML techniques to forecast sales trends from historical data.</p>
        <a class="link" href="https://github.com/dharshinirj-beep/notebooks-Sales-Forecasting-using-AI.ipynb" target="_blank" rel="noopener">View on GitHub →</a>
      </div>
    </div>
  </div>
</section>

<footer id="contact">
  <div class="wrap">
    <div class="footer-card glass">
      <h2>Let's connect 🚀</h2>
      <p class="sub">I'm open to entry-level Software Developer and Full-Stack Engineer roles. Reach out directly — I reply quickly.</p>
      <div class="connect-row">
        <a href="mailto:dharshinidhanya80@gmail.com">✉ Email</a>
        <a href="https://github.com/dharshinirj-beep" target="_blank" rel="noopener">GitHub ↗</a>
        <a href="#" target="_blank" rel="noopener">LinkedIn ↗</a>
      </div>
      <p class="fine">Designed &amp; built by Dharshini R J</p>
    </div>
  </div>
</footer>

<script>
  const sections = ['home','about','skills','project','contact'].map(id => document.getElementById(id));
  const navLinks = document.querySelectorAll('.navbar-inner a');

  const setActive = (id) => {
    navLinks.forEach(a => a.classList.toggle('active', a.dataset.file === id));
  };

  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if(entry.isIntersecting){
        setActive(entry.target.id);
      }
    });
  }, { rootMargin: '-40% 0px -55% 0px', threshold: 0 });

  sections.forEach(s => s && observer.observe(s));
</script>

</body>
</html>
