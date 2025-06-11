---
layout: single
title: "Projects"
permalink: /projects/
author_profile: true
---

Below are some of my featured projects. Click each tab to learn more.

{% capture projects %}
<!-- Example Project Tab Structure -->
<div class="project-tabs">
  <details>
    <summary><strong>Project Name 1</strong> &mdash; Short headline result/product</summary>
    <ul>
      <li><strong>Description:</strong> Concise summary of what the project does and why.</li>
      <li><strong>Main Results:</strong> Key outcomes, metrics, or features.</li>
      <li><strong>Technologies:</strong> Python, R, SQL, etc.</li>
      <li><a href="https://github.com/mpaulinv/PROJECT_REPO">View on GitHub</a></li>
    </ul>
  </details>
  <details>
    <summary><strong>Project Name 2</strong> &mdash; Short headline result/product</summary>
    <ul>
      <li><strong>Description:</strong> Concise summary of what the project does and why.</li>
      <li><strong>Main Results:</strong> Key outcomes, metrics, or features.</li>
      <li><strong>Technologies:</strong> Python, R, SQL, etc.</li>
      <li><a href="https://github.com/mpaulinv/PROJECT_REPO">View on GitHub</a></li>
    </ul>
  </details>
  <!-- Repeat for more projects -->
</div>
{% endcapture %}

{{ projects | markdownify }}
