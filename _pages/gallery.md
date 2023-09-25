---
title: "Image Gallery"
layout: default
permalink: /gallery/

---

<!-- Lightbox library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css" crossorigin="anonymous" />

<!-- Masonry library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/masonry/4.2.2/masonry.pkgd.min.js"></script>

<!-- <div class="grid gallery">
  {% for image in page.static_files %}
    {% if image.path contains '/gallery_images' %}
      <div class="grid-item">
        <a href="{{ image.path }}" data-toggle="lightbox" data-gallery="gallery">
          <img src="{{ image.path }}" alt="{{ image.name | remove: '.png' | replace: '_', ' ' }}" />
        </a>
      </div>
    {% endif %}
  {% endfor %} 
</div> -->

<div class="grid gallery">
  <div class="grid-item">
    <a href="/images/gallery_images/BelarusInfographic.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/BelarusInfographic.png" alt="Image 1" />
    </a>
  </div>
  <div class="grid-item">
    <a href="/images/gallery_images/2019YearInReviewImage.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/2019YearInReviewImage.png"  alt="Image 2" />
    </a>
  </div>
  <div class="grid-item">
    <a href="/images/gallery_images/CDT_South-Africa.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/CDT_South-Africa.png"  alt="Image 3" />
    </a>
  </div>
  <div class="grid-item">
    <a href="/images/gallery_images/FIG-1-POST-COVID-MAP-DASH.png" data-toggle="lightbox" data-gallery="gallery">
      <img src="/images/gallery_images/FIG-1-POST-COVID-MAP-DASH.png"  alt="Image 2" />
    </a>
  </div>
  <!-- Add more images here -->
</div>

<style>
  .grid-item {
    margin-bottom: 20px;
  }
</style>

<script>
  var grid = document.querySelector('.grid');
  var masonry = new Masonry(grid, {
    itemSelector: '.grid-item',
    columnWidth: '.grid-sizer',
    fitwidth: true,
    percentPosition: true
  });
</script>