---
layout: page
title: projects
permalink: /projects/
description: Rocket propulsion and aerospace engineering projects.
nav: true
nav_order: 2
---

<style>
/* Tag filter buttons */
.tag-filters {
  margin-bottom: 1.5rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tag-filter-btn {
  background: none;
  border: 1px solid var(--global-divider-color);
  border-radius: 1rem;
  padding: 0.25rem 0.75rem;
  font-size: 0.8rem;
  color: var(--global-text-color-light);
  cursor: pointer;
  transition: all 0.2s ease;
}

.tag-filter-btn:hover,
.tag-filter-btn.active {
  background-color: var(--global-theme-color);
  border-color: var(--global-theme-color);
  color: white;
}

/* Project list */
.project-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.project-item {
  margin-bottom: 1.25rem;
  padding-bottom: 1rem;
  border-bottom: 1px solid var(--global-divider-color);
}

.project-item:last-child {
  border-bottom: none;
}

.project-item.hidden {
  display: none;
}

.project-title {
  font-size: 1.15rem;
  font-weight: 500;
  margin-bottom: 0.2rem;
  line-height: 1.3;
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
  margin-bottom: 0.3rem;
  font-size: 0.9rem;
  line-height: 1.4;
}

.project-meta {
  font-size: 0.8rem;
  color: var(--global-text-color-light);
  display: flex;
  align-items: center;
  gap: 0.4rem;
  flex-wrap: wrap;
  line-height: 1.3;
}

.project-meta .year {
  color: var(--global-text-color-light);
}

.project-meta .divider {
  color: var(--global-text-color-light);
}

.project-meta .tag-link {
  color: var(--global-text-color-light);
  text-decoration: none;
  cursor: pointer;
}

.project-meta .tag-link:hover {
  color: var(--global-theme-color);
}
</style>

<!-- Tag filter buttons -->
<div class="tag-filters">
  <button class="tag-filter-btn active" data-tag="all">All</button>
  <button class="tag-filter-btn" data-tag="buz-aerospace">#buz-aerospace</button>
  <button class="tag-filter-btn" data-tag="rocket">#rocket</button>
  <button class="tag-filter-btn" data-tag="research">#research</button>
</div>

<ul class="project-list">

<li class="project-item" data-tags="buz-aerospace rocket research">
  <h3 class="project-title">
    <a href="{{ '/projects/1_project/' | relative_url }}">Hybrid End-Burning Rocket Engine</a>
  </h3>
  <p class="project-description">First-author research on Korea's second end-burning hybrid rocket engine</p>
  <div class="project-meta">
    <span class="year">2026</span>
    <span class="divider">&middot;</span>
    <a class="tag-link" onclick="filterByTag('buz-aerospace')">#buz-aerospace</a>
    <a class="tag-link" onclick="filterByTag('rocket')">#rocket</a>
    <a class="tag-link" onclick="filterByTag('research')">#research</a>
  </div>
</li>

<li class="project-item" data-tags="buz-aerospace rocket">
  <h3 class="project-title">
    <a href="{{ '/projects/2_project/' | relative_url }}">Solid Rocket Motor</a>
  </h3>
  <p class="project-description">KNO₃ fueled solid rocket achieving 400m+ altitude</p>
  <div class="project-meta">
    <span class="year">2025</span>
    <span class="divider">&middot;</span>
    <a class="tag-link" onclick="filterByTag('buz-aerospace')">#buz-aerospace</a>
    <a class="tag-link" onclick="filterByTag('rocket')">#rocket</a>
  </div>
</li>

</ul>

<script>
function filterByTag(tag) {
  // Update active button
  document.querySelectorAll('.tag-filter-btn').forEach(btn => {
    btn.classList.remove('active');
    if (btn.dataset.tag === tag) {
      btn.classList.add('active');
    }
  });

  // Filter projects
  document.querySelectorAll('.project-item').forEach(item => {
    if (tag === 'all') {
      item.classList.remove('hidden');
    } else {
      const tags = item.dataset.tags.split(' ');
      if (tags.includes(tag)) {
        item.classList.remove('hidden');
      } else {
        item.classList.add('hidden');
      }
    }
  });
}

// Add click handlers to filter buttons
document.querySelectorAll('.tag-filter-btn').forEach(btn => {
  btn.addEventListener('click', () => filterByTag(btn.dataset.tag));
});
</script>
