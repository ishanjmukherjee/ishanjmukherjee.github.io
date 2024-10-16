---
layout: page
title: Notes
permalink: /notes/
---

<div class="home">

    {% if site.paginate %}
        {% assign notes = paginator.notes | sort: 'date' | reverse %}
    {% else %}
        {% assign notes = site.notes | sort: 'date' | reverse %}
    {% endif %}

    <ul class="post-list">
        {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
        {% for note in notes %}
            {% unless note.hidden %}
            <li>
                <span class="post-meta">{{ note.date | date: date_format }}</span>
                <h3>
                <a class="post-link" href="{{ note.url | relative_url }}">
                    {{ note.title | escape }}
                </a>
                </h3>
                {%- if site.show_excerpts -%}
                    {{ note.excerpt }}
                {%- endif -%}
            </li>
            {% endunless %}
        {% endfor %}
    </ul>

</div>