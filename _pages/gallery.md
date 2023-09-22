---
title: "Image Gallery"
layout: default
permalink: /gallery/

---

<!-- Lightbox library -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/css/lightbox.min.css" crossorigin="anonymous" />

<!-- Masonry library -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/masonry/4.2.2/masonry.pkgd.min.js"></script>

<div class="grid gallery">
  {% for image in page.static_files %}
    {% if image.path contains 'images/gallery_images' %}
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