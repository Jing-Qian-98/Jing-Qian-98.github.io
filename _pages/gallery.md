---
layout: single
title: "Gallery"
permalink: /gallery/
author_profile: true
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300&family=DM+Sans:wght@300;400&display=swap');

.gallery-wrap { padding: 1.5rem 0; font-family: 'DM Sans', sans-serif; }
.gallery-header { margin-bottom: 2rem; }
.gallery-header h2 {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 300; font-size: 28px;
  letter-spacing: 0.05em; color: #222; margin: 0 0 6px;
}
.gallery-header p {
  font-size: 13px; color: #888; font-weight: 300;
  letter-spacing: 0.08em; text-transform: uppercase; margin: 0;
}
.gallery-divider { width: 40px; height: 1px; background: #ccc; margin: 12px 0 0; }

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 180px;
  gap: 8px;
}
.photo-item {
  position: relative; overflow: hidden;
  border-radius: 3px; cursor: pointer;
}
.photo-bg {
  width: 100%; height: 100%;
  background-size: cover; background-position: center;
  transition: transform 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}
.photo-item:hover .photo-bg { transform: scale(1.04); }
.photo-overlay {
  position: absolute; inset: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.55) 0%, transparent 55%);
  opacity: 0; transition: opacity 0.35s ease;
  display: flex; flex-direction: column;
  justify-content: flex-end; padding: 14px;
}
.photo-item:hover .photo-overlay { opacity: 1; }
.photo-title {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 300; font-size: 15px;
  color: rgba(255,255,255,0.95); letter-spacing: 0.03em;
  margin: 0 0 3px;
  transform: translateY(6px); transition: transform 0.35s ease;
}
.photo-caption {
  font-size: 11px; color: rgba(255,255,255,0.7);
  letter-spacing: 0.06em; text-transform: uppercase; margin: 0;
  transform: translateY(6px); transition: transform 0.35s ease 0.04s;
}
.photo-item:hover .photo-title,
.photo-item:hover .photo-caption { transform: translateY(0); }
.gallery-footer {
  margin-top: 1.2rem; font-size: 12px; color: #aaa;
  letter-spacing: 0.06em; text-transform: uppercase;
}

