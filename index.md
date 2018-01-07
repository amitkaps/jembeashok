---
layout: default
---

<!-- 
<div class="lead">
  <img class="lead-img" src="img/jembeashok1.jpg" title="Ashok Kumar">
</div> -->

{% assign sorted_pages = site.pages | sort: 'nav' %}

<div class="container">
<div class="pages">
{% for page in sorted_pages %}
  <div class="page">
    <a href="{{ page.url}}">
      <p class="title"> <span> {{page.title}} </span> </p>
    </a>
  </div>
{% endfor %}
</div>
</div>
