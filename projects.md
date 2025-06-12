---
title: "Projects"
permalink: /projects/
layout: single
---

<style>
/* Sleek Project Tabs Styles */
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
  font-weight: 500; /* Not bold, but not light */
  color: #374151;
  border-bottom: 2px solid transparent;
  transition: border-color 0.2s, color 0.2s, background 0.2s;
  letter-spacing: 0.02em;
  border-radius: 8px 8px 0 0;
  text-transform: capitalize;
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

@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}
</style>

<h1 style="font-family:'Inter','Segoe UI','system-ui',sans-serif; font-weight:600; letter-spacing:0.01em;">Projects</h1>
<p style="font-family:'Inter','Segoe UI','system-ui',sans-serif;">Explore my open source work. Click a tab to view details about each project.</p>

<!-- Tab navigation -->
<div class="project-tabs" id="projectTabs">
  {% assign repos = site.github.public_repositories | where: "owner.login", "mpaulinv" %}
  {% assign filtered_repos = repos | reject: 'name', 'mpaulin' | reject: 'name', 'mpaulin.github.io' %}
  {% for repo in filtered_repos %}
    <button class="project-tab{% if forloop.first %} active{% endif %}" data-tab="project{{ forloop.index }}">
      {{ repo.name | replace: '-', ' ' | capitalize }}
    </button>
  {% endfor %}
</div>

<!-- Tab contents -->
{% for repo in filtered_repos %}
  <div class="project-content{% if forloop.first %} active{% endif %}" id="project{{ forloop.index }}">
    <h2 style="font-weight:500; font-family:'Inter','Segoe UI','system-ui',sans-serif;">
      <a href="{{ repo.html_url }}" target="_blank" rel="noopener" style="color:#2563eb;text-decoration:none;">
        {{ repo.name }}
      </a>
    </h2>
    <p>{{ repo.description | default: "No description provided." }}</p>
    <ul style="list-style: none; padding: 0; margin: 0 0 1em 0; color: #4b5563;">
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
