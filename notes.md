---
layout: page
title: Notes
permalink: /notes/
---

<div class="home">

    {% if site.paginate %}
        {% assign posts = paginator.posts %}
    {% else %}
        {% assign posts = site.posts %}
    {% endif %}

    <ul class="post-list">
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        {% for note in site.notes %}
            {% unless note.hidden %}
            <li>
                <span class="post-meta">{{ note.date | date: date_format }}</span>
                <h3>
                <a class="post-link" href="{{ note.url | relative_url }}">
                    {{ note.title | escape }}
                </a>
                </h3>
                {%- if site.show_excerpts -%}
                    {{ post.excerpt }}
                {%- endif -%}
            </li>
            {% endunless %}
        {% endfor %}
    </ul>
    
</div>