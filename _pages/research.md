---
layout: page
permalink: /research/
title: research
description: Physics research and experiments
nav: true
nav_order: 1
---

<style>
.research-item {
  margin-bottom: 2rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid var(--global-divider-color);
}

.research-item:last-child {
  border-bottom: none;
}

.research-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.3rem;
  color: var(--global-text-color);
}

.research-meta {
  font-size: 0.9rem;
  color: var(--global-text-color-light);
  margin-bottom: 0.5rem;
}

.research-collaborators {
  font-size: 0.9rem;
  color: var(--global-text-color-light);
  margin-bottom: 0.5rem;
  font-style: italic;
}

.abstract-toggle {
  background: none;
  border: none;
  color: var(--global-theme-color);
  cursor: pointer;
  font-size: 0.9rem;
  padding: 0;
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
}

.abstract-toggle:hover {
  text-decoration: underline;
}

.abstract-toggle .arrow {
  transition: transform 0.2s ease;
  font-size: 0.7rem;
}

.abstract-toggle.active .arrow {
  transform: rotate(90deg);
}

.abstract-content {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease, padding 0.3s ease;
  padding: 0 0 0 1rem;
  border-left: 2px solid var(--global-theme-color);
  margin-top: 0;
}

.abstract-content.show {
  max-height: 500px;
  padding: 0.8rem 0 0.8rem 1rem;
  margin-top: 0.8rem;
}

.abstract-content p {
  margin: 0;
  font-size: 0.95rem;
  line-height: 1.6;
  color: var(--global-text-color);
}
</style>

<div class="research-list">

<!-- 2025.08 -->
<div class="research-item">
  <div class="research-title">Acoustic Analysis of Fluid Motion in Metallic Containers</div>
  <div class="research-meta">Gangwon State Science Fair, National Science Fair, 2025.08</div>
  <div class="research-collaborators">with Seongyul Choi, Seowoo Park</div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> View Abstract
  </button>
  <div class="abstract-content">
    <p>Developed sensor technology to detect dangerous fuel sloshing conditions inside opaque rocket tanks using acoustic signal processing. Addresses critical aerospace safety challenges.</p>
  </div>
</div>

<div class="research-item">
  <div class="research-title">Development of Hybrid End-Burning Rocket Engine</div>
  <div class="research-meta">Personal Study, 2025.08</div>
  <div class="research-collaborators">with Changun Jeong, Chanmin Chung</div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> View Abstract
  </button>
  <div class="abstract-content">
    <p>First-author research on hybrid propulsion systems. Secured $62K funding to establish rocket combustion laboratory and developed Korea's second end-burning hybrid engine. Journal submitted.</p>
  </div>
</div>

<!-- 2025.02 -->
<div class="research-item">
  <div class="research-title">Flight Dynamics and Return Mechanism of a Paper Boomerang</div>
  <div class="research-meta">KYPT (Korean Youth Physicists Tournament), 2025.02</div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> View Abstract
  </button>
  <div class="abstract-content">
    <p>Investigated the aerodynamic principles behind paper boomerang flight, analyzing how rotation and torque interact to create the characteristic curved return path.</p>
  </div>
</div>

<div class="research-item">
  <div class="research-title">Wave Propagation and Dynamic Behavior in a Twisted Slinky</div>
  <div class="research-meta">KYPT (Korean Youth Physicists Tournament), 2025.02</div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> View Abstract
  </button>
  <div class="abstract-content">
    <p>Studied wave mechanics in twisted slinky springs, examining how geometric constraints and tension affect wave velocity and propagation patterns.</p>
  </div>
</div>

<!-- 2024.12 -->
<div class="research-item">
  <div class="research-title">Design of Perforated Wind Turbine Blades for Noise Reduction</div>
  <div class="research-meta">KSEF (Korea Science & Engineering Fair), 2024.12</div>
  <div class="research-collaborators">with Seongyul Choi</div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> View Abstract
  </button>
  <div class="abstract-content">
    <p>Experimentally studied wind turbine blade designs with strategic perforations to reduce aeroacoustic noise. Discovered that certain perforation patterns also improved power generation efficiency.</p>
  </div>
</div>

<!-- 2024.08 -->
<div class="research-item">
  <div class="research-title">Design Strategies for Maximizing the Efficiency of Rotary Pumps</div>
  <div class="research-meta">Gangwon State Science Fair, National Science Fair, 2024.08</div>
  <div class="research-collaborators">with Chanmin Chung</div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> View Abstract
  </button>
  <div class="abstract-content">
    <p>Investigated how design parameters affect rotary pump performance by building and testing 3D-printed pump prototypes with varying geometries.</p>
  </div>
</div>

<!-- 2024.02 -->
<div class="research-item">
  <div class="research-title">Maximum Launch Height of a Ping Pong Ball Rocket with Water Loading</div>
  <div class="research-meta">KYPT (Korean Youth Physicists Tournament), 2024.02</div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> View Abstract
  </button>
  <div class="abstract-content">
    <p>Analyzed how water mass inside a ping pong ball rocket increases launch height by examining momentum transfer during different phases of flight.</p>
  </div>
</div>

<div class="research-item">
  <div class="research-title">Magnification and Resolution of a Water Droplet Lens</div>
  <div class="research-meta">KYPT (Korean Youth Physicists Tournament), 2024.02</div>
  <button class="abstract-toggle" onclick="toggleAbstract(this)">
    <span class="arrow">&#9654;</span> View Abstract
  </button>
  <div class="abstract-content">
    <p>Studied how a single water droplet can act as a magnifying lens and investigated the factors that limit resolution when observing small details through droplet optics.</p>
  </div>
</div>

</div>

<script>
function toggleAbstract(button) {
  button.classList.toggle('active');
  const content = button.nextElementSibling;
  content.classList.toggle('show');

  const arrow = button.querySelector('.arrow');
  if (content.classList.contains('show')) {
    button.innerHTML = '<span class="arrow">&#9654;</span> Hide Abstract';
  } else {
    button.innerHTML = '<span class="arrow">&#9654;</span> View Abstract';
  }
}
</script>
