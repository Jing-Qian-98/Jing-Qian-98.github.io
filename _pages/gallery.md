---
layout: single
title: "Gallery"
permalink: /gallery/
author_profile: true
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300&family=DM+Sans:wght@300;400&display=swap');

.gallery-wrap { padding: 1.5rem 0; font-family: 'DM Sans', sans-serif; }

/* ── Section header ── */
.g-section { margin-bottom: 3rem; }
.g-section-header { margin-bottom: 1.2rem; }
.g-section-header h3 {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 300; font-size: 24px;
  letter-spacing: 0.04em; color: #222; margin: 0 0 4px;
}
.g-section-header .g-meta {
  font-size: 12px; color: #999; letter-spacing: 0.08em;
  text-transform: uppercase; margin: 0 0 6px;
}
.g-award {
  display: inline-block;
  font-size: 11px; letter-spacing: 0.07em; text-transform: uppercase;
  color: #b07d4a;
  border: 0.5px solid #c9a06e;
  padding: 3px 10px; border-radius: 2px;
  margin-bottom: 10px;
}
.g-divider { width: 36px; height: 1px; background: #ddd; margin-top: 10px; }

/* ── Grid ── */
.g-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
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
.photo-item:hover .photo-bg { transform: scale(1.03); }
.photo-overlay {
  position: absolute; inset: 0;
  background: linear-gradient(to top, rgba(0,0,0,0.52) 0%, transparent 55%);
  opacity: 0; transition: opacity 0.35s ease;
  display: flex; flex-direction: column;
  justify-content: flex-end; padding: 14px;
}
.photo-item:hover .photo-overlay { opacity: 1; }
.photo-title {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 300; font-size: 15px;
  color: rgba(255,255,255,0.95); letter-spacing: 0.03em; margin: 0 0 3px;
  transform: translateY(6px); transition: transform 0.35s ease;
}
.photo-caption {
  font-size: 11px; color: rgba(255,255,255,0.7);
  letter-spacing: 0.06em; text-transform: uppercase; margin: 0;
  transform: translateY(6px); transition: transform 0.35s ease 0.04s;
}
.photo-item:hover .photo-title,
.photo-item:hover .photo-caption { transform: translateY(0); }

.g-hint {
  margin-top: 1rem; font-size: 12px; color: #bbb;
  letter-spacing: 0.06em; text-transform: uppercase;
}

/* ── Lightbox ── */
.lb-backdrop {
  display: none; position: fixed; inset: 0; z-index: 9999;
  background: rgba(0,0,0,0.9);
  align-items: center; justify-content: center;
}
.lb-backdrop.active { display: flex; }
.lb-box {
  position: relative; display: flex; flex-direction: column;
  align-items: center;
  animation: lb-in 0.28s ease;
}
@keyframes lb-in {
  from { opacity: 0; transform: scale(0.95); }
  to   { opacity: 1; transform: scale(1); }
}
.lb-img-wrap {
  width: 780px; max-width: 90vw;
  height: 500px; max-height: 62vh;
  border-radius: 3px; overflow: hidden;
}
.lb-img-bg {
  width: 100%; height: 100%;
  background-size: cover; background-position: center;
}
.lb-info { margin-top: 14px; text-align: center; }
.lb-title {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 300; font-size: 21px;
  color: rgba(255,255,255,0.95); letter-spacing: 0.04em; margin: 0 0 5px;
}
.lb-caption {
  font-size: 11px; color: rgba(255,255,255,0.45);
  letter-spacing: 0.1em; text-transform: uppercase; margin: 0;
}
.lb-close {
  position: absolute; top: -38px; right: 0;
  background: none; border: none;
  color: rgba(255,255,255,0.5); font-size: 22px;
  cursor: pointer; padding: 4px 8px; line-height: 1;
  transition: color 0.2s;
}
.lb-close:hover { color: #fff; }
.lb-nav { display: flex; gap: 18px; margin-top: 18px; }
.lb-nav button {
  background: rgba(255,255,255,0.08);
  border: 0.5px solid rgba(255,255,255,0.18);
  color: rgba(255,255,255,0.7); font-size: 12px;
  letter-spacing: 0.08em; text-transform: uppercase;
  padding: 7px 20px; border-radius: 2px; cursor: pointer;
  transition: background 0.2s; font-family: 'DM Sans', sans-serif;
}
.lb-nav button:hover { background: rgba(255,255,255,0.18); }

@media (max-width: 640px) {
  .g-grid { grid-template-columns: repeat(2, 1fr); }
}
</style>

<div class="gallery-wrap">

  <!-- ═══ Lillian Fountain-Smith Conference 2026 ═══ -->
  <div class="g-section">
    <div class="g-section-header">
      <span class="g-award">🏆 Best Abstract Award</span>
      <h3>Lillian Fountain-Smith Conference 2026</h3>
      <p class="g-meta">April 16–17, 2026 &nbsp;·&nbsp; Fort Collins, CO</p>
      <p style="font-size:13px; color:#666; margin:6px 0 0; max-width:600px; line-height:1.65;">
        <em>IgA Targeting in the Infant Gut Is Modulated by Diet and Increasingly Directed Towards Persistent Species</em>
      </p>
      <div class="g-divider"></div>
    </div>
    <div class="g-grid" id="lfsGrid"></div>
    <p class="g-hint">Click any photo to enlarge &nbsp;·&nbsp; ← → to navigate</p>
  </div>

  <!-- ═══ Add more event sections below following the same pattern ═══ -->

</div>

<!-- Lightbox (shared across all sections) -->
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
// ═══════════════════════════════════════════════════════════════
//  SECTION: Lillian Fountain-Smith Conference 2026
//
//  Layout (3-column grid, all photos horizontal):
//  ┌─────────────────────────────────────────┐  ← Photo 1 (full width hero)
//  ├───────────────────────┬─────────────────┤
//  │   Photo 2 (2 cols)    │    Photo 3      │
//  ├─────────────────┬─────┴─────────────────┤
//  │    Photo 4      │   Photo 5 (2 cols)    │
//  └─────────────────┴───────────────────────┘
// ═══════════════════════════════════════════════════════════════
const lfsPhotos = [
  {
    url:     "https://drive.google.com/thumbnail?id=1aJmt5WFQYkUBn96nqX0GkHkqSghg6vMY&sz=w1200",
    title:   "Lightning Talk",
    caption: "Lillian Fountain-Smith Conference · April 2026",
    col: "span 3", height: "240px"
  },
  {
    url:     "https://drive.google.com/thumbnail?id=1AFzdsTFsmrDMcLH2eSSjtK4bgJx-lqPm&sz=w1200",
    title:   "Lightning Talk",
    caption: "Lillian Fountain-Smith Conference · April 2026",
    col: "span 2", height: "185px"
  },
  {
    url:     "https://drive.google.com/thumbnail?id=1DHhOxRpBTFeJ6ZQBE-R18vLqHVlI4UTq&sz=w1200",
    title:   "Best Abstract Award",
    caption: "Lillian Fountain-Smith Conference · April 2026",
    col: "",       height: "185px"
  },
  {
    url:     "https://drive.google.com/thumbnail?id=1rcDK4FNJlFk8Iud4YIRwMC_A4jJlM4Di&sz=w1200",
    title:   "Lightning Talk",
    caption: "Lillian Fountain-Smith Conference · April 2026",
    col: "",       height: "185px"
  },
  {
    url:     "https://drive.google.com/thumbnail?id=1hVrXqyLAGUxiz-brUmI9-EaBwzzzs9bz&sz=w1200",
    title:   "Lightning Talk",
    caption: "Lillian Fountain-Smith Conference · April 2026",
    col: "span 2", height: "185px"
  }
];

// ── Build grid ──
function buildGrid(containerId, arr) {
  const grid = document.getElementById(containerId);
  arr.forEach((p, i) => {
    const item = document.createElement('div');
    item.className = 'photo-item';
    item.style.height = p.height;
    if (p.col) item.style.gridColumn = p.col;
    item.innerHTML = `
      <div class="photo-bg" style="background-image:url('${p.url}')"></div>
      <div class="photo-overlay">
        <p class="photo-title">${p.title}</p>
        <p class="photo-caption">${p.caption}</p>
      </div>`;
    item.addEventListener('click', () => openLB(arr, i));
    grid.appendChild(item);
  });
}
buildGrid('lfsGrid', lfsPhotos);

// ── Lightbox ──
let curArr = [], cur = 0;
const backdrop  = document.getElementById('lbBackdrop');
const lbImg     = document.getElementById('lbImg');
const lbTitle   = document.getElementById('lbTitle');
const lbCaption = document.getElementById('lbCaption');

function render() {
  const p = curArr[cur];
  lbImg.style.backgroundImage = `url('${p.url}')`;
  lbTitle.textContent   = p.title;
  lbCaption.textContent = p.caption;
}
function openLB(arr, i) { curArr = arr; cur = i; render(); backdrop.classList.add('active'); }
function closeLB()       { backdrop.classList.remove('active'); }

document.getElementById('lbClose').onclick = closeLB;
backdrop.addEventListener('click', e => { if (e.target === backdrop) closeLB(); });
document.getElementById('lbPrev').onclick  = () => { cur = (cur - 1 + curArr.length) % curArr.length; render(); };
document.getElementById('lbNext').onclick  = () => { cur = (cur + 1) % curArr.length; render(); };
document.addEventListener('keydown', e => {
  if (!backdrop.classList.contains('active')) return;
  if (e.key === 'Escape')     closeLB();
  if (e.key === 'ArrowLeft')  { cur = (cur - 1 + curArr.length) % curArr.length; render(); }
  if (e.key === 'ArrowRight') { cur = (cur + 1) % curArr.length; render(); }
});
</script>
