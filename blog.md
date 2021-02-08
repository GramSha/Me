---
layout: default
title: Blog
---

<h1>Posts organized by tags</h1>

<!-- markdown version of list -->
{% for tag in site.tags %}
## {{ tag[0] }}
{% for post in tag[1] %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
{% endfor %}