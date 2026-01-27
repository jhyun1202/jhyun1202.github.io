---
layout: page
title: work
permalink: /work/
description: Research papers and engineering projects
nav: true
nav_order: 1
---

<style>
/* Filter UI */
.work-filters {
  margin-bottom: 1.5rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  align-items: center;
}

.filter-group {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  align-items: center;
}

.filter-separator {
  color: var(--global-divider-color);
  margin: 0 0.3rem;
}

.filter-btn {
  background: none;
  border: 1px solid var(--global-divider-color);
  border-radius: 1rem;
  padding: 0.2rem 0.6rem;
  font-size: 0.75rem;
  color: var(--global-text-color-light);
  cursor: pointer;
  transition: all 0.15s ease;
}

.filter-btn:hover,
.filter-btn.active {
  background-color: var(--global-theme-color);
  border-color: var(--global-theme-color);
  color: white;
}

.filter-btn.type-btn {
  font-weight: 500;
}

/* Section headers */
.section-header {
  font-size: 1rem;
  font-weight: 600;
  color: var(--global-text-color-light);
  margin: 1.5rem 0 0.75rem 0;
  padding-bottom: 0.4rem;
  border-bottom: 1px solid var(--global-divider-color);
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.section-header.hidden {
  display: none;
}

/* Work items */
.work-item {
  margin-bottom: 1rem;
  padding-bottom: 0.75rem;
  border-bottom: 1px solid var(--global-divider-color);
}

.work-item:last-child {
  border-bottom: none;
}

.work-item.hidden {
  display: none;
}

.work-title {
  font-size: 1rem;
  font-weight: 500;
  margin-bottom: 0.15rem;
  line-height: 1.35;
  color: var(--global-text-color);
}

.work-title a {
  color: var(--global-text-color);
  text-decoration: none;
}

.work-title a:hover {
  color: var(--global-theme-color);
}

.work-desc {
  font-size: 0.85rem;
  color: var(--global-text-color-light);
  margin-bottom: 0.2rem;
  line-height: 1.4;
}

.work-meta {
  font-size: 0.8rem;
  color: var(--global-text-color-light);
  margin-bottom: 0.2rem;
}

.work-collaborators {
  font-size: 0.8rem;
  color: var(--global-text-color-light);
  font-style: italic;
  margin-bottom: 0.25rem;
}

.work-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.3rem;
  margin-bottom: 0.3rem;
}

.tag {
  font-size: 0.7rem;
  color: var(--global-theme-color);
  cursor: pointer;
  transition: opacity 0.15s;
}

.tag:hover {
  opacity: 0.7;
  text-decoration: underline;
}

/* PDF buttons */
.pdf-buttons {
  display: flex;
  gap: 0.4rem;
  margin-top: 0.3rem;
}

.pdf-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  padding: 0.2rem 0.5rem;
  font-size: 0.7rem;
  border: 1px solid var(--global-theme-color);
  border-radius: 4px;
  color: var(--global-theme-color);
  text-decoration: none;
  transition: all 0.15s ease;
}

.pdf-btn:hover {
  background-color: var(--global-theme-color);
  color: white;
}

/* Abstract toggle */
.abstract-toggle {
  background: none;
  border: none;
  color: var(--global-theme-color);
  cursor: pointer;
  font-size: 0.8rem;
  padding: 0;
  display: inline-flex;
  align-items: center;
  gap: 0.2rem;
}

.abstract-toggle:hover {
  text-decoration: underline;
}

.abstract-toggle .arrow {
  transition: transform 0.2s ease;
  font-size: 0.6rem;
}

.abstract-toggle.active .arrow {
  transform: rotate(90deg);
}

.abstract-content {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease;
  padding-left: 0.75rem;
  border-left: 2px solid var(--global-theme-color);
  margin-top: 0;
}

.abstract-content.show {
  max-height: 300px;
  margin-top: 0.5rem;
  padding: 0.5rem 0 0.5rem 0.75rem;
}

