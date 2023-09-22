---
title: "Image Gallery"
layout: gallery
excerpt: "Your gallery description here."
permalink: /gallery/
gallery:
  - url: /BelarusInfographic.png
    image_path: /images/gallery_images/BelarusInfographic.png
    alt: "Belarus Infographic"
  - url: /2019YearInReviewImage.png
    image_path: /images/gallery_images/2019YearInReviewImage.png
    alt: "2019 Year In Review"
---


<!-- Lightbox library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css" integrity="sha512-+QZ4yJzJ6x7jzJzv5ZL5t9+J8zJf8Jzv5ZL5t9+J8zJf8Jzv5ZL5t9+J8zJf8Jzv5L5t9+J8zJf8Jzv5ZL5t9g==" crossorigin="anonymous" />

<!-- Masonry library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/masonry/4.2.2/masonry.pkgd.min.js"></script>

<!-- Gallery styles -->
<link rel="stylesheet" href="/assets/css/gallery.css">

<div class="grid">
  {% for image in page.static_files %}
    {% if image.path contains 'gallery_images/' %}
      <div class="grid-item">
        <a href="{{ image.path }}" data-toggle="lightbox" data-gallery="gallery">
          <img src="{{ image.path }}" alt="{{ image.name | remove: '.png' | replace: '_', ' ' }}" />
        </a>
      </div>
    {% endif %}
  {% endfor %}
</div>

<script>
  var grid = document.querySelector('.grid');
  var masonry = new Masonry(grid, {
    itemSelector: '.grid-item',
    columnWidth: '.grid-sizer',
    percentPosition: true
  });
</script>

<link rel="stylesheet" href="/assets/css/gallery.css">
