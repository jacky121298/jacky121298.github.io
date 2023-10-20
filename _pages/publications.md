---
layout: page
permalink: /publications/
title: publications
description:
years_preprint: [2023]
years_conference: [2022, 2021]
years_workshop: [2020]
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->

<article>
<div class="publications">
<h2 class="publ-cat">Preprint</h2>
{%- for y in page.years_preprint %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f preprint -q @*[year={{y}}]* %}
{% endfor %}
</div>

<div class="publications">
<h2 class="publ-cat">Conference Paper</h2>
{%- for y in page.years_conference %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f conference -q @*[year={{y}}]* %}
{% endfor %}
</div>

<div class="publications">
<h2 class="publ-cat">Workshop Paper</h2>
{%- for y in page.years_workshop %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f workshop -q @*[year={{y}}]* %}
{% endfor %}
</div>
</article>