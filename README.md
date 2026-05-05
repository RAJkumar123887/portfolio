<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <meta name="description" content="Rajkumar Muddasani - Data Analyst, Front-end Developer, AI/ML Enthusiast. Professional portfolio showcasing data analytics, AI/ML projects, and full-stack development expertise.">
  <meta name="author" content="Rajkumar Muddasani">
  <!-- iOS / Android specific meta tags for polished Web App feel -->
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
  <meta name="theme-color" content="#0a0a0a" media="(prefers-color-scheme: dark)">
  <meta name="format-detection" content="telephone=no">
  <title>Rajkumar Muddasani | Data Analyst & AI/ML Portfolio</title>
  <!-- Boxicons & Google Fonts -->
  <link href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
    }

    body {
      color: #ededed;
      background: #0a0a0a;
      scroll-behavior: smooth;
      font-family: 'Poppins', sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    /* Header */
    .header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(10, 10, 10, 0.96);
      backdrop-filter: blur(12px);
      padding: 20px 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
      transition: 0.3s;
      border-bottom: 1px solid rgba(0, 238, 255, 0.25);
    }
    .header.sticky {
      padding: 14px 8%;
      background: #0a0a0a;
      box-shadow: 0 5px 25px rgba(0, 0, 0, 0.4);
    }
    .logo {
      font-size: 22px;
      font-weight: 700;
      color: #fff;
      text-decoration: none;
      letter-spacing: 0.5px;
    }
    .logo span {
      color: #0ef;
      font-weight: 800;
    }
    .navbar a {
      margin-left: 35px;
      text-decoration: none;
      font-size: 16px;
      font-weight: 500;
      color: #ededed;
      transition: 0.3s;
      cursor: pointer;
      position: relative;
    }
    .navbar a::after {
      content: '';
      position: absolute;
      bottom: -6px;
      left: 0;
      width: 0;
      height: 2px;
      background: #0ef;
      transition: 0.3s;
    }
    .navbar a:hover::after,
    .navbar a.active::after {
      width: 100%;
    }
    .navbar a:hover,
    .navbar a.active {
      color: #0ef;
    }
    #menu-icon {
      font-size: 36px;
      color: #fff;
      cursor: pointer;
      display: none;
    }

    /* Sections Base */
    section {
      padding: 120px 8% 90px;
    }
    .section-title {
      font-size: 2.8rem;
      text-align: center;
      margin-bottom: 3.5rem;
      color: #0ef;
      position: relative;
      font-weight: 700;
    }
    .section-title::after {
      content: '';
      position: absolute;
      bottom: -15px;
      left: 50%;
      transform: translateX(-50%);
      width: 100px;
      height: 4px;
      background: linear-gradient(90deg, #0ef, #0ac, #0ef);
      border-radius: 2px;
    }

    /* Availability Badge */
    .availability-badge {
      display: inline-flex;
      align-items: center;
      gap: 12px;
      background: rgba(0, 238, 255, 0.12);
      backdrop-filter: blur(4px);
      padding: 10px 24px;
      border-radius: 50px;
      margin-top: 20px;
      flex-wrap: wrap;
      border: 1px solid rgba(0, 238, 255, 0.3);
    }
    .availability-badge span {
      font-size: 14px;
      font-weight: 600;
      color: #0ef;
      letter-spacing: 0.5px;
    }
    .availability-badge i {
      font-size: 18px;
      color: #0ef;
    }

    /* Home Section */
    .home {
      min-height: 100vh;
      display: flex;
      align-items: center;
      gap: 5rem;
      padding-top: 140px;
      background: linear-gradient(135deg, #0a0a0a 0%, #0f0f1a 100%);
    }
    .home-content {
      flex: 1;
    }
    .home-content h1 {
      font-size: 4rem;
      font-weight: 800;
      margin: 0.5rem 0;
      background: linear-gradient(135deg, #fff, #0ef);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .home-content .title-role {
      font-size: 1.5rem;
      font-weight: 500;
      margin-bottom: 1rem;
    }
    .home-content .highlight {
      color: #0ef;
      font-weight: 700;
    }
    .home-content p {
      font-size: 1rem;
      line-height: 1.8;
      margin: 1.5rem 0;
      color: #ccc;
      max-width: 600px;
    }
    .home-sci {
      display: flex;
      gap: 18px;
      margin: 30px 0 25px;
    }
    .home-sci a {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 48px;
      height: 48px;
      background: transparent;
      border: 2px solid #0ef;
      border-radius: 50%;
      font-size: 24px;
      color: #0ef;
      transition: 0.3s;
    }
    .home-sci a:hover {
      background: #0ef;
      color: #0a0a0a;
      transform: translateY(-5px);
      box-shadow: 0 0 20px #0ef;
    }
    .btn {
      display: inline-block;
      padding: 14px 38px;
      background: linear-gradient(135deg, #0ef, #0ac);
      border-radius: 50px;
      font-size: 16px;
      font-weight: 700;
      color: #0a0a0a;
      text-decoration: none;
      transition: 0.3s;
      box-shadow: 0 5px 15px rgba(0, 238, 255, 0.3);
      margin-top: 10px;
      border: none;
      cursor: pointer;
      letter-spacing: 0.5px;
    }
    .btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 10px 25px rgba(0, 238, 255, 0.5);
    }
    .btn-outline {
      background: transparent;
      border: 2px solid #0ef;
      color: #0ef;
      box-shadow: none;
      margin-left: 18px;
    }
    .btn-outline:hover {
      background: #0ef;
      color: #0a0a0a;
    }
    .home-img {
      flex: 1;
      display: flex;
      justify-content: center;
    }
    
    /* Professional Circular Image Frame - Perfect Fit */
    .profile-frame {
      position: relative;
      width: 380px;
      height: 380px;
      border-radius: 50%;
      border: 5px solid #0ef;
      box-shadow: 0 0 40px rgba(0, 238, 255, 0.4);
      overflow: hidden;
      transition: 0.3s;
      background: transparent;
    }
    .profile-frame:hover {
      transform: scale(1.02);
      box-shadow: 0 0 55px #0ef;
    }
    .profile-frame img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center 25%;
      display: block;
      transform: scale(1.12);
    }

    /* About Section */
    .about {
      background: #0f0f0f;
    }
    .about-content {
      max-width: 1100px;
      margin: 0 auto;
    }
    .about-text p {
      margin-bottom: 1.2rem;
      line-height: 1.9;
      color: #ccc;
      text-align: justify;
      font-size: 1rem;
    }
    .skills-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 14px;
      margin: 35px 0;
    }
    .skill-tag {
      background: #1a1a1a;
      padding: 10px 24px;
      border-radius: 50px;
      font-size: 14px;
      font-weight: 600;
      color: #0ef;
      border: 1px solid rgba(0, 238, 255, 0.4);
      transition: 0.2s;
    }
    .skill-tag:hover {
      background: #0ef;
      color: #0a0a0a;
      transform: translateY(-3px);
      border-color: #0ef;
    }
    
    /* Work Preference Cards */
    .work-preference {
      background: linear-gradient(135deg, #111, #1a1a1a);
      border-radius: 20px;
      padding: 25px;
      margin: 30px 0 20px;
      text-align: center;
      border: 1px solid rgba(0, 238, 255, 0.2);
    }
    .work-preference h4 {
      color: #0ef;
      font-size: 1.2rem;
      margin-bottom: 15px;
      font-weight: 600;
    }
    .preference-icons {
      display: flex;
      justify-content: center;
      gap: 35px;
      flex-wrap: wrap;
    }
    .pref-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 8px;
    }
    .pref-item i {
      font-size: 28px;
      color: #0ef;
    }
    .pref-item span {
      font-size: 13px;
      font-weight: 500;
      color: #ccc;
    }
    
    .info-row {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      margin-top: 2rem;
      padding-top: 2rem;
      border-top: 1px solid #2a2a2a;
    }
    .info-col {
      flex: 1;
      min-width: 200px;
    }
    .info-col h4 {
      color: #0ef;
      margin-bottom: 15px;
      font-size: 1.2rem;
      font-weight: 600;
    }
    .info-col p {
      margin: 8px 0;
      font-size: 14px;
      color: #bbb;
    }

    /* Experience Section */
    .experience {
      background: #0a0a0a;
    }
    .timeline {
      max-width: 1000px;
      margin: 0 auto;
    }
    .exp-card {
      background: #111;
      border-radius: 24px;
      padding: 2rem;
      margin-bottom: 2rem;
      border-left: 5px solid #0ef;
      transition: 0.3s;
    }
    .exp-card:hover {
      transform: translateX(10px);
      background: #181818;
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
    }
    .exp-header {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      margin-bottom: 1rem;
    }
    .exp-header h3 {
      font-size: 1.5rem;
      color: #fff;
      font-weight: 700;
    }
    .exp-date {
      color: #0ef;
      font-weight: 600;
      background: rgba(0, 238, 255, 0.1);
      padding: 4px 14px;
      border-radius: 30px;
      font-size: 0.85rem;
    }
    .exp-company {
      color: #aaa;
      margin-bottom: 15px;
      font-size: 0.95rem;
      font-weight: 500;
    }
    .exp-card ul {
      padding-left: 1.2rem;
    }
    .exp-card li {
      margin: 10px 0;
      color: #ccc;
      line-height: 1.7;
    }

    /* Projects */
    .projects {
      background: #0f0f0f;
    }
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));
      gap: 2rem;
      max-width: 1400px;
      margin: 0 auto;
    }
    .project-card {
      background: #111;
      border-radius: 24px;
      padding: 2rem;
      transition: 0.3s;
      border: 1px solid #2a2a2a;
    }
    .project-card:hover {
      transform: translateY(-8px);
      border-color: #0ef;
      box-shadow: 0 15px 35px rgba(0, 238, 255, 0.15);
    }
    .project-card h3 {
      font-size: 1.4rem;
      margin-bottom: 0.7rem;
      color: #0ef;
    }
    .project-tech {
      font-size: 0.8rem;
      color: #aaa;
      margin-bottom: 1.2rem;
      font-family: monospace;
      letter-spacing: 0.5px;
    }
    .project-card p {
      color: #bbb;
      line-height: 1.7;
      margin-bottom: 1.5rem;
    }
    .project-link {
      color: #0ef;
      text-decoration: none;
      font-weight: 600;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      margin-right: 20px;
      font-size: 0.9rem;
      transition: 0.2s;
    }
    .project-link:hover {
      text-decoration: underline;
      gap: 12px;
    }

    /* Contact Section */
    .contact {
      background: #0a0a0a;
    }
    .contact-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
      gap: 3.5rem;
      max-width: 1200px;
      margin: 0 auto;
    }
    .contact-info h3, .contact-form h3 {
      font-size: 2rem;
      margin-bottom: 1.8rem;
      color: #0ef;
      font-weight: 700;
    }
    .contact-details p {
      margin: 1.2rem 0;
      display: flex;
      align-items: center;
      gap: 15px;
      font-size: 1rem;
    }
    .contact-details i {
      font-size: 28px;
      color: #0ef;
    }
    .contact-form form {
      display: flex;
      flex-direction: column;
      gap: 1.3rem;
    }
    .contact-form input, .contact-form textarea {
      padding: 16px;
      background: #111;
      border: 1px solid #333;
      border-radius: 16px;
      font-size: 1rem;
      color: #fff;
      transition: 0.3s;
      font-family: inherit;
    }
    .contact-form input:focus, .contact-form textarea:focus {
      border-color: #0ef;
      outline: none;
      box-shadow: 0 0 10px rgba(0, 238, 255, 0.2);
    }
    .footer {
      text-align: center;
      padding: 2rem;
      background: #050505;
      border-top: 1px solid #1a1a1a;
    }
    .footer p {
      color: #aaa;
      font-size: 0.9rem;
      letter-spacing: 0.5px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-wrap: wrap;
      gap: 8px;
    }
    .footer .portfolio-name {
      color: #0ef;
      font-weight: 700;
      background: rgba(0, 238, 255, 0.12);
      padding: 4px 14px;
      border-radius: 40px;
      font-size: 0.85rem;
      letter-spacing: 0.8px;
    }
    .footer i {
      font-size: 16px;
      color: #0ef;
    }

    /* Hidden class */
    .section-hidden {
      display: none !important;
    }

    /* ========== ANDROID & iOS SPECIFIC CUSTOMIZATION ========== */
    @supports (-webkit-overflow-scrolling: touch) {
      body {
        -webkit-overflow-scrolling: touch;
      }
    }
    .btn, .home-sci a, .skill-tag, .project-link, .navbar a {
      cursor: pointer;
      -webkit-tap-highlight-color: rgba(0, 238, 255, 0.25);
    }
    @media (hover: hover) {
      .btn:hover, .home-sci a:hover {
        transform: translateY(-3px);
      }
    }
    @media (hover: none) {
      .btn:active, .home-sci a:active {
        transform: scale(0.96);
        transition: 0.05s;
      }
      .project-card:active, .exp-card:active {
        transform: scale(0.99);
      }
    }
    ::-webkit-scrollbar {
      width: 5px;
      background: #1a1a1a;
    }
    ::-webkit-scrollbar-thumb {
      background: #0ef;
      border-radius: 10px;
    }
    @media (max-width: 992px) {
      .home {
        flex-direction: column-reverse;
        text-align: center;
        padding-top: 150px;
        gap: 2rem;
      }
      .home-content p {
        margin-left: auto;
        margin-right: auto;
      }
      .home-sci {
        justify-content: center;
      }
      .section-title {
        font-size: 2.2rem;
      }
      .profile-frame {
        width: 300px;
        height: 300px;
      }
    }
    @media (max-width: 768px) {
      #menu-icon {
        display: block;
      }
      .navbar {
        position: absolute;
        top: 100%;
        left: -100%;
        width: 100%;
        background: rgba(10, 10, 10, 0.98);
        backdrop-filter: blur(20px);
        padding: 25px 0;
        transition: 0.3s ease-in-out;
        text-align: center;
        border-bottom: 1px solid #0ef;
      }
      .navbar.active {
        left: 0;
      }
      .navbar a {
        display: block;
        margin: 15px 0;
        font-size: 18px;
      }
      .home-content h1 {
        font-size: 2.5rem;
      }
      .projects-grid {
        grid-template-columns: 1fr;
      }
      .profile-frame {
        width: 260px;
        height: 260px;
      }
      .btn-outline {
        margin-left: 10px;
      }
      .preference-icons {
        gap: 20px;
      }
      .header {
        padding-top: max(20px, env(safe-area-inset-top));
        padding-left: max(8%, env(safe-area-inset-left));
        padding-right: max(8%, env(safe-area-inset-right));
      }
      section {
        padding-left: max(8%, env(safe-area-inset-left));
        padding-right: max(8%, env(safe-area-inset-right));
      }
    }
  </style>
