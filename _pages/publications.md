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
  {% for paper_id in site.data.citations.papers %}
    {% assign paper = site.data.citations.papers[paper_id] %}
    <div class="publication-item">
      <h4>{{ paper.title }}</h4>
      <p><strong>Year:</strong> {{ paper.year }} | <strong>Citations:</strong> {{ paper.citations }}</p>
    </div>
  {% endfor %}
{% else %}
  <p>No publications found.</p>
{% endif %}

</div>
