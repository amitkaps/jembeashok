---
layout: default
title: acting
permalink: acting
nav: 1
menu: true
image: img/pages/acting.jpg
---

{% assign films = site.data.acting | where:"type", "film" %} 

<div class="grid-3">
{% for item in films %}
  <div class="card">
    <div class="upper">
      <a href="img/acting/{{ item.large }}">
        <img class="photo" src="img/acting/{{ item.small }}" alt="{{ item.alt }}">
      </a>
      <p class="title"> {{ item.title }} </p>
    </div>
    <p class="description"> {{ item.role }} </p>
    <p class="sub-text"> Produced by {{ item.group }}</p>
    <p class="special"> {{ item.award }} </p>
    <div class="youtube" data-id="{{ item.video }}">
      <img src="img/acting/youtube-{{ item.video }}.jpg" alt="{{ item.alt }}">
      <div class="play"></div>
    </div>
  </div>
{% endfor %}
</div>

{% assign plays = site.data.acting | where:"type", "theatre" %} 
<div class="grid-3">
{% for item in plays %}
  <div class="card">
    <div class="upper">
      <a href="img/acting/{{ item.large }}">
        <img class="photo" src="img/acting/{{ item.small }}" alt="{{ item.alt }}">
      </a>
      <p class="title"> {{ item.title }} </p>
    </div>
    <p class="description"> {{ item.role }} </p>
    <p class="sub-text"> {{ item.group | upcase }} | Director: {{ item.director }} </p>
    <p class="special"> {{ item.award | upcase }} </p>
  </div>
{% endfor %}
</div>
