---
layout: page
title: Proyectos
description: Hyperlinks to some of my projects and snippets.
keywords: pagina de proyectos, vinculos
---

## Post publicados con tag "proyecto"

<ul>
  {% for post in site.posts %}
    {% if post.tags contains "Project" %}

    <li>
        <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a> — {{ post.description }}
    </li>
    
    {% endif %}
  {% endfor %}
</ul>

## Animación
- [Tsum - Tsum](http://romerorigger.com/projects/LJbW0?album_id=65844) - Tercera Temporada 2017 Disney Channel
- [standUP](http://romerorigger.com/projects/Xv363?album_id=65844) - Corto Animado
- [Brake Bones vs. Al Dente](http://romerorigger.com/projects/nR4z1?album_id=65844) - Corto Animado
- [BIT](http://romerorigger.com/projects/LJbW0?album_id=65844) - Propuesta serie de TV

### Scripts
- [job Finder](http://romerorigger.com/projects/4GZE1?album_id=65845) - Buscador de empleo en CGI integrado a Autodesk Maya
- [wire Deformer setup](http://romerorigger.com/projects/EWLmN?album_id=65845) — Creacion de un sistema de deformacion por capas con deformadores wire
- [offset](http://romerorigger.com/projects/JYl8A?album_id=65845) - Creacion de grupos offset para elementos seleccionados