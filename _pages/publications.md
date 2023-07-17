---
layout: page
permalink: /publications/
title: publications
description: You can find here my main journal and conference publications. Visit my <a href="https://scholar.google.com/citations?user=pRC8DwcAAAAJ" target="_blank"><b>Google Scholar profile</b></a> for a full list of publications.

years: [2023, 2022, 2021, 2020]
nav: true
---
<!-- _pages/publications.md -->
<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

</div>
