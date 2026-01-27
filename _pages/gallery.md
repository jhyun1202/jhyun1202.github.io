---
layout: page
title: gallery
permalink: /gallery/
description: Photo gallery
nav: true
nav_order: 6
---

<style>
/* Pinterest-style Masonry Gallery */
.gallery-container {
  width: 100%;
  min-height: 400px;
}

.gallery-grid {
  column-count: 3;
  column-gap: 16px;
}

@media (max-width: 900px) {
  .gallery-grid {
    column-count: 2;
  }
}

@media (max-width: 600px) {
  .gallery-grid {
    column-count: 1;
  }
}

.gallery-item {
  break-inside: avoid;
  margin-bottom: 16px;
  border-radius: 12px;
  overflow: hidden;
  background-color: var(--global-bg-color);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  cursor: pointer;
}

.gallery-item:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
}

.gallery-item img {
  width: 100%;
  height: auto;
  display: block;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.gallery-item img.loaded {
  opacity: 1;
}

/* Loading placeholder */
.gallery-item.loading {
  background: linear-gradient(90deg, var(--global-bg-color) 25%, var(--global-divider-color) 50%, var(--global-bg-color) 75%);
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
  min-height: 200px;
}

@keyframes shimmer {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}

/* Empty state */
.gallery-empty {
  text-align: center;
  padding: 60px 20px;
  color: var(--global-text-color-light);
}

.gallery-empty h3 {
  margin-bottom: 1rem;
  color: var(--global-text-color);
}

.gallery-empty code {
  background-color: var(--global-code-bg-color);
  padding: 2px 6px;
  border-radius: 4px;
  font-size: 0.85rem;
}

.gallery-empty pre {
  text-align: left;
  background-color: var(--global-code-bg-color);
  padding: 1rem;
  border-radius: 8px;
  overflow-x: auto;
  font-size: 0.8rem;
  margin-top: 1rem;
}

/* Lightbox */
.lightbox {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.95);
  z-index: 9999;
  justify-content: center;
  align-items: center;
  cursor: zoom-out;
}

.lightbox.active {
  display: flex;
}

.lightbox img {
  max-width: 90%;
  max-height: 90%;
  object-fit: contain;
  border-radius: 4px;
}

.lightbox-close {
  position: absolute;
  top: 20px;
  right: 30px;
  font-size: 40px;
  color: white;
  cursor: pointer;
  opacity: 0.8;
  transition: opacity 0.2s;
}

.lightbox-close:hover {
  opacity: 1;
}

.lightbox-nav {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 50px;
  color: white;
  cursor: pointer;
  opacity: 0.8;
  transition: opacity 0.2s;
  user-select: none;
  padding: 20px;
}

.lightbox-nav:hover {
  opacity: 1;
}

.lightbox-prev {
  left: 20px;
}

.lightbox-next {
  right: 20px;
}

/* Photo count */
.photo-count {
  text-align: center;
  margin-bottom: 1.5rem;
  color: var(--global-text-color-light);
  font-size: 0.9rem;
}
</style>

{% assign cloud_name = site.data.gallery.cloudinary.cloud_name %}
{% assign images = site.data.gallery.images %}

<div class="gallery-container">
  {% if images and images.size > 0 %}
    <div class="photo-count">{{ images.size }} photos</div>
    <div id="gallery" class="gallery-grid">
      {% for image in images %}
        <div class="gallery-item loading" data-index="{{ forloop.index0 }}">
          <img
            src="https://res.cloudinary.com/{{ cloud_name }}/image/upload/c_scale,w_600,q_auto,f_auto/{{ image }}"
            data-full="https://res.cloudinary.com/{{ cloud_name }}/image/upload/q_auto,f_auto/{{ image }}"
            alt="Photo {{ forloop.index }}"
            loading="lazy"
            onload="this.classList.add('loaded'); this.parentElement.classList.remove('loading');"
          >
        </div>
      {% endfor %}
    </div>
  {% else %}
    <div class="gallery-empty">
      <h3>Gallery Setup Required</h3>
      <p>Add images to <code>_data/gallery.yml</code></p>

      <p style="margin-top: 1.5rem;"><strong>Quick Setup:</strong></p>
      <p>1. Open Cloudinary Console > Media Library > home/jhyun1202.github</p>
      <p>2. Open browser console (F12) and run:</p>
      <pre><code>copy(Array.from(document.querySelectorAll('[data-test="asset-card"]')).map(card => {
  const img = card.querySelector('img');
  if (!img) return null;
  const match = img.src.match(/upload\/[^/]+\/(.+)\.[^.]+$/);
  return match ? `  - "${match[1]}"` : null;
}).filter(Boolean).join('\n'));</code></pre>
      <p style="margin-top: 1rem;">3. Paste the result under <code>images:</code> in _data/gallery.yml</p>
    </div>
  {% endif %}
</div>

<!-- Lightbox -->
<div id="lightbox" class="lightbox">
  <span class="lightbox-close">&times;</span>
  <span class="lightbox-nav lightbox-prev">&#10094;</span>
  <span class="lightbox-nav lightbox-next">&#10095;</span>
  <img id="lightbox-img" src="" alt="Full size image">
</div>

{% if images and images.size > 0 %}
<script>
(function() {
  const images = Array.from(document.querySelectorAll('.gallery-item img'));
  let currentIndex = 0;

  function openLightbox(index) {
    currentIndex = index;
    const lightbox = document.getElementById('lightbox');
    const img = document.getElementById('lightbox-img');
    img.src = images[index].dataset.full;
    lightbox.classList.add('active');
    document.body.style.overflow = 'hidden';
  }

  function closeLightbox() {
    const lightbox = document.getElementById('lightbox');
    lightbox.classList.remove('active');
    document.body.style.overflow = '';
  }

  function navigateLightbox(direction) {
    currentIndex = (currentIndex + direction + images.length) % images.length;
    const img = document.getElementById('lightbox-img');
    img.src = images[currentIndex].dataset.full;
  }

  // Gallery item click
  document.querySelectorAll('.gallery-item').forEach((item, index) => {
    item.addEventListener('click', () => openLightbox(index));
  });

  // Lightbox events
  document.getElementById('lightbox').addEventListener('click', (e) => {
    if (e.target.id === 'lightbox' || e.target.classList.contains('lightbox-close')) {
      closeLightbox();
    }
  });

  document.querySelector('.lightbox-prev').addEventListener('click', (e) => {
    e.stopPropagation();
    navigateLightbox(-1);
  });

  document.querySelector('.lightbox-next').addEventListener('click', (e) => {
    e.stopPropagation();
    navigateLightbox(1);
  });

  // Keyboard navigation
  document.addEventListener('keydown', (e) => {
    const lightbox = document.getElementById('lightbox');
    if (!lightbox.classList.contains('active')) return;

    if (e.key === 'Escape') closeLightbox();
    if (e.key === 'ArrowLeft') navigateLightbox(-1);
    if (e.key === 'ArrowRight') navigateLightbox(1);
  });
})();
</script>
{% endif %}
