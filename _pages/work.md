---
layout: single
title: Publications
description:
permalink: /pubs/
---

## Main publications

<p>
  <ul>
    {% for post in site.categories.science %}
    {% if post.work-type == 'Paper' and post.paper-type == 'Main' %}
    <li>
      <a href="{% if post.ref-doi %}http://dx.doi.org/{{ post.ref-doi }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}"><h2 class="card__header" itemprop="name">{{ post.ref-title }} ({{ post.ref-year }}).</h2></a>
      <p class="card__count">{{ post.ref-authors }}. <em>{{ post.ref-journal}}</em>{% if post.ref-vol %}, {{ post.ref-vol }}{% endif %}.{% if post.ref-doi %} <a href="http://dx.doi.org/{{ post.ref-doi }}">doi: {{ post.ref-doi }}</a>{% endif %}</p>
    </li>
    {% endif %}
    {% endfor %}
    </ul>
</p>


## Other publications

<p>
  <ul>
    {% for post in site.categories.science %}
    {% if post.work-type == 'Paper' and post.paper-type == 'Other' %}
    <li>
      <a href="{% if post.ref-doi %}http://dx.doi.org/{{ post.ref-doi }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}"><h2 class="card__header" itemprop="name">{{ post.ref-authors }} ({{ post.ref-year }}).</h2></a>
      <p class="card__count">{{ post.ref-title }}. <em>{{ post.ref-journal}}</em>{% if post.ref-vol %}, {{ post.ref-vol }}{% endif %}.{% if post.ref-doi %} <a href="http://dx.doi.org/{{ post.ref-doi }}">doi: {{ post.ref-doi }}</a>{% endif %}</p>
    </li>
    {% endif %}
    {% endfor %}
    </ul>
</p>




## Under review
