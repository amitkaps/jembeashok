---
layout: default
title: quotes
permalink: quotes
nav: 6
menu: true
image: img/pages/quotes.jpg
---

<div class="quotes">
{% for quote in site.data.quotes %}
  <div class="quote">
    <a href="../img/quotes/{{ quote.link }}">
      <img class="photo" alt="{{ quote.alt}}" src="../img/quotes/{{ quote.link }}">
    </a>
  </div>
{% endfor %}
</div>
