<!-- Responsive flexbox for photo + about -->
<div style="display: flex; flex-wrap: wrap; align-items: flex-start; gap: 2.2em; margin-bottom: 2.2em;">

  <!-- Profile Photo -->
  <img src="/assets/images/profile.jpg" alt="Mario Paulin Vega" style="width: 170px; height: 170px; object-fit: cover; border-radius: 50%; box-shadow: 0 4px 20px rgba(0,0,0,0.08); flex-shrink: 0; background: #f7faf7; border: 4px solid #e0eee0;">

  <!-- About Text -->
  <div style="flex: 1; min-width: 260px;">
    <h1 style="margin-top: 0; font-size: 2rem; font-weight: 600;">Hi, I’m Mario Paulin Vega!</h1>

    <p>
      Welcome to my portfolio. I’m a Data Science Manager with a background in economics and a genuine enthusiasm for making sense of complex data.
      Over the years, I’ve led projects in the financial sector that use analytics and machine learning to solve real business challenges—from risk assessment to improving how teams work.
    </p>

    <p>
      I enjoy the hands-on side of data science: building predictive models, validating results, creating data pipelines, and making sure the code is clean and reliable.
      What really drives me is collaborating with others—leading and mentoring teams, and helping people grow while working together toward meaningful results.
    </p>

    <p>
      My technical toolkit includes Python, R, SAS, and SQL, but I’m equally passionate about understanding the bigger picture and connecting data work to strategic decisions.
      Whether it’s model validation, risk analytics, or automating processes, I’m committed to making data science practical, accurate, and impactful.
    </p>

    <p>
      Thanks for stopping by. Feel free to explore my projects, check out my CV, or get in touch if you want to connect.
    </p>
  </div>
</div>

<!-- Professional tiles/cards for navigation -->
<div style="display: flex; gap: 2em; flex-wrap: wrap; margin-bottom: 3em;">

  <!-- Projects Card -->
  <a href="/projects/" style="flex: 1 1 180px; min-width: 180px; max-width: 250px; background: #f7fff8; border-radius: 14px; border: 1.5px solid #b4ecc4; box-shadow: 0 2px 12px rgba(36,139,69,0.07); display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 2.2em 1.3em; text-decoration: none; color: #285a37; font-weight: 600; font-size: 1.13rem; transition: box-shadow 0.18s, border 0.18s;">
    <span style="font-size:2.2em; margin-bottom:0.4em;">💡</span>
    Projects
  </a>

  <!-- CV Card -->
  <a href="/cv/" style="flex: 1 1 180px; min-width: 180px; max-width: 250px; background: #f5fafc; border-radius: 14px; border: 1.5px solid #bed8e6; box-shadow: 0 2px 12px rgba(44,92,126,0.07); display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 2.2em 1.3em; text-decoration: none; color: #34506a; font-weight: 600; font-size: 1.13rem; transition: box-shadow 0.18s, border 0.18s;">
    <span style="font-size:2.2em; margin-bottom:0.4em;">📄</span>
    CV
  </a>

  <!-- Contact Card -->
  <a href="mailto:your@email.com" style="flex: 1 1 180px; min-width: 180px; max-width: 250px; background: #fffef7; border-radius: 14px; border: 1.5px solid #f5e9a8; box-shadow: 0 2px 12px rgba(139,128,36,0.07); display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 2.2em 1.3em; text-decoration: none; color: #7d7422; font-weight: 600; font-size: 1.13rem; transition: box-shadow 0.18s, border 0.18s;">
    <span style="font-size:2.2em; margin-bottom:0.4em;">📬</span>
    Contact
  </a>

</div>

<style>
/* Add tile/card hover effect */
a[style*="box-shadow"] {
  transition: box-shadow 0.18s, border 0.18s;
}
a[style*="box-shadow"]:hover {
  box-shadow: 0 8px 24px rgba(36,139,69,0.13) !important;
  border-color: #41b66e !important;
  text-decoration: none !important;
}
</style>
