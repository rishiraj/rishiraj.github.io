<style>
  /* Import Gallient Font */
  @font-face {
    font-family: 'Gallient';
    src: url('https://raw.githubusercontent.com/rishiraj/rishiraj.github.io/main/assets/Gallient-Regular.woff2') format('woff2');
    font-display: swap;
  }

  :root {
    --primary-color: #007AFF; /* Apple's classic blue */
    --primary-hover-color: #0056b3;
    --text-color: #1d1d1f; /* Apple's dark text color */
    --text-muted-color: #6e6e73; /* Apple's secondary text color */
    --heading-color: #1d1d1f;
    
    /* Backgrounds */
    --bg-body: #f5f5f7; /* Very light Apple-like grey */
    --bg-container-glass-base: rgba(255, 255, 255, 0.7); /* Base for glass */
    --bg-card-glass-base: rgba(255, 255, 255, 0.65);

    /* Borders & Shadows */
    --border-color-soft: rgba(0, 0, 0, 0.08);
    --border-color-glass-edge: rgba(255, 255, 255, 0.5); /* Subtle edge highlight */
    --shadow-glass: 0 15px 35px rgba(0, 0, 0, 0.07), 0 5px 15px rgba(0,0,0,0.05);
    
    /* Radii */
    --border-radius-main: 22px; /* Slightly more rounded, Apple-like */
    --border-radius-card: 18px;
    --border-radius-button: 8px;

    /* Rainbow Gradient Colors (subtle) */
    --rainbow-color-1: hsla(190, 80%, 75%, 0.6); /* Light Blue */
    --rainbow-color-2: hsla(140, 70%, 78%, 0.6); /* Light Green */
    --rainbow-color-3: hsla(60, 80%, 78%, 0.6);  /* Light Yellow */
    --rainbow-color-4: hsla(20, 80%, 80%, 0.6);  /* Light Orange/Peach */
    --rainbow-color-5: hsla(330, 80%, 82%, 0.6); /* Light Pink */
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    line-height: 1.65; /* Slightly more open leading */
    color: var(--text-color);
    background-color: var(--bg-body);
    margin: 0;
    padding: 10px;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-wrap: break-word;
    word-wrap: break-word;
  }

  /* Base for all glass elements */
  .glass-effect {
    position: relative; /* Crucial for pseudo-elements */
    overflow: hidden;   /* Crucial for clipping pseudo-elements */
    background-color: var(--bg-container-glass-base);
    backdrop-filter: blur(20px) saturate(180%); /* Increased blur and saturation */
    -webkit-backdrop-filter: blur(20px) saturate(180%);
    border: 1px solid var(--border-color-glass-edge);
    box-shadow: var(--shadow-glass);
  }

  /* Rainbow highlight pseudo-element for glass */
  .glass-effect::before {
    content: "";
    position: absolute;
    bottom: 0; /* Position at the bottom */
    left: -50%; /* Start gradient off-screen to allow it to sweep across */
    width: 200%; /* Make it wide enough to sweep */
    height: 70%; /* Adjust height of the rainbow effect area */
    background-image: linear-gradient(
      90deg, /* Control angle of the rainbow stripes */
      transparent,
      var(--rainbow-color-1) 20%,
      var(--rainbow-color-2) 40%,
      var(--rainbow-color-3) 60%,
      var(--rainbow-color-4) 80%,
      var(--rainbow-color-5),
      transparent
    );
    opacity: 0.35; /* Make it very subtle */
    filter: blur(35px); /* Heavy blur for diffusion */
    z-index: 1; /* Behind content but above main background */
    pointer-events: none; /* Allow clicks to pass through */
    border-bottom-left-radius: inherit; /* Match parent's rounding */
    border-bottom-right-radius: inherit;
  }
  
  /* Content within glass needs to be above the pseudo-element */
  .glass-effect > * {
    position: relative;
    z-index: 2;
  }

  .container {
    max-width: 900px;
    margin: 40px auto;
    padding: 35px 45px;
    border-radius: var(--border-radius-main);
    /* Inherits .glass-effect styles */
  }
  .container.consultation-container { /* Specific class for consultation if different size needed */
    max-width: 850px;
  }

  h1, h2, h3, h4 {
    font-family: 'Gallient', serif;
    color: var(--heading-color);
    line-height: 1.3;
  }
  
  h1 { font-size: 2.6em; margin-bottom: 0.3em; } /* Slightly reduced default H1 */
  h2 { font-size: 1.9em; margin-top: 2em; margin-bottom: 1em; border-bottom: 1px solid var(--border-color-soft); padding-bottom: 0.5em; }
  h3 { font-size: 1.5em; margin-top: 1.8em; margin-bottom: 0.7em; color: #2c3e50; }
  h4 { font-size: 1.2em; margin-top: 1.5em; margin-bottom: 0.5em; color: #34495e; }

  p, li {
    font-size: 1.02em; /* Slightly smaller base paragraph text */
    color: var(--text-color);
    margin-bottom: 0.8em;
  }

  a {
    color: var(--primary-color);
    text-decoration: none;
    transition: color 0.2s ease-in-out, opacity 0.2s ease-in-out;
    font-weight: 500;
  }
  a:hover {
    color: var(--primary-hover-color);
    opacity: 0.85;
  }

  .profile-header {
    text-align: center;
    margin-bottom: 40px;
  }
  .profile-header img {
    border: 3px solid rgba(255,255,255,0.7); /* Lighter border for profile pic */
    box-shadow: 0 4px 15px rgba(0,0,0,0.08);
    width: 160px;
    border-radius: 50%;
  }
  .profile-header h1 {
    margin-top: 0.5em;
    margin-bottom: 0.1em;
    font-size: 2.8em; /* Restore profile header H1 size */
  }
  .profile-header b {
    font-size: 1.1em;
    color: var(--text-muted-color);
    display: block;
    margin-top: 5px;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    font-weight: 500;
  }

  .section-divider {
    border: 0;
    height: 1px;
    background: var(--border-color-soft);
    margin: 50px 0;
  }

  .button-link {
    display: inline-block;
    background-color: var(--primary-color);
    color: #ffffff !important;
    padding: 12px 24px;
    border-radius: var(--border-radius-button);
    font-weight: 600; /* Apple often uses semi-bold for buttons */
    text-decoration: none;
    transition: background-color 0.2s ease-in-out, transform 0.1s ease-out;
    box-shadow: 0 2px 5px rgba(0, 123, 255, 0.2); /* Softer button shadow */
    border: none;
    margin: 8px 8px 8px 0;
  }
  .button-link:hover {
    background-color: var(--primary-hover-color);
    text-decoration: none;
    transform: translateY(-1px);
    box-shadow: 0 3px 7px rgba(0, 123, 255, 0.3);
  }
  .button-link.large {
    padding: 14px 28px;
    font-size: 1.05em;
  }

  .styled-box, .career-item, .project-highlight, .terms-section .term-item {
    padding: 25px;
    border-radius: var(--border-radius-card);
    margin-bottom: 25px;
    background-color: var(--bg-card-glass-base); /* Specific base for cards */
    /* Inherits .glass-effect styles */
  }
  .terms-section .term-item {
    padding: 20px 25px; /* Slightly different padding for term items */
  }


  .career-item h4, .project-highlight h4 { margin-top: 0; font-size: 1.3em; }
  .career-item p.meta {
    font-size: 0.88em;
    color: var(--text-muted-color);
    margin-bottom: 12px;
    font-style: italic;
  }
  
  ul {
    list-style-type: none;
    padding-left: 0;
  }
  ul li {
    padding-left: 1.8em;
    position: relative;
    margin-bottom: 0.6em;
  }
  ul li::before {
    content: "•"; /* Simple dot, Apple-like */
    position: absolute;
    left: 0.5em; /* Adjust for dot */
    color: var(--primary-color);
    font-weight: bold;
    font-size: 1em;
    top: 0.1em;
  }
  
  .tech-toolbox { padding: 10px 0; }
  .tech-toolbox ul {
    display: flex;
    flex-wrap: wrap;
    gap: 10px; /* Slightly smaller gap */
    padding-left: 0;
    margin-top: 10px;
  }
  .tech-toolbox li {
    background-color: rgba(0, 123, 255, 0.08); /* Even lighter for pills */
    color: var(--primary-color);
    padding: 7px 14px;
    border-radius: 15px; /* More rounded pills */
    font-size: 0.88em;
    font-weight: 500;
    list-style-type: none;
    border: 1px solid rgba(0, 123, 255, 0.15);
  }
  .tech-toolbox li::before { content: ""; }
  
  .tech-category-title {
    font-weight: 600; /* Semi-bold */
    color: var(--heading-color);
    margin-top: 15px;
    margin-bottom: 8px;
    display: block;
    font-size: 1em;
  }

  .achievements-list li::before { content: "🏆"; left: 0px; font-size: 1.1em; top: -1px;}
  .community-list li::before { content: "🌍"; left: 0px; font-size: 1.1em; top: -1px;}
  .contact-list li { padding-left: 2.2em; }
  .contact-list li::before { content: ""; }
  .contact-list .icon { margin-right: 8px; font-size: 1.2em; vertical-align: middle; color: var(--primary-color); }

  .footer-quote {
    text-align: center;
    font-style: italic;
    color: var(--text-muted-color);
    margin-top: 50px;
    font-size: 1.05em;
    padding-top: 20px;
    border-top: 1px solid var(--border-color-soft);
  }

  .consultation-title {
    text-align: center;
    font-size: 2.6em; /* Match H1 */
    margin-bottom: 30px !important;
    padding-bottom: 20px;
    border-bottom: 1px solid var(--border-color-soft);
  }

  .terms-section .term-item strong {
    color: var(--heading-color);
    font-weight: 600;
  }
  .terms-section .term-item span {
    font-weight: 600;
    color: var(--primary-color);
    font-size: 1.02em;
  }

  .pros-cons-list {
    list-style-type: none;
    padding-left: 0;
  }
  .pros-cons-list li {
    padding-left: 2.2em;
    margin-bottom: 1em;
    font-size: 1.02em;
  }
  .pros-cons-list li::before {
    position: absolute;
    left: 0;
    font-size: 1.3em;
    top: -2px;
  }
  .pros-cons-list.dont-get li::before { content: "🚫"; }
  .pros-cons-list.do-get li::before { content: "✅"; }
  
  .pros-cons-list ul, ul ul {
    padding-left: 25px;
    margin-top: 10px;
    margin-bottom: 10px;
  }
  .pros-cons-list ul li, ul ul li {
    font-size: 0.92em;
  }
  .pros-cons-list ul li::before, ul ul li::before {
    content: "–"; /* Em dash for nested, simpler */
    color: var(--text-muted-color);
    font-weight: bold;
    font-size: 1em;
    left: -0.2em; 
    top: 0;
  }
  
  blockquote {
    border-left: 4px solid var(--primary-color);
    padding: 15px 20px;
    margin-left: 0;
    margin-right: 0;
    font-style: italic;
    color: var(--text-muted-color);
    background-color: rgba(230, 242, 255, 0.5); /* Very light blue tint */
    border-radius: 0 var(--border-radius-card) var(--border-radius-card) 0;
  }
  blockquote p {
    margin-bottom: 0;
    color: var(--text-color);
  }

  .gsoc-header-image {
    width: 100%;
    max-width: 650px; /* Slightly smaller max */
    display: block;
    margin: 0 auto 30px auto;
    border-radius: var(--border-radius-card);
    box-shadow: var(--shadow-glass); /* Use glass shadow */
  }
  .gsoc-page-title {
    text-align: center;
    font-size: 2.4em;
    margin-bottom: 0.1em;
    line-height: 1.2;
  }
  .gsoc-subtitle {
    text-align: center;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    font-weight: 500;
    color: var(--text-muted-color);
    margin-top: 0.5em;
    margin-bottom: 2em;
    font-size: 1.05em;
    line-height: 1.4;
  }
  .gsoc-contributions-list li::before {
    content: "✓"; /* SF Symbol like check */
    color: #34C759; /* Apple Green */
    top: 0;
    left: 0.4em;
  }
  .gsoc-merged-prs-list li::before {
    content: "🔗";
    top: 0;
    left: 0.4em;
  }

  img {
    max-width: 100%;
    height: auto;
    border-radius: var(--border-radius-button);
  }

  h2 .icon, h3 .icon, h4 .icon {
    font-size: 0.8em;
    vertical-align: middle;
    margin-right: 10px;
    display: inline-block;
    color: var(--primary-color);
  }

  /* --- Responsive Adjustments --- */
  @media (max-width: 992px) {
    .container { padding: 30px; margin: 30px auto; }
    .container.consultation-container { max-width: 800px; }
  }

  @media (max-width: 768px) {
    body { padding: 5px; }
    .container { margin: 20px auto; padding: 25px 20px; }
    h1, .profile-header h1, .consultation-title, .gsoc-page-title { font-size: 2.1em; }
    .profile-header h1 {font-size: 2.3em;} /* Keep profile H1 a bit larger */
    h2 { font-size: 1.6em; }
    h3 { font-size: 1.35em; }
    h4 { font-size: 1.1em; }
    p, li { font-size: 0.98em; }
    .button-link { padding: 10px 20px; font-size: 0.92em; }
    .button-link.large { padding: 12px 22px; font-size: 0.98em; }
    .tech-toolbox ul { gap: 8px; }
    .tech-toolbox li { padding: 6px 12px; font-size: 0.82em; }
    .profile-header img { width: 120px; }
    .profile-header b { font-size: 1em; }
    .gsoc-subtitle { font-size: 1em; }
    .section-divider { margin: 40px 0; }
    .glass-effect::before { height: 60%; filter: blur(30px); opacity: 0.3; }
  }

  @media (max-width: 576px) {
    .container { padding: 20px 15px; margin: 15px auto; border-radius: 18px; }
    h1, .profile-header h1, .consultation-title, .gsoc-page-title { font-size: 1.8em; }
    .profile-header h1 {font-size: 2em;} /* Keep profile H1 a bit larger */
    h2 { font-size: 1.45em; }
    h3 { font-size: 1.25em; }
    p, li { font-size: 0.92em; }
    .profile-header img { width: 100px; }
    .profile-header b { font-size: 0.9em; }
    .contact-list li { padding-left: 2em; }
    .contact-list .icon { font-size: 1.1em; }
    .gsoc-subtitle { font-size: 0.9em; }
    .terms-section .term-item { padding: 15px; flex-direction: column; align-items: flex-start; text-align: left; }
    .terms-section .term-item strong { margin-bottom: 5px; }
    .terms-section .term-item span { font-size: 0.98em; }
    .footer-quote { font-size: 0.95em; margin-top: 40px; padding-top: 15px; }
    .button-link, .button-link.large { display: block; text-align: center; margin-left: 0; margin-right: 0; }
    .profile-header { margin-bottom: 30px; }
    .glass-effect::before { height: 50%; filter: blur(25px); opacity: 0.25; }
    ul li::before {left: 0.4em;}
  }
</style>

<div class="container glass-effect">
  <div class="profile-header">
    <img src="assets/profile.png" alt="Rishiraj's Profile Picture" width="160" style="border-radius: 50%;">
    <h1>Hi, I'm Rishiraj Acharya 👋</h1>
    <b>AI Engineer | Google Developer Expert (ML, Cloud, Kaggle) | Hugging Face 🤗 Fellow</b>
  </div>

  <hr class="section-divider">

  <section id="who-i-am">
    <h2><span class="icon">💡</span> Who I Am</h2>
    <p>I'm a Machine Learning Engineer currently leading AI development at <strong>IntelliTek</strong>, where I focus on using <strong>Generative AI</strong> to enhance the healthcare domain — automating clinical workflows like SOAP note generation, extracting structured data from unstructured conversations, and ensuring HIPAA-compliant ML pipelines.</p>
    <p>As a <strong>triple Google Developer Expert</strong> in <strong>Machine Learning</strong>, <strong>Cloud</strong>, and <strong>Kaggle</strong>, I bring both depth and breadth to real-world AI systems. My work sits at the intersection of <strong>NLP</strong>, <strong>Speech Technologies</strong>, and <strong>Medical AI</strong>.</p>
    <p>
      <a href="/consultation" class="button-link">👉 Consulting? Here’s how I work</a>
      <a href="/gsoc2022" class="button-link">🛠️ My GSoC project at TensorFlow</a>
    </p>
  </section>

  <hr class="section-divider">

  <section id="career-snapshot">
    <h2><span class="icon">🚀</span> Career Snapshot</h2>
    
    <div class="career-item">
      <h4>IntelliTek Products Pvt. Ltd. — <em>ML Engineer</em></h4>
      <p class="meta">📍 Sep 2024 – Present</p>
      <ul>
        <li>Designing GenAI solutions for clinical settings: automated SOAP notes, issue lists, and medical summaries.</li>
        <li>Built adversarial-robust, compliant pipelines with data security guardrails under HIPAA.</li>
      </ul>
    </div>

    <div class="career-item">
      <h4>TensorLake Inc. — <em>ML Engineer</em></h4>
      <p class="meta">📍 Apr 2024 – Aug 2024</p>
      <ul>
        <li>Designed <strong>Indexify</strong>, a real-time multimodal unstructured data engine.</li>
        <li>Improved processing speed by 30% and boosted query efficiency by 25%.</li>
        <li><a href="https://github.com/tensorlakeai/indexify">Project Link: Indexify</a></li>
      </ul>
    </div>

    <div class="career-item">
      <h4>PrediQt Business Solutions Pvt. Ltd. — <em>Senior AI/ML Engineer</em></h4>
      <p class="meta">📍 Jun 2023 – Nov 2023</p>
      <ul>
        <li>Led LLM finetuning and model optimization efforts.</li>
        <li>Achieved 40% faster inference and 50% uplift in model serving throughput.</li>
      </ul>
    </div>

    <div class="career-item">
      <h4>Dynopii Inc. — <em>ML Engineer</em></h4>
      <p class="meta">📍 Apr 2021 – Mar 2024</p>
      <ul>
        <li>Engineered full-stack speech and audio ML pipelines for Conversational AI.</li>
        <li>Drove 35% increase in engagement and cut training costs by half.</li>
      </ul>
    </div>
    
    <div class="career-item">
      <h4>Celebal Technologies Pvt. Ltd. — <em>Data Scientist</em></h4>
      <p class="meta">📍 Sep 2021 – Dec 2021</p>
      <ul>
        <li>Applied Classical ML, NLP, and CV techniques to enterprise use cases.</li>
        <li>Improved algorithm speed by 25% through Python-SQL optimization.</li>
      </ul>
    </div>

    <div class="career-item">
      <h4>TensorFlow (Google) — <em>GSoC 2022 Contributor</em></h4>
      <p class="meta">📍 May 2022 – Sep 2022</p>
      <ul>
        <li>Contributed to <a href="https://summerofcode.withgoogle.com/programs/2022/projects/RmEpoyDX">TensorFlow Decision Forests</a>, improving ease-of-use for Kaggle competitions.</li>
        <li>Created real-world examples for YDF and interpretability tools, boosting adoption by 15%.</li>
      </ul>
    </div>
  </section>

  <hr class="section-divider">

  <section id="firerequests" class="project-highlight">
    <h2><span class="icon">🧪</span> FireRequests</h2>
    <p><a href="https://github.com/rishiraj/firerequests" style="font-weight:bold; font-size: 1.1em;">FireRequests</a> is a high-performance, asynchronous HTTP client designed for large-scale ML workloads. It’s used by companies like <strong>Roboflow</strong> and supports concurrent interaction with providers like <strong>OpenAI</strong> and <strong>Google</strong>.</p>
    
    <h4>Key Highlights:</h4>
    <ul>
      <li>⚡ 10x faster I/O for uploading/downloading large payloads</li>
      <li>🔄 Robust retry logic, fault tolerance, and concurrency using <code>asyncio</code>, <code>aiohttp</code>, and <code>aiofiles</code></li>
      <li>📦 Seamless support for Jupyter, batch processing, and streaming APIs</li>
      <li>🧵 Integrated with <code>nest_asyncio</code>, <code>Semaphore</code>, and exponential backoff for reliability under load</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section id="tech-toolbox" class="tech-toolbox">
    <h2><span class="icon">📚</span> Tech Toolbox</h2>
    <span class="tech-category-title">ML/DL:</span>
    <ul>
      <li>TensorFlow</li><li>PyTorch</li><li>Transformers</li><li>Scikit-Learn</li><li>XGBoost</li>
    </ul>
    <span class="tech-category-title">NLP/Speech:</span>
    <ul>
      <li>LLMs</li><li>Audio ML</li><li>Speech-to-Text</li><li>Text-to-Speech</li><li>vLLM</li>
    </ul>
    <span class="tech-category-title">Deployment:</span>
    <ul>
      <li>GCP</li><li>AWS</li><li>FastAPI</li><li>Flask</li><li>Redis</li><li>TensorRT</li><li>Docker</li>
    </ul>
    <span class="tech-category-title">Tools:</span>
    <ul>
      <li>PEFT</li><li>TRL</li><li>Optuna</li><li>GitHub Actions</li><li>LangChain</li><li>Weights & Biases</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section id="achievements">
    <h2><span class="icon">🏅</span> Achievements & Recognition</h2>
    <ul class="achievements-list">
      <li>Kaggle Competitions Master & 2× Expert</li>
      <li>Gold Medalist (Top 10) in <strong>RSNA MICCAI Brain Tumor Segmentation Challenge</strong></li>
      <li>Endorsed by experts like <strong>Sayak Paul</strong> (Hugging Face, GDE)</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section id="community">
    <h2><span class="icon">🌍</span> Community Involvement</h2>
    <ul class="community-list">
      <li>Co-Organizer of <strong>TensorFlow User Group Kolkata</strong> and <strong>GDG Cloud Kolkata</strong></li>
      <li>Regular speaker and mentor in the global open-source AI ecosystem</li>
      <li>Hugging Face 🤗 <strong>Fellow</strong>, building public LLM tools and sharing cutting-edge research</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section id="contact">
    <h2><span class="icon">📫</span> Let’s Talk</h2>
    <ul class="contact-list">
      <li><span class="icon">📧</span> Email: <a href="mailto:heyrishiraj@gmail.com">heyrishiraj@gmail.com</a></li>
      <li><span class="icon">🔗</span> <a href="https://www.linkedin.com/in/rishirajacharya">LinkedIn</a> | <a href="https://github.com/rishiraj">GitHub</a></li>
    </ul>
  </section>

  <hr class="section-divider">

  <p class="footer-quote">
    <i>Building the future of AI — one transformer at a time.</i>
  </p>
</div>
