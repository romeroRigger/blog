---
layout: page
title: Proyectos
description: Hyperlinks to some of my projects and snippets.
keywords: pagina de proyectos, vinculos
---

## Post publicados con tag "Clases"

<ul>
  {% for post in site.posts %}
    {% if post.tags contains "Clases" %}

    <li>
        <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> — {{ post.description }}
    </li>
    
    {% endif %}
  {% endfor %}
</ul>

## Rigging
- [Rigging de Personajes](http://bit.ly/riggingPersonajes) - Intermedio