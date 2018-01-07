---
layout: default
title: photos
permalink: photos
nav: 4
menu: true
image: img/pages/photos.jpg
---

<div class="gallery">
{% for photos in site.data.photos %}
  <div class="card">
    <a class="img-link" href="img/{{ photos.large }}" alt="{{ photos.title}}">
      <img class="img-photo" src="img/{{ photos.small }}">
    </a>
    <p class="img-desc"> {{ photos.desc}} </p>
  </div>
{% endfor %}
</div>