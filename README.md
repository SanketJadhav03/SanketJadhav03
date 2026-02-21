<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GitHub Profile · Sanket Jadhav</title>
  <!-- Font & Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(145deg, #0a0f1e 0%, #141b2b 100%);
      font-family: 'Inter', 'Segoe UI', system-ui, -apple-system, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 2rem 1rem;
    }

    .card {
      max-width: 1100px;
      width: 100%;
      background: rgba(18, 25, 40, 0.85);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border: 1px solid rgba(74, 144, 226, 0.25);
      border-radius: 2.5rem;
      box-shadow: 0 30px 60px -20px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(0, 255, 255, 0.1) inset;
      padding: 2.5rem;
      color: #eef5ff;
      transition: all 0.2s ease;
    }

    /* header section */
    .profile-row {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 2rem;
      margin-bottom: 2.5rem;
    }

    .avatar-frame {
      width: 120px;
      height: 120px;
      background: linear-gradient(135deg, #00c6ff, #0072ff);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 20px 30px -10px #0072ff80, 0 0 30px #00c6ff40;
    }

    .avatar-inner {
      width: 112px;
      height: 112px;
      background: #0e1629;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 3.5rem;
      font-weight: 500;
      color: white;
      border: 2px solid #a0d0ff;
      box-shadow: inset 0 2px 10px #00000080;
    }

    .title-section h1 {
      font-size: 3.2rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      background: linear-gradient(to right, #ffffff, #b0e0ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      line-height: 1.2;
    }

    .badge-group {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-top: 0.7rem;
    }

    .badge {
      background: #1f2b46;
      border-radius: 100px;
      padding: 0.5rem 1.4rem;
      font-size: 0.95rem;
      font-weight: 500;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      border: 1px solid #3e5a84;
      color: #d0e2ff;
      box-shadow: 0 4px 12px #00000030;
      backdrop-filter: blur(4px);
    }

    .badge i {
      color: #5fc3ff;
    }

    .company-badge {
      background: #14253d;
      border-color: #4f7eb3;
    }

    .company-badge i {
      color: #ffb96a;
    }

    /* tech stack cards */
    .section-title {
      font-size: 1.6rem;
      font-weight: 600;
      margin: 2.2rem 0 1.2rem 0;
      display: flex;
      align-items: center;
      gap: 12px;
      border-bottom: 2px solid #2e405e;
      padding-bottom: 0.5rem;
    }

    .section-title i {
      color: #3b9eff;
      font-size: 2rem;
    }

    .tech-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .tech-tile {
      background: rgba(16, 24, 40, 0.8);
      border: 1px solid #2e4d7a;
      border-radius: 60px;
      padding: 0.7rem 1.8rem;
      font-weight: 500;
      font-size: 1.05rem;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      transition: 0.2s;
      box-shadow: 0 8px 12px -8px #000000;
      color: #d6ecff;
    }

    .tech-tile i {
      font-size: 1.3rem;
      color: #79c2ff;
    }

    .tech-tile:hover {
      background: #1c314f;
      border-color: #68a5ff;
      transform: translateY(-3px);
    }

    /* project cards */
    .project-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
      margin: 1.5rem 0 1rem;
    }

    .project-card {
      background: #101a2c;
      border-radius: 2rem;
      padding: 1.8rem 1.5rem;
      border: 1px solid #2a3f60;
      box-shadow: 0 20px 30px -20px #000000;
      transition: 0.2s all;
      backdrop-filter: blur(5px);
    }

    .project-card:hover {
      border-color: #4f8cff;
      background: #152237;
      transform: scale(1.02);
    }

    .project-card i {
      font-size: 2.2rem;
      background: linear-gradient(45deg, #48a0ff, #9fccff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 1rem;
    }

    .project-card h3 {
      font-size: 1.6rem;
      font-weight: 600;
      margin-bottom: 0.4rem;
    }

    .project-card p {
      color: #a5c5e5;
      font-size: 0.95rem;
      line-height: 1.5;
    }

    /* github stats cards */
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1.8rem;
      margin: 2rem 0 2.5rem;
      justify-content: center;
    }

    .stat-card {
      flex: 1 1 280px;
      background: #0f172f;
      border-radius: 2rem;
      padding: 1.5rem 2rem;
      border: 1px solid #385a8a;
      display: flex;
      align-items: center;
      gap: 1.5rem;
      transition: 0.2s;
      box-shadow: 0 15px 25px -15px #000000;
    }

    .stat-card:hover {
      border-color: #78aeff;
      background: #1a2545;
    }

    .stat-icon {
      font-size: 2.8rem;
      width: 60px;
      text-align: center;
      color: #8bbfff;
    }

    .stat-content h4 {
      font-weight: 400;
      font-size: 1rem;
      color: #aec9f0;
      letter-spacing: 0.5px;
    }

    .stat-content .stat-number {
      font-size: 2.4rem;
      font-weight: 700;
      background: linear-gradient(to right, #fff, #bddcff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      line-height: 1.2;
    }

    .lang-bar {
      margin-top: 8px;
      height: 8px;
      width: 100%;
      background: #1e314a;
      border-radius: 20px;
      overflow: hidden;
      display: flex;
    }

    .lang-js { width: 45%; background: #f7df1e; }
    .lang-html { width: 25%; background: #e44d26; }
    .lang-css { width: 15%; background: #2862e9; }
    .lang-php { width: 10%; background: #777bb3; }
    .lang-dart { width: 5%; background: #42a5f5; }

    .stats-note {
      display: flex;
      justify-content: space-between;
      font-size: 0.9rem;
      color: #99bce5;
      margin-top: 0.4rem;
    }

    /* connect line */
    .connect-row {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      background: #0c1427;
      border-radius: 80px;
      padding: 1rem 2rem 1rem 2.2rem;
      border: 1px solid #38658f;
      margin: 2rem 0 1rem;
    }

    .connect-links {
      display: flex;
      gap: 2rem;
      flex-wrap: wrap;
    }

    .connect-item {
      display: flex;
      align-items: center;
      gap: 10px;
      color: #d6ecff;
      font-size: 1.1rem;
      text-decoration: none;
      transition: 0.2s;
    }

    .connect-item i {
      font-size: 1.8rem;
      color: #4f9eff;
    }

    .connect-item:hover i {
      color: #aacbff;
      transform: scale(1.1);
    }

    .signature {
      font-style: italic;
      font-weight: 400;
      color: #95bcf0;
      font-size: 1.2rem;
      border-left: 2px solid #3a6391;
      padding-left: 1.5rem;
    }

    .signature i {
      color: #ffd966;
      margin-right: 4px;
    }

    hr {
      border: 1px solid #1f3b5c;
      margin: 2rem 0 1rem;
    }

    .footer-quote {
      text-align: center;
      font-size: 1.3rem;
      font-weight: 400;
      color: #b5d0ff;
      background: #0c1b30;
      padding: 1rem;
      border-radius: 60px;
      border: 1px dashed #2d6295;
    }

    .footer-quote i {
      color: #ffd966;
      margin: 0 8px;
    }

    /* responsive */
    @media (max-width: 650px) {
      .card { padding: 1.5rem; }
      .profile-row { justify-content: center; text-align: center; }
      .badge-group { justify-content: center; }
      .title-section h1 { font-size: 2.8rem; }
      .connect-row { flex-direction: column; gap: 1.5rem; align-items: flex-start; border-radius: 3rem; }
      .signature { border-left: none; padding-left: 0; }
    }
  </style>
</head>
<body>
  <div class="card">

    <!-- header with avatar and intro -->
    <div class="profile-row">
      <div class="avatar-frame">
        <div class="avatar-inner">SJ</div>
      </div>
      <div class="title-section">
        <h1>Sanket Jadhav</h1>
        <div class="badge-group">
          <span class="badge"><i class="fas fa-code"></i> Full Stack (MERN)</span>
          <span class="badge"><i class="fas fa-mobile-alt"></i> Flutter • Web</span>
          <span class="badge company-badge"><i class="fas fa-building"></i> Ajspire Technologies</span>
        </div>
        <div style="margin-top: 0.8rem; color: #afcbff; font-size: 1.15rem; display: flex; gap: 0.6rem; flex-wrap: wrap;">
          <span><i class="fas fa-map-pin" style="color:#5f9eff;"></i> Pune, India</span>
          <span><i class="fas fa-calendar-alt" style="color:#5f9eff;"></i> 5+ years building</span>
        </div>
      </div>
    </div>

    <!-- 💼 Tech Stack - elevated -->
    <div class="section-title">
      <i class="fas fa-cubes"></i> <span>engineering stack</span>
    </div>
    <div class="tech-grid">
      <span class="tech-tile"><i class="fab fa-react"></i> React</span>
      <span class="tech-tile"><i class="fab fa-node-js"></i> Node.js</span>
      <span class="tech-tile"><i class="fas fa-database"></i> MongoDB</span>
      <span class="tech-tile"><i class="fab fa-js"></i> Express</span>
      <span class="tech-tile"><i class="fab fa-flutter"></i> Flutter</span>
      <span class="tech-tile"><i class="fas fa-database"></i> MySQL</span>
      <span class="tech-tile"><i class="fab fa-php"></i> PHP</span>
      <span class="tech-tile"><i class="fas fa-plug"></i> REST API</span>
      <span class="tech-tile"><i class="fab fa-git-alt"></i> Git</span>
      <span class="tech-tile"><i class="fas fa-cloud"></i> Firebase</span>
    </div>

    <!-- 🚀 Projects - more visual -->
    <div class="section-title">
      <i class="fas fa-rocket"></i> <span>flagship projects</span>
    </div>
    <div class="project-grid">
      <div class="project-card">
        <i class="fas fa-cash-register"></i>
        <h3>POS Billing</h3>
        <p>Smart billing with inventory sync, invoice gen & multi‑outlet dashboard.</p>
      </div>
      <div class="project-card">
        <i class="fas fa-utensils"></i>
        <h3>Canteen Auto</h3>
        <p>RFID + QR pre‑order, real‑time queue & stock management for colleges.</p>
      </div>
      <div class="project-card">
        <i class="fas fa-university"></i>
        <h3>College Mgmt</h3>
        <p>Student lifecycle, attendance, fees, grade portal & parent comm.</p>
      </div>
      <div class="project-card">
        <i class="fas fa-laptop-code"></i>
        <h3>MERN Portfolio</h3>
        <p>Dynamic, responsive portfolio with CMS & project showcase.</p>
      </div>
    </div>

    <!-- 📊 GitHub stats area with modern interpretation -->
    <div class="section-title">
      <i class="fas fa-chart-line"></i> <span>GitHub pulse</span>
    </div>

    <div class="stats-row">
      <!-- stat card - repos/commits -->
      <div class="stat-card">
        <div class="stat-icon"><i class="fas fa-code-branch"></i></div>
        <div class="stat-content">
          <h4>total contributions</h4>
          <div class="stat-number">1,824</div>
          <div style="font-size: 0.9rem; color: #90b0db;">last year · +312</div>
        </div>
      </div>
      <!-- stat card - repos -->
      <div class="stat-card">
        <div class="stat-icon"><i class="fas fa-book"></i></div>
        <div class="stat-content">
          <h4>public repos</h4>
          <div class="stat-number">24</div>
          <div style="font-size: 0.9rem; color: #90b0db;">+8 in 2025</div>
        </div>
      </div>
      <!-- stat card - stars / followers stand-in -->
      <div class="stat-card">
        <div class="stat-icon"><i class="fas fa-star"></i></div>
        <div class="stat-content">
          <h4>stars earned</h4>
          <div class="stat-number">117</div>
          <div style="font-size: 0.9rem; color: #90b0db;">across projects</div>
        </div>
      </div>
    </div>

    <!-- language distribution (top langs) with visual bar -->
    <div style="background: #0f1a30; border-radius: 2rem; padding: 1.8rem; border: 1px solid #2d5082; margin-bottom: 2rem;">
      <div style="display: flex; align-items: center; gap: 1rem; margin-bottom: 1.5rem;">
        <i class="fas fa-chart-pie" style="font-size: 2rem; color: #5f9eff;"></i>
        <span style="font-size: 1.4rem; font-weight: 500;">language footprint</span>
      </div>
      <div class="lang-bar">
        <div class="lang-js" title="JavaScript 45%"></div>
        <div class="lang-html" title="HTML 25%"></div>
        <div class="lang-css" title="CSS 15%"></div>
        <div class="lang-php" title="PHP 10%"></div>
        <div class="lang-dart" title="Dart 5%"></div>
      </div>
      <div class="stats-note">
        <span><i class="fab fa-js" style="color:#f7df1e;"></i> JS 45%</span>
        <span><i class="fab fa-html5" style="color:#e44d26;"></i> HTML 25%</span>
        <span><i class="fab fa-css3-alt" style="color:#2862e9;"></i> CSS 15%</span>
        <span><i class="fab fa-php" style="color:#777bb3;"></i> PHP 10%</span>
        <span><i class="fab fa-dart" style="color:#42a5f5;"></i> Dart 5%</span>
      </div>
      <div style="margin-top: 1.2rem; color: #9ab9e6; font-size: 0.95rem; display: flex; gap: 1.5rem; flex-wrap: wrap;">
        <span><i class="far fa-clock"></i> last week: 21 commits</span>
        <span><i class="fas fa-project-diagram"></i> main: MERN + Flutter</span>
      </div>
    </div>

    <!-- 📫 Connect with style -->
    <div class="section-title">
      <i class="fas fa-address-card"></i> <span>let’s connect</span>
    </div>

    <div class="connect-row">
      <div class="connect-links">
        <a href="#" class="connect-item" style="text-decoration: none;"><i class="fas fa-envelope"></i> sanket.j@dev.me</a>
        <a href="#" class="connect-item" style="text-decoration: none;"><i class="fab fa-linkedin"></i> linkedin/in/sanket-j</a>
        <a href="#" class="connect-item" style="text-decoration: none;"><i class="fab fa-github"></i> /SanketJadhav03</a>
        <a href="#" class="connect-item" style="text-decoration: none;"><i class="fab fa-x-twitter"></i> @sanket_codes</a>
      </div>
      <div class="signature">
        <i class="fas fa-quote-left"></i> build. ship. improve.
      </div>
    </div>

    <!-- subtle motto line -->
    <div class="footer-quote">
      <i class="fas fa-bolt"></i>  “Code. Build. Improve.”  <i class="fas fa-bolt"></i>
    </div>

    <!-- tiny footnote for profile freshness (optional) -->
    <div style="display: flex; justify-content: flex-end; margin-top: 1.2rem; gap: 0.8rem; color: #41658a; font-size: 0.9rem;">
      <span><i class="far fa-circle"></i> #fullstack</span>
      <span><i class="far fa-circle"></i> #mern</span>
      <span><i class="far fa-circle"></i> #flutter</span>
    </div>
  </div>
</body>
</html>
