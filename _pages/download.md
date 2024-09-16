---
layout: archive
title: "Download"
permalink: /download/
author_profile: true
---
TBA
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
