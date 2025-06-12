---
title: "Projects"
permalink: /projects/
layout: single
---

<style>
/* Tab navigation styles */
.project-tabs {
  display: flex;
  border-bottom: 2px solid #e2e8f0;
  margin-bottom: 2em;
  gap: 2px;
}

.project-tab {
  padding: 0.75em 1.75em;
  cursor: pointer;
  background: none;
  border: none;
  font-size: 1.1em;
  font-weight: 600;
  color: #2d3748;
  border-bottom: 2px solid transparent;
  transition: border-color 0.2s, color 0.2s;
}

.project-tab.active {
  border-bottom: 2.5px solid #4299e1;
  color: #4299e1;
  background: #f7fafc;
}

.project-content {
  display: none;
  animation: fadeIn 0.3s;
  padding-top: 1.5em;
}

.project-content.active {
  display: block;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}
</style>

<h1>Projects</h1>
<p>Explore my open source work. Click on a tab to view details about each project.</p>

<!-- Tab navigation -->
<div class="project-tabs" id="projectTabs">
  {% assign repos = site.github.public_repositories | where: "owner.login", "mpaulinv" %}
  {% for repo in repos %}
    <button class="project-tab{% if forloop.first %} active{% endif %}" data-tab="project{{ forloop.index }}">
      {{ repo.name }}
    </button>
  {% endfor %}
</div>

<!-- Tab contents -->
{% for repo in repos %}
  <div class="project-content{% if forloop.first %} active{% endif %}" id="project{{ forloop.index }}">
    <h2>
      <a href="{{ repo.html_url }}" target="_blank" rel="noopener">
        {{ repo.name }}
      </a>
    </h2>
    <p>{{ repo.description | default: "No description provided." }}</p>
    <ul style="list-style: none; padding: 0; margin: 0 0 1em 0; color: #4a5568;">
      <li>
        <strong>Language:</strong> {{ repo.language | default: "N/A" }}
        &nbsp;|&nbsp;
        <strong>★</strong> {{ repo.stargazers_count }}
        &nbsp;|&nbsp;
        <strong>Last updated:</strong> {{ repo.updated_at | date: "%b %d, %Y" }}
      </li>
    </ul>
    <a href="{{ repo.html_url }}" class="btn" target="_blank" rel="noopener">View on GitHub</a>
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
