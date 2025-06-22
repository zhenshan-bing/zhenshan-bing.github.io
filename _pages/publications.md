---
layout: page
permalink: /publications/
title: Publications
description: <b>* indicates the corresponding author and &#35; indicates co-first authorship.</b>
nav: true
nav_order: 1
---

<div class="publications">
  {% assign counter = 0 %}
  {% for entry in site.scholar.bibliography %}
    {% assign counter = counter | plus: 1 %}
    {% include bib.html entry=entry count=counter %}
  {% endfor %}
</div>
