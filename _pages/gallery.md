---
title: "Image Gallery"
layout: default
permalink: /gallery/
---

<!-- Lightbox library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css" integrity="sha512-+QZ4yJzJ6x7jzJzv5ZL5t9+J8zJf8Jzv5ZL5t9+J8zJf8Jzv5ZL5t9+J8zJf8Jzv5L5t9+J8zJf8Jzv5ZL5t9g==" crossorigin="anonymous" />

<!-- Masonry library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/masonry/4.2.2/masonry.pkgd.min.js"></script>

<!-- Gallery styles -->
<style>
/* Lightbox styles */
.lb-outerContainer {
    background: rgba(0, 0, 0, 0.8);
  }
  
  .lb-image {
    display: block;
    max-width: 100%;
    height: auto;
  }
  
  .lb-nav a.lb-prev, .lb-nav a.lb-next {
    background: rgba(0, 0, 0, 0.8);
  }
  
  /* Masonry styles */
  .grid {
    /* display: flex;
    flex-wrap: wrap; */
    margin: 0 auto;
  }
  
  .grid-item {
    margin-bottom: 20px;
  }
  
  .grid-sizer {
    width: 33.333%;
  }

  .grid-item img {
    max-width: 25% !important;
  }
</style>

<div class="grid">
  {% for image in page.static_files %}
    {% if image.path contains 'images/gallery_images/' %}
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