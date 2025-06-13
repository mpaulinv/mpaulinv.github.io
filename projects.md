---
title: "Projects"
permalink: /projects/
layout: single
---

<style>
.project-tabs {
  display: flex;
  border-bottom: 2px solid #e5e7eb;
  margin-bottom: 2em;
  gap: 2px;
  font-family: 'Inter', 'Segoe UI', 'system-ui', sans-serif;
}

.project-tab {
  padding: 0.75em 1.5em;
  cursor: pointer;
  background: none;
  border: none;
  font-size: 1.08em;
  font-weight: 500;
  color: #374151;
  border-bottom: 2px solid transparent;
  transition: border-color 0.2s, color 0.2s, background 0.2s;
  letter-spacing: 0.02em;
  border-radius: 8px 8px 0 0;
  text-transform: none;
}

.project-tab.active {
  border-bottom: 2.5px solid #2563eb;
  color: #2563eb;
  background: #f3f4f6;
}

.project-tab:focus {
  outline: none;
  background: #e0e7ef;
}

.project-content {
  display: none;
  animation: fadeIn 0.3s;
  padding-top: 1.5em;
  font-family: 'Inter', 'Segoe UI', 'system-ui', sans-serif;
  color: #2d3748;
}

.project-content.active {
  display: block;
}

.project-section-title {
  font-size: 1.1em;
  font-weight: 600;
  color: #2563eb;
  margin-bottom: 0.3em;
  margin-top: 1.3em;
}

.project-meta {
  font-size: 0.97em;
  color: #6b7280;
  margin-bottom: 1em;
  font-family: 'Inter', 'Segoe UI', 'system-ui', sans-serif;
}

.project-tech {
  font-size: 0.97em;
  color: #374151;
  margin-bottom: 1em;
  font-family: 'Inter', 'Segoe UI', 'system-ui', sans-serif;
}

.project-images {
  display: flex;
  gap: 1.5em;
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
@media (max-width: 600px) {
  .project-images {
    flex-direction: column;
    gap: 1em;
  }
  .project-images img {
    max-width: 100%;
  }
}

@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}
</style>

<h1 style="font-family:'Inter','Segoe UI','system-ui',sans-serif; font-weight:600; letter-spacing:0.01em;">Projects</h1>
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
    <h2>
      <a href="{{ project.url }}" target="_blank" rel="noopener" style="color:#2563eb;text-decoration:none;">
        {{ project.tab }}
      </a>
    </h2>
    <p class="project-meta">
      {% if project.date %}<strong>Date:</strong> {{ project.date }}{% endif %}
    </p>
    <p style="font-style:italic; color:#64748b;">{{ project.description }}</p>

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
