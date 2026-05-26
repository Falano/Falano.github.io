\
\
If you use RSS, [here's the feed with all the articles](https://falano.github.io/feed/ceramics.xml). \
If you are considering subscribing to the newsletter, you can check out the past ones here: \
2026: [May, 2026](https://preview.mailerlite.io/preview/1104578/emails/188516538236536236) \
2025: [April, 2025](https://preview.mailerlite.io/preview/1104578/emails/152064619987338362); [May, 2025](https://preview.mailerlite.io/preview/1104578/emails/155859734021277095); [September, 2025](https://preview.mailerlite.io/preview/1104578/emails/165188050595349609); [November, 2025](https://preview.mailerlite.io/preview/1104578/emails/172063314337072757); \
2024: [September, 2024](https://preview.mailerlite.io/preview/1104578/emails/132651687770850853)

\
And here are blog posts on specific things:
<ul>
  {% for post in site.posts %}
    {% if post.tags contains "EN" %}
    <li>
      <a href="{{ post.url }}">{{ post.date| date: "%Y-%m-%d" }} - {{ post.title }}</a>
    </li>
      {% endif %}
  {% endfor %}
</ul>
