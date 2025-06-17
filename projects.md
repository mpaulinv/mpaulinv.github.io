---
title: "Projects"
permalink: /projects/
layout: single
---

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Inter:400,500,700&display=swap">

<style>
:root {
  --accent: #2563eb;
  --accent-light: #e8f1ff;
  --bg: #f8fafc;
  --border: #e5e7eb;
  --text-main: #222;
  --text-muted: #60646c;
}

body, .project-content, .project-tab, .project-section-title, .project-meta, .project-tech {
  font-family: 'Inter', 'Segoe UI', 'system-ui', sans-serif;
  color: var(--text-main);
  line-height: 1.7;
}

.projects-title {
  text-align: center;
  font-size: 2.1rem;
  margin: 0.1em 0 0.25em 0;
  font-weight: 700;
  letter-spacing: -1px;
  color: var(--text-main);
}
.projects-intro {
  text-align: center;
  color: var(--text-main);
  font-size: 1.1em;
  margin-bottom: 2em;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

/* Tab navigation */
.project-tabs {
  display: flex;
  flex-wrap: wrap;
  border-bottom: 2px solid var(--border);
  margin-bottom: 0;
  gap: 0.5em;
  background: var(--bg);
  padding-left: 0.5em;
  justify-content: center;
  max-width: 950px;
  margin-left: auto;
  margin-right: auto;
}

.project-tab {
  padding: 0.8em 1.9em 0.7em 1.9em;
  cursor: pointer;
  background: none;
  border: none;
  font-size: 1.08em;
  font-weight: 500;
  color: var(--text-main);
  border-bottom: 2.5px solid transparent;
  border-radius: 8px 8px 0 0;
  letter-spacing: 0.01em;
  transition: border-color 0.2s, background 0.2s, color 0.2s;
  outline: none;
  margin-bottom: -2px;
  position: relative;
}

.project-tab.active {
  border-bottom: 2.5px solid var(--accent);
  background: #fff;
  color: var(--text-main);
  z-index: 2;
}

.project-tab:focus {
  background: var(--accent-light);
  outline: none;
}

/* Project content area */
.project-content {
  display: none;
  max-width: 950px;
  margin: 0 auto 2.2em auto;
  padding: 2.1em 2.2em 2.2em 2.2em;
  background: #fff;
  border: 2px solid var(--border);
  border-top: none;
  border-radius: 0 0 14px 14px;
  word-break: break-word;
  overflow-wrap: anywhere;
  font-size: 1.09em;
  box-sizing: border-box;
  position: relative;
  top: -2px;
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
  font-size: 1.37rem;
  font-weight: 700;
  margin: 0 0 0.3em 0;
  color: var(--text-main);
  letter-spacing: -0.5px;
}

.project-meta, .project-tech {
  font-size: 0.99em;
  color: var(--text-muted);
  margin-bottom: 0.7em;
}
.project-section-title {
  font-size: 1.12em;
  font-weight: 600;
  color: var(--text-main);
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
  color: var(--text-main);
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
  border: 1px solid var(--border);
  background: #e5e7eb;
}
@media (max-width: 1050px) {
  .project-content, .project-tabs { max-width: 99vw; }
}
@media (max-width: 700px) {
  .project-content { padding: 1.3em 0.5em 1.5em 0.5em; }
  .project-images { flex-direction: column; gap: 1em; }
  .project-images img { max-width: 100%; }
  .projects-title { font-size: 1.35rem; }
  .projects-intro { font-size: 1em; }
  .project-tab { padding: 0.6em 1em 0.6em 1em; }
}

/* Badges & tags */
.project-tags {
  margin: 0.7em 0 1.2em 0;
}
.tag {
  display: inline-block;
  background: #eef1f7;
  color: var(--text-muted);
  font-size: 0.95em;
  border-radius: 7px;
  padding: 0.22em 0.88em;
  margin: 0 0.37em 0.37em 0;
  font-weight: 500;
  letter-spacing: 0.02em;
}

/* Buttons */
a, a:visited {
  color: var(--accent);
  text-decoration: underline;
  transition: color .15s;
}
a:hover {
  color: var(--accent);
  text-decoration: underline;
}
a.btn {
  background: var(--accent);
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
  background: var(--accent-light);
  color: var(--accent) !important;
  box-shadow: 0 4px 18px rgba(40,60,140,0.13);
}
</style>

<h1 class="projects-title">Projects</h1>
<p class="projects-intro">
  Select a project tab to see details, images, key methods, and results.
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
      <a href="{{ project.demo }}" class="btn" target="_blank" rel="noopener" style="background: #eef1f7; color: #2563eb !important; margin-left:1em;">Live Demo</a>
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
      if (window.innerWidth < 700) {
        contents[idx].scrollIntoView({behavior: 'smooth', block: 'start'});
      }
    });
  });
});
</script>
