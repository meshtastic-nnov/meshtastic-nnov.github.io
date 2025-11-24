---
layout: default
permalink: links
---
## Полезные ссылки

{% for item in site.data.links %}
* [{{ item.title}}]({{ item.url }})
{% endfor %}
