---
layout: default
title: acting
permalink: acting
nav: 1
menu: true
image: img/pages/acting.jpg
---

{% assign films = site.data.acting | where:"type", "film" %} 

<div class="grid">
{% for act in films %}
  <div class="card">
    <div class="upper">
      <a href="img/acting/{{ act.large }}" alt="{{ act.title }}">
        <img class="photo" src="img/acting/{{ act.small }}">
      </a>
      <p class="title"> <span class="title-text"> {{ act.title | upcase }} </span> </p>
    </div>
    <p class="description"> {{ act.role }} </p>
    <div class="youtube" data-id="{{ act.video }}">
        <img src="img/acting/youtube-{{ act.video }}.jpg">
        <div class="play"></div>
    </div>
    <p class="sub-text"> Produced by {{ act.group | upcase }}</p>
    <p class="special"> {{ act.award }} </p>
  </div>
{% endfor %}
</div>

{% assign plays = site.data.acting | where:"type", "theatre" %} 
<div class="grid">
{% for act in plays %}
  <div class="card">
    <div class="upper">
      <a href="img/acting/{{ act.large }}" alt="{{ act.title }}">
        <img class="photo" src="img/acting/{{ act.small }}">
      </a>
      <p class="title"> <span class="title-text"> {{ act.title | upcase }} </span> </p>
    </div>
    <p class="description"> {{ act.role }} </p>
    <p class="sub-text"> {{ act.group | upcase }} | Director: {{ act.director }} </p>
    <p class="special"> {{ act.award | upcase }} </p>
  </div>
{% endfor %}
</div>
