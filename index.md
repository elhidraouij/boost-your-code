---
layout: default
title: Home
---

# Welcome on my blog 🚀
## 📌 Articles récents :
<ul>
  {% for post in site.posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>