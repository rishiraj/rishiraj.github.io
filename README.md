<style>
  /* Import Gallient Font */
  @font-face {
    font-family: 'Gallient';
    src: url('https://raw.githubusercontent.com/rishiraj/rishiraj.github.io/main/assets/Gallient-Regular.woff2') format('woff2');
    font-display: swap;
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji";
    line-height: 1.6;
    color: #333;
    background-color: #f9fafb; /* Light gray background */
    margin: 0;
    padding: 0;
  }

  .container {
    max-width: 900px;
    margin: 20px auto;
    padding: 25px;
    background-color: #ffffff;
    border-radius: 12px;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
  }

  h1, h2, h3, h4 {
    font-family: 'Gallient', serif;
    color: #1a202c; /* Darker heading color */
  }
  
  h1 { font-size: 2.8em; margin-bottom: 0.2em; }
  h2 { font-size: 2.0em; margin-top: 1.8em; margin-bottom: 0.8em; border-bottom: 2px solid #e2e8f0; padding-bottom: 0.4em; }
  h3 { font-size: 1.6em; margin-top: 1.5em; margin-bottom: 0.6em; color: #2d3748; }
  h4 { font-size: 1.2em; margin-top: 1.2em; margin-bottom: 0.4em; color: #4a5568; }

  p, li {
    font-size: 1.05em;
    color: #4a5568; /* Slightly lighter text color */
  }

  a {
    color: #4299e1; /* Blue link color */
    text-decoration: none;
    transition: color 0.2s ease-in-out;
  }
  a:hover {
    color: #2b6cb0; /* Darker blue on hover */
    text-decoration: underline;
  }

  .profile-header {
    text-align: center;
    margin-bottom: 30px;
  }
  .profile-header img {
    border: 4px solid #e2e8f0; /* Light border around image */
  }
  .profile-header b {
    font-size: 1.2em;
    color: #2d3748;
    display: block;
    margin-top: 10px;
  }

  .section-divider {
    border: 0;
    height: 1px;
    background: #e2e8f0;
    margin: 40px 0;
  }

  .button-link {
    display: inline-block;
    background-color: #4299e1;
    color: #ffffff !important; /* Important to override default link color */
    padding: 10px 18px;
    border-radius: 8px;
    font-weight: bold;
    text-decoration: none;
    transition: background-color 0.2s ease-in-out;
    margin: 5px 5px 5px 0;
  }
  .button-link:hover {
    background-color: #2b6cb0;
    text-decoration: none;
  }

  .career-item, .project-highlight {
    background-color: #f7fafc; /* Very light gray for cards */
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 20px;
    border: 1px solid #e2e8f0;
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
  }
  .career-item h4 { margin-top: 0; }
  .career-item p.meta {
    font-size: 0.9em;
    color: #718096; /* Gray for meta info */
    margin-bottom: 10px;
  }
  
  ul {
    list-style-type: none;
    padding-left: 0;
  }
  ul li {
    padding-left: 1.5em;
    position: relative;
    margin-bottom: 0.5em;
  }
  ul li::before {
    content: "›"; /* Custom bullet */
    position: absolute;
    left: 0;
    color: #4299e1; /* Bullet color */
    font-weight: bold;
  }
  
  .tech-toolbox ul {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    padding-left: 0;
  }
  .tech-toolbox li {
    background-color: #e2e8f0;
    color: #2d3748;
    padding: 6px 12px;
    border-radius: 15px; /* Pill shape */
    font-size: 0.9em;
    list-style-type: none; /* Remove default bullet */
  }
  .tech-toolbox li::before { content: ""; } /* Remove custom bullet for these */
  
  .tech-category-title {
    font-weight: bold;
    color: #2d3748;
    margin-top: 10px;
    margin-bottom: 5px;
    display: block; /* Make it take full width before tags */
  }

  .achievements-list li::before { content: "🏆"; left: -5px; font-size: 1.1em; }
  .community-list li::before { content: "🌍"; left: -5px; font-size: 1.1em; }
  .contact-list li { padding-left: 2em; } /* More space for emoji icons */
  .contact-list li::before { content: ""; } /* Remove default bullet */
  .contact-list .icon { margin-right: 8px; font-size: 1.2em; }

  .footer-quote {
    text-align: center;
    font-style: italic;
    color: #718096;
    margin-top: 40px;
    font-size: 1.1em;
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
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">💡</span> Who I Am</h2>
    <p>I'm a Machine Learning Engineer currently leading AI development at <strong>IntelliTek</strong>, where I focus on using <strong>Generative AI</strong> to enhance the healthcare domain — automating clinical workflows like SOAP note generation, extracting structured data from unstructured conversations, and ensuring HIPAA-compliant ML pipelines.</p>
    <p>As a <strong>triple Google Developer Expert</strong> in <strong>Machine Learning</strong>, <strong>Cloud</strong>, and <strong>Kaggle</strong>, I bring both depth and breadth to real-world AI systems. My work sits at the intersection of <strong>NLP</strong>, <strong>Speech Technologies</strong>, and <strong>Medical AI</strong>.</p>
    <p>
      <a href="/consultation" class="button-link">👉 Consulting? Here’s how I work</a>
      <a href="/gsoc2022" class="button-link">🛠️ My GSoC project at TensorFlow</a>
    </p>
  </section>

  <hr class="section-divider">

  <section id="career-snapshot">
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">🚀</span> Career Snapshot</h2>
    
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
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">🧪</span> FireRequests</h2>
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
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">📚</span> Tech Toolbox</h2>
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
      <li>GCP</li><li>AWS</li><li>FastAPI</li><li>Redis</li><li>TensorRT</li><li>Docker</li>
    </ul>
    <span class="tech-category-title">Tools:</span>
    <ul>
      <li>PEFT</li><li>TRL</li><li>Optuna</li><li>GitHub Actions</li><li>LangChain</li><li>Weights & Biases</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section id="achievements">
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">🏅</span> Achievements & Recognition</h2>
    <ul class="achievements-list">
      <li>Kaggle Competitions Master & 2× Expert</li>
      <li>Gold Medalist (Top 10) in <strong>RSNA MICCAI Brain Tumor Segmentation Challenge</strong></li>
      <li>Endorsed by experts like <strong>Sayak Paul</strong> (Hugging Face, GDE)</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section id="community">
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">🌍</span> Community Involvement</h2>
    <ul class="community-list">
      <li>Co-Organizer of <strong>TensorFlow User Group Kolkata</strong> and <strong>GDG Cloud Kolkata</strong></li>
      <li>Regular speaker and mentor in the global open-source AI ecosystem</li>
      <li>Hugging Face 🤗 <strong>Fellow</strong>, building public LLM tools and sharing cutting-edge research</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section id="contact">
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">📫</span> Let’s Talk</h2>
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