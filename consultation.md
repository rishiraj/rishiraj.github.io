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
  <h1 class="consultation-title">AI Consulting by Rishiraj</h1>
  <p style="text-align: center; font-size: 1.15em; color: #2d3748; margin-top: -15px; margin-bottom: 30px;">
    I offer premium AI consulting services tailored to clients who need focused, high-impact support in developing, scaling, or refining their AI/ML systems — especially in Natural Language Processing, Speech Technologies, and AI for Medicine.
  </p>

  <hr class="section-divider">

  <section class="terms-section">
    <h2><span class="icon">💼</span> Consulting Terms</h2>
    <div class="term-item"><strong>Monthly Rate:</strong> <span>₹2,00,000 INR</span></div>
    <div class="term-item"><strong>Availability:</strong> <span>5 days a week (Monday–Friday)</span></div>
    <div class="term-item"><strong>Hours per Day:</strong> <span>5 hours</span></div>
    <div class="term-item"><strong>Total Monthly Hours:</strong> <span>100 hours</span></div>
    <div class="term-item"><strong>Effective Hourly Rate:</strong> <span>₹2,000 INR/hour</span></div>
  </section>

  <hr class="section-divider">

  <section>
    <h2><span class="icon">🚫</span> What You <em>Don’t</em> Get</h2>
    <ul class="pros-cons-list dont-get">
      <li>No random or recurring sync calls</li>
      <li>No daily stand-ups or updates</li>
      <li>No micromanagement</li>
    </ul>
    <p style="margin-top: 15px;">I work independently and deliver with clear goals, timelines, and communication when necessary. You bring a problem, I bring a solution.</p>
  </section>

  <hr class="section-divider">

  <section>
    <h2><span class="icon">🧠</span> What You <em>Do</em> Get</h2>
    <ul class="pros-cons-list do-get">
      <li>Expert-level guidance and hands-on development in:
        <ul>
          <li>Natural Language Processing (NLP)</li>
          <li>Speech & Audio AI + Medical AI systems</li>
          <li>End-to-end ML pipeline design</li>
          <li>Scalable cloud-based ML deployment (GCP, AWS)</li>
          <li>Kaggle-style rapid experimentation and prototyping</li>
        </ul>
      </li>
      <li>High-quality, maintainable code and models</li>
      <li>Research-backed methods and optimization</li>
      <li>Integration with Hugging Face and GCP ecosystems</li>
    </ul>
  </section>

  <hr class="section-divider">

  <section style="text-align: center;">
    <h2><span class="icon">💬</span> Contact</h2>
    <p>To discuss your project or explore a consulting engagement, get in touch with a brief outline of your needs.</p>
    <a href="mailto:heyrishiraj@gmail.com" class="button-link large">Get in Touch</a>
    <blockquote style="margin-top: 25px; text-align: left;">
      <p>I only take on a limited number of clients to ensure deep focus and quality. Serious inquiries only.</p>
    </blockquote>
  </section>

  <hr class="section-divider">
  <p class="footer-quote">
    <i>Empowering your projects with cutting-edge AI expertise.</i>
  </p>
</div>
