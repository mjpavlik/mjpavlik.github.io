---
title: "Gallery"
layout: default
author_profile: true
permalink: /gallery/

---

{% include base_path %}

<!-- Lightbox library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css" crossorigin="anonymous" />

<!-- Masonry library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/masonry/4.2.2/masonry.pkgd.min.js"></script>

<div class="grid gallery">
<div class="grid-sizer"></div>
  <div class="grid-item">
    <a href="/images/gallery_images/BelarusInfographic.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/BelarusInfographic.png" alt="Belarus Infographic" />
    </a>
  </div>

  <div class="grid-item">
    <a href="/images/gallery_images/2019YearInReviewImage.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/2019YearInReviewImage.png"  alt="2019 Year in Review" />
    </a>
  </div>

  <div class="grid-item">
    <a href="/images/gallery_images/CDT_South-Africa.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/CDT_South-Africa.png"  alt="Covid Disorder Tracker: South Africa" />
    </a>
  </div>

  <div class="grid-item">
    <a href="/images/gallery_images/conflict-dash.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/conflict-dash.png"  alt="Post-Covid conflict trends" />
    </a>
  </div>

  <div class="grid-item">
    <a href="/images/gallery_images/10ConflictsInteractive.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/10ConflictsInteractive.png"  alt="10 Conflicts to watch for in 2019 (Interactive)" />
    </a>
  </div>

  <div class="grid-item">
    <a href="/images/gallery_images/alqaeda.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/alqaeda.png"  alt="Al Qaeda Worldwide" />
    </a>
  </div>

  <div class="grid-item">
    <a href="/images/gallery_images/alshabaab.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/alshabaab.png"  alt="Al Shabaab Infographic" />
    </a>
  </div>
  
  <div class="grid-item">
    <a href="/images/gallery_images/CAR-Infographic.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/CAR-Infographic.png"  alt="Central African Republic (CAR) Infographic" />
    </a>
  </div>

  <!-- Add more images here -->
</div>

<style>
  .grid-item {
    margin: 1px;
  }
  .grid-sizer,
  .grid-item {
    width: calc(33.33% - 2px);
    margin: 1px;
  }
   img {
    max-width: 100%;
    height: auto;
  }
</style>

<script>
  var grid = document.querySelector('.gallery');
  var masonry = new Masonry(grid, {
    itemSelector: '.grid-item',
    columnWidth: '.grid-sizer',
    fitWidth: true,
    percentPosition: true
  });
</script>