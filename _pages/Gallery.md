---
layout: page
permalink: /Gallery/
title: Gallery
nav: true
nav_order: 6
---

This section includes photos from conferences and field work trips.<br>

### Amboseli field trip - June 2026

<div class="gallery-grid">
  <img src="/assets/img/Gallery/Amboseli_1.jpg" alt="Field Trip Amboseli" onclick="openLightbox(this)">
  <img src="/assets/img/Gallery/Amboseli_2.jpg" alt="Baboon_1" onclick="openLightbox(this)">
</div>

<br>

### Human Milk Institute (HMI) Symposium - April 2026

<div class="gallery-grid">
  <img src="/assets/img/Gallery/hmi_1.jpeg" alt="HMI 2026 poster award" onclick="openLightbox(this)">
  <img src="/assets/img/Gallery/hmi_2.jpeg" alt="HMI 2026 participants" onclick="openLightbox(this)">
</div>


<!-- Lightbox Overlay -->
<div id="lightbox" onclick="closeLightbox()">
  <span id="lightbox-close">&times;</span>
  <img id="lightbox-img" src="" alt="">
</div>

<style>
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, 75px);
  gap: 8px;
  margin-top: 10px;
}

.gallery-grid img {
  width: 110px;
  height: 110px;
  object-fit: cover;
  border-radius: 4px;
  cursor: pointer;
  transition: opacity 0.2s, transform 0.2s;
}

.gallery-grid img:hover {
  opacity: 0.85;
  transform: scale(1.05);
}

#lightbox {
  display: none;
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.85);
  z-index: 9999;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

#lightbox.active {
  display: flex;
}

#lightbox img {
  max-width: 90%;
  max-height: 90%;
  border-radius: 6px;
  box-shadow: 0 0 40px rgba(0,0,0,0.5);
  cursor: default;
}

#lightbox-close {
  position: absolute;
  top: 20px; right: 30px;
  font-size: 40px;
  color: white;
  cursor: pointer;
  line-height: 1;
}
</style>

<script>
function openLightbox(img) {
  const lb = document.getElementById('lightbox');
  document.getElementById('lightbox-img').src = img.src;
  document.getElementById('lightbox-img').alt = img.alt;
  lb.classList.add('active');
}

function closeLightbox() {
  document.getElementById('lightbox').classList.remove('active');
}

document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') closeLightbox();
});
</script>