</head>
<body>

<header class="header">
  <a href="#" class="logo" id="homeLogoLink">Rajkumar <span>Muddasani</span></a>
  <div class="navbar">
    <a class="nav-link" data-target="home">Home</a>
    <a class="nav-link" data-target="about">About</a>
    <a class="nav-link" data-target="experience">Experience</a>
    <a class="nav-link" data-target="projects">Projects</a>
    <a class="nav-link" data-target="contact">Contact</a>
  </div>
  <i class='bx bx-menu' id="menu-icon"></i>
</header>

<!-- ==================== HOME SECTION ==================== -->
<section id="home" class="home">
  <div class="home-content">
    <h1>Rajkumar Muddasani</h1>
    <div class="title-role"><span class="highlight">Data Analyst & AI/ML Engineer</span></div>
    <p>Results-driven technology professional with 2+ years of experience in Data Analytics, Front-end Development, and AI/ML. Proficient in Power BI, Python, SQL, and React.js. Passionate about leveraging machine learning and AI-powered tools to deliver actionable business insights that drive organizational growth.</p>
    <div class="availability-badge">
      <i class='bx bx-briefcase'></i>
      <span>Open to Work</span>
      <i class='bx bx-dots-vertical-rounded'></i>
      <span>On-site</span>
      <i class='bx bx-dots-vertical-rounded'></i>
      <span>Hybrid</span>
      <i class='bx bx-dots-vertical-rounded'></i>
      <span>Remote</span>
    </div>
    <div class="home-sci">
      <a href="https://www.linkedin.com/in/muddasani-rajkumar/" target="_blank"><i class='bx bxl-linkedin'></i></a>
      <a href="https://github.com/RAJkumar123887" target="_blank"><i class='bx bxl-github'></i></a>
      <a href="https://rajkumar123887.github.io/AIML/" target="_blank"><i class='bx bx-brain'></i></a>
      <a href="https://wa.me/919705515734" target="_blank"><i class='bx bxl-whatsapp'></i></a>
    </div>
    <div>
      <a href="#" class="btn" id="hireMeBtn">Hire Me</a>
      <a href="#" class="btn btn-outline" id="viewProjectsBtn">View Projects</a>
    </div>
  </div>
  <div class="home-img">
    <div class="profile-frame">
      <img id="profileImage" src="https://github.com/RAJkumar123887/PORTFOLIO/blob/main/passport.jpeg?raw=true" alt="Rajkumar Muddasani - Professional Photo" onerror="this.src='https://via.placeholder.com/400x400?text=Photo'">
    </div>
  </div>
