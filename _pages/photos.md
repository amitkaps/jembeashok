---
layout: default
name: photos
permalink: photos
---

<div class="img-gallery">
{% for photos in site.data.photos %}
  <div class="img-container">
    <a class="img-link" href="img/{{ photos.large }}" alt="{{ photos.title}}">
      <img class="img-photo" src="img/{{ photos.small }}">
    </a>
    <p class="img-desc"> {{ photos.desc}} </p>
  </div>
{% endfor %}
</div>
