---
layout: page
title:  "Blog Index"
last_updated: August 30, 2024
permalink: /portfolio/volume/blog_FR.html
topnav: topnav_Portfolio_Volume_FR
---

<ul>
  {% for post in site.posts %}
      {% if post.tags contains "FR" %}
    <li>
      <a href="{{ post.url }}">{{ post.date| date: "%-d-%m-%Y" }} - {{ post.title }}</a>
    </li>
      {% endif %}
  {% endfor %}
</ul>
