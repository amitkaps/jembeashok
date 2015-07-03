---
layout: default
---

<div>
  {% for post in site.posts %}
    <section id="{{ post.name }}">
      <div class="container">
        {{ post.content }}
      </div>
    </section>
  {% endfor %}
</div>
