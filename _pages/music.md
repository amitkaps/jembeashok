---
layout: default
title: music
permalink: music
nav: 2
menu: true
image: img/pages/music.jpg
---

<div class="grid-2">
{% for item in site.data.music %}
  <div class="card">
    <div class="upper">
      <a href="img/music/{{ item.large }}">
        <img class="photo" src="img/music/{{ item.small }}" alt="{{ item.alt }}">
      </a>
      <p class="title"> <span class="title-text"> {{ item.title | upcase }} </span> </p>
    </div>
    <p class="description"> {{ item.role }} </p>
    <p class="sub-text">{{ item.more }}</p>
    <div class="youtube" data-id="{{ item.video }}">
      <img src="img/music/youtube-{{ item.video }}.jpg" alt="{{ item.alt }}-video">
      <div class="play"></div>
    </div>
    <div class="youtube" data-id="{{ item.video-alt }}">
      <img src="img/music/youtube-{{ item.video-alt }}.jpg" alt="{{ item.alt }}-video-alt">
      <div class="play"></div>
    </div>
  </div>
{% endfor %}
</div>