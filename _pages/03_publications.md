---
layout: page
permalink: /publications/
title: publications
order: 3
description: in reversed chronological order | <sup>+</sup> denotes co-first authorship | <sup>*</sup> denotes corresponding authorship
years: [2023, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013]
nav: true
---

<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>