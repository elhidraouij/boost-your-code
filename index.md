---
layout: default
title: Home
---

# Welcome on my blog 🚀

Unlock the exciting world of algorithms, programming, and artificial intelligence with clear examples and hands-on projects that bring knowledge to life!

## 📌 Check my recent articles :
<ul>
  {% for post in site.posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## 📌 Follow me
- [LinkedIn](https://linkedin.com/in/jelhi)