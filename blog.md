---
layout: blog
title: "Blog"
permalink: "blog"
---

# Últimas Entradas

{% for post in site.posts %}
    {{ post }}
    "title": "{{ post.title | xml_escape }}",
    "url": "{{ site.url }}{{ post.url }}",
    "date": "{{ post.date | date_to_xmlschema }}"
{% unless forloop.last %},{% endunless %}
{% endfor %}