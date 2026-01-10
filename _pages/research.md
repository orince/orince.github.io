---
layout: archive
permalink: /researchs/
author_profile: true
---
{% if site.author.googlescholar %}

<div class="wordwrap">You can find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

{% for category in site.publication_category %}

<section class="publication-category">
  <h1>{{ category[1].title }}</h1>
  <hr />
  {% assign posts = site.researchs | where: "category", category[0] | sort: "date" | reverse %}
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
</section>
{% endfor %}
