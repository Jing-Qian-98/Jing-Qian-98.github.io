---
layout: single
title: "Gallery"
permalink: /gallery/
author_profile: true
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300&family=DM+Sans:wght@300;400&display=swap');

.gallery-wrap { padding: 1.5rem 0; font-family: 'DM Sans', sans-serif; }
.g-section { margin-bottom: 3.5rem; }
.g-section-header { margin-bottom: 1.2rem; }
.g-section-header h3 {
  font-family: 'Cormorant Garamond', serif;
  font-weight: 300; font-size: 24px;
  letter-spacing: 0.04em; color: #222; margin: 0 0 4px;
}
.g-meta {
  font-size: 12px; color: #999; letter-spacing: 0.08em;
  text-transform: uppercase; margin: 0 0 6px;
}
.g-award {
  display: inline-block;
  font-size: 11px; letter-spacing: 0.07em; text-transform: uppercase;
  color: #b07d4a; border: 0.5px solid #c9a06e;
  padding: 3px 10px; border-radius: 2px; margin-bottom: 10px;
}
.g-tag {
  display: inline-block;
  font-size: 11px; letter-spacing: 0.07em; text-transform: uppercase;
  color: #5a7a8a; border: 0.5px solid #8aacbc;
  padding: 3px 10px; border-radius: 2px; margin-bottom: 10px;
}
.g-divider { width: 36px; height: 1px; background: #ddd; margin-top: 10px; }
.g-sub {
  font-size: 12px; letter-spacing: 0.07em; text-transform: uppercase;
  color: #aaa; margin: 16px 0 8px; font-family: 'DM Sans', sans-serif;
}
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
.lb-backdrop {
  display: none; position: fixed; inset: 0; z-index: 9999;
  background: rgba(0,0,0,0.9);
  align-items: center; justify-content: center;
}
.lb-backdrop.active { display: flex; }
.lb-box {
  position: relative; display: flex; flex-direction: column;
  align-items: center; animation: lb-in 0.28s ease;
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
.lb-img-bg { width: 100%; height: 100%; background-size: cover; background-position: center; }
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
  cursor: pointer; padding: 4px 8px; line-height: 1; transition: color 0.2s;
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

  <!-- ═══ MDRS 2026 ═══ -->
  <div class="g-section">
    <div class="g-section-header">
      <span class="g-tag">🚀 ASEN 5226 · Medicine in Space</span>
      <h3>Mars Desert Research Station</h3>
      <p class="g-meta">March 2026 &nbsp;·&nbsp; Hanksville, UT</p>
      <p style="font-size:13px; color:#666; margin:6px 0 0; max-width:600px; line-height:1.65;">
        <em>Extravehicular Activity (EVA) simulations at the MDRS habitat as part of ASEN 5226 — Medicine in Space and Surface Environments.</em>
      </p>
      <div class="g-divider"></div>
    </div>
    <p class="g-sub">EVA &amp; Habitat</p>
    <div class="g-grid" id="mdrsGrid"></div>
    <p class="g-sub" style="margin-top:20px;">Aerial · DJI</p>
    <div class="g-grid" id="droneGrid"></div>
    <p class="g-hint">Click any photo to enlarge &nbsp;·&nbsp; ← → to navigate</p>
  </div>

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

</div>

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
var mdrsPhotos = [
  { url: "/images/gallery/MDRS/01.JPG",              title: "MDRS · March 2026",    caption: "Hanksville, UT",  col: "span 3", height: "220px" },
  { url: "/images/gallery/MDRS/02.jpeg",             title: "MDRS · March 2026",         caption: "Hanksville, UT",       col: "",       height: "180px" },
  { url: "/images/gallery/MDRS/03.JPG",              title: "MDRS · March 2026",     caption: "Hanksville, UT",         col: "",       height: "180px" },
  { url: "/images/gallery/MDRS/04.JPG",              title: "MDRS · March 2026",       caption: "Hanksville, UT",     col: "",       height: "180px" },
  { url: "/images/gallery/MDRS/05.JPG",              title: "MDRS · March 2026",           caption: "Hanksville, UT",          col: "span 2", height: "180px" },
  { url: "/images/gallery/MDRS/06.JPG",              title: "MDRS · March 2026",   caption: "Hanksville, UT",  col: "",       height: "180px" },
  { url: "/images/gallery/MDRS/07.JPG",              title: "MDRS · March 2026", caption: "Hanksville, UT",         col: "",       height: "180px" },
  { url: "/images/gallery/MDRS/08.JPG",              title: "MDRS · March 2026",         caption: "Hanksville, UT",          col: "span 2", height: "180px" },
  { url: "/images/gallery/MDRS/09.JPG",              title: "MDRS · March 2026",           caption: "Hanksville, UT",     col: "",       height: "180px" },
  { url: "/images/gallery/MDRS/IMG_7897%202.jpeg",   title: "MDRS · March 2026",            caption: "Hanksville, UT",  col: "",       height: "180px" },
  { url: "/images/gallery/MDRS/IMG_8234%202.jpeg",   title: "MDRS · March 2026",               caption: "Hanksville, UT",          col: "",       height: "180px" },
  { url: "/images/gallery/MDRS/IMG_9942%202.jpeg",   title: "MDRS · March 2026",         caption: "Hanksville, UT",     col: "span 3", height: "160px" }
];

// ── Drone / aerial photos (3 photos) ──
var dronePhotos = [
  { url: "/images/gallery/MDRS/dji_fly_01.JPG", title: "Aerial View I",   caption: "DJI · MDRS", col: "span 2", height: "200px" },
  { url: "/images/gallery/MDRS/dji_fly_02.JPG", title: "Aerial View II",  caption: "DJI · MDRS", col: "",       height: "200px" },
  { url: "/images/gallery/MDRS/dji_fly_03.JPG", title: "Aerial View III", caption: "DJI · MDRS", col: "span 3", height: "200px" }
];

// ── LFS Conference photos (5 photos) ──
var lfsPhotos = [
  { url: "/images/gallery/LFS4.JPG", title: "Lightning Talk",      caption: "Fort Collins, CO · April 2026", col: "span 3", height: "240px" },
  { url: "/images/gallery/LFS1.JPG", title: "Lightning Talk", caption: "Fort Collins, CO · April 2026",                               col: "span 2", height: "240px" },
  { url: "/images/gallery/LFS2.JPG", title: "Lightning Talk", caption: "Fort Collins, CO · April 2026",                   col: "",       height: "240px" },
  { url: "/images/gallery/LFS3.JPG", title: "Lightning Talk",   caption: "Fort Collins, CO · April 2026",                             col: "",       height: "240px" },
  { url: "/images/gallery/LFS5.JPG", title: "Lightning Talk",       caption: "Fort Collins, CO · April 2026",                         col: "span 2", height: "240px" }
];

// ── Build grid ──
function buildGrid(containerId, arr) {
  var grid = document.getElementById(containerId);
  for (var i = 0; i < arr.length; i++) {
    var p = arr[i];
    var item = document.createElement('div');
    item.className = 'photo-item';
    item.style.height = p.height;
    if (p.col) { item.style.gridColumn = p.col; }
    var bg = document.createElement('div');
    bg.className = 'photo-bg';
    bg.style.backgroundImage = "url('" + p.url + "')";
    var overlay = document.createElement('div');
    overlay.className = 'photo-overlay';
    var titleEl = document.createElement('p');
    titleEl.className = 'photo-title';
    titleEl.textContent = p.title;
    var captionEl = document.createElement('p');
    captionEl.className = 'photo-caption';
    captionEl.textContent = p.caption;
    overlay.appendChild(titleEl);
    overlay.appendChild(captionEl);
    item.appendChild(bg);
    item.appendChild(overlay);
    (function(a, idx) {
      item.addEventListener('click', function() { openLB(a, idx); });
    })(arr, i);
    grid.appendChild(item);
  }
}

buildGrid('mdrsGrid',  mdrsPhotos);
buildGrid('droneGrid', dronePhotos);
buildGrid('lfsGrid',   lfsPhotos);

// ── Lightbox ──
var curArr = [];
var cur = 0;
var backdrop  = document.getElementById('lbBackdrop');
var lbImg     = document.getElementById('lbImg');
var lbTitle   = document.getElementById('lbTitle');
var lbCaption = document.getElementById('lbCaption');

function render() {
  var p = curArr[cur];
  lbImg.style.backgroundImage = "url('" + p.url + "')";
  lbTitle.textContent   = p.title;
  lbCaption.textContent = p.caption;
}
function openLB(arr, i) {
  curArr = arr; cur = i; render();
  backdrop.classList.add('active');
}
function closeLB() { backdrop.classList.remove('active'); }

document.getElementById('lbClose').onclick = closeLB;
backdrop.addEventListener('click', function(e) { if (e.target === backdrop) { closeLB(); } });
document.getElementById('lbPrev').onclick = function() { cur = (cur - 1 + curArr.length) % curArr.length; render(); };
document.getElementById('lbNext').onclick = function() { cur = (cur + 1) % curArr.length; render(); };
document.addEventListener('keydown', function(e) {
  if (!backdrop.classList.contains('active')) { return; }
  if (e.key === 'Escape')     { closeLB(); }
  if (e.key === 'ArrowLeft')  { cur = (cur - 1 + curArr.length) % curArr.length; render(); }
  if (e.key === 'ArrowRight') { cur = (cur + 1) % curArr.length; render(); }
});
</script>