</section>

<!-- ==================== ABOUT SECTION ==================== -->
<section id="about" class="about section-hidden">
  <h2 class="section-title">About Me</h2>
  <div class="about-content">
    <div class="about-text">
      <p>I'm Rajkumar Muddasani, a Data Analyst and Front-end Developer with strong expertise in AI/ML. I specialize in transforming raw data into actionable insights and building interactive dashboards that empower businesses. With hands-on experience in Python, Power BI, SQL, and modern web frameworks, I help organizations make data-driven decisions that deliver measurable results.</p>
      <p>Data Analyst and Full-Stack Developer with over 2 years of experience in delivering data-driven insights and building scalable web applications. Proficient in data analysis, business intelligence, and machine learning, with strong expertise in Python, SQL, and Power BI, along with modern web technologies including React.js and Django. Demonstrated success in developing predictive models, achieving up to 82% accuracy in HR attrition analysis and 79% accuracy in customer churn prediction.</p>
      <p>Experienced in designing interactive dashboards, optimizing data pipelines, and automating reporting processes to enhance business decision-making and operational efficiency. Adept at integrating advanced AI solutions using OpenAI API and LangChain to streamline workflows and enable intelligent automation. Committed to delivering high-quality, impactful solutions that drive business value.</p>
    </div>
    
    <div class="work-preference">
      <h4><i class='bx bx-briefcase'></i> Work Availability</h4>
      <div class="preference-icons">
        <div class="pref-item"><i class='bx bx-buildings'></i><span>On-site</span></div>
        <div class="pref-item"><i class='bx bx-calendar'></i><span>Hybrid</span></div>
        <div class="pref-item"><i class='bx bx-wifi'></i><span>Remote</span></div>
      </div>
    </div>
    
    <div class="skills-grid">
      <span class="skill-tag">Python</span><span class="skill-tag">Power BI</span><span class="skill-tag">SQL</span>
      <span class="skill-tag">React.js</span><span class="skill-tag">HTML5</span><span class="skill-tag">CSS3</span>
      <span class="skill-tag">JavaScript</span><span class="skill-tag">Advanced Excel</span><span class="skill-tag">PowerPoint</span>
      <span class="skill-tag">Machine Learning</span><span class="skill-tag">LangChain</span><span class="skill-tag">Pandas/NumPy</span>
      <span class="skill-tag">Scikit-learn</span><span class="skill-tag">Django</span><span class="skill-tag">Streamlit</span>
      <span class="skill-tag">OpenAI API</span><span class="skill-tag">Generative AI</span><span class="skill-tag">Power Query</span>
    </div>
    <div class="info-row">
      <div class="info-col"><h4>Education</h4><p>B.Tech - Computer Science & Engineering</p><p>CSI Wesley Institute of Technology & Science</p><p>Intermediate (MPC), SR Junior College</p></div>
      <div class="info-col"><h4>Location</h4><p>Hyderabad, Telangana, India</p><p>Open to Relocation</p><p>Available Worldwide</p></div>
      <div class="info-col"><h4>Languages</h4><p>English (Professional Fluency)</p><p>Telugu (Native)</p><p>Hindi (Conversational)</p></div>
    </div>
  </div>
