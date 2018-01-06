---
layout: default
title: quotes
permalink: quotes
nav: 6
---

<div class="container">
<div class="grid">
{% for quote in site.data.quotes %}
  <div class="cell">
    <a class="image" href="../img/quotes/{{ quote.link }}">
      <img class="cell-photo" alt="{{ quote.alt}}" src="../img/quotes/{{ quote.link }}">
    </a>
  </div>
{% endfor %}
</div>
</div>