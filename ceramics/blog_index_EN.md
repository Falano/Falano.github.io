---
layout: page_cera_EN
title:  "Blog Index"
last_updated: August 30, 2024
permalink: /ceramics/blog_EN.html
redirect_from: /ceramics/blog
topnav: topnav_Portfolio_Volume_EN
---

If you use RSS, [here's the feed with all the articles](https://falano.github.io/feed/ceramics.xml). \
If you are considering subscribing to the newsletter, you can check out the past ones here: [September, 2024](https://preview.mailerlite.io/preview/1104578/emails/132651687770850853); [April, 2025](https://preview.mailerlite.io/preview/1104578/emails/152064619987338362); [May, 2025](https://preview.mailerlite.io/preview/1104578/emails/155859734021277095); [September, 2025](https://preview.mailerlite.io/preview/1104578/emails/165188050595349609); [November, 2025](https://preview.mailerlite.io/preview/1104578/emails/172063314337072757)

<ul>
  {% for post in site.posts %}
    {% if post.tags contains "EN" %}
    <li>
      <a href="{{ post.url }}">{{ post.date| date: "%Y-%m-%d" }} - {{ post.title }}</a>
    </li>
      {% endif %}
  {% endfor %}
</ul>