</section>

<!-- ==================== EXPERIENCE SECTION ==================== -->
<section id="experience" class="experience section-hidden">
  <h2 class="section-title">Professional Experience</h2>
  <div class="timeline">
    <div class="exp-card">
      <div class="exp-header"><h3>Data Analyst (Freelance)</h3><span class="exp-date">Aug 2024 – Aug 2025</span></div>
      <div class="exp-company">RATECHI — Hyderabad, India</div>
      <ul><li>Performed end-to-end data cleaning, transformation, and preparation on large business datasets ensuring accuracy and consistency.</li><li>Wrote complex SQL queries to extract trends; built interactive Power BI dashboards tracking KPIs, sales metrics, and operational performance.</li><li>Reduced manual reporting effort by ~35% and delivered Python-based customer segmentation for targeted marketing decisions.</li><li>Conducted exploratory data analysis using Pandas/NumPy and presented insights via PowerPoint reports to stakeholders.</li></ul>
    </div>
    <div class="exp-card">
      <div class="exp-header"><h3>Frontend Developer (Freelance)</h3><span class="exp-date">Aug 2023 – Jul 2024</span></div>
      <div class="exp-company">RATECHI — Hyderabad, India</div>
      <ul><li>Designed responsive websites using React.js, HTML5, CSS3, and JavaScript; optimized Core Web Vitals and SEO achieving 90+ performance scores.</li><li>Integrated REST APIs, contact forms, and Google Analytics, improving user engagement by 22%.</li><li>Built component-based SPAs and enhanced UI/UX for measurable retention gains across client platforms.</li></ul>
    </div>
  </div>
