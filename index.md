---
layout: default
title: articles
---

<h2>articles</h2>
<ul>
  {% comment %}
    1. Get all pages from the site.
    2. Sort them by date.
    3. Reverse the order to show the newest articles first.
  {% endcomment %}
  {% assign sorted_pages = site.pages | sort: 'date' | reverse %}
  
  {% for p in sorted_pages %}
    {% comment %}
      Filtering logic:
      1. Exclude the current page (this index page).
      2. Ensure the page has a 'title' (skips system files without front matter).
      3. Ensure the file extension is .html (skips css, xml, etc.).
    {% endcomment %}
    {% if p.url != page.url and p.title %}
      {% if p.url contains '.html' %}
        <li>
          <a href="{{ p.url | relative_url }}">
            {{ p.title | default: p.name }}
          </a>
          <small>({{ p.date | date: "%Y-%m-%d" }})</small>
        </li>
      {% endif %}
    {% endif %}
  {% endfor %}
</ul>
