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
    max-width: 800px;
    margin: 20px auto;
    padding: 30px;
    background-color: #ffffff;
    border-radius: 12px;
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
  }

  h1, h2 {
    font-family: 'Gallient', serif;
    color: #1a202c; /* Darker heading color */
  }
  h1 { 
    font-size: 2.8em; 
    text-align: center;
    margin-bottom: 25px;
    padding-bottom: 15px;
    border-bottom: 2px solid #e2e8f0;
  }
  h2 { 
    font-size: 2.0em; 
    margin-top: 1.8em; 
    margin-bottom: 0.8em; 
    padding-bottom: 0.4em;
    border-bottom: 1px solid #e2e8f0;
  }

  p, li {
    font-size: 1.05em;
    color: #4a5568; /* Slightly lighter text color */
  }

  a {
    color: #3182ce; /* A slightly different blue for this page */
    text-decoration: none;
    transition: color 0.2s ease-in-out;
  }
  a:hover {
    color: #2c5282; /* Darker blue on hover */
    text-decoration: underline;
  }

  .section-divider {
    border: 0;
    height: 1px;
    background: #e2e8f0;
    margin: 40px 0;
  }

  .terms-section .term-item {
    background-color: #f7fafc;
    border: 1px solid #e2e8f0;
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
    color: #3182ce;
  }

  .pros-cons-list {
    list-style-type: none;
    padding-left: 0;
  }
  .pros-cons-list li {
    padding-left: 2.2em;
    position: relative;
    margin-bottom: 0.8em;
    font-size: 1.1em;
  }
  .pros-cons-list.dont-get li::before {
    content: "🚫"; /* No/Cross emoji */
    position: absolute;
    left: 0;
    font-size: 1.2em;
    top: -2px;
  }
  .pros-cons-list.do-get li::before {
    content: "✅"; /* Checkmark emoji */
    position: absolute;
    left: 0;
    font-size: 1.2em;
    top: -2px;
  }
  
  .contact-button {
    display: inline-block;
    background-color: #3182ce;
    color: #ffffff !important;
    padding: 12px 25px;
    border-radius: 8px;
    font-weight: bold;
    text-decoration: none;
    transition: background-color 0.2s ease-in-out;
    font-size: 1.1em;
  }
  .contact-button:hover {
    background-color: #2c5282;
    text-decoration: none;
  }

  blockquote {
    border-left: 4px solid #3182ce;
    padding-left: 20px;
    margin-left: 0;
    margin-right: 0;
    font-style: italic;
    color: #4a5568;
    background-color: #f0f9ff; /* Light blue background for quote */
    padding-top: 10px;
    padding-bottom: 10px;
    border-radius: 0 8px 8px 0; /* Rounded on right side */
  }
  blockquote p {
    margin-bottom: 0;
  }
</style>

<div class="container">
  <h1>AI Consulting by Rishiraj</h1>
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
        <ul style="list-style-type: disc; padding-left: 25px; margin-top: 8px;">
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
    <a href="mailto:heyrishiraj@gmail.com" class="contact-button">Get in Touch</a>
    <blockquote style="margin-top: 25px; text-align: left;">
      <p>I only take on a limited number of clients to ensure deep focus and quality. Serious inquiries only.</p>
    </blockquote>
  </section>
</div>