---
layout: null
title: "Blog"
permalink: "blog"
---
Categorias:
{% for category in site.categories %}
    {{ category | first }}{% unless forloop.last %},{% endunless %}
{% endfor %}

Últimas entradas:
{% for post in site.posts %}
    "title": "{{ post.title | xml_escape }}",
    "url": "{{ site.url }}{{ post.url }}",
    "date": "{{ post.date | date_to_xmlschema }}"
{% unless forloop.last %},{% endunless %}
{% endfor %}

Tags:
{% for tag in site.tags %}
{{ tag | first }}{% unless forloop.last %},{% endunless %}
{% endfor %}