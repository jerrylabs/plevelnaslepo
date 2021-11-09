---
layout: default
type: gallery
---

<h1>Fotogalerie</h1>
<div class="photos">
  <div class="grid">
    <div class="grid-sizer"></div>
    {% for image in site.static_files %}
      {% if image.path contains 'images/gallery/thumbs' %}
        <a class="grid-item" data-fancybox="foto" href="{{'assets/images/gallery/' | append: image.name | relative_url }}">
          <img src="{{'assets/images/gallery/thumbs/' | append: image.name | relative_url }}" alt="Fotka">
        </a>
      {% endif %}
    {% endfor %}
  </div>
</div>
