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
<div class="publications">

<!-- {%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %} -->

{% assign counter = 0 %}
{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {%- assign entries = site.scholar.bibliography | where: "year", y | sort: "month" | reverse %}
  {% for entry in entries %}
    {% assign counter = counter | plus: 1 %}
    {% include bib.html entry=entry count=counter %}
  {% endfor %}
{%- endfor %}

</div>