---
layout: page
permalink: /publications/
title: Publications
description: <b>* indicates the corresponding author and &#35; indicates co-first authorship.</b>
years: [2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<!-- <div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div> -->




<div class="publications">
  {% assign pubs = site.bibliography | sort: "year" | reverse %}
  {% for pub in pubs %}
    <p>
      [{{ forloop.index }}]
      {% if pub.author %}<strong>{{ pub.author }}</strong>. {% endif %}
      {% if pub.title %}<em>{{ pub.title }}</em>. {% endif %}
      {% if pub.journal %}{{ pub.journal }}, {% endif %}
      {% if pub.year %}{{ pub.year }}.{% endif %}
    </p>
  {% endfor %}
</div>
