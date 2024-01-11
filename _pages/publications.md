---
layout: page
permalink: /publications/
title: selected publications
description: You can find here my main journal and conference publications. Visit my Google Scholar profile for a full list of publications.

years: [2024, 2023, 2022, 2021, 2020]
nav: true
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
