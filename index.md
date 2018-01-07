---
layout: default
---

{% assign sorted_pages = site.pages | sort: 'nav' %}

<!-- <div class="cover">
<div class="img-gallery">
{% for page in sorted_pages %}
  {% if page.menu == true %}

  <div class="img-container">
    <div class="upper">
      <a href="{{ page.url}}" alt="{{ page.title }}">
        <img class="photo" src="{{ page.image }}">
        <p class="title"> <span class="title-text"> {{ page.title | upcase }} </span> </p>
      </a>
    </div>
  </div>
  {% endif %}
{% endfor %}
</div>
</div> -->

<div class="cover">
<div class="pages">
{% for page in sorted_pages %}
  {% if page.menu == true %}
  <div class="page">
    <div class="upper">
      <a href="{{ page.url}}" alt="{{ page.title }}">
        <img class="photo" src="{{ page.image }}">
        <p class="title"> <span class="title-text"> {{ page.title | upcase }} </span> </p>
      </a>
    </div>
  </div>
  {% endif %}
{% endfor %}
</div>
</div>