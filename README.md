<style>
  /* Import Gallient Font */
  @font-face {
    font-family: 'Gallient';
    src: url('https://raw.githubusercontent.com/rishiraj/rishiraj.github.io/main/assets/Gallient-Regular.woff2') format('woff2');
    font-display: swap;
  }

  :root {
    --primary-color: #007bff;
    --primary-hover-color: #0056b3;
    --text-color: #343a40;
    --text-muted-color: #6c757d;
    --heading-color: #212529;
    --bg-body: #e9ecef;
    --bg-container-glass: rgba(255, 255, 255, 0.85);
    --bg-card-glass: rgba(255, 255, 255, 0.75);
    --border-color-soft: rgba(0, 0, 0, 0.1);
    --border-color-glass: rgba(255, 255, 255, 0.3);
    --shadow-soft: 0 8px 24px rgba(0, 0, 0, 0.1);
    --shadow-strong: 0 12px 30px rgba(0, 0, 0, 0.15);
    --border-radius-main: 20px;
    --border-radius-card: 15px;
    --border-radius-button: 8px;
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    line-height: 1.7;
    color: var(--text-color);
    background-color: var(--bg-body);
    background-image: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
    margin: 0;
    padding: 10px; /* Base padding for body, container will have more */
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-wrap: break-word;
    word-wrap: break-word; /* Legacy */
  }

  .container {
    max-width: 900px;
    margin: 40px auto;
    padding: 35px 45px;
    background-color: var(--bg-container-glass);
    backdrop-filter: blur(12px) saturate(150%);
    -webkit-backdrop-filter: blur(12px) saturate(150%);
    border-radius: var(--border-radius-main);
    box-shadow: var(--shadow-strong);
    border: 1px solid var(--border-color-glass);
  }

  h1, h2, h3, h4 {
    font-family: 'Gallient', serif;
    color: var(--heading-color);
    line-height: 1.3;
  }
  
  h1 { font-size: 2.8em; margin-bottom: 0.3em; }
  h2 { font-size: 2.0em; margin-top: 2em; margin-bottom: 1em; border-bottom: 1px solid var(--border-color-soft); padding-bottom: 0.5em; }
  h3 { font-size: 1.6em; margin-top: 1.8em; margin-bottom: 0.7em; color: #2c3e50; }
  h4 { font-size: 1.25em; margin-top: 1.5em; margin-bottom: 0.5em; color: #34495e; }

  p, li {
    font-size: 1.05em;
    color: var(--text-color);
    margin-bottom: 0.8em;
  }

  a {
    color: var(--primary-color);
    text-decoration: none;
    transition: color 0.2s ease-in-out, background-color 0.2s ease-in-out;
    font-weight: 500;
  }
  a:hover {
    color: var(--primary-hover-color);
    text-decoration: none;
  }

  .profile-header {
    text-align: center;
    margin-bottom: 40px;
  }
  .profile-header img {
    border: 5px solid var(--border-color-glass);
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    width: 160px; /* Keep initial size */
    border-radius: 50%;
  }
  .profile-header h1 {
    margin-top: 0.5em;
    margin-bottom: 0.1em;
  }
  .profile-header b {
    font-size: 1.15em;
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
    font-weight: bold;
    text-decoration: none;
    transition: background-color 0.2s ease-in-out, transform 0.1s ease-out;
    box-shadow: 0 4px 10px rgba(0, 123, 255, 0.3);
    border: none;
    margin: 8px 8px 8px 0;
  }
  .button-link:hover {
    background-color: var(--primary-hover-color);
    text-decoration: none;
    transform: translateY(-2px);
    box-shadow: 0 6px 12px rgba(0, 123, 255, 0.4);
  }
  .button-link.large {
    padding: 15px 30px;
    font-size: 1.1em;
  }

  .styled-box, .career-item, .project-highlight, .terms-section .term-item {
    background-color: var(--bg-card-glass);
    backdrop-filter: blur(8px) saturate(120%);
    -webkit-backdrop-filter: blur(8px) saturate(120%);
    padding: 25px;
    border-radius: var(--border-radius-card);
    margin-bottom: 25px;
    border: 1px solid var(--border-color-glass);
    box-shadow: var(--shadow-soft);
    transition: transform 0.2s ease-out, box-shadow 0.2s ease-out;
  }

  .career-item h4, .project-highlight h4 { margin-top: 0; font-size: 1.4em; }
  .career-item p.meta {
    font-size: 0.9em;
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
    content: "❖";
    position: absolute;
    left: 0;
    color: var(--primary-color);
    font-weight: bold;
    font-size: 1.1em;
    top: -1px;
  }
  
  .tech-toolbox { padding: 10px 0; }
  .tech-toolbox ul {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    padding-left: 0;
    margin-top: 10px;
  }
  .tech-toolbox li {
    background-color: rgba(0, 123, 255, 0.1);
    color: var(--primary-color);
    padding: 8px 15px;
    border-radius: 20px;
    font-size: 0.9em;
    font-weight: 500;
    list-style-type: none;
    border: 1px solid rgba(0, 123, 255, 0.2);
  }
  .tech-toolbox li::before { content: ""; }
  
  .tech-category-title {
    font-weight: bold;
    color: var(--heading-color);
    margin-top: 15px;
    margin-bottom: 8px;
    display: block;
    font-size: 1.05em;
  }

  .achievements-list li::before { content: "🏆"; left: -2px; font-size: 1.2em; top: -2px;}
  .community-list li::before { content: "🌍"; left: -2px; font-size: 1.2em; top: -2px;}
  .contact-list li { padding-left: 2.5em; }
  .contact-list li::before { content: ""; }
  .contact-list .icon { margin-right: 10px; font-size: 1.3em; vertical-align: middle; color: var(--primary-color); }

  .footer-quote {
    text-align: center;
    font-style: italic;
    color: var(--text-muted-color);
    margin-top: 50px;
    font-size: 1.1em;
    padding-top: 20px;
    border-top: 1px solid var(--border-color-soft);
  }

  .consultation-title {
    text-align: center;
    margin-bottom: 30px !important;
    padding-bottom: 20px;
    border-bottom: 1px solid var(--border-color-soft);
  }

  .terms-section .term-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 18px 25px;
  }
  .terms-section .term-item strong {
    color: var(--heading-color);
    font-weight: 600;
  }
  .terms-section .term-item span {
    font-weight: 600;
    color: var(--primary-color);
    font-size: 1.05em;
  }

  .pros-cons-list {
    list-style-type: none;
    padding-left: 0;
  }
  .pros-cons-list li {
    padding-left: 2.5em;
    margin-bottom: 1em;
    font-size: 1.05em;
  }
  .pros-cons-list li::before {
    position: absolute;
    left: 0;
    font-size: 1.4em;
    top: -3px;
  }
  .pros-cons-list.dont-get li::before { content: "🚫"; }
  .pros-cons-list.do-get li::before { content: "✅"; }
  
  .pros-cons-list ul, ul ul {
    padding-left: 25px;
    margin-top: 10px;
    margin-bottom: 10px;
  }
  .pros-cons-list ul li, ul ul li {
    font-size: 0.95em;
  }
  .pros-cons-list ul li::before, ul ul li::before {
    content: "›";
    color: var(--primary-color);
    font-weight: bold;
    font-size: 1em;
    left: -1.2em;
    top: 0;
  }
  
  blockquote {
    border-left: 5px solid var(--primary-color);
    padding: 15px 25px;
    margin-left: 0;
    margin-right: 0;
    font-style: italic;
    color: var(--text-muted-color);
    background-color: rgba(0, 123, 255, 0.05);
    border-radius: 0 var(--border-radius-card) var(--border-radius-card) 0;
  }
  blockquote p {
    margin-bottom: 0;
    color: var(--text-color);
  }

  .gsoc-header-image {
    width: 100%;
    max-width: 700px;
    display: block;
    margin: 0 auto 30px auto;
    border-radius: var(--border-radius-card);
    box-shadow: var(--shadow-soft);
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
    font-size: 1.1em;
    line-height: 1.4;
  }
  .gsoc-contributions-list li::before {
    content: "✔";
    color: #28a745;
    top: 0;
  }
  .gsoc-merged-prs-list li::before {
    content: "🔗";
    top: 0;
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

  @media (max-width: 992px) { /* Medium devices (tablets, less than 992px) */
    .container {
      padding: 30px 30px; /* Adjusted for symmetry */
      margin: 30px auto;
    }
    .consultation-container { /* If consultation page needs slightly different width */
        max-width: 800px;
    }
  }

  @media (max-width: 768px) { /* Small devices (landscape phones, 768px and down) */
    body {
      padding: 5px; /* Less body padding on small screens */
    }
    .container {
      margin: 20px auto;
      padding: 25px 20px; /* Reduced padding for smaller screens */
    }
    h1, .profile-header h1, .consultation-title, .gsoc-page-title {
      font-size: 2.2em; 
    }
    h2 {
      font-size: 1.7em; 
    }
    h3 {
      font-size: 1.4em;
    }
    h4 {
      font-size: 1.15em;
    }
    p, li {
      font-size: 1em; 
    }
    .button-link {
      padding: 10px 18px;
      font-size: 0.95em;
    }
    .button-link.large {
      padding: 12px 22px;
      font-size: 1em;
    }
    .tech-toolbox ul {
      gap: 8px; 
    }
    .tech-toolbox li {
      padding: 6px 12px;
      font-size: 0.85em;
    }
    .profile-header img {
      width: 120px; 
    }
    .profile-header b {
      font-size: 1.05em;
    }
    .gsoc-subtitle {
      font-size: 1em;
    }
    .section-divider {
        margin: 40px 0;
    }
  }

  @media (max-width: 576px) { /* Extra small devices (portrait phones, less than 576px) */
    .container {
      padding: 20px 15px; 
      margin: 15px auto;
      border-radius: 15px; 
    }
    h1, .profile-header h1, .consultation-title, .gsoc-page-title {
      font-size: 1.9em; /* Even smaller h1, adjusted from 1.8 */
    }
    h2 {
      font-size: 1.5em;
    }
    h3 {
      font-size: 1.3em;
    }
    p, li {
      font-size: 0.95em;
    }
    .profile-header img {
      width: 100px;
    }
    .profile-header b {
      font-size: 0.95em;
    }
    .contact-list li {
      padding-left: 2.2em; /* Adjust for smaller icons/text */
    }
    .contact-list .icon {
      font-size: 1.2em;
    }
    .gsoc-subtitle {
      font-size: 0.9em;
    }
    .terms-section .term-item {
      padding: 15px 15px; /* Smaller padding in term items */
      flex-direction: column; /* Stack term items on very small screens */
      align-items: flex-start;
      text-align: left;
    }
    .terms-section .term-item strong {
      margin-bottom: 5px;
    }
    .terms-section .term-item span {
        font-size: 1em; /* Ensure rate is readable */
    }
    .footer-quote {
      font-size: 1em;
      margin-top: 40px;
      padding-top: 15px;
    }
    .button-link, .button-link.large { /* Make buttons take more width if needed, or just ensure they wrap nicely */
        display: block; /* Make buttons stack on smallest screens */
        text-align: center;
        margin-left: 0;
        margin-right: 0;
    }
    .profile-header {
        margin-bottom: 30px;
    }
  }
</style>

<div class="container">
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
