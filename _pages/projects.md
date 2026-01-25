---
layout: page
title: projects
permalink: /projects/
description: Rocket propulsion and aerospace engineering projects.
nav: true
nav_order: 2
---

<style>
.project-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.project-item {
  margin-bottom: 2rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid var(--global-divider-color);
}

.project-item:last-child {
  border-bottom: none;
}

.project-title {
  font-size: 1.25rem;
  font-weight: 500;
  margin-bottom: 0.25rem;
}

.project-title a {
  color: var(--global-text-color);
  text-decoration: none;
}

.project-title a:hover {
  color: var(--global-theme-color);
}

.project-description {
  color: var(--global-text-color-light);
  margin-bottom: 0.4rem;
  font-size: 0.95rem;
  line-height: 1.4;
}

.project-meta {
  font-size: 0.875rem;
  color: var(--global-text-color-light);
  display: flex;
  align-items: center;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.project-meta .year,
.project-meta .tag {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
}

.project-meta .tag span {
  color: var(--global-text-color-light);
}

.project-meta .divider {
  color: var(--global-text-color-light);
}
</style>

<ul class="project-list">

<li class="project-item">
  <h3 class="project-title">
    <a href="{{ '/projects/1_project/' | relative_url }}">Hybrid End-Burning Rocket Engine</a>
  </h3>
  <p class="project-description">First-author research on Korea's second end-burning hybrid rocket engine</p>
  <div class="project-meta">
    <span class="year">2026</span>
    <span class="divider">&middot;</span>
    <span class="tag"><span>BUZ-Aerospace</span></span>
  </div>
</li>

<li class="project-item">
  <h3 class="project-title">
    <a href="{{ '/projects/2_project/' | relative_url }}">Solid Rocket Motor</a>
  </h3>
  <p class="project-description">KNO₃ fueled solid rocket achieving 400m+ altitude</p>
  <div class="project-meta">
    <span class="year">2025</span>
    <span class="divider">&middot;</span>
    <span class="tag"><span>BUZ-Aerospace</span></span>
  </div>
</li>

</ul>
