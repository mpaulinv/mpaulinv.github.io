---
title: "Projects"
permalink: /projects/
layout: single
---

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Inter:400,500,600&display=swap">

<style>
:root {
  --accent: #1184b1;
  --accent-light: #f0fbff;
  --neutral: #23272f;
  --neutral-light: #f8fafc;
  --muted: #6b7280;
  --section-title: #1184b1;
}

body, .project-content, .project-tab, .project-section-title, .project-meta, .project-tech {
  font-family: 'Inter', 'Segoe UI', 'system-ui', sans-serif;
  color: var(--neutral);
  line-height: 1.7;
}

.project-tabs {
  display: flex;
  border-bottom: 2px solid #e5e7eb;
  margin-bottom: 2em;
  gap: 0.5em;
  background: var(--neutral-light);
  padding-left: 0.5em;
}

.project-tab {
  padding: 0.7em 1.3em;
  cursor: pointer;
  background: #f5f6fa;
  border: none;
  font-size: 1.08em;
  font-weight: 500;
  color: var(--muted);
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
  background: var(--accent-light);
}

.project-content {
  display: none;
  max-width: 750px;
  margin: 0 auto 2.5em auto;
  padding: 2.2em 1.5em 2.5em 1.5em;
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 4px 24px rgba(80,90,120,0.07);
  word-break: break-word;
  overflow-wrap: anywhere;
  font-size: 1.06em;
}

.project-content.active {
  display: block;
}

.project-section-title {
  font-size: 1.12em;
  font-weight: 600;
  color: var(--section-title);
  margin-bottom: 0.35em;
  margin-top: 1.25em;
  letter-spacing: 0.01em;
}

.project-meta, .project-tech {
  font-size: 0.98em;
  color: var(--muted);
  margin-bottom: 1em;
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
  border: 1px solid #e5e7eb;
}

a, a:visited {
  color: var(--accent);
  text-decoration: underline;
  transition: color .15s;
}
a:hover {
  color: #0d6d98;
  text-decoration: underline;
}

a.btn {
  background: linear-gradient(90deg, #1184b1 0%, #4dd0e1 100%);
  color: #fff !important;
  padding: 0.48em 1.18em;
  border: none;
  border-radius: 7px;
  text-decoration: none;
  font-weight: bold;
  font-size: 1em;
  margin-top: 1.1em;
  display: inline-block;
  box-shadow: 0 2px 8px rgba(80,90,120,0.1);
  transition: background 0.15s;
}
a.btn:hover {
  background: linear-gradient(90deg, #0d6d98 0%, #00bcd4 100%);
}

@media (max-width: 900px) {
  .project-content {
    padding: 1.3em 0.4em 2em 0.4em;
  }
  .project-images {
    flex-direction: column;
    gap: 1em;
  }
  .project-images img {
    max-width: 100%;
  }
}
</style>

<h1 style="font-family:'Inter','Segoe UI','system-ui',sans-serif; font-weight:600; letter-spacing:0.01em; color: #23272f;">Projects</h1>
<p style="font-family:'Inter','Segoe UI','system-ui',sans-serif;">Explore my open source work. Click a tab to view details about each project.</p>

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
    <h2 style="margin-top:0; margin-bottom:0.7em; font-size:1.5em; font-weight:600;">
      <a href="{{ project.url }}" target="_blank" rel="noopener">
        {{ project.tab }}
      </a>
    </h2>
    <p class="project-meta">
      {% if project.date %}<strong>Date:</strong> {{ project.date }}{% endif %}
    </p>
    <p style="font-style:italic; color: #495670; margin-bottom: 1.3em;">{{ project.description }}</p>
    {% if project.objective %}
      <div class="project-section-title">Objective</div>
      <p>{{ project.objective }}</p>
    {% endif %}
    {% if project.overview %}
      <div class="project-section-title">Overview</div>
      <p>{{ project.overview }}</p>
    {% endif %}
    {% if project.tech_stack %}
      <div class="project-tech"><strong>Tech Stack:</strong> {{ project.tech_stack | join: ', ' }}</div>
    {% endif %}
    {% if project.methods %}
      <div class="project-section-title">Key Methods & Challenges</div>
      <div style="white-space:pre-line;">{{ project.methods }}</div>
    {% endif %}
    {% if project.results %}
      <div class="project-section-title">Results</div>
      <p>{{ project.results }}</p>
    {% endif %}
    {% if project.images %}
      <div class="project-images">
        {% for image in project.images %}
          <img src="{{ image }}" alt="Project image: {{ project.tab }} {{ forloop.index }}">
        {% endfor %}
      </div>
    {% endif %}
    {% if project.impact %}
      <div class="project-section-title">Impact / Lessons Learned</div>
      <p>{{ project.impact }}</p>
    {% endif %}
    <a href="{{ project.url }}" class="btn" target="_blank" rel="noopener">View on GitHub</a>
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
    });
  });
});
</script>
