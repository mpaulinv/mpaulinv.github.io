<!-- Professional header section with square photo -->
<div style="display: flex; flex-wrap: wrap; align-items: flex-start; gap: 3em; margin-bottom: 3.5em; padding: 2em 0;">

  <!-- Square Profile Photo -->
  <img src="/assets/images/profile.jpg" alt="Mario Paulin Vega" style="width: 200px; height: 200px; object-fit: cover; border-radius: 12px; box-shadow: 0 8px 32px rgba(0,0,0,0.12); flex-shrink: 0; border: 2px solid #f8f9fa;">

  <!-- About Text -->
  <div style="flex: 1; min-width: 300px;">
    <h1 style="margin-top: 0; font-size: 2.4rem; font-weight: 700; color: #1a202c; margin-bottom: 0.5em;">Mario Paulin Vega</h1>
    <h2 style="font-size: 1.2rem; font-weight: 400; color: #4a5568; margin-bottom: 1.5em; letter-spacing: 0.5px;">Data Science Manager | Economics | Machine Learning</h2>

    <p style="font-size: 1.05rem; line-height: 1.7; color: #2d3748; margin-bottom: 1.2em;">
      Welcome to my portfolio. I'm a Data Science Manager with a background in economics and a genuine enthusiasm for making sense of complex data.
      Over the years, I've led projects in the financial sector that use analytics and machine learning to solve real business challenges.
    </p>

    <p style="font-size: 1.05rem; line-height: 1.7; color: #2d3748; margin-bottom: 1.2em;">
      I enjoy the hands-on side of data science: building predictive models, validating results, creating data pipelines, and ensuring code quality.
      What drives me is collaborating with others—leading and mentoring teams while working together toward meaningful results.
    </p>

    <p style="font-size: 1.05rem; line-height: 1.7; color: #2d3748;">
      My technical expertise includes Python, R, SAS, and SQL, combined with strategic business understanding to connect data work to actionable decisions.
    </p>
  </div>
</div>

<!-- Professional navigation cards -->
<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 2em; margin-bottom: 4em;">

  <!-- Projects Card -->
  <a href="/projects/" class="nav-card" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border: none; border-radius: 16px; box-shadow: 0 10px 40px rgba(102, 126, 234, 0.2); display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 2.5em 2em; text-decoration: none; color: white; font-weight: 600; font-size: 1.1rem; transition: all 0.3s ease; position: relative; overflow: hidden;">
    <div style="font-size: 3em; margin-bottom: 0.8em; opacity: 0.9;">💼</div>
    <div style="font-size: 1.2rem; font-weight: 700; margin-bottom: 0.3em;">Projects</div>
    <div style="font-size: 0.9rem; opacity: 0.8; text-align: center;">View my data science work</div>
  </a>

  <!-- CV Card -->
  <a href="/cv/" class="nav-card" style="background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); border: none; border-radius: 16px; box-shadow: 0 10px 40px rgba(240, 147, 251, 0.2); display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 2.5em 2em; text-decoration: none; color: white; font-weight: 600; font-size: 1.1rem; transition: all 0.3s ease; position: relative; overflow: hidden;">
    <div style="font-size: 3em; margin-bottom: 0.8em; opacity: 0.9;">📋</div>
    <div style="font-size: 1.2rem; font-weight: 700; margin-bottom: 0.3em;">Curriculum Vitae</div>
    <div style="font-size: 0.9rem; opacity: 0.8; text-align: center;">Download my resume</div>
  </a>

  <!-- Contact Card -->
  <a href="mailto:mpaulinv@gmail.com" class="nav-card" style="background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%); border: none; border-radius: 16px; box-shadow: 0 10px 40px rgba(79, 172, 254, 0.2); display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 2.5em 2em; text-decoration: none; color: white; font-weight: 600; font-size: 1.1rem; transition: all 0.3s ease; position: relative; overflow: hidden;">
    <div style="font-size: 3em; margin-bottom: 0.8em; opacity: 0.9;">💬</div>
    <div style="font-size: 1.2rem; font-weight: 700; margin-bottom: 0.3em;">Get In Touch</div>
    <div style="font-size: 0.9rem; opacity: 0.8; text-align: center;">Let's connect and collaborate</div>
  </a>

</div>

<style>
/* Professional hover effects */
.nav-card:hover {
  transform: translateY(-8px) !important;
  box-shadow: 0 20px 60px rgba(0,0,0,0.15) !important;
  text-decoration: none !important;
}

/* Subtle animations */
.nav-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(255,255,255,0.1);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.nav-card:hover::before {
  opacity: 1;
}

/* Overall page styling */
body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}

/* Professional spacing */
.page__content {
  max-width: 1000px;
  margin: 0 auto;
  padding: 0 2em;
}
</style>