.abstract-content p {
  margin: 0;
  font-size: 0.85rem;
  line-height: 1.5;
  color: var(--global-text-color);
}

/* Project detail link */
.detail-link {
  font-size: 0.8rem;
  color: var(--global-theme-color);
  text-decoration: none;
}

.detail-link:hover {
  text-decoration: underline;
}

/* Status badge */
.status-badge {
  display: inline-block;
  font-size: 0.65rem;
  padding: 0.1rem 0.4rem;
  border-radius: 3px;
  background-color: var(--global-theme-color);
  color: white;
  margin-left: 0.4rem;
  vertical-align: middle;
}
</style>

<!-- Filter UI -->
<div class="work-filters">
  <div class="filter-group">
    <button class="filter-btn type-btn active" data-type="all">All</button>
    <button class="filter-btn type-btn" data-type="paper">Papers</button>
    <button class="filter-btn type-btn" data-type="project">Projects</button>
  </div>
  <span class="filter-separator">|</span>
  <div class="filter-group" id="tag-filters">
    <button class="filter-btn" data-tag="BUZAerospace">#BUZAerospace</button>
    <button class="filter-btn" data-tag="WingOfThoughts">#WingOfThoughts</button>
    <button class="filter-btn" data-tag="Physics">#Physics</button>
    <button class="filter-btn" data-tag="Rocket">#Rocket</button>
  </div>
</div>

<!-- Papers Section -->
<h2 class="section-header" data-section="paper">Papers</h2>

<div class="work-item" data-type="paper" data-tags="Physics">
  <div class="work-title">Acoustic Analysis of Fluid Motion in Metallic Containers</div>
  <div class="work-meta">Gangwon State Science Fair, National Science Fair &middot; 2025</div>
  <div class="work-collaborators">with Seongyul Choi, Seowoo Park</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('Physics')">#Physics</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Abstract
  </button>
  <div class="abstract-content">
    <p>Developed sensor technology to detect dangerous fuel sloshing conditions inside opaque rocket tanks using acoustic signal processing. Addresses critical aerospace safety challenges.</p>
  </div>
  <!-- TODO: Add PDF links when available -->
  <div class="pdf-buttons">
    <a href="#" class="pdf-btn" target="_blank">PDF (KOR)</a>
    <a href="#" class="pdf-btn" target="_blank">PDF (ENG)</a>
  </div>
</div>

<div class="work-item" data-type="paper" data-tags="Physics">
  <div class="work-title">Design of Perforated Wind Turbine Blades for Noise Reduction</div>
  <div class="work-meta">Korea Science & Engineering Fair (KSEF) &middot; 2024</div>
  <div class="work-collaborators">with Seongyul Choi</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('Physics')">#Physics</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Abstract
  </button>
  <div class="abstract-content">
    <p>Experimentally studied wind turbine blade designs with strategic perforations to reduce aeroacoustic noise. Discovered that certain perforation patterns also improved power generation efficiency.</p>
  </div>
  <div class="pdf-buttons">
    <a href="https://drive.google.com/file/d/1QFs-XbIajMgKSUkPurV2NiE6L7ETvKcF/view?usp=drive_link" class="pdf-btn" target="_blank">PDF (KOR)</a>
    <a href="https://drive.google.com/file/d/1QFs-XbIajMgKSUkPurV2NiE6L7ETvKcF/view?usp=drive_link" class="pdf-btn" target="_blank">PDF (ENG)</a>
  </div>
</div>

<div class="work-item" data-type="paper" data-tags="Physics">
  <div class="work-title">Design Strategies for Maximizing the Efficiency of Rotary Pumps</div>
  <div class="work-meta">Gangwon State Science Fair, National Science Fair &middot; 2024</div>
  <div class="work-collaborators">with Chanmin Chung</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('Physics')">#Physics</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Abstract
  </button>
  <div class="abstract-content">
    <p>Investigated how design parameters affect rotary pump performance by building and testing 3D-printed pump prototypes with varying geometries.</p>
  </div>
  <!-- TODO: Add PDF links when available -->
  <div class="pdf-buttons">
    <a href="#" class="pdf-btn" target="_blank">PDF (KOR)</a>
    <a href="#" class="pdf-btn" target="_blank">PDF (ENG)</a>
  </div>
