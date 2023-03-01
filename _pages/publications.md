---
layout: page
permalink: /publications/
title: publications
description: Test 1
years: [2023, 2022, 2020, 2019, 2018]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">

**If you are unable to access any of these papers, please contact me at rmoglen@utexas.edu**

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