</section>

<!-- ==================== PROJECTS SECTION ==================== -->
<section id="projects" class="projects section-hidden">
  <h2 class="section-title">Featured Projects</h2>
  <div class="projects-grid">
    <div class="project-card"><h3>Sales Performance Dashboard</h3><div class="project-tech">Power BI · SQL · Python · Power Query · Advanced Excel</div><p>Interactive enterprise dashboard tracking revenue KPIs, regional performance, and customer segmentation. Reduced manual reporting by ~35% and enabled real-time visibility for executive decisions.</p></div>
    <div class="project-card"><h3>Customer Churn Prediction</h3><div class="project-tech">Python · Scikit-learn · Pandas · SQL · Matplotlib</div><p>Machine learning model (Logistic Regression & Random Forest) achieving 79% accuracy. Feature engineering and EDA to identify key churn drivers, enabling proactive retention strategies.</p><a href="https://github.com/RAJkumar123887" target="_blank" class="project-link">GitHub Repository <i class='bx bx-link-external'></i></a></div>
    <div class="project-card"><h3>Smart HR Analytics Dashboard</h3><div class="project-tech">Streamlit · Scikit-learn · LangChain · OpenAI API · Plotly</div><p>AI-powered workforce intelligence platform: Random Forest attrition prediction (82% accuracy), NLP sentiment analysis on employee feedback, and natural language query interface for HR.</p><a href="https://rajkumar123887.github.io/AIML/" target="_blank" class="project-link">Live Demo <i class='bx bx-link-external'></i></a> <a href="https://github.com/RAJkumar123887/AIML" target="_blank" class="project-link">GitHub <i class='bx bxl-github'></i></a></div>
    <div class="project-card"><h3>RR TechCreative Blend (Full-Stack)</h3><div class="project-tech">React.js · Django REST · HTML5 · CSS3 · JavaScript · Google Maps API</div><p>Production-grade full-stack startup web application for AI & tech services. SPA with dark theme, dynamic service data, contact form, Google Maps integration, and responsive design.</p><a href="https://rrtechcreativeblend-create.github.io/RRTech/" target="_blank" class="project-link">Live Website <i class='bx bx-link-external'></i></a></div>
    <div class="project-card"><h3>RAG-POWER (RAG Chatbot)</h3><div class="project-tech">n8n · OpenAI API · Retrieval-Augmented Generation</div><p>Implemented end-to-end RAG chatbot workflow using n8n orchestration. Context-aware LLM responses with document retrieval, demonstrating advanced AI integration capabilities.</p><a href="https://github.com/RAJkumar123887/RAG-POWER" target="_blank" class="project-link">GitHub Repository <i class='bx bxl-github'></i></a></div>
  </div>
