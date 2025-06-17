---
title: "Projects"
permalink: /projects/
layout: single
---

<!-- Load modern font for improved typography -->
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Inter:400,500,700&display=swap">
<style>
:root {
  --primary: #2563eb;
  --primary-dark: #1e40af;
  --bg: #f8fafc;
  --card-bg: #fff;
  --border: #e5e7eb;
  --text-main: #23272f;
  --text-muted: #6b7280;
  --badge-bg: #e0e7ef;
  --badge-text: #2563eb;
  --shadow: 0 4px 24px rgba(80,90,120,0.08);
}

/* Layout */
body, .page__content {
  font-family: 'Inter', 'Segoe UI', 'system-ui', sans-serif;
  background: var(--bg) !important;
  color: var(--text-main);
}
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(345px, 1fr));
  gap: 2.2rem;
  margin: 2rem 0 3rem 0;
  padding: 0;
}
.project-card {
  background: var(--card-bg);
  border-radius: 16px;
  box-shadow: var(--shadow);
  display: flex;
  flex-direction: column;
  overflow: hidden;
  border: 1px solid var(--border);
  transition: box-shadow 0.18s, transform 0.15s;
  min-width: 0;
}
.project-card:hover {
  transform: translateY(-5px) scale(1.02);
  box-shadow: 0 8px 28px rgba(40,60,140,0.13);
}

/* Visual elements */
.project-image {
  width: 100%;
  height: 180px;
  object-fit: cover;
  background: #e5e7eb;
  border-bottom: 1px solid var(--border);
  transition: filter 0.18s;
}
.project-card:hover .project-image {
  filter: brightness(0.96) saturate(1.15);
}
.project-content {
  padding: 1.3rem 1.3rem 1.8rem 1.3rem;
  display: flex;
  flex-direction: column;
  height: 100%;
}
.project-title {
  font-size: 1.3rem;
  font-weight: 700;
  margin: 0 0 0.45em 0;
  color: var(--primary-dark);
  letter-spacing: -0.5px;
}
.project-summary {
  font-size: 1.08em;
  color: var(--text-main);
  margin-bottom: 0.65em;
}
.project-description {
  font-size: 1em;
  color: var(--text-muted);
  margin-bottom: 1.1em;
  line-height: 1.6;
}
/* Badges & tags */
.project-tags {
  margin: 0.7em 0 1.2em 0;
}
.tag {
  display: inline-block;
  background: var(--badge-bg);
  color: var(--badge-text);
  font-size: 0.95em;
  border-radius: 7px;
  padding: 0.22em 0.88em;
  margin: 0 0.37em 0.37em 0;
  font-weight: 500;
  letter-spacing: 0.02em;
}
/* Achievements */
.project-achievements {
  margin: 0.7em 0 1em 0;
  padding-left: 1.2em;
}
.project-achievements li {
  font-size: 0.99em;
  color: var(--text-main);
  margin-bottom: 0.5em;
  line-height: 1.5;
}

/* Links and buttons */
.project-links {
  margin-top: auto;
  display: flex;
  gap: 1em;
  flex-wrap: wrap;
}
a.btn {
  background: linear-gradient(90deg, var(--primary) 0%, #4dd0e1 100%);
  color: #fff !important;
  padding: 0.45em 1.2em;
  border: none;
  border-radius: 7px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1em;
  transition: background 0.15s, box-shadow 0.13s;
  box-shadow: 0 2px 8px rgba(80,90,120,0.10);
  display: inline-block;
}
a.btn:hover {
  background: linear-gradient(90deg, var(--primary-dark) 0%, #00bcd4 100%);
  box-shadow: 0 4px 18px rgba(40,60,140,0.13);
}
a.btn-secondary {
  background: #e0e7ef;
  color: var(--primary) !important;
}
a.btn-secondary:hover {
  background: #c7d2fe;
  color: #1e40af !important;
}

/* Headings and text hierarchy */
.projects-title {
  text-align: center;
  font-size: 2.4rem;
  margin: 0.1em 0 0.25em 0;
  font-weight: 700;
  letter-spacing: -1px;
  color: var(--primary-dark);
}
.projects-intro {
  text-align: center;
  color: var(--text-muted);
  font-size: 1.13em;
  margin-bottom: 2.5em;
  max-width: 620px;
  margin-left: auto;
  margin-right: auto;
}

/* Responsive */
@media (max-width: 700px) {
  .project-content { padding: 0.95em 0.5em 1.3em 0.5em; }
  .projects-title { font-size: 1.7rem; }
  .projects-intro { font-size: 1em; }
}
</style>

<h1 class="projects-title">Projects</h1>
<p class="projects-intro">
  A selection of my technical projects, featuring hands-on machine learning, analytics, and automation.<br>
  <span style="color: #2563eb; font-weight:500;">Click a card</span> to view more, or use the GitHub/demo links for code and live results.
</p>

<div class="projects-grid">
  {% for project in site.data.projects %}
  <div class="project-card">
    <!-- Project Image -->
    {% if project.images and project.images[0] %}
      <img src="{{ project.images[0] }}" class="project-image" alt="Screenshot for {{ project.tab }}">
    {% else %}
      <!-- Placeholder image if none provided -->
      <img src="/assets/images/placeholder.png" class="project-image" alt="Project placeholder">
    {% endif %}

    <div class="project-content">
      <!-- Title and quick summary -->
      <div class="project-title">{{ project.tab }}</div>
      <div class="project-summary">{{ project.summary | default: project.description | truncatewords: 24 }}</div>
      <!-- Badges/tech tags -->
      {% if project.tech_stack %}
        <div class="project-tags">
        {% for tech in project.tech_stack %}
          <span class="tag">{{ tech }}</span>
        {% endfor %}
        </div>
      {% endif %}
      <!-- Key achievements (optional, add to your YAML) -->
      {% if project.achievements %}
        <ul class="project-achievements">
        {% for item in project.achievements %}
          <li>{{ item }}</li>
        {% endfor %}
        </ul>
      {% endif %}
      <!-- Description (hidden on card, show on click/modal for next-level UX) -->
      <div class="project-description">{{ project.description }}</div>
      <!-- Project links -->
      <div class="project-links">
        {% if project.url %}
        <a href="{{ project.url }}" class="btn" target="_blank" rel="noopener">GitHub</a>
        {% endif %}
        {% if project.demo %}
        <a href="{{ project.demo }}" class="btn btn-secondary" target="_blank" rel="noopener">Live Demo</a>
        {% endif %}
      </div>
    </div>
  </div>
  {% endfor %}
</div>
