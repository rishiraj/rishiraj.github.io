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
    max-width: 850px; /* Adjusted slightly for content, can be 900px or 800px too */
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
  
  h1 { 
    font-size: 2.8em; 
    margin-bottom: 0.2em; 
  }
  /* Specific H1 styling for consultation page title */
  .consultation-title {
    text-align: center;
    margin-bottom: 25px !important; /* Overriding generic h1 margin */
    padding-bottom: 15px;
    border-bottom: 2px solid #e2e8f0;
  }

  h2 { 
    font-size: 2.0em; 
    margin-top: 1.8em; 
    margin-bottom: 0.8em; 
    border-bottom: 2px solid #e2e8f0; 
    padding-bottom: 0.4em; 
  }
  h3 { 
    font-size: 1.6em; 
    margin-top: 1.5em; 
    margin-bottom: 0.6em; 
    color: #2d3748; 
  }
  h4 { 
    font-size: 1.2em; 
    margin-top: 1.2em; 
    margin-bottom: 0.4em; 
    color: #4a5568; 
  }

  p, li {
    font-size: 1.05em;
    color: #4a5568; /* Slightly lighter text color */
  }

  a {
    color: #4299e1; /* Blue link color from readme */
    text-decoration: none;
    transition: color 0.2s ease-in-out;
  }
  a:hover {
    color: #2b6cb0; /* Darker blue on hover from readme */
    text-decoration: underline;
  }

  .profile-header { /* Kept for potential future use, not directly used here */
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

  .button-link { /* This is the primary button style from readme.md */
    display: inline-block;
    background-color: #4299e1;
    color: #ffffff !important; /* Important to override default link color */
    padding: 10px 18px;
    border-radius: 8px;
    font-weight: bold;
    text-decoration: none;
    transition: background-color 0.2s ease-in-out;
    margin: 5px 5px 5px 0;
    font-size: 1.0em; /* Base font size for buttons */
  }
  .button-link:hover {
    background-color: #2b6cb0;
    text-decoration: none;
  }
  /* Larger button variant if needed */
  .button-link.large {
    padding: 12px 25px;
    font-size: 1.1em;
  }


  .career-item, .project-highlight, .styled-box { /* Generic styled box */
    background-color: #f7fafc; /* Very light gray for cards */
    padding: 20px;
    border-radius: 10px;
    margin-bottom: 20px;
    border: 1px solid #e2e8f0;
    box-shadow: 0 4px 12px rgba(0,0,0,0.05);
  }
  .career-item h4 { margin-top: 0; } /* Specific to career-item */
  .career-item p.meta { /* Specific to career-item */
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
    content: "›"; /* Custom bullet from readme */
    position: absolute;
    left: 0;
    color: #4299e1; /* Bullet color from readme */
    font-weight: bold;
  }
  
  .tech-toolbox ul { /* Kept for potential future use, not directly used here */
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
  
  .tech-category-title { /* Kept for potential future use */
    font-weight: bold;
    color: #2d3748;
    margin-top: 10px;
    margin-bottom: 5px;
    display: block; /* Make it take full width before tags */
  }

  /* Specific list styles from readme.md that might be useful */
  .achievements-list li::before { content: "🏆"; left: -5px; font-size: 1.1em; }
  .community-list li::before { content: "🌍"; left: -5px; font-size: 1.1em; }
  .contact-list li { padding-left: 2em; } /* More space for emoji icons */
  .contact-list li::before { content: ""; } /* Remove default bullet */
  .contact-list .icon { margin-right: 8px; font-size: 1.2em; }

  .footer-quote { /* From readme.md */
    text-align: center;
    font-style: italic;
    color: #718096;
    margin-top: 40px;
    font-size: 1.1em;
  }

  /* Styles specific to consultation.md, now integrated */
  .terms-section .term-item {
    background-color: #f7fafc; /* Consistent with .career-item */
    border: 1px solid #e2e8f0; /* Consistent */
    border-radius: 8px;
    padding: 15px 20px;
    margin-bottom: 12px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .terms-section .term-item strong {
    color: #2d3748;
  }
  .terms-section .term-item span {
    font-weight: 500;
    color: #4299e1; /* Using readme link color */
  }

  .pros-cons-list {
    list-style-type: none;
    padding-left: 0; /* Base ul already has this */
  }
  .pros-cons-list li {
    padding-left: 2.2em; /* Specific padding for these emoji bullets */
    position: relative;
    margin-bottom: 0.8em;
    font-size: 1.05em; /* Consistent with p, li */
  }
  .pros-cons-list li::before { /* Base styles for emoji bullets */
    position: absolute;
    left: 0;
    font-size: 1.2em;
    top: -2px; /* Adjust vertical alignment if needed */
  }
  .pros-cons-list.dont-get li::before {
    content: "🚫"; /* No/Cross emoji */
  }
  .pros-cons-list.do-get li::before {
    content: "✅"; /* Checkmark emoji */
  }
  /* Nested list styling within pros-cons-list */
  .pros-cons-list ul {
    list-style-type: disc; /* Or keep custom › if preferred */
    padding-left: 25px; /* Indent nested list */
    margin-top: 8px;
  }
  .pros-cons-list ul li::before {
    content: "›"; /* Or use standard disc/circle by removing this for nested */
    color: #4299e1;
    font-weight: bold;
    font-size: 1em; /* Adjust if needed */
    left: -1.2em; /* Adjust positioning for nested bullets */
  }
  /* If you prefer standard bullets for nested lists: */
  /*
  .pros-cons-list ul li::before {
    content: ""; 
  }
  .pros-cons-list ul li {
    padding-left: 0; 
  }
  */


  blockquote {
    border-left: 4px solid #4299e1; /* Using readme link color for accent */
    padding-left: 20px;
    margin-left: 0;
    margin-right: 0;
    font-style: italic;
    color: #4a5568;
    background-color: #f0f5ff; /* Lighter blue background for quote */
    padding-top: 10px;
    padding-bottom: 10px;
    border-radius: 0 8px 8px 0; /* Rounded on right side */
  }
  blockquote p {
    margin-bottom: 0;
  }

</style>

<div class="container">
  <h1 class="consultation-title">AI Consulting by Rishiraj</h1>
  <p style="text-align: center; font-size: 1.15em; color: #2d3748; margin-top: -15px; margin-bottom: 30px;">
    I offer premium AI consulting services tailored to clients who need focused, high-impact support in developing, scaling, or refining their AI/ML systems — especially in Natural Language Processing, Speech Technologies, and AI for Medicine.
  </p>

  <hr class="section-divider">

  <section class="terms-section">
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">💼</span> Consulting Terms</h2>
    <div class="term-item"><strong>Monthly Rate:</strong> <span>₹2,00,000 INR</span></div>
    <div class="term-item"><strong>Availability:</strong> <span>5 days a week (Monday–Friday)</span></div>
    <div class="term-item"><strong>Hours per Day:</strong> <span>5 hours</span></div>
    <div class="term-item"><strong>Total Monthly Hours:</strong> <span>100 hours</span></div>
    <div class="term-item"><strong>Effective Hourly Rate:</strong> <span>₹2,000 INR/hour</span></div>
  </section>

  <hr class="section-divider">

  <section>
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">🚫</span> What You <em>Don’t</em> Get</h2>
    <ul class="pros-cons-list dont-get">
      <li>No random or recurring sync calls</li>
      <li>No daily stand-ups or updates</li>
      <li>No micromanagement</li>
    </ul>
    <p style="margin-top: 15px;">I work independently and deliver with clear goals, timelines, and communication when necessary. You bring a problem, I bring a solution.</p>
  </section>

  <hr class="section-divider">

  <section>
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">🧠</span> What You <em>Do</em> Get</h2>
    <ul class="pros-cons-list do-get">
      <li>Expert-level guidance and hands-on development in:
        <!-- Using a nested ul. Adjusted styling for nested list bullets -->
        <ul>
          <li>Natural Language Processing (NLP)</li>
          <li>Speech & Audio AI</li>
          <li>Medical AI systems</li>
          <li>End-to-end ML pipeline design</li>
          <li>Scalable cloud-based ML deployment (GCP preferred)</li>
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
    <h2><span style="font-size: 0.8em; vertical-align: middle; margin-right: 8px;">💬</span> Contact</h2>
    <p>To discuss your project or explore a consulting engagement, get in touch with a brief outline of your needs.</p>
    <a href="mailto:heyrishiraj@gmail.com" class="button-link large">Get in Touch</a>
    <blockquote style="margin-top: 25px; text-align: left;">
      <p>I only take on a limited number of clients to ensure deep focus and quality. Serious inquiries only.</p>
    </blockquote>
  </section>

  <!-- Optional: Add a footer quote similar to readme.md -->
  <hr class="section-divider">
  <p class="footer-quote">
    <i>Empowering your projects with cutting-edge AI expertise.</i>
  </p>
</div>