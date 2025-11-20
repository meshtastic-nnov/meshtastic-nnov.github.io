---
layout: default
permalink: links
---
{% for item in site.data.links %}
* [{{ item.title}}]({{ item.url }})
{% endfor %}