</div>

<!-- Projects Section -->
<h2 class="section-header" data-section="project">Projects</h2>

<div class="work-item" data-type="project" data-tags="BUZAerospace Rocket">
  <div class="work-title">
    <a href="{{ '/projects/1_project/' | relative_url }}">Hybrid End-Burning Rocket Engine</a>
    <span class="status-badge">Journal Submitted</span>
  </div>
  <div class="work-desc">Korea's second end-burning hybrid rocket engine with $62K funding for dedicated Rocket Combustion Laboratory</div>
  <div class="work-meta">BUZ Aerospace &middot; 2025–2026</div>
  <div class="work-collaborators">with Changun Jeong, Chanmin Chung, Seorak Hong</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('BUZAerospace')">#BUZAerospace</span>
    <span class="tag" onclick="filterByTag('Rocket')">#Rocket</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Details
  </button>
  <div class="abstract-content">
    <p>Developed novel ignition system enabling controlled end-burning combustion. Successfully demonstrated stable end-burning with reproducible results across multiple test fires. Featured in <a href="https://www.kwnews.co.kr/page/view/2025100111404844847" target="_blank">Gangwon State News</a> and <a href="https://www.youtube.com/watch?v=YQR4buIWb48" target="_blank">YouTube</a>.</p>
  </div>
</div>

<div class="work-item" data-type="project" data-tags="BUZAerospace Rocket">
  <div class="work-title">
    <a href="{{ '/projects/2_project/' | relative_url }}">Solid Rocket Motor</a>
  </div>
  <div class="work-desc">KNO₃ fueled solid rocket achieving 400m+ altitude with $580K makerspace funding</div>
  <div class="work-meta">BUZ Aerospace &middot; 2025</div>
  <div class="work-collaborators">with Minjae Kim, Sungjoo Kim, Chanmin Chung, Changun Jeong, Sangyeon Moon</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('BUZAerospace')">#BUZAerospace</span>
    <span class="tag" onclick="filterByTag('Rocket')">#Rocket</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Details
  </button>
  <div class="abstract-content">
    <p>Led the design and development of a solid rocket motor using potassium nitrate composite propellant. Developed fuel formulation protocols and safety systems. Featured in official school promotional materials.</p>
  </div>
</div>

<div class="work-item" data-type="project" data-tags="WingOfThoughts Physics">
  <div class="work-title">Flight Dynamics and Return Mechanism of a Paper Boomerang</div>
  <div class="work-meta">Korean Youth Physicists Tournament (KYPT) &middot; 2025</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('WingOfThoughts')">#WingOfThoughts</span>
    <span class="tag" onclick="filterByTag('Physics')">#Physics</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Abstract
  </button>
  <div class="abstract-content">
    <p>Investigated the aerodynamic principles behind paper boomerang flight, analyzing how rotation and torque interact to create the characteristic curved return path.</p>
  </div>
</div>

<div class="work-item" data-type="project" data-tags="WingOfThoughts Physics">
  <div class="work-title">Wave Propagation and Dynamic Behavior in a Twisted Slinky</div>
  <div class="work-meta">Korean Youth Physicists Tournament (KYPT) &middot; 2025</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('WingOfThoughts')">#WingOfThoughts</span>
    <span class="tag" onclick="filterByTag('Physics')">#Physics</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Abstract
  </button>
  <div class="abstract-content">
    <p>Studied wave mechanics in twisted slinky springs, examining how geometric constraints and tension affect wave velocity and propagation patterns.</p>
  </div>
</div>

