---
layout: blog
title: "Blog"
permalink: "blog"
---

{% for category in site.categories %}
    {{ category | first }}{% unless forloop.last %},{% endunless %}
{% endfor %}


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