---
layout: archive
permalink: /work/
title: "Projects"
---

<div class="">
  <ul class="post-list">
{% for post in site.categories.work %}

{% if post.published == true %}
<li>
    <span class="post-meta">{{ post.startdate | date: "%b, %Y" }} - {{ post.enddate | date: "%b, %Y" }}</span>

    <h2>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
    </h2>
    <div class="crux">{{ post.excerpt }}</div>
</li>
{% endif %}

{% endfor %}
</ul>
</div>
