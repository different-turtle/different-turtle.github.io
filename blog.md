---
layout: blog
title: "Blog"
permalink: "blog"
---

# Últimas Entradas

{% for post in site.posts %}
    [{{ post.title | xml_escape }}]({{ site.url }}{{ post.url }})
    {{ post.date | date_to_xmlschema }}
{% endfor %}