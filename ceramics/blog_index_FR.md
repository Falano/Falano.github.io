---
layout: page_cera_FR
title:  "Blog Index"
last_updated: August 30, 2024
permalink: /ceramics/blog_FR.html
topnav: topnav_Portfolio_Volume_FR
---

Si vous utilisez RSS, [voici le flux avec tous les articles](https://falano.github.io/feed/ceramique.xml). \
Si vous envisagez de vous inscrire à la newsletter, vous pouvez en consulter les éditions passées: [Septembre 2024](https://preview.mailerlite.io/preview/1104578/emails/132636150743434595), [Avril 2025](https://preview.mailerlite.io/preview/1104578/emails/152097059621570516), [Mai 2025](https://preview.mailerlite.io/preview/1104578/emails/155881363323487993), [Septembre 2025](https://preview.mailerlite.io/preview/1104578/emails/164712990915954447)

<ul>
  {% for post in site.posts %}
      {% if post.tags contains "FR" %}
    <li>
      <a href="{{ post.url }}">{{ post.date| date: "%-d-%m-%Y" }} - {{ post.title }}</a>
    </li>
      {% endif %}
  {% endfor %}
</ul>
