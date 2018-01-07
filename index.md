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
    <div class="upper">
      <a href="{{ page.url}}" alt="{{ page.title }}">
        <img class="photo" src="img/acting/{{ act.small }}">
        <p class="title"> <span class="title-text"> {{ page.title | upcase }} </span> </p>
      </a>
    </div>
  </div>
{% endfor %}
</div>
</div>