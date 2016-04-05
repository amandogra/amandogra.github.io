---
layout: archive
permalink: /blog/
title: "Blog"
---

<div class="">
  <ul class="post-list">
{% for post in site.categories.blog %}
	{% include post-list.html %}
{% endfor %}
</ul>
</div>
