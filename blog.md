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

{% for post in site.posts %}
    <p>
        <a href="{{ site.url }}{{ post.url }}">{{ post.title | xml_escape }}</a>
        <h6>{{ post.date | date_to_xmlschema }}</h6>
    </p>
{% endfor %}