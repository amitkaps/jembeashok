---
layout: default
title: photos
permalink: photos
nav: 4
menu: true
image: img/pages/photos.jpg
---

<div class="grid-4">
{% for photo in site.data.photos %}
  <div class="card">
    <a class="img-link" href="img/photos/{{ photo.large }}">
      <img class="img-photo" src="img/photos/{{ photo.small }}" alt="{{ photo.desc }}">
    </a>
    <p class="img-desc"> {{ photo.desc}} </p>
  </div>
{% endfor %}
</div>