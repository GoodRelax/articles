---
layout: default
title: Articles
lang: en
---

<h1>Articles</h1>

{% assign sorted_pages = site.pages | sort: 'date' | reverse %}

<section>
  <h2>English</h2>
  <ul>
    {% for p in sorted_pages %}
      {% if p.title and p.lang == 'en' and p.url != page.url %}
        <li>
          <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
          <small>({{ p.date | date: "%Y-%m-%d" }})</small>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
</section>

<hr>

<section>
  <h2>Japanese</h2>
  <ul>
    {% for p in sorted_pages %}
      {% if p.title and p.lang == 'ja' and p.url != page.url %}
        <li>
          <a href="{{ p.url | relative_url }}">{{ p.title }}</a>
          <small>({{ p.date | date: "%Y-%m-%d" }})</small>
        </li>
      {% endif %}
    {% endfor %}
  </ul>
</section>
