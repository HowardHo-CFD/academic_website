---
title: "Testing"
showDate: false
layout: "simple"
showReadingTime: false
showWordCount: false
---

{{< gallery >}}
  <img src="/img/my-photo.jpg" data-caption="My Handsome" class="grid-w33 gallery-media" />
  <img src="/img/projects/gearbox-2.JPG" class="grid-w33 gallery-media" />
  <img src="/img/projects/MASc-cover.png" class="grid-w33 gallery-media" />
  <img src="/img/backgrounds/fluids-bg-2.jpg" class="grid-w33 gallery-media" />

  <video src="/img/gallery/cylinder-baseline-iso.mp4" data-caption="Baseline cylinder flow at ISO view" class="grid-w33 gallery-media gallery-video" autoplay loop muted playsinline></video>
  <video src="/img/gallery/naca-0025.mp4" data-caption="NACA 0025 airfoil simulation" class="grid-w33 gallery-media gallery-video" autoplay loop muted playsinline></video>
  <video src="/img/gallery/cylinder-rotating-iso.mp4" data-caption="Rotating cylinder mechanics" class="grid-w33 gallery-media gallery-video" autoplay loop muted playsinline></video>
  <video src="/img/gallery/sja-flat-plate-iso.mp4" data-caption="SJA flat plate (ISO view)" class="grid-w33 gallery-media gallery-video" autoplay loop muted playsinline></video>
  <video src="/img/gallery/sja-flat-plate-side.mp4" data-caption="SJA flat plate (Side view)" class="grid-w33 gallery-media gallery-video" autoplay loop muted playsinline></video>
{{< /gallery >}}

<div id="media-lightbox" 
     class="fixed inset-0 z-50 hidden bg-black/80 flex flex-col items-center justify-center p-4 cursor-pointer" 
     style="backdrop-filter: blur(12px); -webkit-backdrop-filter: blur(12px);"
     onclick="closeMediaLightbox()">
  <img id="lightbox-image" class="rounded shadow-lg hidden" style="max-width: 90%; max-height: 75vh;" onclick="event.stopPropagation()" />
  <video id="lightbox-video" class="rounded shadow-lg hidden" style="max-width: 90%; max-height: 75vh;" controls autoplay loop onclick="event.stopPropagation()"></video>
  <p id="lightbox-caption" 
     class="text-white text-center mt-0 text-sm max-w-2xl rounded"
     style="background: rgba(0,0,0,0.5); padding: 0.25rem 0.25rem;"></p>
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
  const lightbox = document.getElementById('media-lightbox');
  const lightboxImage = document.getElementById('lightbox-image');
  const lightboxVideo = document.getElementById('lightbox-video');
  const lightboxCaption = document.getElementById('lightbox-caption');

  function openLightbox(el) {
    const caption = el.getAttribute('data-caption') || '';
    lightboxCaption.textContent = caption;
    lightboxCaption.style.display = caption ? 'block' : 'none';

    if (el.tagName === 'VIDEO') {
      lightboxImage.classList.add('hidden');
      lightboxImage.src = '';
      lightboxVideo.classList.remove('hidden');
      lightboxVideo.src = el.src;
      lightboxVideo.play();
    } else {
      lightboxVideo.classList.add('hidden');
      lightboxVideo.pause();
      lightboxVideo.src = '';
      lightboxImage.classList.remove('hidden');
      lightboxImage.src = el.src;
    }
    lightbox.classList.remove('hidden');
  }

  function closeMediaLightbox() {
    lightbox.classList.add('hidden');
    lightboxVideo.pause();
    lightboxVideo.src = '';
    lightboxImage.src = '';
  }
  window.closeMediaLightbox = closeMediaLightbox;

  document.querySelectorAll('.gallery-media').forEach(el => {
    // Clone to strip any listeners/behavior Blowfish's own gallery script attached
    const clone = el.cloneNode(true);
    el.replaceWith(clone);

    clone.style.cursor = 'pointer';
    clone.addEventListener('click', (e) => {
      e.preventDefault();
      e.stopPropagation();
      openLightbox(clone);
    });
  });
});
</script>