/* Lightbox */
.lb-backdrop {
  display: none; position: fixed; inset: 0; z-index: 9999;
  background: rgba(0,0,0,0.88);
  align-items: center; justify-content: center;
}
.lb-backdrop.active { display: flex; }
.lb-box {
  position: relative; display: flex; flex-direction: column;
  align-items: center;
  animation: lb-in 0.3s ease;
}
@keyframes lb-in {
  from { opacity: 0; transform: scale(0.94); }
  to   { opacity: 1; transform: scale(1); }
}
.lb-img-wrap {
  width: 560px; max-width: 88vw;
  height: 370px; max-height: 60vh;
  border-radius: 4px; overflow: hidden;
}
.lb-img-bg {
  width: 100%; height: 100%;
  background-size: cover; background-position: center;
}
.lb-info { margin-top: 16px; text-align: center; }
.lb-title {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 300; font-size: 22px;
  color: rgba(255,255,255,0.95); letter-spacing: 0.04em; margin: 0 0 4px;
}
.lb-caption {
  font-size: 11px; color: rgba(255,255,255,0.5);
  letter-spacing: 0.1em; text-transform: uppercase; margin: 0;
}
.lb-close {
  position: absolute; top: -40px; right: 0;
  background: none; border: none;
  color: rgba(255,255,255,0.55); font-size: 22px;
  cursor: pointer; padding: 4px 8px; line-height: 1;
  transition: color 0.2s;
}
.lb-close:hover { color: #fff; }
.lb-nav { display: flex; gap: 20px; margin-top: 20px; }
.lb-nav button {
  background: rgba(255,255,255,0.08);
  border: 0.5px solid rgba(255,255,255,0.2);
  color: rgba(255,255,255,0.75); font-size: 12px;
  letter-spacing: 0.08em; text-transform: uppercase;
  padding: 7px 20px; border-radius: 2px; cursor: pointer;
  transition: background 0.2s; font-family: 'DM Sans', sans-serif;
}
.lb-nav button:hover { background: rgba(255,255,255,0.18); }

@media (max-width: 600px) {
  .gallery-grid { grid-template-columns: repeat(2, 1fr); grid-auto-rows: 140px; }
}
</style>

<div class="gallery-wrap">
  <div class="gallery-header">
    <h2>Gallery</h2>
    <p>Moments &amp; Places</p>
    <div class="gallery-divider"></div>
  </div>

  <div class="gallery-grid" id="galleryGrid"></div>
  <p class="gallery-footer">Click any photo to enlarge &nbsp;·&nbsp; ← → to navigate</p>
</div>

<!-- Lightbox -->
<div class="lb-backdrop" id="lbBackdrop">
  <div class="lb-box">
    <button class="lb-close" id="lbClose">✕</button>
    <div class="lb-img-wrap">
      <div class="lb-img-bg" id="lbImg"></div>
    </div>
    <div class="lb-info">
      <p class="lb-title" id="lbTitle"></p>
      <p class="lb-caption" id="lbCaption"></p>
    </div>
    <div class="lb-nav">
      <button id="lbPrev">← Prev</button>
      <button id="lbNext">Next →</button>
    </div>
  </div>
</div>

<script>
// =====================================================
// 📷 YOUR PHOTOS — edit this array to add your images
// =====================================================
// For each photo:
//   url   : direct image link (see instructions below)
//   title : photo title shown in lightbox
//   caption: subtitle (location, date, etc.)
//   span  : layout span — "" | "tall" (2 rows tall) | "wide" (2 columns wide)
// =====================================================
const photos = [
  {
    url:     "https://YOUR_IMAGE_URL_1",
    title:   "Rocky Mountain Trail",
    caption: "Colorado · 2024",
    span:    "tall"
  },
  {
    url:     "https://YOUR_IMAGE_URL_2",
    title:   "Golden Hour",
    caption: "Boulder · Autumn",
    span:    ""
  },
  {
    url:     "https://YOUR_IMAGE_URL_3",
    title:   "Salt Lake City",
    caption: "January 2026",
    span:    ""
  },
  {
    url:     "https://YOUR_IMAGE_URL_4",
    title:   "Grand Teton",
    caption: "Wyoming · Panorama",
    span:    "wide"
  },
  {
    url:     "https://YOUR_IMAGE_URL_5",
    title:   "Lab Life",
    caption: "CU Boulder",
    span:    ""
  },
  {
    url:     "https://YOUR_IMAGE_URL_6",
    title:   "Harvest",
    caption: "Wine Country",
    span:    ""
  },
  {
    url:     "https://YOUR_IMAGE_URL_7",
    title:   "Yellowstone",
    caption: "Wyoming · 2026",
    span:    "wide"
  }
];
// =====================================================

const grid = document.getElementById('galleryGrid');
photos.forEach((p, i) => {
  const item = document.createElement('div');
  item.className = 'photo-item';
  if (p.span === 'tall') item.style.gridRow = 'span 2';
  if (p.span === 'wide') item.style.gridColumn = 'span 2';
  item.innerHTML = `
    <div class="photo-bg" style="background-image:url('${p.url}')"></div>
    <div class="photo-overlay">
      <p class="photo-title">${p.title}</p>
      <p class="photo-caption">${p.caption}</p>
    </div>`;
  item.addEventListener('click', () => openLB(i));
  grid.appendChild(item);
});

let cur = 0;
const backdrop = document.getElementById('lbBackdrop');
const lbImg    = document.getElementById('lbImg');
const lbTitle  = document.getElementById('lbTitle');
const lbCaption= document.getElementById('lbCaption');

function render() {
  const p = photos[cur];
  lbImg.style.backgroundImage = `url('${p.url}')`;
  lbTitle.textContent   = p.title;
  lbCaption.textContent = p.caption;
}
function openLB(i) { cur = i; render(); backdrop.classList.add('active'); }
function closeLB()  { backdrop.classList.remove('active'); }

document.getElementById('lbClose').onclick = closeLB;
backdrop.addEventListener('click', e => { if (e.target === backdrop) closeLB(); });
document.getElementById('lbPrev').onclick = () => { cur = (cur - 1 + photos.length) % photos.length; render(); };
document.getElementById('lbNext').onclick = () => { cur = (cur + 1) % photos.length; render(); };
document.addEventListener('keydown', e => {
  if (!backdrop.classList.contains('active')) return;
  if (e.key === 'Escape')    closeLB();
  if (e.key === 'ArrowLeft') { cur = (cur - 1 + photos.length) % photos.length; render(); }
  if (e.key === 'ArrowRight'){ cur = (cur + 1) % photos.length; render(); }
});
</script>
