---
layout: page_cera_FR
title:  "Blog Index"
last_updated: August 30, 2024
permalink: /ceramics/blog_FR.html
topnav: topnav_Portfolio_Volume_FR
---

Si vous utilisez RSS, [voici le flux avec tous les articles](https://falano.github.io/feed/ceramique.xml).

<ul>
  {% for post in site.posts %}
      {% if post.tags contains "FR" %}
    <li>
      <a href="{{ post.url }}">{{ post.date| date: "%-d-%m-%Y" }} - {{ post.title }}</a>
    </li>
      {% endif %}
  {% endfor %}
</ul>
