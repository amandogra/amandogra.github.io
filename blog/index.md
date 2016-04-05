---
layout: archive
permalink: /blog/
title: "Blog"
---

<div class="">
  <ul class="blog-post-list">
{% for post in site.categories.blog %}
    {% include post-list-bullets.html %}
{% endfor %}
</ul>
</div>
