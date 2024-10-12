---
layout: page
permalink: /publications/
title: Publications
description: <h6>For the complete list, please see my <b><a href='https://scholar.google.com/citations?user=p5OmQIwAAAAJ&hl=en&oi=ao'>Google Scholar Profile</a></b>.</h6>
#years: [Preprints, 2023, 2022, 2020, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2009, Thesis] #, 1967, 1956, 1950, 1935, 1905]
nav: true
nav_order: 2
---
<!-- _pages/publications.md -->
<div class="publications">

{% bibliography -f {{ site.scholar.bibliography }} %}

</div>


{% for publication in site.publications %}
<div class="publication-item">
  {% if publication.thumbnail %}
  <img src="{{ publication.thumbnail }}" alt="Thumbnail for {{ publication.title }}" class="thumbnail">
  {% endif %}
  <div class="publication-info">
    <strong>{{ publication.title }}</strong><br>
    <span>{{ publication.author }}</span><br>
    <span>{{ publication.journal }} ({{ publication.year }})</span><br>
    <a href="{{ publication.url }}">Read more</a>
  </div>
</div>
{% endfor %}
