---
layout: default
title: training
permalink: training
nav: 3
menu: true
image: img/pages/training.jpg
---

<!-- > Jembe means "Everyone gather together in peace". -->

{% assign music = site.data.training | where:"type", "music" %} 

<div class="grid-3">
{% for item in music %}
  <div class="card">
    <div class="upper">
      <a href="img/training/{{ item.large }}">
        <img class="photo" src="img/training/{{ item.small }}" alt="{{ item.alt }}">
      </a>
      <p class="title"> <span class="title-text"> {{ item.title | upcase }} </span> </p>
    </div>
    <p class="description"> {{ item.role }} </p>
    <p class="special">{{ item.more }}</p>
    <!-- <div class="youtube" data-id="{{ item.video }}">
      <img src="img/music/youtube-{{ item.video }}.jpg" alt="{{ item.alt }}-video">
      <div class="play"></div>
    </div> -->
  </div>
{% endfor %}
</div>


{% assign acting = site.data.training | where:"type", "acting" %} 

<div class="grid-3">
{% for item in acting %}
  <div class="card">
    <div class="upper">
      <a href="img/training/{{ item.large }}">
        <img class="photo" src="img/training/{{ item.small }}" alt="{{ item.alt }}">
      </a>
      <p class="title"> <span class="title-text"> {{ item.title | upcase }} </span> </p>
    </div>
    <p class="description"> {{ item.role }} </p>
    <p class="special">{{ item.more }}</p>
    <!-- <div class="youtube" data-id="{{ item.video }}">
      <img src="img/music/youtube-{{ item.video }}.jpg" alt="{{ item.alt }}-video">
      <div class="play"></div>
    </div> -->
  </div>
{% endfor %}
</div>
