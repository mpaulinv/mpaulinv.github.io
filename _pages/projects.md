---
title: "Projects"
permalink: /projects/
layout: single
---

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Inter:400,500,700&display=swap">

<style>
:root {
  --accent: #2563eb;
  --accent-dark: #1e40af;
  --bg: #f8fafc;
  --card-bg: #fff;
  --border: #e5e7eb;
  --text-main: #23272f;
  --text-muted: #6b7280;
  --badge-bg: #e0e7ef;
  --badge-text: #2563eb;
  --shadow: 0 4px 24px rgba(80,90,120,0.08);
}

body, .project-content, .project-tab, .project-section-title, .project-meta, .project-tech {
  font-family: 'Inter', 'Segoe UI', 'system-ui', sans-serif;
  color: var(--text-main);
  line-height: 1.7;
}

.projects-title {
  text-align: center;
  font-size: 2.2rem;
  margin: 0.1em 0 0.25em 0;
  font-weight: 700;
  letter-spacing: -1px;
  color: var(--accent-dark);
}
.projects-intro {
  text-align: center;
  color: var(--text-muted);
  font-size: 1.15em;
  margin-bottom: 2.5em;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

/* Tab navigation */
.project-tabs {
  display: flex;
  flex-wrap: wrap;
  border-bottom: 2px solid var(--border);
  margin-bottom: 2em;
  gap: 0.5em;
  background: var(--bg);
  padding-left: 0.5em;
  justify-content: center;
}

.project-tab {
  padding: 0.7em 1.3em;
  cursor: pointer;
  background: #f5f6fa;
  border: none;
  font-size: 1.08em;
  font-weight: 500;
  color: var(--text-muted);
  border-bottom: 2px solid transparent;
  transition: border-color 0.2s, color 0.2s, background 0.2s, box-shadow 0.2s;
  border-radius: 10px 10px 0 0;
  outline: none;
  letter-spacing: 0.01em;
}

.project-tab.active {
  color: var(--accent);
  background: #fff;
  border-bottom: 2.5px solid var(--accent);
  box-shadow: 0 2px 8px rgba(0,0,0,0.04);
  position: relative;
  z-index: 2;
}

.project-tab:focus {
  outline: none;
  box-shadow: 0 0 0 2px #b8e5f5;
  background: #f0fbff;
}

/* Project content area */
.project-content {
  display: none;
  max-width: 750px;
  margin: 0 auto 2.5em auto;
  padding: 2.2em 1.5em 2.5em 1.5em;
  background: #fff;
  border-radius: 14px;
  box-shadow: var(--shadow);
  word-break: break-word;
  overflow-wrap: anywhere;
  font-size: 1.07em;
}

.project-content.active {
  display: block;
  animation: fadeIn 0.3s;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}

.project-title {
  font-size: 1.4rem;
  font-weight: 700;
  margin: 0 0 0.35em 0;
  color: var(--accent-dark);
  letter-spacing: -0.5px;
}

.project-meta, .project-tech {
  font-size: 0.99em;
  color: var(--text-muted);
  margin-bottom: 0.7em;
}
.project-section-title {
  font-size: 1.10em;
  font-weight: 600;
  color: var(--accent);
  margin-bottom: 0.35em;
  margin-top: 1.25em;
  letter-spacing: 0.01em;
}

.project-summary {
  font-size: 1.04em;
  color: var(--text-main);
  margin-bottom: 0.9em;
  font-weight: 500;
}

.project-description {
  font-size: 1em;
  color: var(--text-muted);
  margin-bottom: 1.2em;
  line-height: 1.6;
}

.project-images {
  display: flex;
  gap: 1.2em;
  flex-wrap: wrap;
  margin-bottom: 1.5em;
  margin-top: 1em;
}
.project-images img {
  max-width: 340px;
  width: 100%;
  border-radius: 8px;
  box-shadow: 0 2px 12px rgba(80,90,120,0.10);
  border: 1px solid var(--border);
  background: #e5e7eb;
}
@media (max-width: 700px) {
  .project-content { padding: 1.3em 0.4em 2em 0.4em; }
  .project-images { flex-direction: column; gap: 1em; }
  .project-images img { max-width: 100%; }
  .projects-title { font-size: 1.5rem; }
  .projects-intro { font-size: 1em; }
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

a, a:visited {
  color: var(--accent);
  text-decoration: underline;
  transition: color .15s;
}
a:hover {
  color: var(--accent-dark);
  text-decoration: underline;
}
a.btn {
  background: linear-gradient(90deg, var(--accent) 0%, #4dd0e1 100%);
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
  margin-top: 1.1em;
}
a.btn:hover {
  background: linear-gradient(90deg, var(--accent-dark) 0%, #00bcd4 100%);
  box-shadow: 0 4px 18px rgba(40,60,140,0.13);
}
</style>

<h1 class="projects-title">Projects</h1>
<p class="projects-intro">
  Explore my technical work. Select a project tab to see details, images, key methods, and results.<br>
  <span style="color: #2563eb; font-weight:500;">Each project is fully described below with images and links.</span>
</p>

<!-- Tab navigation -->
<div class="project-tabs" id="projectTabs">
  {% for project in site.data.projects %}
    <button class="project-tab{% if forloop.first %} active{% endif %}" data-tab="project{{ forloop.index }}">
      {{ project.tab }}
    </button>
  {% endfor %}
</div>

<!-- Tab contents -->
{% for project in site.data.projects %}
  <div class="project-content{% if forloop.first %} active{% endif %}" id="project{{ forloop.index }}">
    <div class="project-title">
      <a href="{{ project.url }}" target="_blank" rel="noopener" style="text-decoration:none; color:inherit;">
        {{ project.tab }}
      </a>
    </div>
    <p class="project-meta">
      {% if project.date %}<strong>Date:</strong> {{ project.date }}{% endif %}
    </p>
    {% if project.summary %}
      <div class="project-summary">{{ project.summary }}</div>
    {% endif %}
    {% if project.tech_stack %}
      <div class="project-tags">
      {% for tech in project.tech_stack %}
        <span class="tag">{{ tech }}</span>
      {% endfor %}
      </div>
    {% endif %}
    {% if project.images %}
      <div class="project-images">
        {% for image in project.images %}
          <img src="{{ image }}" alt="Project image: {{ project.tab }} {{ forloop.index }}">
        {% endfor %}
      </div>
    {% endif %}
    <div class="project-description">{{ project.description }}</div>

    {% if project.objective %}
      <div class="project-section-title">Objective</div>
      <p>{{ project.objective }}</p>
    {% endif %}
    {% if project.overview %}
      <div class="project-section-title">Overview</div>
      <p>{{ project.overview }}</p>
    {% endif %}
    {% if project.methods %}
      <div class="project-section-title">Key Methods & Challenges</div>
      <div style="white-space:pre-line;">{{ project.methods }}</div>
    {% endif %}
    {% if project.results %}
      <div class="project-section-title">Results</div>
      <p>{{ project.results }}</p>
    {% endif %}
    {% if project.impact %}
      <div class="project-section-title">Impact / Lessons Learned</div>
      <p>{{ project.impact }}</p>
    {% endif %}
    <a href="{{ project.url }}" class="btn" target="_blank" rel="noopener">View on GitHub</a>
    {% if project.demo %}
      <a href="{{ project.demo }}" class="btn" target="_blank" rel="noopener" style="background: #e0e7ef; color: #2563eb !important; margin-left:1em;">Live Demo</a>
    {% endif %}
  </div>
{% endfor %}

<script>
document.addEventListener('DOMContentLoaded', function() {
  const tabs = document.querySelectorAll('.project-tab');
  const contents = document.querySelectorAll('.project-content');
  tabs.forEach((tab, idx) => {
    tab.addEventListener('click', () => {
      tabs.forEach(t => t.classList.remove('active'));
      contents.forEach(c => c.classList.remove('active'));
      tab.classList.add('active');
      contents[idx].classList.add('active');
      // Scroll to top of content area on mobile
      if (window.innerWidth < 700) {
        contents[idx].scrollIntoView({behavior: 'smooth', block: 'start'});
      }
    });
  });
});
</script>
