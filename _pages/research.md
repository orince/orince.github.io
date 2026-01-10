---
layout: archive
title: ""
permalink: /research/
author_profile: true
---
{% if site.publication_category %}

{% for category in site.publication_category %}

<section class="publication-category">
  <h2 style="font-size: 2em; font-weight: bold; margin-top: 1.5em; margin-bottom: 0.5em;">{{ category[1].title }}</h2>
  <hr />
  {% assign posts = site.research | where: "category", category[0] | sort: "date" | reverse %}
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
</section>
{% endfor %}
{% endif %}