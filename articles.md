---
layout: default
permalink: /articles/
title: Articles
---
<ul>
{% for article in site.articles %}
 <li><a href="{{ article.url }}">{{ article.title }}</a>-{{ article.description }}<div style="text-color=gray">{{ article.tags }}</div></li>
{% endfor %}
</ul>
