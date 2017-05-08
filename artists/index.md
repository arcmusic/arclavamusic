---
layout: page
title: Artists
excerpt: "Learn about our artists. Click on an artist to view their discography, preview and buy their music"
search_omit: true
image:
  feature: artists_header_thin.png
  credit: 
  creditlink:
---

<ul class="post-list">
{% for post in site.categories.artists %} 
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} {% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>