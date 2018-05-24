---
layout: page
title: Clases
description: vinculos a las clases y tutoriales que realizo
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
- [Rigging de Personajes - CREHANA](http://bit.ly/riggingPersonajes) - Intermedio