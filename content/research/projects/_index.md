---
title: "Projects"
layout: "simple"
showDate: false
showReadingTime: false
showWordCount: false
---

<style>
  .project-row {
    display: flex;
    align-items: center;
    gap: 1.5rem;
    margin-bottom: 2rem;
    flex-wrap: wrap;
  }

  .project-img {
    flex: 0 0 220px;
    max-width: 220px;
  }

  .project-img img,
  .project-img video {
    width: 100%;
    height: auto;
    border-radius: 8px;
    object-fit: cover;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
    cursor: pointer;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .project-img img:hover,
  .project-img video:hover {
    transform: scale(1.02);
    box-shadow: 0 6px 16px rgba(0, 0, 0, 0.3);
  }

  .project-info {
    flex: 1;
    min-width: 260px;
  }

  .project-info h3 {
    margin-top: 0;
    margin-bottom: 0.25rem;
  }

  .project-degree {
    font-size: 0.85rem;
    font-weight: 600;
    color: #93c5fd;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    margin-bottom: 0.5rem;
    display: block;
  }

  .project-thesis {
    font-style: italic;
    font-size: 0.95rem;
    margin-bottom: 0.75rem;
    color: #cbd5e1;
  }

  .btn-row {
    margin-top: 0.75rem;
    display: flex;
    gap: 0.75rem;
    flex-wrap: wrap;
  }
</style>

<!-- PhD PROJECT -->
<div class="project-row">
<div class="project-img">
<video src="/img/projects/PhD-cover.mp4" autoplay loop muted playsinline onclick="openMediaLightbox(this)"></video>
</div>
<div class="project-info">
<span class="project-degree">University of Toronto (2022 – 2026)</span>
<h3>3D Synthetic Jets in Crossflow & Active Flow Control</h3>
<div class="project-thesis">Numerical Investigation of 3D Synthetic Jet In Crossflow</div>
<div class="btn-row">
{{< button href="../../files/PhD-thesis.pdf" target="_blank" >}}📥 Thesis (PDF){{< /button >}}
{{< button href="../../files/posters/2026-MIE-Symposium.pdf" target="_blank" >}}📄 Poster (2026){{< /button >}}
{{< button href="../../files/posters/SJA-Modelling-Poster.pdf" target="_blank" >}}📄 Poster (2024) {{< /button >}}
</div>
</div>
</div>

---

<!-- ENGINEERING EDUCATION PROJECT -->
<div class="project-row">
<div class="project-img">
<img src="/img/me-teaching.jpg" alt="Engineering Education Case Study" onclick="openMediaLightbox(this)">
</div>
<div class="project-info">
<span class="project-degree">University of Toronto (2024 - 2026)</span>
<h3>Learning Analytics & Forum Data to Target Student Support</h3>
<div class="project-thesis"> Using Forum and Assessment Analytics to Target Student Support Needs in Engineering Dynamics</div>
<div class="btn-row">
{{< button href="../../files/Piazza-poster.pdf" target="_blank" >}}📄 Poster (2026){{< /button >}}
</div>
</div>
</div>

---

<!-- MASC PROJECT -->
<div class="project-row">
<div class="project-img">
<img src="/img/projects/MASc-cover.png" alt="M.A.Sc. Research Project" onclick="openMediaLightbox(this)">
</div>
<div class="project-info">
<span class="project-degree">University of Toronto (2019 – 2021)</span>
<h3>Backward-Facing Step Flow & Initial SJA Studies</h3>
<div class="project-thesis">Numerical Investigation on Flow Past A Backward Facing Step and Initial Study of Synthetic Jets</div>
<div class="btn-row">
{{< button href="../../files/MASc-thesis.pdf" target="_blank" >}}📥 Thesis (PDF){{< /button >}}
</div>
</div>
</div>

---

<!-- BENG PROJECT -->
<div class="project-row">
<div class="project-img">
<video src="/img/gallery/oil-churning.mp4" autoplay loop muted playsinline onclick="openMediaLightbox(this)"></video>
</div>
<div class="project-info">
<span class="project-degree">University of Nottingham & Romax Technology (2018 – 2019)</span>
<h3>Oil Churning & Flow Regimes in a Model Gearbox</h3>
<div class="project-thesis">Experimental Investigation of Oil Churning and Flow Regimes Within a Model Gearbox</div>
<div class="btn-row">
{{< button href="../../files/BEng-dissertation.pdf" target="_blank" >}}📥 Technical Report (PDF){{< /button >}}
{{< button href="../../files/BEng-presentation.pdf" target="_blank" >}}📊 Presentation to Sponsor (PDF){{< /button >}}
{{< button href="../../files/BEng-poster.pdf" target="_blank" >}}📄 Poster (2019){{< /button >}}
</div>
</div>
</div>

<!-- LIGHTBOX OVERLAY -->
<div id="mediaLightbox" onclick="closeMediaLightbox()" style="display:none; position:fixed; z-index:9999; left:0; top:0; width:100%; height:100%; background-color:rgba(0,0,0,0.85); justify-content:center; align-items:center; cursor:pointer;">
<div id="mediaContainer" style="max-width:90%; max-height:85%;"></div>
</div>

<script>
function openMediaLightbox(element) {
  var modal = document.getElementById('mediaLightbox');
  var container = document.getElementById('mediaContainer');
  container.innerHTML = '';

  if (element.tagName.toLowerCase() === 'video') {
    var video = document.createElement('video');
    video.src = element.src;
    video.autoplay = true;
    video.loop = true;
    video.muted = true;
    video.controls = true;
    video.style.maxWidth = '100%';
    video.style.maxHeight = '85vh';
    video.style.borderRadius = '8px';
    video.style.boxShadow = '0 0 20px rgba(0,0,0,0.8)';
    container.appendChild(video);
  } else {
    var img = document.createElement('img');
    img.src = element.src;
    img.style.maxWidth = '100%';
    img.style.maxHeight = '85vh';
    img.style.borderRadius = '8px';
    img.style.boxShadow = '0 0 20px rgba(0,0,0,0.8)';
    container.appendChild(img);
  }

  modal.style.display = 'flex';
}

function closeMediaLightbox() {
  var modal = document.getElementById('mediaLightbox');
  var container = document.getElementById('mediaContainer');
  modal.style.display = 'none';
  container.innerHTML = '';
}
</script>