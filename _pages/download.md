---
layout: archive
title: "Download"
permalink: /download/
author_profile: true
---
Proteome-phenome-wide MR atlas covering up to 2,265 unique proteins on a curated list of 355 distinct phenotypes, identifying 726,035 protein-phenotype pairs in European, 33,078 in African, and 115,352 in East Asian ancestries.
Link: [https://broad.io/protein_mr_atlas](https://broad.io/protein_mr_atlas)
Source paper: [Su et al. *medRxiv* 2024](https://www.medrxiv.org/content/10.1101/2024.10.17.24315553v2)  
[atlas](atlas.png)

{% include base_path %}

<!-- New style rendering if download categories are defined -->
{% if site.download_category %}
  {% for category in site.download_category  %}
    {% assign title_shown = false %}
    {% for post in site.download reversed %}
      {% if post.category != category[0] %}
        {% continue %}
      {% endif %}
      {% unless title_shown %}
        <h2>{{ category[1].title }}</h2><hr />
        {% assign title_shown = true %}
      {% endunless %}
      {% include archive-single.html %}
    {% endfor %}
  {% endfor %}
{% else %}
  {% for post in site.download reversed %}
    {% include archive-single.html %}
  {% endfor %}
{% endif %}