<div class="work-item" data-type="project" data-tags="WingOfThoughts Physics Rocket">
  <div class="work-title">Maximum Launch Height of a Ping Pong Ball Rocket with Water Loading</div>
  <div class="work-meta">Korean Youth Physicists Tournament (KYPT) &middot; 2024</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('WingOfThoughts')">#WingOfThoughts</span>
    <span class="tag" onclick="filterByTag('Physics')">#Physics</span>
    <span class="tag" onclick="filterByTag('Rocket')">#Rocket</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Abstract
  </button>
  <div class="abstract-content">
    <p>Analyzed how water mass inside a ping pong ball rocket increases launch height by examining momentum transfer during different phases of flight.</p>
  </div>
</div>

<div class="work-item" data-type="project" data-tags="WingOfThoughts Physics">
  <div class="work-title">Magnification and Resolution of a Water Droplet Lens</div>
  <div class="work-meta">Korean Youth Physicists Tournament (KYPT) &middot; 2024</div>
  <div class="work-tags">
    <span class="tag" onclick="filterByTag('WingOfThoughts')">#WingOfThoughts</span>
    <span class="tag" onclick="filterByTag('Physics')">#Physics</span>
  </div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> Abstract
  </button>
  <div class="abstract-content">
    <p>Studied how a single water droplet can act as a magnifying lens and investigated the factors that limit resolution when observing small details through droplet optics.</p>
  </div>
</div>

<script>
// Current filter state
let currentType = 'all';
let currentTag = null;

function updateFilters() {
  const items = document.querySelectorAll('.work-item');
  const paperHeader = document.querySelector('.section-header[data-section="paper"]');
  const projectHeader = document.querySelector('.section-header[data-section="project"]');

  let paperVisible = false;
  let projectVisible = false;

  items.forEach(item => {
    const itemType = item.dataset.type;
    const itemTags = item.dataset.tags.split(' ');

    let typeMatch = currentType === 'all' || itemType === currentType;
    let tagMatch = !currentTag || itemTags.includes(currentTag);

    if (typeMatch && tagMatch) {
      item.classList.remove('hidden');
      if (itemType === 'paper') paperVisible = true;
      if (itemType === 'project') projectVisible = true;
    } else {
      item.classList.add('hidden');
    }
  });

  // Show/hide section headers
  paperHeader.classList.toggle('hidden', !paperVisible);
  projectHeader.classList.toggle('hidden', !projectVisible);
}

function filterByType(type) {
  currentType = type;
  currentTag = null;

  // Update type buttons
  document.querySelectorAll('.type-btn').forEach(btn => {
    btn.classList.toggle('active', btn.dataset.type === type);
  });

  // Clear tag buttons
  document.querySelectorAll('#tag-filters .filter-btn').forEach(btn => {
    btn.classList.remove('active');
  });

  updateFilters();
}

function filterByTag(tag) {
  if (currentTag === tag) {
    // Toggle off
    currentTag = null;
  } else {
    currentTag = tag;
  }
  currentType = 'all';

  // Update type buttons
  document.querySelectorAll('.type-btn').forEach(btn => {
    btn.classList.toggle('active', btn.dataset.type === 'all');
  });

  // Update tag buttons
  document.querySelectorAll('#tag-filters .filter-btn').forEach(btn => {
    btn.classList.toggle('active', btn.dataset.tag === currentTag);
  });

  updateFilters();
}

function toggleAbstract(button) {
  button.classList.toggle('active');
  const content = button.nextElementSibling;
  content.classList.toggle('show');

  const isShow = content.classList.contains('show');
  const label = button.closest('.work-item').dataset.type === 'paper' ? 'Abstract' : 'Details';
  button.innerHTML = `<span class="arrow">&#9654;</span> ${isShow ? 'Hide' : label}`;
}

// Event listeners for type buttons
document.querySelectorAll('.type-btn').forEach(btn => {
  btn.addEventListener('click', () => filterByType(btn.dataset.type));
});

// Event listeners for tag buttons
document.querySelectorAll('#tag-filters .filter-btn').forEach(btn => {
  btn.addEventListener('click', () => filterByTag(btn.dataset.tag));
});
</script>
