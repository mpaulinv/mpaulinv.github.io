---
title: "Projects"
permalink: /projects/
layout: single
---

<div style="margin-bottom: 2em;">
  <h1 style="margin: 0; font-size: 2.2rem; font-weight: 700; color: #1a202c;">Projects</h1>
  <p style="color: #718096; margin: 0.5em 0 0 0;">Explore my projects and their results</p>
</div>

<!-- Tabs for navigating between projects -->
<div class="tabs">
  <button class="tab-link" onclick="showProject('project1')">Project 1</button>
  <button class="tab-link" onclick="showProject('project2')">Project 2</button>
  <button class="tab-link" onclick="showProject('project3')">Project 3</button>
</div>

<!-- Project content -->
<div id="project1" class="tab-content">
  <h2>Project 1: Machine Learning Model for Risk Assessment</h2>
  <p>This project involved developing a machine learning model to assess financial risks...</p>
  <img src="/assets/images/project1-visualization.png" alt="Project 1 Visualization" style="width: 100%; height: auto;">
</div>

<div id="project2" class="tab-content">
  <h2>Project 2: Credit Scoring Optimization</h2>
  <p>This project optimized credit scoring processes using predictive modeling...</p>
  <img src="/assets/images/project2-visualization.png" alt="Project 2 Visualization" style="width: 100%; height: auto;">
</div>

<div id="project3" class="tab-content">
  <h2>Project 3: Fraud Detection System</h2>
  <p>This project implemented a fraud detection system using advanced analytics...</p>
  <img src="/assets/images/project3-visualization.png" alt="Project 3 Visualization" style="width: 100%; height: auto;">
</div>

<style>
/* Styling for tabs */
.tabs {
  display: flex;
  gap: 1em;
  margin-bottom: 1em;
}

.tab-link {
  background-color: #667eea;
  color: white;
  padding: 0.5em 1em;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-weight: 600;
}

.tab-link:hover {
  background-color: #5a67d8;
}

.tab-content {
  display: none;
  animation: fadeIn 0.3s ease-in-out;
}

.tab-content.active {
  display: block;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>

<script>
/* JavaScript for tab switching */
function showProject(projectId) {
  // Hide all tabs
  const tabs = document.querySelectorAll('.tab-content');
  tabs.forEach(tab => tab.classList.remove('active'));

  // Show selected tab
  const selectedTab = document.getElementById(projectId);
  selectedTab.classList.add('active');
}

// Show the first tab by default on page load
document.addEventListener('DOMContentLoaded', () => {
  showProject('project1');
});
</script>
