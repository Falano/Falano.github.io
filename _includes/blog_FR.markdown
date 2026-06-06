## Newsletter
Vous pouvez vous inscrire à la newsletter [ici](https://docs.google.com/forms/d/e/1FAIpQLSedwS8JsWUfuZA-yHkGMzSA6AxQPGIW-3C9pQj_ziMbYS8pKQ/viewform) et en consulter les éditions passées ci-dessous: \
2026: [Mai 2026](https://preview.mailerlite.io/preview/1104578/emails/188468901862966819) \
2025: [Avril 2025](https://preview.mailerlite.io/preview/1104578/emails/152097059621570516), [Mai 2025](https://preview.mailerlite.io/preview/1104578/emails/155881363323487993), [Septembre 2025](https://preview.mailerlite.io/preview/1104578/emails/164712990915954447), [Novembre 2025](https://preview.mailerlite.io/preview/1104578/emails/172071147058234805), \
2024: [Septembre 2024](https://preview.mailerlite.io/preview/1104578/emails/132636150743434595)

## Billets de Blog
Si vous utilisez RSS, [voici le flux avec tous les articles](https://falano.github.io/feed/ceramique.xml). \
Et ci-dessous les billets de blog sur des sujets précis:
<ul>
  {% for post in site.posts %}
      {% if post.tags contains "FR" %}
    <li>
      <a href="{{ post.url }}"> {{ post.categories[0]}} - {{ post.date| date: "%-d-%m-%Y" }} - {{ post.title }}</a>
    </li>
      {% endif %}
  {% endfor %}
</ul>
