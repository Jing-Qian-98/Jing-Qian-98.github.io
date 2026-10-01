---
permalink: /
title: ""
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---



Hello, I'm Jing
======

📄 [**CV**](https://drive.google.com/file/d/1xy1ZOE_R70Ij-LB78fU0swIOhcjfUKYI/view?usp=drive_link) &nbsp;·&nbsp; 🎓 [**Google Scholar**](https://scholar.google.com/citations?user=P1HOw1gAAAAJ) &nbsp;·&nbsp; ✉️ [**Email**](mailto:Jing.Qian@colorado.edu)

I am a third-year Ph.D. candidate in [Integrative Physiology](https://www.colorado.edu/iphy/) at the [University of Colorado Boulder](https://www.colorado.edu/), where I work with [Dr. Matthew R. Olm](https://www.colorado.edu/iphy/people/faculty/matthew-r-olm) in the [Integrative Microbiome Research Laboratory](https://www.colorado.edu/lab/olm/). I study how the infant immune system shapes the developing gut microbiome, focusing on IgA-mediated microbiome-immune interactions during the first year of life. [Read more about my research](/projects/).

Previously, I completed my Master of Medicine at [Shanghai Jiao Tong University School of Medicine](https://www.shsmu.edu.cn/english), where I worked on antibiotic resistance genes and One Health surveillance, and my Bachelor of Medicine at [Anhui Medical University](https://english.ahmu.edu.cn/).

I am always excited to discuss science and potential collaborations. Feel free to reach out!

News
======
+ [2026.09] I passed my **Comprehensive Examination** and have officially advanced to **Ph.D. candidacy** at the Department of Integrative Physiology, CU Boulder! 🎓 Onward to the dissertation work on IgA-mediated microbiome–immune interactions in the infant gut. [[Research](/projects/#current-research)]
+ [2026.05] Our new preprint ["IgA Targeting in the Infant Gut Is Modulated by Diet and Increasingly Directed Towards Persistent Species"](https://www.biorxiv.org/content/10.64898/2026.05.19.726352v1.abstract) is now available on **bioRxiv**! [[Project](/projects/#featured-project-diet-shaped-iga-targeting-in-the-infant-gut-2024-present)]
+ [2026.04] I received the 🏆 **Best Abstract Award** at the **Lillian Fountain-Smith Conference 2026** (April 16–17, Fort Collins, CO) for "IgA Targeting in the Infant Gut Is Modulated by Diet and Increasingly Directed Towards Persistent Species." I also had a wonderful time delivering a 15-minute Lightning Talk and discussing nutrition science with everyone! [[Photos](/gallery/#lfs-2026)] [[Poster](/files/Jing_LFS2026_IgA_poster.pdf)]<br><span class="news-thumbs"><a href="/gallery/#lfs-2026"><img src="/images/news/lfs3.jpg" alt="Best Abstract Award, LFS 2026" loading="lazy"></a><a href="/gallery/#lfs-2026"><img src="/images/news/lfs4.jpg" alt="Lightning Talk, LFS 2026" loading="lazy"></a><a href="/gallery/#lfs-2026"><img src="/images/news/lfs1.jpg" alt="Lightning Talk, LFS 2026" loading="lazy"></a></span>
+ [2026.03] Our paper ["Evaluation of antimicrobial resistance governance across 193 countries to inform the 2026 Global Action Plan update"](https://doi.org/10.1038/s41591-026-04257-1) is now published online in **Nature Medicine**!
+ [2026.01] I attended the microbiome data science workshop hosted by **the Mountain West Microbiome Alliance (MoWMA)** in Salt Lake City, UT (January 26-29, 2026). Thank you to **the MoWMA workshop team (Greg Caporaso, Seth Walk, Cathy Lozupone, Jeff Meilander, Colin Wood, Chloe Herman, John O'Conner, and Nick Pinkham)** for the excellent training! [[Photo](/gallery/#mowma-2026)]<br><span class="news-thumbs"><a href="/gallery/#mowma-2026"><img src="/images/news/mowma.jpg" alt="MoWMA workshop group photo" loading="lazy"></a></span>
+ [2026.01] I presented a poster titled "Quantifying the Impact of First Foods on the Infant Gut Microbiota and Immune Health via IgA" at the **2026 Winter Pediatric Research Poster Session** hosted by Colorado Clinical & Translational Research Sciences Institute (CCTSI) at Children's Hospital on the Anschutz Medical Campus, Aurora, CO! [[Project](/projects/#featured-project-diet-shaped-iga-targeting-in-the-infant-gut-2024-present)] [[Photo](/gallery/#cctsi-2026)]
+ [2025.10] I presented a poster titled "Quantifying the Impact of First Foods on the Infant Gut Microbiota and Immune Health via IgA" at the **Colorado NORC Retreat**, Anschutz Medical Campus, Aurora, CO! [[Project](/projects/#featured-project-diet-shaped-iga-targeting-in-the-infant-gut-2024-present)]
+ [2025.02] Our paper ["Metagenomic insights into correlation of microbiota and antibiotic resistance genes in the worker-pig-soil interface: A One Health surveillance on Chongming Island, China"](https://doi.org/10.1016/j.hazadv.2025.100648) has been accepted by **Journal of Hazardous Materials Advances**! [[Project](/projects/#microbiota-and-antibiotic-resistance-genes-at-human-pig-soil-interface-2022-2023)]
+ [2024.10] Our "In Translation" article ["Hospitalization throws the preterm gut microbiome off-key"](https://doi.org/10.1016/j.chom.2024.09.009) was published in **Cell Host & Microbe**!
+ [2024.08] I am thrilled to join the [Integrative Microbiome Research Laboratory](https://www.colorado.edu/lab/olm/) at University of Colorado Boulder as a first-year Ph.D. student!

<style>
  .news-toggle {
    display: inline-block; margin-top: 0.5em; padding: 0.4em 1.1em;
    font-size: 0.85em; letter-spacing: 0.04em; color: #52adc8;
    border: 1px solid #52adc8; border-radius: 4px; background: #fff; cursor: pointer;
  }
  .news-toggle:hover { background: #52adc8; color: #fff; }
  .news-collapsed li.news-hidden { display: none; }
  .news-thumbs { display: flex; gap: 6px; margin: 6px 0 4px; flex-wrap: wrap; }
  .news-thumbs img { height: 72px; width: auto; border-radius: 4px; display: block; }
</style>
<script>
  /* Collapse the News list to the latest few items with a Show more button */
  (function () {
    var SHOW = 4;
    var heads = document.querySelectorAll("h1");
    for (var h = 0; h < heads.length; h++) {
      if (heads[h].textContent.trim() !== "News") { continue; }
      var list = heads[h].nextElementSibling;
      while (list && list.tagName !== "UL") { list = list.nextElementSibling; }
      if (!list || list.children.length <= SHOW) { return; }
      var items = list.children, hidden = items.length - SHOW;
      for (var i = SHOW; i < items.length; i++) { items[i].classList.add("news-hidden"); }
      list.classList.add("news-collapsed");
      var btn = document.createElement("button");
      btn.className = "news-toggle";
      btn.textContent = "Show " + hidden + " more";
      btn.onclick = function () {
        var open = list.classList.toggle("news-collapsed");
        btn.textContent = open ? "Show " + hidden + " more" : "Show less";
      };
      list.parentNode.insertBefore(btn, list.nextSibling);
      return;
    }
  })();
</script>
