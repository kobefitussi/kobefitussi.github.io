---
layout: default
permalink: /posts/
title: Blog
---
<ul>
{% for post in site.categories.blog %}
 <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>
