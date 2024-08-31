---
layout: page
title:  "Blog Index"
last_updated: August 30, 2024
permalink: /portfolio/volume/blog_EN.html
topnav: topnav_Portfolio_Volume_EN
---

<ul>
  {% for post in site.posts %}
    {% if post.tags contains "EN" %}
    <li>
      <a href="{{ post.url }}">{{ post.date| date: "%Y-%m-%d" }} - {{ post.title }}</a>
    </li>
      {% endif %}
  {% endfor %}
</ul>
