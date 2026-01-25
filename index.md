---
layout: default
title: articles
---

<h2>articles</h2>

<ul>
  {% assign sorted_pages = site.pages | sort: 'date' | reverse %}
  
  {% for p in sorted_pages %}
    {% if p.url contains '/articles/' and p.url != '/articles/' and p.name != 'index.md' %}
      <li>
        <a href="{{ p.url | relative_url }}">
          {{ p.title | default: p.name }}
        </a>
      </li>
    {% endif %}
  {% endfor %}
</ul>
