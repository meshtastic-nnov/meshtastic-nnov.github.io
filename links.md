---
layout: default
---

## Полезные ссылки

{% for item in site.data.links.page %}
* [{{ item.title}}]({{ item.url }})
{% endfor %}
