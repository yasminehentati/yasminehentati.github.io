---
layout: page
permalink: /publications/
title: publications
description: publications from Google Scholar
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

{% include bib_search.liquid %}

<div class="publications">

{% if site.data.citations.papers %}
  {% for paper in site.data.citations.papers %}
    <div class="publication-item">
      <h4>{{ paper[1].title }}</h4>
      <p><strong>Year:</strong> {{ paper[1].year }} | <strong>Citations:</strong> {{ paper[1].citations }}</p>
    </div>
  {% endfor %}
{% else %}
  <p>No publications found.</p>
{% endif %}

</div>