</section>

<!-- ==================== CONTACT SECTION ==================== -->
<section id="contact" class="contact section-hidden">
  <h2 class="section-title">Get In Touch</h2>
  <div class="contact-container">
    <div class="contact-info">
      <h3>Let's Connect</h3>
      <div class="contact-details">
        <p><i class='bx bx-map'></i> Alwal Hills, Hyderabad, India - 500010</p>
        <p><i class='bx bx-phone'></i> <a href="tel:+919705515734" style="color:#0ef;">+91 97055 15734</a></p>
        <p><i class='bx bx-envelope'></i> muddasanirajkumar908@gmail.com</p>
      </div>
      <div class="availability-badge" style="margin-top: 25px;">
        <i class='bx bx-briefcase'></i>
        <span>Open to: On-site · Hybrid · Remote</span>
      </div>
      <div class="home-sci" style="margin-top: 35px;">
        <a href="https://www.linkedin.com/in/muddasani-rajkumar/" target="_blank"><i class='bx bxl-linkedin'></i></a>
        <a href="https://github.com/RAJkumar123887" target="_blank"><i class='bx bxl-github'></i></a>
        <a href="https://wa.me/919705515734" target="_blank"><i class='bx bxl-whatsapp'></i></a>
      </div>
    </div>
    <div class="contact-form">
      <h3>Send a Message</h3>
      <form id="contactForm" action="#">
        <input type="text" placeholder="Full Name" required id="contactName">
        <input type="email" placeholder="Email Address" required id="contactEmail">
        <input type="text" placeholder="Subject" id="contactSubject">
        <textarea rows="5" placeholder="Your Message..." required id="contactMessage"></textarea>
        <button type="submit" class="btn" style="width:100%; text-align:center;">Send Message <i class='bx bx-send'></i></button>
      </form>
      <p id="formStatus" style="margin-top:15px; color:#0ef; font-size:14px;"></p>
    </div>
  </div>
