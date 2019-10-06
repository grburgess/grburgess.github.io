---
layout: single
title: Publications
description:
permalink: /pubs/
---

## Main publications
These are works where I played a primary role or contributed significantly to the data analysis.
<p>
  <ul>
    {% for post in site.categories.science %}
    {% if post.work-type == 'Paper' and post.paper-type == 'Main' %}
    <li>
      <a href="{% if post.ref-doi %}http://dx.doi.org/{{ post.ref-doi }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}"><h2 class="card__header" itemprop="name">{{ post.ref-title }} </h2></a>
      <p class="card__count">{{ post.ref-authors }}. {{post.ref-year}},  <em>{{ post.ref-journal}}</em> <b>{% if post.ref-vol %}{{ post.ref-vol }}{% endif %}</b>:{% if post.ref-page %}{{ post.ref-page }}{% endif %}. {% if post.ref-doi %} <a href="http://dx.doi.org/{{ post.ref-doi }}">doi: {{ post.ref-doi }}</a>{% endif %}</p>
    </li>
    {% endif %}
    {% endfor %}
    </ul>
</p>


## Other publications
These are works where I contributed, but not enough to have played a fundemental role. This includes collaboration papers. 
<p>
  <ul>
    {% for post in site.categories.science %}
    {% if post.work-type == 'Paper' and post.paper-type == 'Other' %}
    <li>
	
<a href="{% if post.ref-doi %}http://dx.doi.org/{{ post.ref-doi }}{% else %}{{ post.url | prepend: site.baseurl }}{% endif %}"><h2 class="card__header" itemprop="name">{{ post.ref-title }} </h2></a>
      <p class="card__count">{{ post.ref-authors }}. {{post.ref-year}},  <em>{{ post.ref-journal}}</em> <b>{% if post.ref-vol %}{{ post.ref-vol }}{% endif %}</b>:{% if post.ref-page %}{{ post.ref-page }}{% endif %}. {% if post.ref-doi %} <a href="http://dx.doi.org/{{ post.ref-doi }}">doi: {{ post.ref-doi }}</a>{% endif %}</p>
    </li>
    {% endif %}
    {% endfor %}
    </ul>
</p>




## Under review
