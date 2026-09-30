---
layout: default
title: Blog
---

# Blog


{% for post in site.posts limit:6 [{{ post.title }}]({{ post.url }})
  
  **{{ post.date | date: "%d/%m/%Y" }}**
  
  {{ post.excerpt }}

{% endfor %}