</section>

<!-- ========== UPDATED FOOTER WITH PORTFOLIO NAME ========== -->
<footer class="footer">
  <p>
    <i class='bx bx-code-alt'></i>
    <span class="portfolio-name">RAJKUMAR MUDDASANI PORTFOLIO</span>
    <i class='bx bx-data'></i>
    <span style="color:#555;">|</span>
    <span>Data Analyst & AI/ML Engineer</span>
  </p>
</footer>

<script>
  // Navigation System (same as original robust implementation)
  const navLinks = document.querySelectorAll('.nav-link');
  const sections = document.querySelectorAll('section');
  
  function showSection(targetId, updateHash = true) {
    sections.forEach(section => {
      section.classList.add('section-hidden');
    });
    const activeSection = document.getElementById(targetId);
    if (activeSection) activeSection.classList.remove('section-hidden');
    
    navLinks.forEach(link => {
      if (link.getAttribute('data-target') === targetId) {
        link.classList.add('active');
      } else {
        link.classList.remove('active');
      }
    });
    
    if (updateHash) {
      window.location.hash = targetId;
    }
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
  
  navLinks.forEach(link => {
    link.addEventListener('click', (e) => {
      e.preventDefault();
      const target = link.getAttribute('data-target');
      showSection(target, true);
      if (navbar.classList.contains('active')) {
        navbar.classList.remove('active');
        menuIcon.classList.remove('bx-x');
      }
    });
  });
  
  const homeLogoLink = document.getElementById('homeLogoLink');
  if (homeLogoLink) {
    homeLogoLink.addEventListener('click', (e) => {
      e.preventDefault();
      showSection('home', true);
    });
  }
  
  const viewProjectsBtn = document.getElementById('viewProjectsBtn');
  if (viewProjectsBtn) {
    viewProjectsBtn.addEventListener('click', (e) => {
      e.preventDefault();
      showSection('projects', true);
    });
  }
  
  const hireMeBtn = document.getElementById('hireMeBtn');
  if (hireMeBtn) {
    hireMeBtn.addEventListener('click', (e) => {
      e.preventDefault();
      showSection('contact', true);
    });
  }
  
  function handleInitialHash() {
    const hash = window.location.hash.substring(1);
    if (hash && ['home', 'about', 'experience', 'projects', 'contact'].includes(hash)) {
      showSection(hash, false);
    } else {
      showSection('home', false);
    }
  }
  
  window.addEventListener('scroll', () => {
    const header = document.querySelector('.header');
    header.classList.toggle('sticky', window.scrollY > 50);
  });
  
  const menuIcon = document.getElementById('menu-icon');
  const navbar = document.querySelector('.navbar');
  menuIcon.addEventListener('click', () => {
    navbar.classList.toggle('active');
    menuIcon.classList.toggle('bx-x');
  });
  
  const profileImg = document.getElementById('profileImage');
  if (profileImg) {
    const applyImageStyles = () => {
      profileImg.style.objectFit = 'cover';
      profileImg.style.objectPosition = 'center 25%';
      profileImg.style.transform = 'scale(1.12)';
      profileImg.style.width = '100%';
      profileImg.style.height = '100%';
    };
    profileImg.onload = applyImageStyles;
    if (profileImg.complete) applyImageStyles();
  }
  
  const contactForm = document.getElementById('contactForm');
  const formStatus = document.getElementById('formStatus');
  if (contactForm) {
    contactForm.addEventListener('submit', (e) => {
      e.preventDefault();
      const name = document.getElementById('contactName')?.value || '';
      const email = document.getElementById('contactEmail')?.value || '';
      const message = document.getElementById('contactMessage')?.value || '';
      if (name && email && message) {
        formStatus.innerHTML = '✓ Thank you ' + name + '! Your message has been sent. I will respond within 24 hours.';
        contactForm.reset();
        setTimeout(() => { formStatus.innerHTML = ''; }, 5000);
      } else {
        formStatus.innerHTML = '⚠ Please fill all required fields.';
        setTimeout(() => { formStatus.innerHTML = ''; }, 3000);
      }
    });
  }
  
  const revealElements = document.querySelectorAll('.exp-card, .project-card, .skill-tag');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1 });
  revealElements.forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(25px)';
    el.style.transition = '0.5s ease';
    observer.observe(el);
  });
  
  handleInitialHash();
</script>
</body>
</html>
